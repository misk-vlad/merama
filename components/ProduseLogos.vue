
<template>
  <div>
      <li v-for="(item,index) in logos " :key="index">
               <img :src="item.image" :alt="item.name">
      </li>
  </div>
  
</template>




<script>
    

  const logoss = {
    logos: [
      {image:"https://www.w3schools.com/images/w3schools_green.jpg",name:"W3Schools.com"},
      {image:"https://www.w3schools.com/images/w3schools_green.jpg",name:"1"},
      {image:"https://www.w3schools.com/images/w3schools_green.jpg",name:"W3Schools.com"},
      {image:"https://www.w3schools.com/images/w3schools_green.jpg",name:"W3Schools.com"},
      {image:"https://www.w3schools.com/images/w3schools_green.jpg",name:"W3Schools.com"},
      {image:"https://www.w3schools.com/images/w3schools_green.jpg",name:"W3Schools.com"},
      
    ]

  }
  
module.exports  = {
  name: "logosss",
  data() { return logoss
  },
}

</script>

<style>
li {
    display: inline-block;
}

ul{
  list-style-type: none; 
}
</style>


