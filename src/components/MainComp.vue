<template>
  <div>
    <div class="container">
     <CardComp
      v-for="(elem, index) in cards"
      :key="index"
      :card="elem"
      />
    </div>
  </div>
</template>

<script>
import CardComp from '@/components/CardComp.vue';
import axios from 'axios';

export default {
  name: 'MainComp',
  components: {
    CardComp,
  },
  data() {
    return {
      cards: [],
    };
  },
  created() {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music')
      .then((response) => {
        console.log(response);
        this.cards = response.data.response;
      });
  },
};
</script>

<style lang="scss" scoped>
.container {
  height: 90vh;
  background-color: #1e2d3b;
  display: flex;
  justify-content: center;
align-content: center;
  flex-wrap: wrap;
  gap: 3rem;
}
</style>
