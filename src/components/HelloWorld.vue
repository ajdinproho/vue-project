<template>
  <div class="hello">
      <div class="prvi-input">
      <input type="text" v-model="ime" placeholder="Ime">
      </div>
      <div class="drugi-input">
      <input type="text" v-model="prezime" placeholder="Prezime">
      </div>
      <div>
      <p v-show='klik'> {{ imeprezime }} </p>
      <button v-on:click="prikaziPoruku" class="klik">Prikazi poruku</button>
      </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      ime: '',
      prezime: '',
      klik: false,
    };
  },
  computed: {
    imeprezime() {
      return `Zdravo, ${this.ime} ${this.prezime}`;
    },
  },
  methods: {
    prikaziPoruku() {
      if (!this.klik) {
        this.klik = true;
      } else {
        this.klik = false;
      }
    },
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
.klik{
  margin-top:20px;
}
.prvi-input{
  margin-bottom:5px;
}
</style>
