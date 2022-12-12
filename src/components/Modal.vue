<template>
    <div class="backdrop" @click.self="closeModal">
        <p class="fakeclosebtn" @click="closeModal">X</p>
        <div class="modal">


            <div class="imgtop" @click="BackgroundColors = 'cornflowerblue'" >
             <slot></slot>
            </div>
        
        
        <section class="clmrw">

        <div class="rate">
            <slot name="ratings">
            </slot>
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
    data(){
        return{
            BackgroundColors:["tomato"],
        }
    },

    methods : {
        closeModal () {
            this.$emit('close')
        },
    }
}
</script>

<style>
.modal{
    width:70vw;
    height: 90vh;
    padding: 0px;
    margin: 20px auto;
    border-radius: 15px;

    display: flex;
    flex-direction: column;
    align-items: center;
    gap:15px;
}

.imgtop{
    width:100%;
    height: 25vh;
    border-radius: 15px;
    background: v-bind(BackgroundColors);
    display: flex;
    justify-content: center;
    align-items: center;
}
.clmrw{
    display: flex;
    flex-direction: row;
    height: 100%;
    width: 100%;
    box-sizing: border-box;
    justify-content: space-evenly;
    gap:15px;    
}
.rate{
    width:50%;
    height:100%;
    background-color: white;
    border-radius:15px;
    box-sizing: border-box;
    padding: 25px;
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
    font-size:4rem;
    right:100px;
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
    margin-top:-25px
    }
    .rate{
        width: 100%;
    }
    .maps{
        display: none;
    }
    .fakeclosebtn{
        right:20px;
        font-size: 2rem;
    }
}
</style>