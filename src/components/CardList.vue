<template>
    <div class="card-list">
      <Card v-for="(card, index) in cards" :key="index" :cardData="card" @card-clicked="handleCardClick">
        <template v-slot:button-label>Vote for this movie</template>
      </Card>
    </div>
  </template>
  
  <script>
  import Card from './Card.vue';
  
  export default {
    props: {
      cards: Array,
    },
    methods: {
      handleCardClick(card) {
        this.$emit('card-clicked', card);
      },
    },
    components: {
      Card,
    },
  };
  </script>
  
  <style scoped>
  .card-list {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
  }
  </style>