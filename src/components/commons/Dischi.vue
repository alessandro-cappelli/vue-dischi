<template>
  <div class="dischi text-center">
    <img :src="info.image" >
    <h3>{{info.title}}</h3>
    <div>{{info.author}}</div>
    <div>{{info.year}}</div>
    
    
  </div>
</template>

<script>
export default {
    name: 'Dischi',
    props:{
      info: Object,
      // poster: String,
      // title: String,
      // author: String,
      // year: String,

    }
}
</script>

<style lang='scss' scoped>
img{
  width: 100%;
}

</style>