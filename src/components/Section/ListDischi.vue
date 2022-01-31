<template>
    <main class="container">
        <div class="row row-cols-5">
            <div v-for="dischi in dischiArray" 
            :key="dischi.id"
            :info="dischi"
            class="col mb-3">
                <Dischi />
            </div>
        </div>
    </main>
  
</template>

<script>
import axios from "axios";
import Dischi from "../commons/Dischi.vue";

export default {
    name: 'ListDischi',
    data(){
        return{
            apiURL: "https://flynn.boolean.careers/exercises/api/array/music", 
            dischiArray: [],
        }
    },
    components:{
        Dischi,
    },
    created(){
        this.getDischi();
    },
    methods:{
        getDischi(){
            axios.get(this.apiURL)
            .then( (album) => {
                // handle success
                this.dischiArray = album.data;
            })
            .catch(function (error) {
                // handle error
                console.log(error);
            })
            
        }
            
    }
}
</script>

<style lang='scss' scoped>
.row{
    text-align: center;
}

</style>