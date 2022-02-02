<template>
  <section>
      <div class="container">
          <div class="row row-cols-5">
              <Dischi 
              v-for="dischi in dischiArray" 
              :key="dischi"
              :info="dischi"
              class="col mb-3 " />
          </div>
      </div>

  </section>
</template>

<script>
import axios from "axios"
import Dischi from "../commons/Dischi.vue"

export default {
    name: 'ListDischi',
    data(){
      return {
        apiURL: "https://flynn.boolean.careers/exercises/api/array/music",
        dischiArray: []
      }
    },
    components: {
      Dischi,
    },
    created(){
      this.getDischi();
    },
    methods:{
      getDischi(){
        axios.get(this.apiURL)
      .then((risposta) => {
        // handle success
        this.dischiArray = risposta.data.response;
      })
      .catch(function (error) {
        // handle error
        console.log(error);
      });
    }
  }

}
</script>

<style lang='scss' scoped>
.col{
  background-color: #2E3A46;
  color: white;
}

section{
  background-color: #1E2D3B;
}

.row{
  text-align: center;
}

</style>