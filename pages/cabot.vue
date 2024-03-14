<template>
  <div>
    <button @click="obtenerCotizacion">pulsa</button>
   {{  datosjson}}
   </div>
</template>

<script>
export default {
  name: 'CabotPage',
  data ()
  {
    return{
      datosjson:[],
    }
  },
  methods:{
    async obtenerCotizacion(){
       const response = await this.$axios.$get('http://localhost:8000/shop');
        this.datosjson = response;
      
    },
  }
}
</script>


