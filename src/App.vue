<template>
<div class="ThOME">
   <div class="Survey">
    <p>Complete a survey to get 1 year of luck</p>
   </div>
   <h1>{{title}}</h1>
</div>

 <div v-if="showModal1">
  //slot example instead of [props]
  <Modal @close="toggleModal1">
       
    <div class="title" v-for="title in titles" :key="title">
      <p>{{title.rdr}}</p>
    </div>

    <template v-slot:ratings>
      <div class="details" v-for="value in RDR" :key="value">
        <div>
         <li>{{value.dtl}}</li>
        </div>
        
        
        <div>
          <li>{{value.val}}</li>         
        </div>
      </div>
    </template>

    <template v-slot:map>
      <div class="maps" v-for="mapss in maps" :key="mapss">
        <img :src="`${mapss.rdr}`" alt="map not loaded"/> 
      </div>
    </template>
  </Modal>
 </div>


 <div v-if="showModal2">
  <Modal @close="toggleModal2">
    <h1>modal 2 h1 </h1>
    <p>Modal 2 paragrapht</p>  
    <img src="./assets/logo.png" style="width:50px" />
    <a href="a">Logdddd up</a>

    <template v-slot:ratings>
      <div v-for="value in SVN" :key="value">
        <li>{{value.val}}</li>
      </div>
    </template>
    
   
  </Modal>
 </div>


<section class="grid">

 <button style="background-image:url(https://cdn.sanity.io/images/e7woiqxp/production/6c088b7f878c304a7058a3fb51ca76ea8b70b149-1232x822.jpg?w=2000&fit=max&auto=format)"
 @click="toggleModal1">Riveie du rempard</button>

 <button style="background-image:url(https://cdn.sanity.io/images/e7woiqxp/production/2361c8951baad05401955038d2b893053b030485-1243x1303.jpg?w=2000&fit=max&auto=format)"
 @click="toggleModal2">Savamme</button>

 <button style="background-image:url(https://cdn.sanity.io/images/e7woiqxp/production/c1e1d5ef19744aba3bff6b66ffdf6055c0cb39ec-2048x875.jpg?w=2000&fit=max&auto=format)"
 @click="toggleModal3">Port LOiuis</button>

 <button style="background-image:url(https://cdn.sanity.io/images/e7woiqxp/production/21b390df9a8f8d77d6e5ee8107c4c6359bb3de34-1100x732.jpg?w=2000&fit=max&auto=format)"
 @click="toggleModal4">plaine will</button>

 <button style="background-image:url()"
 @click="toggleModal5">Modal 5</button>

 <button style="background-image:url()"
 @click="toggleModal6">Modal 6</button>

 <button style="background-image:url()"
 @click="toggleModal7">Modal 7</button>

 <button style="background-image:url()"
 @click="toggleModal8">Modal 8</button>

 <button style="background-image:url()"
 @click="toggleModal9">Modal 9</button>

 <button style="background-image:url()"
 @click="toggleModal10">Modal 10</button>

</section>


<footer>
  <div>
    <h3>Footer content</h3>
  </div>
</footer>


</template>

<script>
import Modal from './components/Modal.vue'
export default {
  name: 'App',

  components:{Modal},

  data(){
      return{

        title:'Molocal version2',
        titles:[],
        img:[],
        maps:[],
        RDR:[],
        SVN:[],

        showModal1: true,
        showModal2 : false,
        showModal3 : false,
        showModal4 : false,
        showModal5 : false,
        showModal6 : false,
        showModal7 : false,
        showModal8 : false,
        showModal9 : false,
        showModal10 : false,
      }
    },

    mounted(){
      fetch('http://localhost:3000/titles')
      .then(res => res.json())
      .then(data => this.titles = data)
      .catch(err => console.log(err.message))

      fetch('http://localhost:3000/RDR')
      .then(res => res.json())
      .then(data => this.RDR = data)

      fetch('http://localhost:3000/SVN')
      .then(res => res.json())
      .then(data => this.SVN = data)

      fetch('http://localhost:3000/maps')
      .then(res => res.json())
      .then(data => this.maps = data)

      fetch('http://localhost:3000/img')
      .then(res => res.json())
      .then(data => this.img = data)
    },


    methods:{
      toggleModal1() {
        this.showModal1 = !this.showModal1
        
      },
      toggleModal2(){
        this.showModal2 = !this.showModal2

      },
      toggleModal3(){
        this.showModal3 = !this.showModal3

      },
      toggleModal4(){
        this.showModal4 = !this.showModal4

      },
      toggleModal5(){
        this.showModal5 = !this.showModal5

      },
      toggleModal6(){
        this.showModal6 = !this.showModal6

      },
      toggleModal7(){
        this.showModal7 = !this.showModal7

      },

      toggleModal8(){
        this.showModal8 = !this.showModal8

      },
      toggleModal9(){
        this.showModal9 = !this.showModal9

      },
      toggleModal10(){
        this.showModal10 = !this.showModal10
      }
    }
  }
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  padding: 0;
  margin: 0;
  display: flex;
  flex-direction: column;
  justify-content: center;

}

.dftop{
  height: 100%;
  width: 100%;
  background-size: cover;
  background-position: center;
  opacity: 0.4;
  z-index: 0;
}

.title p{
  font-size: 2.5rem; 
  color: white;
  text-align: center;

}

.details{
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    width:100%;
    height: 10%;
    
}
.details div{
    display: flex;
    justify-content: space-evenly;
    list-style: none;
    font-size: 1.2rem;
}

.maps img {
    background-size: contain;
    background-position: center;
    border-radius: 15px;
    height:100%;
    width: 100%;
}



.ThOME{
  /*background-image:url("https://source.unsplash.com/random/") ;*/
  background-position: center;
  color:white;
  width: 100vw;
  height: 50vh;
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  align-items: center;
}
.Survey{
  width:200px;
  height:200px;
  background-color: #222222;
  color:tomato;
  border-radius: 15px;
  display: flex;
  align-items: center;
  justify-items: center;
  cursor: pointer;
}
.Survey p{
  font-size: 1.2rem;
}


.grid{
  width: 100vw;
  height:100%;
  background-color: #181818;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  gap: 10px;
  padding-top: 30px;
  padding-bottom: 30px;
}
.grid button {
width: 600px;
height: 250px;
cursor: pointer;
border-radius: 15px;
background-repeat: no-repeat;
background-position: center;
background-size: cover;
}

footer{
  background-color: aqua;
}

/*input range Slider bad good great */



@media only screen and (max-width: 600px){
  .grid button {
    width:350px
  }
  .Survey{
    margin-left: 20px;
  }
}


</style>
