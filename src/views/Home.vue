<template>
  <div class="home">
    <Navbar />
    <div class="container">
      <Carousel />
      <div class="row mt-3">
        <div class="col-md-5" v-for="manhwa in manhwas" :key="manhwa.id">
          <CardList :manhwa="manhwa" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";
import Carousel from "@/components/Carousel.vue";
import CardList from "@/components/CardList.vue";
import axios from "axios";
export default {
  name: "Home",
  components: {
    Navbar,
    Carousel,
    CardList
  },
  data() {
    return {
      manhwas: []
    };
  },
  methods: {
    setManhwa(data) {
      this.manhwas = data;
    }
  },
  mounted() {
    // axios
    //   .get("http://localhost:3000/best-products")
    //   .then((response) => this.setProducts(response.data))
    //   .catch((error) => console.log(error))
    axios
      .get("http://localhost:3000/recommendation-list")
      .then(response => this.setManhwa(response.data))
      .catch(error => console.log("Failed Connected API, Try Again", error));
    // axios
    //   .get("http://localhost:3000/recommendation-list")
    //   .then(function(response) {
    //     // handle success
    //     console.log(response);
    //   })
    //   .catch(function(error) {
    //     // handle error
    //     console.log(error);
    //   });
  }
};
</script>
