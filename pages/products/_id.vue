<template>
  <div>
    <Nav class=""/>
    <div v-if="product" class="container py-5">
        <div class="hero-container">
            <img :src="require(`@/assets/images/${product.image}`)" alt="prduct image" class="image">
            <div class="info-box">
                <h1>{{ product.title }}</h1>
                <p class="snippet">{{ product.snippet }}</p>
                <RentModal />
            </div>
        </div>
        <div class="whats-included-container">
            <div class="included-container">
                <h6>Super Effective</h6>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores, dolore.</p>
            </div>
            <div class="included-container">
                <h6>Clean & Tidy</h6>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores, dolore.</p>
            </div>
            <div class="included-container">
                <h6>Cancel Anytime</h6>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores, dolore.</p>
            </div>
            <div class="included-container">
                <h6>Satisfaction Guaranteed</h6>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores, dolore.</p>
            </div>        
        </div>
        <div class="description-container">
            <p>
                {{ product.description }}
            </p>
        </div>

        <Reviews />
    </div>
  </div>
</template>

<script>

export default {
  computed: {
    product () {
      return this.$store.getters.getProductById(this.$route.params.id)
    }
  }
}
</script>

<style scoped>
.hero-container {
  display: flex;
  justify-content: space-between;
}
.image {
  width: 59%;
  height: 25rem;
}
.info-box {
  width: 39%;
  background-color: #cfc9c952;
  padding: 1rem;
  border-radius: 0.5rem;
}
.whats-included-container {
  border-bottom: 0.1rem solid #80808027;
}
.description-container {
  border-bottom: 0.1rem solid #80808027;
  padding-bottom: 2rem;
  margin-bottom: 2rem;
}
.included-container {
  margin-top: 1.5rem;
}
h1 {
  font-size: 1.75rem;
}
h6 {
  font-size: 1.15rem;
  font-weight: 500;
}
p {
  color: #808080;
}
.snippet {
  color: #000000c5;
  margin-top: 1rem;
}
button {
  width: 100%;
  border: none;
  padding: 0.5rem;
  color: white;
  font-weight: 700;
  padding: 1rem 4rem;
  border-radius: 100rem;
  background-color: #e7512b;
  color: white;
  font-weight: 700;
  transition: 0.5s;
}
.description-container {
  margin-top: 3rem;
  color: grey;
}
.padding {
  padding: 10rem 0;
}

@media (max-width: 740px) {
  .hero-container {
    width: 100%;
    flex-flow: column;
  }
  .image {
    width: 100%;
    height: 100%;
  }
  .info-box {
    width: 100%;
  }
}
</style>