<template>
  <div class="review-card">
    <div class="image-container">
      <img :src="review.picture.large" alt="">
    </div>
    <div class="text-container" >
      <h6 class="username">{{review.login.username}}</h6>
      <p>Lorem ipsum dolor, sitametconsecteturadipisicing elit. Repellendusquammagnibeatae possimus debitis.</p>
    </div>
  </div>
</template>

<script>
  export default {
    props: ['review'],
  }
</script>

<style scoped>
  .review-card {
    width: 100%;
    margin: 2.5rem 0;
    height: 5rem;
    display: flex;
    border-bottom: 1px dashed gray;
  }
  .review-card:nth-last-child(1) {
    border-bottom: none;
  }
  .text-container {
    margin-left: 2rem
  }
  .username {
    font-weight: 500;
    color: #dd6060;
    text-transform: initial;
    cursor: pointer;
  }
  .username:hover {
    color: #e4a7a7;
    text-decoration:underline;
  }
  img {
    width: 4rem;
    height: 4rem;
    border-radius: 100%;
  }
  p {
    color: grey
  }

  @media (max-width:800px) {
    .review-card {
      width: 100%;
      margin: 3rem 0rem;
      height: 10em;
      justify-content: center;
      align-items: center;
    }
    .text-container {
      margin-left: 2rem
    }
  }
</style>