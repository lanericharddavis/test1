<template>
  <header class="container-fluid">
    <div class="row">
      <div class="col">
<h1>Click The Button || The Game</h1>
      </div>
    </div>
  </header>

  <main class="container-fluid">
    <div class="row">
      <div class="col">
    <h3>Go Ahead... Click It</h3>
      <button class="btn btn-success" @click="count" :disabled="state.value >= 100">Click ME!</button>
      <p>You have clicked the button {{ state.value }} times.</p>
      <h4 v-if="state.value > 1 && state.value < 10">Congrats. You can click the button.</h4>
      <h4 v-if="state.value >= 10 && state.value < 20">Good Job.</h4>
      <h4 v-if="state.value >= 20 && state.value < 30">Clickity clickity click....</h4>
      <h4 v-if="state.value >= 30 && state.value < 40">Ok, settle down there cowboy.</h4>
      <h4 v-if="state.value >= 40 && state.value < 50">Alright, you're really getting into this.</h4>
      <h4 v-if="state.value >= 50 && state.value < 60">50 clicks, impressive.</h4>
      <h4 v-if="state.value >= 60 && state.value < 70">You still clicking?</h4>
      <h4 v-if="state.value >= 70 && state.value < 80">Awesome! This is the end btw.</h4>
      <h4 v-if="state.value >= 80 && state.value < 90">Seriously, go home.</h4>
      <h4 v-if="state.value >= 90 && state.value < 100">I'm not playing anymore, you lost your clicking privileges.</h4>
      <h4 v-if="state.value >= 100">No more clicking.  For real this time.</h4>
      </div>
    </div>

  </main>

  <footer class="container-fluid ">
  <p>Page created by Lane Davis with the help of <img class="smallVue" alt="Vue logo" src="./assets/logo.png">ue</p>
  </footer>
</template>

<script>
import { reactive } from 'vue'
export default {
  setup() {
    const state = reactive({
        value: 0
      })
    return {
      state,
      count(){
        state.value++
      }
    }
  },
}
</script>

<style>
#app {
  text-align: center;
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

main{
  flex-grow: 1;
}

.smallImage{
  height: 10rem;
  width: 10rem;
}

.smallVue{
  height: 1em;
}
</style>

