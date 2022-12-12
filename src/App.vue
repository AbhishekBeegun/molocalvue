<template>
<div class="ThOME">
   <div class="Survey">
    <p>Complete a survey to get 1 year of luck</p>
   </div>
   <h1>{{title}}</h1>
</div>

 <div v-if="showModal1">
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
        <img :src="`${mapss.rdr}`" alt="."/> 
      </div>
    </template>
  </Modal>
 </div>


 <div v-if="showModal2">
  <Modal @close="toggleModal2">
       
       <div class="title" v-for="title in titles" :key="title">
         <p>{{title.svn}}</p>
       </div>
   
       <template v-slot:ratings>
         <div class="details" v-for="value in SVN" :key="value">
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
           <img :src="`${mapss.svn}`" alt="."/> 
         </div>
       </template>
  </Modal>
 </div>

 <div v-if="showModal3">
  <Modal @close="toggleModal3">
       
       <div class="title" v-for="title in titles" :key="title">
         <p>{{title.pl}}</p>
       </div>
   
       <template v-slot:ratings>
         <div class="details" v-for="value in PL" :key="value">
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
           <img :src="`${mapss.pl}`" alt="."/> 
         </div>
       </template>
  </Modal>
 </div>

 <div v-if="showModal4">
  <Modal @close="toggleModal4">
       
       <div class="title" v-for="title in titles" :key="title">
         <p>{{title.pw}}</p>
       </div>
   
       <template v-slot:ratings>
         <div class="details" v-for="value in PW" :key="value">
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
           <img :src="`${mapss.pw}`" alt="."/> 
         </div>
       </template>
  </Modal>
 </div>

 <div v-if="showModal5">
  <Modal @close="toggleModal5">
       
       <div class="title" v-for="title in titles" :key="title">
         <p>{{title.moka}}</p>
       </div>
   
       <template v-slot:ratings>
         <div class="details" v-for="value in MOKA" :key="value">
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
           <img :src="`${mapss.moka}`" alt="."/> 
         </div>
       </template>
  </Modal>
 </div>
 
 <div v-if="showModal6">
  <Modal @close="toggleModal6">
       
       <div class="title" v-for="title in titles" :key="title">
         <p>{{title.pample}}</p>
       </div>
   
       <template v-slot:ratings>
         <div class="details" v-for="value in PAMPLE" :key="value">
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
           <img :src="`${mapss.pample}`" alt="."/> 
         </div>
       </template>
  </Modal>
 </div>

 <div v-if="showModal7">
  <Modal @close="toggleModal7">
       
       <div class="title" v-for="title in titles" :key="title">
         <p>{{title.gp}}</p>
       </div>
   
       <template v-slot:ratings>
         <div class="details" v-for="value in GP" :key="value">
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
           <img :src="`${mapss.gp}`" alt="."/> 
         </div>
       </template>
  </Modal>
 </div>

 <div v-if="showModal8">
  <Modal @close="toggleModal8">
       
       <div class="title" v-for="title in titles" :key="title">
         <p>{{title.flq}}</p>
       </div>
   
       <template v-slot:ratings>
         <div class="details" v-for="value in FLQ" :key="value">
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
           <img :src="`${mapss.flq}`" alt="."/> 
         </div>
       </template>
  </Modal>
 </div>

 <div v-if="showModal9">
  <Modal @close="toggleModal9">
       
       <div class="title" v-for="title in titles" :key="title">
         <p>{{title.br}}</p>
       </div>
   
       <template v-slot:ratings>
         <div class="details" v-for="value in BR" :key="value">
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
           <img :src="`${mapss.br}`" alt="."/> 
         </div>
       </template>
  </Modal>
 </div>

 <div v-if="showModal10">
  <Modal @close="toggleModal10">
       
       <div class="title" v-for="title in titles" :key="title">
         <p>{{title.rdg}}</p>
       </div>
   
       <template v-slot:ratings>
         <div class="details" v-for="value in RDG" :key="value">
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
           <img :src="`${mapss.rdg}`" alt="."/> 
         </div>
       </template>
  </Modal>
 </div>



<section class="grid">

 <button v-for="btntle in btntitle.slice(0,1)" :key="btntle" style="background-image:url(https://cdn.sanity.io/images/e7woiqxp/production/6c088b7f878c304a7058a3fb51ca76ea8b70b149-1232x822.jpg?w=2000&fit=max&auto=format)"
 @click="toggleModal1">{{btntle}}</button>

 <button v-for="btntle in btntitle.slice(1,2)" :key="btntle" style="background-image:url(https://cdn.sanity.io/images/e7woiqxp/production/2361c8951baad05401955038d2b893053b030485-1243x1303.jpg?w=2000&fit=max&auto=format)"
 @click="toggleModal2">{{btntle}}</button>

 <button v-for="btntle in btntitle.slice(2,3)" :key="btntle" style="background-image:url(https://cdn.sanity.io/images/e7woiqxp/production/c1e1d5ef19744aba3bff6b66ffdf6055c0cb39ec-2048x875.jpg?w=2000&fit=max&auto=format)"
 @click="toggleModal3">{{btntle}}</button>

 <button v-for="btntle in btntitle.slice(3,4)" :key="btntle" style="background-image:url(https://cdn.sanity.io/images/e7woiqxp/production/21b390df9a8f8d77d6e5ee8107c4c6359bb3de34-1100x732.jpg?w=2000&fit=max&auto=format)"
 @click="toggleModal4">{{btntle}}</button>

 <button v-for="btntle in btntitle.slice(4,5)" :key="btntle" style="background-image:url(https://cdn.sanity.io/images/e7woiqxp/production/f6035ecffe9e28d8af8dae6c663f4d2797adca3b-1600x900.jpg?w=2000&fit=max&auto=format)"
 @click="toggleModal5">{{btntle}}</button>

 <button v-for="btntle in btntitle.slice(5,6)" :key="btntle" style="background-image:url(https://cdn.sanity.io/images/e7woiqxp/production/3158ebf725b7816a9fa69df490e70d552c2a2056-1024x768.jpg?w=2000&fit=max&auto=format)"
 @click="toggleModal6">{{btntle}}</button>

 <button v-for="btntle in btntitle.slice(6,7)" :key="btntle" style="background-image:url(https://cdn.sanity.io/images/e7woiqxp/production/a76af7843510a36d54a4429a40aeef055fcdbb6c-1024x768.jpg?w=2000&fit=max&auto=format)"
 @click="toggleModal7">{{btntle}}</button>

 <button v-for="btntle in btntitle.slice(7,8)" :key="btntle" style="background-image:url(https://cdn.sanity.io/images/e7woiqxp/production/c2d16540dbd945da75a8434bb273024124b9ec73-1280x720.jpg?w=2000&fit=max&auto=format)"
 @click="toggleModal8">{{btntle}}</button>

 <button v-for="btntle in btntitle.slice(8,9)" :key="btntle"  style="background-image:url(https://cdn.sanity.io/images/e7woiqxp/production/146d85c61c7af2b3539d5004994270b7f07ee9db-1400x974.jpg?w=2000&fit=max&auto=format)"
 @click="toggleModal9">{{btntle}}</button>

 <button v-for="btntle in btntitle.slice(9,10)" :key="btntle" style="background-image:url()"
 @click="toggleModal10">{{btntle}}</button>

</section>


<footer>
  <h5>Find an issue with this page?</h5>
  
  <a href="https://github.com/AbhishekBeegun/molocalvue" target="_blank" rel="noreferrer">Fix it on GitHub</a>

  <marquee>Take a survey to get 1 year of good luck</marquee>

  <p>Copyright © 2022 Abhishek Beegun</p>
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
        btntitle:['Riviere Du Rempart','Savanne','Port Louis','Plaine Willhems','Moka','Pamplemousse','Grand Port','Flacq','Black River','Rodrigues'],
        titles:[],
        img:[],
        maps:[],
        RDR:[],
        SVN:[],
        PL:[],
        PW:[],
        MOKA:[],
        PAMPLE:[],
        GP:[],
        FLQ:[],
        BR:[],
        RDG:[],


        showModal1: false,
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

      fetch('http://localhost:3000/PL')
      .then(res => res.json())
      .then(data => this.PL = data)

      fetch('http://localhost:3000/PW')
      .then(res => res.json())
      .then(data => this.PW = data)

      fetch('http://localhost:3000/MOKA')
      .then(res => res.json())
      .then(data => this.MOKA = data)

      fetch('http://localhost:3000/PAMPLE')
      .then(res => res.json())
      .then(data => this.PAMPLE = data)

      fetch('http://localhost:3000/GP')
      .then(res => res.json())
      .then(data => this.GP = data)

      fetch('http://localhost:3000/FLQ')
      .then(res => res.json())
      .then(data => this.FLQ= data)

      fetch('http://localhost:3000/BR')
      .then(res => res.json())
      .then(data => this.BR = data)

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
      },

      RandomColor(){
        this.colors[Math.floor(Math.random() * colors.length)]
        document.getElementById('imgtop').style.backgroundColor = this.RandomColor
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
  opacity: 1;
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
.details div:nth-child(2){
  padding:10px;
  color:black;
  border-radius: 10px;
}

.Green{
  background-color: limegreen;
}

.maps img{
    background-size: contain;
    background-position: center;
    border-radius: 15px;
    height:100%;
    width: 100%;
    overflow: hidden;
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
background-color: black;
background-size: cover;
font-size: 1.5rem;
color: white;
}

footer{
  background-color:white;
  height: 25vh;
  width: 100vw;
  color: black;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
}

footer a{
  color: cornflowerblue;
  text-decoration: none;
  font-size: 1.2rem;
  padding: 5px;
  border-radius: 10px;
}
footer marquee{
  cursor: pointer;
  padding: 10px;
  background-color: #222222;
  color: white;
}
footer p{
  font-size: 0.7rem;
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
