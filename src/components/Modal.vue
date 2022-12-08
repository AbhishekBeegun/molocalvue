<template>
    <div class="backdrop" @click.self="closeModal">
        <p class="fakeclosebtn" @click="closeModal">X</p>
        <div class="modal">


            <div class="imgtop">
             <slot></slot>
            </div>
        
        
        <section class="clmrw">

        <div class = "rate">
            <div class="fixedrate">
                    <li>🏆 Overall Score</li>
                    <li>❤️ Liked by residents</li>
                    <li>🦺 Safety</li>
                    <li>🚦 Traffic density</li>
                    <li>🙃 Happiness</li>
                    <li>👪 Population</li>
                    <li>🌡️ Temperature</li>
                    <li>🏢 Place to work</li>
                    <li>🥳 Fun / Nightlife</li>
                    <li>🚶 Walkability</li>
            </div>


            <div class="variblerate">
            <slot name="ratings">
             
            </slot>

        </div>
        </div>

        <div class="maps">
            <slot name="map"></slot>
        </div>

        </section>

        </div>
    </div>  
</template>

<script>
export default {
    props:[ ],

    methods : {
        closeModal () {
            this.$emit('close')
        }
    }
}
</script>

<style scoped>
.modal{
    width:65vw;
    height: 90vh;
    padding: 0px;
    margin: 20px auto;
    border-radius: 15px;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap:10px;
}

.imgtop{
    width:100%;
    height: 25vh;
    background-color:pink;
    border-radius: 15px;
    box-sizing: border-box;
}
.clmrw{
    display: flex;
    flex-direction: row;
    height: 100%;
    width: 100%;
    box-sizing: border-box;
    justify-content: space-evenly;
    gap:10px;    
}
.rate{
    display: flex;
    flex-direction: row;
    width:100%;
    height:100%;
    background-color: white;
    border-radius:15px;
    box-sizing: border-box;
    padding: 10px;
}
.maps{
    width: 100%;
    height: 100%;
    background: blue;
    border-radius: 15px;
    box-sizing: border-box;
}
.fixedrate{
    width: 50%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
}
.fixedrate li{
    list-style: none;
    font-size: 1.2rem;
    text-align: center;
}

.backdrop {
    top:0;
    position: fixed;
    background: rgba(0,0,0,0.7);
    width: 100%;
    height: 100%;
}
.fakeclosebtn{
    position: fixed;
    color: white;
    font-size:2rem;
    right:20px;
    top:10px;
    cursor:pointer;
    font-weight: bold;
}
@media only screen and (max-width: 600px){
    .modal{
     width:100vw;
     height: 100%;
     margin:0px;
    }
    .imgtop{
        border-radius: 0px;
    }
    .clmrw{
    flex-direction: column;
    padding: 0px;
    margin-top:-10px
    }
    .maps{
        display: none;
    }
}
</style>