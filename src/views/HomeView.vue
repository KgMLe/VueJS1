<template>
  <div class="home">
    <img alt="Vue logo" src="https://cdn-icons-png.flaticon.com/512/43/43742.png">
    <HelloWorld msg="Hi, welcome to my page"/>
  </div>
  <div id="list">
    </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'


export default {
  name: 'HomeView',
  components: {
    HelloWorld
  }
}

async function getData() {
      let data = await fetch("https://kgmle.github.io/jsonServerPrac/database.json")
      let peopleData = await data.json()
      let extractedData = peopleData.students
      let display = document.querySelector("#list")
      extractedData.forEach(person => {
          display.innerHTML +=`
            <div class = "column">
              <div class="card">
              <h4>${person.last_name}</h4>
              <h4>${person.first_name}</h4>
              <h4>${person.email}</h4>
          </div>  
            </div>
          `
      })
  }
  getData()
</script>

<style>
.column {
  padding: 0 10px;
}


.card {
 
  width: 50%;
  padding: 10px;
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
  width: 40%;
  text-align: center;
  display: grid;
  grid-template-columns: auto auto auto;
}

.card:hover {
  box-shadow: 0 8px 16px 0 orangered;
}

.container {
  padding: 2px 16px;}
</style>