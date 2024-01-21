<!-- eslint-disable vuejs-accessibility/form-control-has-label -->
<template>
  <div class="hello">
   <span v-pre>{{ myName }}</span> <br>
   <span>{{ myName }}</span>
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
      myName: 'Nkeshimana',
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
