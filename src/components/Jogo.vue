<template>
    <div class="jogo">

       <Forca
       :erros = "erros"
       />

       <Palavra
       :palavra = "palavra"
       :dica = "dica"
       :verificarLetra = "verificarLetra"
       :etapa="etapa"
       />

       <Teclado 
       v-if = "etapa === 'jogo'" 
       :letras = "letras"
       :verificarLetra = "verificarLetra"
       :jogar = "jogar"
       />

       <Final 
       :etapa="etapa"
       v-if="etapa != 'jogo'"
       :texto = "etapa === 'ganhador' ? 'Parabéns :)' : 'Tadinho :('"
       :jogarNovamente="jogarNovamente"
       />

    </div>
</template>

<script>
import Forca from './Forca.vue'
import Palavra from './Palavra.vue'
import Teclado from './Teclado.vue'
import Final from './final.vue'

 export default 
 {
    name: 'Jogo-Name',
    props:
    {
        erros: Number,
        palavra: String,
        dica: String,
        verificarLetra: Function,
        etapa: String,
        letras: Array,
        jogar: Function,
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
        Forca,
        Palavra,
        Teclado,
        Final
    }
  }

</script>

<style>

.jogo
{
   width: 100%;
   display: flex;
   flex-direction: column;
   align-items: center;
   text-align: center;
}
  
</style>