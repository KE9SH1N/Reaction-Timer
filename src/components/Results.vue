<template>
  <p>Reaction Time: {{ score }} ms </p>
  <p class="rank">{{rank}}</p>
</template>

<script>
export default {
    props: ['score'],
    data(){
        return{
            rank: null
        }
    },
    mounted(){
        if(this.score < 250){
            this.rank = 'Samurai'
        }
        else if(this.score < 350){
            this.rank = 'Soldier'
        }
        else if(this.score < 500){
            this.rank = 'Noob'
        }
        else{
            this.rank = 'Bot'
        }
    },
}
</script>

<style>
    .rank{
        font-size: 1.4em;
        color: #0faf87;
        font-weight: bold;
    }
</style>