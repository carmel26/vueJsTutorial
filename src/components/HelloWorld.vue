<template>
  <div class="hello">
    <button @click="handleClick"> Click me! </button>
    <h1 id="header">{{ name }}</h1>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  methods: {
    handleClick(event) {
      const header = document.getElementById('header');
      header.style.color = 'brown';
      // eslint-disable-next-line no-console
      console.log(event);
      // eslint-disable-next-line no-param-reassign
      event.target.style.backgroundColor = 'purple';
      // eslint-disable-next-line no-param-reassign
      event.target.style.color = 'white';
    },
  },
  data() {
    return {
      name: 'Carmel Nkeshi',

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
