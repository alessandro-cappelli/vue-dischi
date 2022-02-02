<template>
<div class="dischi">
    <img :src="info.poster" style="height: 236px">
    <h2>{{info.title}}</h2>
    <div>{{info.author}}</div>
    <div>{{info.year}}</div>
</div>
</template>

<script>
export default {
    name: 'Dischi',
    props: {
        info: Object
    }
}
</script>

<style lang='scss' scoped>
img{
    width: 100%;
}
</style>