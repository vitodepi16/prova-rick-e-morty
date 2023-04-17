<template>
  <div>
   <HeaderComponent/>
   <CharacterList/>

  </div>
</template>

<script>
import {store} from '../data/store.js';
import axios from 'axios';
import HeaderComponent from './components/HeaderComponent.vue';
import CharacterList from './components/CharacterList.vue';

  export default {
    name:'App',
    components: {
      HeaderComponent, CharacterList, 
    },
    data(){
      return{
        store
      }
    },
    methods:{
      getCharacters(){
        const url = store.baseUrl + store.endpoint
        axios.get(url).then((res)=>{
          console.log(res.data.results)
          store.characterList =  res.data.results
        });
      }
    },
    mounted(){
      store.endpoint = 'character'
      this.getCharacters();
    }
  }
</script>

<style lang="scss" scoped>

</style>