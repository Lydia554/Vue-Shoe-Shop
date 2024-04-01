<template>
 <router-link :to="`/product/${product.slug}`" @click="clickHandler">
  <article class="card">
    <img :src="editSrc" :alt="product.name" class="card__image" />
    <h4 class="card__title">{{ product.name }}</h4>
   
  </article> </router-link>
</template>

<script>
export default {
  name: "OthersCard",
  props: { product: Object },
  data() {
    return {
      windowSize: null,
    };
  },
  methods: {
    setWindowSize() {
      let windowWidth = window.innerWidth;
      if (windowWidth < 768) {
        this.windowSize = "mobile";
      } else if (windowWidth < 1205) {
        this.windowSize = "tablet";
      } else {
        this.windowSize = "desktop";
      }
    },
    scrollToTop() {
      window.scrollTo(0, 0);
    },
    clickHandler() {
      this.scrollToTop();
      this.$emit("reset-total");
    },
  },
  computed: {
    editSrc() {
      if (this.windowSize === "mobile") {
        return require(`../../${this.product.image.mobile.slice(2)}`);
      } else if (this.windowSize === "tablet") {
        return require(`../../${this.product.image.tablet.slice(2)}`);
      } else {
        return require(`../../${this.product.image.desktop.slice(2)}`);
      }
    },
  },
  created() {
    this.setWindowSize();
    window.addEventListener("resize", this.setWindowSize);
  },
};
</script>

<style lang="scss" scoped>
.card {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 5.6rem;
  color: #000;


  @media (min-width: 768px) {
    width: 22.3rem;
    margin-bottom: 0;
    margin-right: 1.1rem;
  }

  @media (min-width: 1205px) {
    width: 35rem;
    margin-right: 3rem;
  }

  &:last-child {
    margin-bottom: 0;
    margin-left: 1.1rem;

    @media (min-width: 768px) {
      margin-right: 0;
    }
  }

  * {
    text-align: center;
  }

  &__image {
    width: 100%;
    height: 12rem;
    object-fit: cover;
    object-position: center;
    border-radius: 0.8rem;
    

    @media (min-width: 768px) {
      height: 31.8rem;
    }
  }

  &__title {
    margin-top: 3.2rem;
    font-weight: 700;
    font-size: 2.4rem;
    line-height: 3.278rem;
    letter-spacing: 0.171rem;
    text-transform: uppercase;

    @media (min-width: 768px) {
      margin-top: 4rem;
    }
  }

 
}


.card__image:hover {
  box-shadow: 0 0 10px 5px #e7e3e1;
}
</style>
