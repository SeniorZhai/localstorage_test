<template>
  <div class="hello">
    <h1>{{ a }}</h1>
    <button @click="save">save</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
   data() {
    return {
      a: 0
    }
  },
  mounted() {
    console.log(localStorage.a);
    if (localStorage.a) {
      this.a = localStorage.a;
    }
  },
  methods:{
    save(){
      localStorage.a = this.a + 1;
      console.log(localStorage.a);
    }
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
