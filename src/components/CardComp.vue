<template>
  <div>
    <div>
      <img :src="card.poster" alt="">
    </div>
    <div>
      <div>{{card.title}}</div>
      <div>{{card.author}}</div>
      <div>{{card.year}}</div>
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

</style>
