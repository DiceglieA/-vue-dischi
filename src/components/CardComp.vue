<template>
  <div class="card">
    <div class="img-card">
      <img :src="card.poster" alt="">
    </div>
    <div>
      <div class="white">{{card.title}}</div>
      <div class="lightgrey">
        <div>{{card.author}}</div>
        <div>{{card.year}}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CardComp',
  props: {
    card: Object,
  },
};
</script>

<style lang="scss" scoped>
.card {
  width: calc(100% - 2rem - 12rem) / 5;
  margin: 1rem 1rem;
  background-color: #2e3a46;
  text-align: center;
}

.white{
  color: white;
}

.lightgrey{
  color: lightgrey;
}
.img-card img{
  width: 180px;
  height: 180px;
}
</style>
