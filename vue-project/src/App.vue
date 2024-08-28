<script>
export default {
  data() {
    return {
      name: "bubun",
      roll: "201004",
      status: "ac",
      Task : ["bubun","jemmy","radwan","shawon","Kamrul"],
      Link :"https://google.com"
    };
  },
    methods:{
 toggleSTatus(){
   if(this.status==="active"){
     this.name = "radwan"
   }
   else{
    this.name = "shawon"
   }
 }

    }

};
</script>

<template>
  <h1>bybyn {{ name }} {{ roll }}</h1>
  <p v-if="status === 'pending'">my name is Nur</p>
  <p v-else-if="status ==='lerger'">Bububn is lerger</p>
  <p v-else>hahaha</p>
  <ul>
    <p v-for ="task in Task" :key="task"><li>{{task}}</li></p>
  </ul>
  <a v-bind:href="Link">Click here to  go to google</a>
  <button @click="toggleSTatus">Click me to see the name</button>
</template>
