<template>
  <div>
    <Navbar />

    <div class="container">
      <div class="row mt-2">
        <div class justified>
          <h3>About this Page</h3>
          <p>Just implementation use simple fake API</p>
          <p>with Vue.Js</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";

export default {
  name: "About",
  components: {
    Navbar
  }
};
</script>
