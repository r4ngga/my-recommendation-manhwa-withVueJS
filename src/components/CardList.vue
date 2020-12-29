<template>
  <div>
    ( {{manhwa.id}} )
    <h4>{{manhwa.title}}</h4>
    <p>Score : {{manhwa.score}}</p>
    <p>Date Release : {{manhwa.date_release}}</p>
    <p>Link : {{manhwa.link}}</p>
  </div>
</template>

<script>
export default {
  name: "CardList",
  props: ["manhwa"]
};
</script>

<style>
</style>