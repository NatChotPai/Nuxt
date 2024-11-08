<template>
    <div>
        <Head>
            <Title> NatShop | {{ product.title }}</Title>
            <Meta name="description" :content=product.description />
        </Head>
        <div class="container">
            <img :src=product.thumbnail>
            <div class="detail"> 
                <h1 > ชื่อ : {{ product.title }} </h1>
                <h2 > ราคา : ${{ product.price }} </h2>
                <h2 > หมวดหมู่ : {{ product.category}} </h2>
                <h2 > ยี่ห้อ : {{ product.brand }} </h2>
                <h2 > ข้อมูลพื้นฐาน : {{ product.description }} </h2>
            </div>
        </div>
    </div>
</template>

<script setup>
const {id} = useRoute().params
const { data: product } = await useFetch('https://dummyjson.com/products/'+id)
console.log(product)
useHead(
    {
        title:"Product Detail Page Website",
        meta:[
            {name:"Description" , content:"รายละเอียดสินค้าชิ้นที่"}
        ]
    }
)
</script>

<style scoped>
.container{
    display: flex;
    justify-content: center;
}

.detail{
    padding-left: 10px;
}


</style>