 <script setup>
 import { ref } from 'vue';
 const numero = ref(0);
 const props = defineProps({
    guitarra: {
        type: Object,
        required: true
    }
 });
                    
</script>
<template>
      <div  class="col-md-6 col-lg-4 my-4 row align-items-center">
                <div class="col-4">
                    <img class="img-fluid" v-bind:src="'/img/' + guitarra.imagen + '.jpg'" :alt="'imagen guitarra' + guitarra.nombre">
                </div>
                <div class="col-8">
                    <h3 class="text-black fs-4 fw-bold text-uppercase">{{guitarra.nombre}}</h3>
                    <p>{{guitarra.descripcion}}</p>
                    <p class="">{{ numero }}</p>
                    <p class="fw-black text-primary fs-3">${{guitarra.precio}}</p>
                    <button 
                        type="button"
                        class="btn btn-dark w-100 "
                        @click="incrementar"
                    >Agregar al Carrito
                </button>
                </div>
            </div>
</template>


<style lang="scss" scoped>

</style>