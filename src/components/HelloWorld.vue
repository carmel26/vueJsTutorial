<!-- eslint-disable vuejs-accessibility/form-control-has-label -->
<template>
  <div class="hello">
    <h3 v-for="(letter, index) in alphabet" :key="letter">{{ index+1 +')'+ letter }}</h3>
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
      alphabet: ['One', 'Two', 'Three', 'Four'],
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
