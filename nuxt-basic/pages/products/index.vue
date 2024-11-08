<template>
    <div class="container">
        <div v-for="product in data.products" v-bind:key="product.products"> 
            <NuxtLink :to="`/products/${product.id}`">
                <h2 class="title"> {{ product.title }} </h2>
            </NuxtLink>
            <img :src=product.thumbnail>
        </div>
    </div>
</template>

<script setup>
const { data: data } = await useFetch('https://dummyjson.com/products?limit=30')

useHead(
    {
        title:"NatShop | Product Page Website",
        meta:[
            {name:"Description" , content:"รายการสินค้า"}
        ]
    }
)
</script>

<style scoped>
.container{
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}

.container div{
    width: 300px;
    height: 300px;
    margin: 30px 15px;
    background: #333;
}

.container div:hover{
    background: #c7b6b6;
}

.title{
    color: white;
    text-align: center;
    font-size: 1.2em;
}

.img{
    width: 300px;
    height: 300px;
}

a {
    text-decoration: none;
}
</style>