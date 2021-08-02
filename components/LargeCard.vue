<template>
  <NuxtLink :to="`/products/${card.id}`" class="card">
    <img class="image" :src="require(`@/assets/images/${card.image || 'fe1.jpg'}`)" alt="">
    <h3 class="header">
      {{ card.title }}
    </h3>
    <p class="snippet">
      {{card.snippet }}
    </p>
  </NuxtLink>
</template>

<script>
export default {
  props: ['card']
}
</script>

<style scoped>
  .card {
    width: 31.5%;
    height: 25rem;
    border: none;
    overflow: hidden;
    padding: 0;
    cursor: pointer;
    color: #dd6060;
    filter: grayscale(1);
    transition: 0.3s;
  }
  .card:hover, .header:active{
    filter: grayscale(0);
  }
  .image {
    height: 65%;
    border-radius: 0.5rem;
  }
  .header {
    font-size: 1.15rem;
    font-weight: 600;
    margin-top: 0.4rem;
  }
  .header:hover {
    color: #dd6060;
  }
  a {
    text-decoration: none;
  }
  .snippet {
    color: grey;
  }

  @media (max-width:1024px) {
    .image {
      height: 50%;
      border-radius: 0.5rem;
    }
  }

  @media (max-width:800px) {
    .image {
      height: 28%;
      border-radius: 0.5rem;
    }
    .header {
      font-size: 1rem;
    }
  }
</style>