<template>
<div class="ThOME">

  <img width="100" alt="Flag of Mauritius" src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/77/Flag_of_Mauritius.svg/512px-Flag_of_Mauritius.svg.png"/>
  <h2>Mo Local</h2>
  <div>
<svg class="waves" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"
viewBox="0 24 150 28" preserveAspectRatio="none" shape-rendering="auto">
<defs>
<path id="gentle-wave" d="M-160 44c30 0 58-18 88-18s 58 18 88 18 58-18 88-18 58 18 88 18 v44h-352z" />
</defs>
<g class="parallax">
<use xlink:href="#gentle-wave" x="48" y="0" fill="tomato" />
<use xlink:href="#gentle-wave" x="48" y="3" fill="cornflowerblue" />
<use xlink:href="#gentle-wave" x="48" y="5" fill="yellow" />
<use xlink:href="#gentle-wave" x="48" y="7" fill="limegreen" />
</g>
</svg>
</div>
  
</div>

 <div v-if="showModal1">
  <Modal @close="toggleModal1">
       
    <div class="title">
      <!-- v-for="title in titles" :key="title" kav servi pu display all item in array <p>{{title}}</p> -->
      <p>{{titles.br}}</p>
    </div>

    <template v-slot:ratings>
      <div class="details" v-for="item in fix" :key="item">{{item}}</div>
      <div class="detailval" v-for="items in BR" :key="items">{{items}}</div>
    </template>

    <template v-slot:map>
      <div class="maps">
        <img :src="`${maps.br}`" alt="not loaded" />
      </div>
    </template>
  </Modal>
 </div>

 <div v-if="showModal2">
  <Modal @close="toggleModal2">
       
       <div class="title">
         <p>{{titles.svn}}</p>
       </div>
   
       <template v-slot:ratings>
        <div class="details" v-for="item in fix" :key="item">{{item}}</div>
        <div class="detailval" v-for="items in SVN" :key="items">{{items}}</div>
       </template>
   
       <template v-slot:map>
         <div class="maps">
           <img :src="`${maps.svn}`" alt="."/> 
         </div>
       </template>
  </Modal>
 </div>

 <div v-if="showModal3">
  <Modal @close="toggleModal3">
       
       <div class="title">
         <p>{{titles.pl}}</p>
       </div>
   
       <template v-slot:ratings>
        <div class="details" v-for="item in fix" :key="item">{{item}}</div>
        <div class="detailval" v-for="items in PL" :key="items">{{items}}</div>
       </template>
   
       <template v-slot:map>
         <div class="maps">
           <img :src="`${maps.pl}`" alt="."/> 
         </div>
       </template>
  </Modal>
 </div>

 <div v-if="showModal4">
  <Modal @close="toggleModal4">
       
       <div class="title">
         <p>{{titles.pw}}</p>
       </div>
   
       <template v-slot:ratings>
        <div class="details" v-for="item in fix" :key="item">{{item}}</div>
        <div class="detailval" v-for="items in PW" :key="items">{{items}}</div>
       </template>
   
       <template v-slot:map>
         <div class="maps">
           <img :src="`${maps.pw}`" alt="."/> 
         </div>
       </template>
  </Modal>
 </div>

 <div v-if="showModal5">
  <Modal @close="toggleModal5">
       
       <div class="title">
         <p>{{titles.moka}}</p>
       </div>
   
       <template v-slot:ratings>
        <div class="details" v-for="item in fix" :key="item">{{item}}</div>
        <div class="detailval" v-for="items in MOKA" :key="items">{{items}}</div>
       </template>
   
       <template v-slot:map>
         <div class="maps">
           <img :src="`${maps.moka}`" alt="."/> 
         </div>
       </template>
  </Modal>
 </div>
 
 <div v-if="showModal6">
  <Modal @close="toggleModal6">
       
       <div class="title">
         <p>{{titles.pample}}</p>
       </div>
   
       <template v-slot:ratings>
        <div class="details" v-for="item in fix" :key="item">{{item}}</div>
        <div class="detailval" v-for="items in PAMPLE" :key="items">{{items}}</div>
       </template>
   
       <template v-slot:map>
         <div class="maps">
           <img :src="`${maps.pample}`" alt="."/> 
         </div>
       </template>
  </Modal>
 </div>

 <div v-if="showModal7">
  <Modal @close="toggleModal7">
       
       <div class="title">
         <p>{{titles.gp}}</p>
       </div>
   
       <template v-slot:ratings>
        <div class="details" v-for="item in fix" :key="item">{{item}}</div>
        <div class="detailval" v-for="items in GP" :key="items">{{items}}</div>
       </template>
   
       <template v-slot:map>
         <div class="maps">
           <img :src="`${maps.gp}`" alt="."/> 
         </div>
       </template>
  </Modal>
 </div>

 <div v-if="showModal8">
  <Modal @close="toggleModal8">
       
       <div class="title">
         <p>{{titles.flq}}</p>
       </div>
   
       <template v-slot:ratings>
        <div class="details" v-for="item in fix" :key="item">{{item}}</div>
        <div class="detailval" v-for="items in FLQ" :key="items">{{items}}</div>
       </template>
   
       <template v-slot:map>
         <div class="maps">
           <img :src="`${maps.flq}`" alt="."/> 
         </div>
       </template>
  </Modal>
 </div>

 <div v-if="showModal9">
  <Modal @close="toggleModal9">
       
       <div class="title">
         <p>{{titles.rdr}}</p>
       </div>
   
       <template v-slot:ratings>
        <div class="details" v-for="item in fix" :key="item">{{item}}</div>
        <div class="detailval" v-for="items in RDR" :key="items">{{items}}</div>
       </template>
   
       <template v-slot:map>
         <div class="maps">
           <img :src="`${maps.rdr}`" alt="."/> 
         </div>
       </template>
  </Modal>
 </div>

 <div v-if="showModal10">
  <Modal @close="toggleModal10">
       
       <div class="title">
         <p>{{titles.rdg}}</p>
       </div>
   
       <template v-slot:ratings>
        <div class="details" v-for="item in fix" :key="item">{{item}}</div>
        <div class="detailval" v-for="items in RDG" :key="items">{{items}}</div>
       </template>
   
       <template v-slot:map>
         <div class="maps">
           <img :src="`${maps.rdg}`" alt="."/> 
         </div>
       </template>
  </Modal>
 </div>

 <div v-if="showSurvey">
  <Survey @closeSurvey="toggleSurvey">
  </Survey>

 </div>



<section class="grid">
  
  <!-- v-for="btntle in btntitle.slice(1,2)" :key="btntle" in array btntitle -->
 <button style="background-image:url(https://cdn.sanity.io/images/e7woiqxp/production/146d85c61c7af2b3539d5004994270b7f07ee9db-1400x974.jpg?w=2000&fit=max&auto=format)"
 @click="toggleModal1">{{titles.br}}</button>

 <button style="background-image:url(https://cdn.sanity.io/images/e7woiqxp/production/2361c8951baad05401955038d2b893053b030485-1243x1303.jpg?w=2000&fit=max&auto=format)"
 @click="toggleModal2">{{titles.svn}}</button>

 <button style="background-image:url(https://cdn.sanity.io/images/e7woiqxp/production/c1e1d5ef19744aba3bff6b66ffdf6055c0cb39ec-2048x875.jpg?w=2000&fit=max&auto=format)"
 @click="toggleModal3">{{titles.pl}}</button>

 <button style="background-image:url(https://cdn.sanity.io/images/e7woiqxp/production/21b390df9a8f8d77d6e5ee8107c4c6359bb3de34-1100x732.jpg?w=2000&fit=max&auto=format)"
 @click="toggleModal4">{{titles.pw}}</button>

 <button style="background-image:url(https://cdn.sanity.io/images/e7woiqxp/production/f6035ecffe9e28d8af8dae6c663f4d2797adca3b-1600x900.jpg?w=2000&fit=max&auto=format)"
 @click="toggleModal5">{{titles.moka}}</button>

 <button style="background-image:url(https://cdn.sanity.io/images/e7woiqxp/production/3158ebf725b7816a9fa69df490e70d552c2a2056-1024x768.jpg?w=2000&fit=max&auto=format)"
 @click="toggleModal6">{{titles.pample}}</button>

 <button style="background-image:url(https://cdn.sanity.io/images/e7woiqxp/production/a76af7843510a36d54a4429a40aeef055fcdbb6c-1024x768.jpg?w=2000&fit=max&auto=format)"
 @click="toggleModal7">{{titles.gp}}</button>

 <button style="background-image:url(https://cdn.sanity.io/images/e7woiqxp/production/c2d16540dbd945da75a8434bb273024124b9ec73-1280x720.jpg?w=2000&fit=max&auto=format)"
 @click="toggleModal8">{{titles.flq}}</button>

 <button style="background-image:url(https://cdn.sanity.io/images/e7woiqxp/production/6c088b7f878c304a7058a3fb51ca76ea8b70b149-1232x822.jpg?w=2000&fit=max&auto=format)"
 @click="toggleModal9">{{titles.rdr}}</button>

 <button style="background-image:url()"
 @click="toggleModal10">{{titles.rdg}}</button>

</section>


<footer>
  <h5>Find an issue with this page?</h5>
  
  <a href="https://github.com/AbhishekBeegun/molocalvue" target="_blank" rel="noreferrer">Fix it on GitHub</a>
   
  <marquee @click="toggleSurvey">Take a survey to get 1 year of good luck</marquee>
  <p>Copyright © 2022 Abhishek Beegun</p>
</footer>


</template>

<script>
const baseURL = "https://abhishekbeegun.github.io/Data/molocal.json";


import Modal from './components/Modal.vue';
import Survey from './components/Survey.vue';
export default {
  name: 'App',

  components:{Modal,Survey},


  data(){
      return{
        btntitle:['Riviere Du Rempart','Savanne','Port Louis','Plaine Willhems','Moka','Pamplemousse','Grand Port','Flacq','Black River','Rodrigues'],
        titles:[],
        fix:[],
        imgs:[],
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
        showSurvey: false,
      }
    },

    mounted(){
      fetch(`${baseURL}`)
      .then(res => res.json())
      .then(data => this.titles = data[0])
      .catch(err => console.log(err.message))

      fetch(`${baseURL}`)
      .then(res => res.json())
      .then(data => this.fix = data[13])

      fetch(`${baseURL}`)
      .then(res => res.json())
      .then(data => this.RDR = data[1])

      fetch(`${baseURL}`)
      .then(res => res.json())
      .then(data => this.SVN = data[2])

      fetch(`${baseURL}`)
      .then(res => res.json())
      .then(data => this.PL = data[3])

      fetch(`${baseURL}`)
      .then(res => res.json())
      .then(data => this.PW = data[4])

      fetch(`${baseURL}`)
      .then(res => res.json())
      .then(data => this.MOKA = data[5])

      fetch(`${baseURL}`)
      .then(res => res.json())
      .then(data => this.PAMPLE = data[6])

      fetch(`${baseURL}`)
      .then(res => res.json())
      .then(data => this.GP = data[7])

      fetch(`${baseURL}`)
      .then(res => res.json())
      .then(data => this.FLQ = data[8])

      fetch(`${baseURL}`)
      .then(res => res.json())
      .then(data => this.BR = data[9])

      fetch(`${baseURL}`)
      .then(res => res.json())
      .then(data => this.RDG = data[10])

      fetch(`${baseURL}`)
      .then(res => res.json())
      .then(data => this.maps = data[11])



      //fetch('http://localhost:3000/SVN')
      //.then(res => res.json())
      //.then(data => this.SVN = data)
    },


    methods:{

      toggleSurvey(){
        this.showSurvey = !this.showSurvey
      },

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
  overflow-x: hidden;

}

.title p{
  font-size: 2rem; 
  color: white;
  text-align: center;

}

.details{
    display: flex;
    flex-direction: row;
    align-items: center;
    text-align: left;
    width: 50%;
    height: 10%;
    list-style: none;
    font-size: 1.2rem;
    color: black;
}
.detailval{
    display: flex;
    flex-direction: column;
    text-align: right;
    justify-content: center;
    width:50%;
    height: 10%;
    font-size:1.2rem;
    list-style: none;
    color: black; 
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
  position: relative;
 /* background-image:url("https://source.unsplash.com/random/") ;*/
  background-color: black;
  color:white;
  width: 100vw;
  height: 50vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
.ThOME div {
  position: absolute;
  bottom: 0;
  width: 100vw;
}
.ThOME h2{
  padding-left: 25px;
  font-size: 2rem;
}
.ThOME img{
  border-radius: 10px;
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
border: 0px;
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
  z-index: 1;
  /*problem with marquee when on Survey TO CHECK */
}
footer p{
  font-size: 0.7rem;
}

.waves {
  position:relative;
  width: 100%;
  height:15vh;
  margin-bottom:-7px;
  min-height:100px;
  max-height:150px;
}

.parallax > use {
  animation: move-forever 25s cubic-bezier(.55,.5,.45,.5)     infinite;
}
.parallax > use:nth-child(1) {
  animation-delay: -2s;
  animation-duration: 7s;
}
.parallax > use:nth-child(2) {
  animation-delay: -3s;
  animation-duration: 10s;
}
.parallax > use:nth-child(3) {
  animation-delay: -4s;
  animation-duration: 13s;
}
.parallax > use:nth-child(4) {
  animation-delay: -5s;
  animation-duration: 20s;
}
@keyframes move-forever {
  0% {
   transform: translate3d(-90px,0,0);
  }
  100% { 
    transform: translate3d(85px,0,0);
  }
}

@media (max-width: 768px) {
  .waves {
    height:40px;
    min-height:40px;
  }
  .content {
    height:30vh;
  }
  h1 {
    font-size:24px;
  }
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
