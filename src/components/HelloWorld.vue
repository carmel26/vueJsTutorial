<!-- eslint-disable vuejs-accessibility/form-control-has-label -->
<template>
  <div class="hello">
    <h3 v-if="location==='One'">One</h3>
    <h3 v-else-if="location === 'Two'">Two</h3>
    <h3 v-else>Home</h3>
    <button @click="location = 'Two'">Click me!</button>
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
      location: 'One',
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
