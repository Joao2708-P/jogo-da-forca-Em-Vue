<template>
    <div class="forca">
        <img :src="`https://raw.githubusercontent.com/william-costa/wdev-hangman-game-resources/master/images/hangman/${erros}.svg`">
    </div>
</template>

<script>

 export default 
 {
    name: 'forca-name',
    props:
    {
        erros: Number
    },

    data()
    {
       return{
        
       }
    },

    methods: {

    }
  }

</script>

<style>

.forca img
{
   height: 100px;
}
  
</style>