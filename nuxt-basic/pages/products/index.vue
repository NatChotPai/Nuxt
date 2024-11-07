<template>
    <div>
        <h1>สินค้าทั้งหมด</h1>
        <ul v-for="product in data.products" v-bind:key="product.products">
            <li>{{ product.title }}</li>
        </ul>
    </div>
</template>

<script setup>
const { data: data } = await useFetch('https://dummyjson.com/products')
console.log(data)

useHead(
    {
        title:"Product Page Website",
        meta:[
            {name:"Description" , content:"รายการสินค้า"}
        ]
    }
)
</script>

<style scoped></style>