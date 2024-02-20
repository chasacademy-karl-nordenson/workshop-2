<template>
  <div class="card">
    <div class="card-content">
      <h2>{{ cardData.title }}</h2>
      <p>{{ cardData.description }}</p>
      <button @click="handleButtonClick">
        <slot name="button-label">Click me</slot>
      </button>
    </div>
  </div>
</template>
  
  <script>
  export default {
    props: {
      cardData: Object,
    },
    methods: {
      handleButtonClick() {
        this.$emit('card-clicked', this.cardData);
      },
    },
  };
  </script>
  
  <style scoped>
  .card {
    border: 1px solid #ccc;
    border-radius: 8px;
    margin: 10px;
    padding: 10px;
  }
  
  .card-content {
    text-align: center;
  }
  </style>