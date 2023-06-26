<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
     The following document is based on the class work that was given on the 26th of June 2023 where we were asked to build a view app which consisted of a nav bar, a footer and to display data from our previously created JSON server    </p>
    <h3>Students are as follows</h3>

        <!-- <div v-for="data in myJson" :key ="students.id">{{data}}</div> -->

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
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

mounted (){

}