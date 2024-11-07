<template>
    <div>
        <h1>รายละเอียดสินค้าชิ้นที่ {{ id }}</h1>
    </div>
</template>

<script setup>
const {id} = useRoute().params
useHead(
    {
        title:"Product Detail Page Website",
        meta:[
            {name:"Description" , content:"รายละเอียดสินค้าชิ้นที่"}
        ]
    }
)
</script>

<style scoped></style>