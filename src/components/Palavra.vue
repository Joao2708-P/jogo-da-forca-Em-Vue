<template>
    <div class="palavra">
         <div class="palavra-letras">
            <div class="palavra-letra" v-for="(letra,key) in palavra" :key="key">
                {{ (verificarLetra(letra) || etapa === 'enforcado') ? letra : '' }}
            </div>
         </div>

         <div class="palavra-dica">
            {{ dica }}
         </div>
    </div>
</template>

<script>


 export default 
 {
    name: 'palavra-Name',
    props:
    {
        palavra: String,
        dica: String,
        verificarLetra: Function,
        etapa: String
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
 
 .palavra
 {
    text-transform: uppercase;
    flex-direction: column;
    align-items: center;
    text-align: center;
 }

 .palavra-letras
 {
    display: flex;
    margin-bottom: 20px;
 }

.palavra-letra
{
  height: 30px;
  width: 30px;
  margin: 0px 5px;
  border-bottom: 1px solid var(--color-text-light);
  align-items: center;
  justify-content: center;
  display: flex;
}

</style>