<template>
    <div class="col-12 col-sm-6 col-md-4 col-lg-3">
        <div class="character text-center">
            <img :src="character.image" :alt="character.alt">
            <h4 class="text-uppercase">{{ character.name }}</h4>
            <div>{{ character.status }}</div>
            <div class="font-weight-bold">{{ character.species }}</div>
        </div>
        
    </div>
</template>

<script>
    export default {
        name: 'CharacterCard',
        props: ['character']
    }
</script>

<style lang="scss" scoped>
img{
    border-radius: 50%;
}
</style>