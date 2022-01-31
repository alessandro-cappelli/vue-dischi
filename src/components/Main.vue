<template>
    <main>
        <div class="container">
            <div class="row">
                <div class="col">
                    <list-dischi/>
                </div>
            </div>
        </div>
    </main>
  
</template>

<script>
import ListDischi from "./Section/ListDischi.vue"
export default {
    name: 'Main',
    components: {
        ListDischi,
    }
}
</script>

<style>
main{
    background-color: #1E2D3B;
}
</style>