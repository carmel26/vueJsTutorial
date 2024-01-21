<!-- eslint-disable vuejs-accessibility/form-control-has-label -->
<template>
  <div class="hello">
    <button @click="handleClick"> Click me! </button>
    <h3>2+23 = {{ 2+23 }}</h3>
    <h3> {{ new Date().toLocaleTimeString() }}</h3>
    <h1 id="header">Hi, my name is : {{ name.toUpperCase() }}</h1>
    <h3>{{ sayHello() }}</h3>
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
    sayHello() {
      return 'HELLÖoOOOO';
    },
  },
  data() {
    return {
      name: 'Carmel Nkeshimana',
      number: 4,
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
