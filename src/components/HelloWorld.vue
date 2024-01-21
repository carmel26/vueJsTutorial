<!-- eslint-disable vuejs-accessibility/form-control-has-label -->
<template>
  <div class="hello">
    <button @click="handleClick"> Click me! </button>
    <h1 id="header">Hi, my name is : {{ name.toUpperCase() }}</h1>
    <input v-model="text" type="text" name="mytext" id="mytext"> <br>
    {{ text }}
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
      name: 'Carmel Nkeshimana',
      number: 4,
      text: '',
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
