<template>
  <div class="backdrop" @click.self="closeSurvey">
    <p class="fakeclosebtn" @click="closeSurvey">X</p>
    <div class="modal">

        <form>
            <label>Select a District :</label>
            <select id="District">
             <option value="br">Black River</option>
             <option value="svn">Savanne</option>
             <option value="pl">Port Louis</option>
             <option value="pw">Plaine Willhems</option>
             <option value="moka">Moka</option>
             <option value="pample">Pamplemousse</option>
             <option value="gp">Grand Port</option>
             <option value="flq">Flacq</option>
             <option value="rdr">Riv Du Rempart</option>
             <option value="rdg">Rodrigues</option>
             <option value="mars">E&M</option>
            </select>

            <label>❤️ or 👎 </label>
            <select id="lr">
                <option value="like">❤️</option>
                <option value="dislike">👎</option>
            </select>

            <label>🦺 Safety :</label>
            <select id="s">
                <option value="great">Great</option>
                <option value="good">Good</option>
                <option value="bad">Bad</option>
            </select>

            <label>🚦 Traffic :</label>
            <select id="td">
                <option value="great">Clear</option>
                <option value="bad">Good</option>
                <option value="clear">Bad</option>
            </select>

            <label>🙃 Happiness (0 - 100)</label>
            <input type="range" id="h" min="0" max="100">

            <label>🏢 Place to work :</label>
            <select id="pw">
                <option value="great">Great</option>
                <option value="good">Good</option>
                <option value="bad">Bad</option>
            </select>

            <label>🥳 Fun / Nightlife :</label>
            <select id="fn">
                <option value="great">Great</option>
                <option value="good">Good</option>
                <option value="bad">Bad</option>
            </select>

            <label>🚶 Walkability :</label>
            <select id="w">
                <option value="great">Great</option>
                <option value="good">Good</option>
                <option value="bad">Bad</option>
            </select>

            <input type="submit" disabled>
        </form>

    </div>
  
  </div>
</template>

<script>
export default {
    methods : {
        closeSurvey () {
            this.$emit('closeSurvey')
        },
    }

}
</script>

<style scoped>

.modal{
  background: rgba(0,0,0,0);
  backdrop-filter: blur(10px);
  z-index: 1;
}
.backdrop{
    background: rgba(0,0,0,0.0);
}
form{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100%;
    width: 100%;
}

.fakeclosebtn{
    z-index: 1;
}
label{
    font-size:1.1rem;
    color: white;
    padding: 10px;
}
select{
    font-size: 1.2rem;

}

</style>