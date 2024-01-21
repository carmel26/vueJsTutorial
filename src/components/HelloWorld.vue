<!-- eslint-disable vuejs-accessibility/form-control-has-label -->
<template>
  <div class="hello">
    <button @click="handleClick"> Click me! </button>
    <h1 id="header">Hi, my name is : {{ myName.toUpperCase() }}</h1>
    <h3 v-once>{{ myName }}</h3>
    <button @click="myName = 'Programmer And Developer'"> Change name </button>
    <div v-html="myContent"></div>
    <div v-show="isShowing" v-text="myText"></div>
    <button @click="isShowing = !isShowing"> {{ isShowing ? 'Hide' : 'Show' }} </button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  methods: {
    handleClick(event) {
      const header = document.getElementById('header');
      header.style.color = 'blue';
      // eslint-disable-next-line no-console
      console.log(event);
    },
  },
  data() {
    return {
      myName: 'Carmel Nkeshimana',
      number: 4,
      myContent: '<b style="color:green"> This is my content </b>',
      myText: 'Hello word, im learning Vue JS!',
      isShowing: true,
    };
  },
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#divId {
  background-color: brown;
}

.myH2 {
  background-color: blueviolet;
}
</style>
