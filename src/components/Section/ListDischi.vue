<template>
    <main class="container">
        <div class="row row-cols-5">
            <div v-for="dischi in 10" :key="dischi"
            class="col mb-3">
                <Dischi />
            </div>
        </div>
    </main>
  
</template>

<script>
import Dischi from "../commons/Dischi.vue"
export default {
    name: 'ListDischi',
    components:{
        Dischi,
    }
}
</script>

<style>

</style>