<template>
    <div id="products">
        <div v-for="element in products" class="individual_products">
            <img :src="element.image" alt="Product Image" width="100%"/>
            <p>{{ element.title }}</p>
            <p>{{ element.price }}</p>
            </div>

    </div>
</template>

<script setup>
    
    import { ref, onMounted,onUpdated } from 'vue';
    import axios from 'axios';

    const products=ref([]);


    

    onMounted (async()=>{
        axios.get('https://fakestoreapi.com/products')
        .then(function (response) {
          // handle success
          products.value=response.data
        })
        .catch(function (error) {
          // handle error
          console.log(error);
        })
        .finally(function () {
          // always executed
        });
    })


    const increment=()=>{
        count.value++;
    }
</script>

<style scoped>
#products{
    margin-top: 3%; 
    display: grid;
    grid-template-columns: repeat(4,1fr);
    grid-gap:3%;
    
}
.individual_products{
    display: flex;
    flex-direction: column;
}
</style>