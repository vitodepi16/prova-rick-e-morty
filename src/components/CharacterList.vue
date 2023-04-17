<template>
  <main>
    <section class="container">
      <div class="row">
          <CharacterCard v-for="(character,index) in store.characterList" :key="character.id" :character="character"/>
   
          
      </div>
   
    </section>
  </main>
</template>

<script>
import {store } from '../../data/store';
import CharacterCard from './CharacterCard.vue';
    export default {
        name: 'CharacterList', 
        components:{
          CharacterCard
        },
        data(){
          return{
            store
          }
        }
    }
</script>

<style lang="scss" scoped>

</style>