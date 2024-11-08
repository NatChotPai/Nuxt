<template>
    <div class="container">
        <h1>First Page Website</h1>
        <img src="/image/shopping.svg">
    </div>
</template>

<script setup>
useHead(
    {
        title:"NatShop |First Page Website",
        meta:[
            {name:"Description" , content:"อุปกรณ์คอมผิวเตอร์"}
        ]
    }
)
</script>

<style scoped>
.container{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

img{
    width: 500px;
    height: 500px;
}
</style>