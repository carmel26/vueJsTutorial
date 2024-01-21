<!-- eslint-disable vuejs-accessibility/form-control-has-label -->
<template>
  <div class="hello">
    <button @click="handleClick"> Click me! </button>
    <h1 id="header">{{ name }}</h1>

    <form @submit.prevent="handleSubmit">
      <input type="text"  /> <br/>
      <button type="submit">Submit</button>
    </form>
    <button @click.once="onBtnClicked">Click Button</button>
    <p>{{ number }}</p>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  methods: {
    handleSubmit() {
      // eslint-disable-next-line no-console
      console.log('Form submitted');
    },
    onBtnClicked() {
      this.number += 1;
    },
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
