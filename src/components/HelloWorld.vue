<template>
  <div class="hello">
      <input type="text" v-model="ime" placeholder="Ime">
      <input type="text" v-model="prezime" placeholder="Prezime">
      <p> {{ imeprezime }} </p>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      ime: '',
      prezime: '',
    };
  },
  computed: {
    imeprezime() {
      return `Zdravo, ${this.ime} ${this.prezime}`;
    },
  },
  methods: {
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
