
<template>
  <div class ="logo">
        <div class="logs_grids">
            <div v-for="(item,index) in logos " :key="index">
                <div class="logos-css">
                    <div class = "bord">
                        <div class ="block" v-on:click="doOnclick(item.onclick) ">
                            <img class="image" :src="item.image" :alt="item.name" >
                        </div>
                    </div>
                </div>
            </div>
        </div>
      </div>  
</template>




<script>



  const logoss = {

    
    /** @description set of theme item 0 default 1- dark 2- poor eyesight */
    theme: 0,
    logos: [
        {image:"https://www.w3schools.com/images/w3schools_green.jpg",name:"W3Schools.com",onclick:"1"},
        {image:"https://swiperjs.com/images/sponsors/appkong.png",name:"1",onclick:"2"},
        {image:"https://swiperjs.com/images/sponsors/parhaatkasinot.png",name:"W3Schools.com",onclick:"3"},
        {image:"https://swiperjs.com/images/sponsors/thecasinodb-h.png",name:"W3Schools.com",onclick:"4"},
        {image:"https://www.w3schools.com/images/w3schools_green.jpg",name:"W3Schools.com",onclick:"5"},
        {image:"https://swiperjs.com/images/sponsors/casinos-hunter-h.png",name:"W3Schools.com",onclick:"6"},
        {image:"https://www.w3schools.com/images/w3schools_green.jpg",name:"W3Schools.com",onclick:"7"},
        {image:"https://www.w3schools.com/images/w3schools_green.jpg",name:"W3Schools.com",onclick:"7"},
        {image:"https://www.w3schools.com/images/w3schools_green.jpg",name:"W3Schools.com",onclick:"7"},
        {image:"https://www.w3schools.com/images/w3schools_green.jpg",name:"W3Schools.com",onclick:"7"},
        {image:"https://www.w3schools.com/images/w3schools_green.jpg",name:"W3Schools.com",onclick:"7"},
        {image:"https://swiperjs.com/images/sponsors/parhaatkasinot.png",name:"W3Schools.com",onclick:"3"},
        {image:"https://www.w3schools.com/images/w3schools_green.jpg",name:"W3Schools.com",onclick:"7"},
        {image:"https://www.w3schools.com/images/w3schools_green.jpg",name:"W3Schools.com",onclick:"7"},
        {image:"https://www.w3schools.com/images/w3schools_green.jpg",name:"W3Schools.com",onclick:"7"},
        {image:"https://swiperjs.com/images/sponsors/parhaatkasinot.png",name:"W3Schools.com",onclick:"3"},
        {image:"https://swiperjs.com/images/sponsors/parhaatkasinot.png",name:"W3Schools.com",onclick:"3"},
        {image:"https://swiperjs.com/images/sponsors/parhaatkasinot.png",name:"W3Schools.com",onclick:"3"}, 
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
    .logo{
        font-weight: 500;
        max-width: 64rem;
        margin-left: auto;
        margin-right: auto;
        margin-top: 2rem;
        margin-bottom: 2rem;
        max-height: 300px;
        overflow:scroll;
        -ms-overflow-style: none; /* ширина scrollbar'a */
        scrollbar-width: none;
    }
    .logo::-webkit-scrollbar {
         width: 0;
        height: 0;
    }


    .logs_grids{ 
        display: grid;
        height: 100%;
        object-fit: cover;
        grid-template-columns: repeat(4,minmax(0,1fr));
        gap: .75rem;
    }
    
    .logos-css{
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .block {
        --tw-border-opacity: 0.2;
        
        height: 5rem;
        border: solid;  
        border-color: rgba(100, 113, 126,var(--tw-border-opacity));
        border-width: 1px;
        padding: .25rem;
    }

    

    .image {
        max-width: 100%;
    }

   

    .bord {
        height: 100%;
        width: 100%;
    }
    
    img {
        width: 100%;
        height: 100%;
        object-fit: contain;
    }

    
    .bord img {
        opacity: 0.8;
        cursor: pointer;
    }
    .bord img:hover {
        opacity: 1;
    }

    

</style>





    
    
    .logos-inside {
              
        
    }
    
    
    .logos_grid {
        width: 100%;
    }
    

    
    .block img {
        opacity: 0.8;
        cursor: pointer;
    }
    .block img:hover {
        color: rgba(99,50,246,var(--tw-text-opacity));
        
        --tw-text-opacity: 1;
    }


    