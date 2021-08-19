<template>
    <div> 
    <div v-if="currentScore < 10"> 
          <button v-on:click="currentScore++" class="cleanButton">
         <img src="@/assets/Bag.jpeg">
          </button>
    </div>
    <div v-else>
          <button  class="cleanButton">
         <img src="@/assets/bagBroken.png">
          </button>
          <div>
          <button v-on:click="currentScore = 0">Reset</button>
          </div>
    </div>
            <p>currentScore: {{currentScore}}</p>
    </div>
</template>

<script>
export default {
      data(){
            return{
                  broken: Boolean = false,
                  currentScore: Number = 0,

            }
      }
}
</script>

<style>
      .cleanButton{
            all:unset;
      }

</style>