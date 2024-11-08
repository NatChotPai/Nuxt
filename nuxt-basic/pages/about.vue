<template>
    <div class="container">
        <h1>เกี่ยวกับผู้พัฒนา Website</h1>
        <img src="/image/about.svg">
    </div>
</template>

<script setup>
useHead(
    {
        title:"NatShop | About Page Website",
        meta:[
            {name:"Description" , content:"เกี่ยวกับเรา"}
        ]
    }
)
</script>

<style  scoped>
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