<template>
  <div class="hello">
  <input
    type="text"
    :value="nasaPoruka"
    @keydown="logiranje"/>
    <h1>{{ msg }}</h1>
    <p>{{novaPoruka}}</p>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
  },
  data(){
    return{
      nasaPoruka: 'nema interneta',
    };
  },
  computed:{
    novaPoruka(){
      return `${this.msg} ${this.nasaPoruka}`;
    },    
  },
  methods:{
    logiranje(e){
      this.nasaPoruka = e.target.value;
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
</style>
