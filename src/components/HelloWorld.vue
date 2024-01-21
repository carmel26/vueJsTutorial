<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2 :class="myH2">Helloo Second App</h2>
    <h3>{{  name }}</h3>
    <div v-bind:id="myId">Hello my di: {{ myId }}</div>
    <img v-bind:src="mySrc" alt="">
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      name: 'Carmel Nkeshi',
      age: 30,
      myId: 'divId',
      mySrc: 'https://strapi.eacgermany.org/uploads/Untitled_design_cb65dbf158.png',
      myH2: 'myH2',
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
