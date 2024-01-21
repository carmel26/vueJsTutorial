<!-- eslint-disable vuejs-accessibility/form-control-has-label -->
<template>
  <div class="hello">
    <button v-on:click="onClickButton">click me!</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  methods: {
    onClickButton() {
      // eslint-disable-next-line no-console
      console.log('Hello my people!!');
    },
  },
  data() {
    return {
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
