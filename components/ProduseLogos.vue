
<template>
  <div class ="logos-css">
        <div class="logos_inside">
                <li v-for="(item,index) in logos " :key="index">
                    <div class="img-center">
                        <div class ="borders">
                            <img :src="item.image" :alt="item.name" v-on:click="doOnclick(item.onclick)">
                        </div>
                    </div>
                </li>
        </div>
      </div>  
</template>




<script>



  const logoss = {

    
    /** @description set of theme item 0 default 1- dark 2- poor eyesight */
    theme: 0,
    logos: [
        {image:"https://www.w3schools.com/images/w3schools_green.jpg",name:"W3Schools.com",onclick:"1"},
        {image:"https://www.w3schools.com/images/w3schools_green.jpg",name:"1",onclick:"2"},
        {image:"https://www.w3schools.com/images/w3schools_green.jpg",name:"W3Schools.com",onclick:"3"},
        {image:"https://www.w3schools.com/images/w3schools_green.jpg",name:"W3Schools.com",onclick:"4"},
        {image:"https://www.w3schools.com/images/w3schools_green.jpg",name:"W3Schools.com",onclick:"5"},
        {image:"https://www.w3schools.com/images/w3schools_green.jpg",name:"W3Schools.com",onclick:"6"},
        {image:"https://www.w3schools.com/images/w3schools_green.jpg",name:"W3Schools.com",onclick:"7"},
      
    ]

  }
    module.exports  = {
    name: "logos",
    data() { return logoss
    },
    computed: {
        getWindow () {return window},
        windowFoo() {
            return this.$store.getters.windowFoo;
        },
    },

    methods: {
        doOnclick (dosome) {
            alert(`${dosome}`)
        },

    },
    props: {
        themeOfPage: Number | 0
    },
    mounted () {
        // mouseScroll(window) // scrolling items by click
    },
    created () {
       // some
    },

    
}


</script>









<style>
    * {
        box-sizing: border-box;
    }
    .logos-css {
        width: 95%;
        background: rgba(75, 105, 122, 0.1);
        display: block;
        margin: 0;
        margin-block-start: 0.5%;
        margin-left: auto;
        margin-right: auto;
        max-height: 360px; /* change if logos be different */
        overflow:scroll;
        border-radius: 30px;
        -ms-overflow-style: none; /* ширина scrollbar'a */
        scrollbar-width: none;
    }
    .logos-css::-webkit-scrollbar {
         width: 0;
        height: 0;
        
    }

    .logos_inside{
        opacity: 1;
        width: 100%;
        align-items: center;
        margin-left: auto;
        margin-right: auto;
        display: flex;
        flex-wrap: wrap;
        clear: both;
        flex-direction: inherit;
        justify-content: space-around;
    }

    li {
        margin: 1%; 
        display: inline-block;
    }




    .img-center {
        float: left;
        padding: 10px;
    }
    .img-center img {
        opacity: 0.8;
        cursor: pointer;
    }
    .img-center img:hover {
        opacity: 1;
    }


    .borders {
        margin: auto;
        overflow:hidden;
        border-radius: 15px;
    }

</style>


