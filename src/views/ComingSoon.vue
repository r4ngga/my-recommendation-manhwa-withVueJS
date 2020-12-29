<template>
  <div>
    <Navbar />

    <div class="container">
      <div class="row mt-2">
        <div class justified>
          <h3>Coming Soon</h3>
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
