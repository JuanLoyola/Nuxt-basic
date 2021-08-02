<template>
  <div class="Hero container">
        <div class="text-container">
            <h1 class="header">Find your Fire Extinguisher</h1>
            <p class="snippet">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Iste iusto illum quidem asperiores, cum nisi aperiam eius ipsa sapiente odit!</p>
            <a class="button btn" href="#category">Start Looking</a>
        </div>
        <img class="image" src="~assets/svg/fire-extinguisher.svg" alt="fire extinguisher">
    </div>
</template>

<script>
export default {
}
</script>

<style scoped>
  .Hero {
    height: 100vh;
    position: relative;
    display: flex;
    padding: 5rem 0;
    align-items: center;
    justify-content: space-between;
  }
  .text-container {
    width: 50%;
    margin-top: 4rem;
  }
  .header {
    font-weight: 900;
    font-size: 5rem;
  }
  .snippet {
    color: grey;
    font-size: 1.25rem;
  }
  .image {
    width: 27.5em;
    margin-top: 2rem;
  }
  .overlay {
    background: rgba(0, 0, 0, 0);
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
  }
  .button {
    padding: 1rem 4rem;
    border-radius: 100rem;
    background-color: #e7512b;
    color: white;
    width: 18rem;
    font-weight: 700;
    transition: 0.5s;
  }
  .button:hover {
    width: 21.5rem;
    background:#cf8b7a;
  }
  @media (max-width: 500px) {
    .Hero {
      height: 40vh;
    }
  }

  @media (max-width: 1024px) {
    .header {
      font-size: 3rem;
    }
    .snippet {
      font-size: 1.25rem;
    }
    .image {
      width: 20.5em;
    }
  }

  @media (max-width: 768px) {
    .header {
      font-size: 2rem;
    }
    .snippet {
      font-size: 1rem;
    }
    .image {
      width: 15.5em;
    }
  }

  @media (max-width: 500px) {
    .header {
      font-size: 1.5rem;
    }
    .snippet {
      font-size: 0.7rem;
    }
    .image {
      width: 10em;
    }
    .button {
      padding: 1rem 1rem;
      border-radius: 100rem;
      background-color: #e7512b;
      color: white;
      font-size: 1rem;
      width: 10rem;
      font-weight: 700;
      transition: 0.5s;
    }
    .button:hover {
      width: 12rem;
      background:#cf8b7a;
    }
  }
</style>