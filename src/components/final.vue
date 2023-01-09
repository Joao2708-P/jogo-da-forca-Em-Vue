<template>
    <div class="final">

        <div :class="`texto-final ${etapa}`">
            {{ texto }}
        </div>

        <button class="final-botao" v-on:click="jogarNovamente">Jogar Novamente</button>
    </div>
</template>

<script>

 export default 
 {
    name: 'final-Name',
    props:
    {
      etapa: String,
      texto: String,
      jogarNovamente: Function
    },

    data()
    {
       return{
         
       }
    },

    methods: {

    },

    components:
    {
        
    }
  }

</script>

<style>

.texto-final
{
    margin: 20px 0px;
    font-size: 24px;
    font-weight: bold;
}

.texto-final.enforcado
{
   color: var(--color-text-error);
}

.texto-final.ganhador
{
    color: var( --color-text-success);
}

</style>