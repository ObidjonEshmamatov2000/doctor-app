<template>
  <div>
    <Header />
    <PopularProducts />
    <Footer />
  </div>
</template>

<script>
  import Header from '../components/home/Header';
  import Footer from '../components/home/Footer';
  import PopularProducts from '../components/home/PopularProducts';
export default {
  name: 'Home',
  components: {
    Header,
    Footer,
    PopularProducts
  },
  data() {
    return {
      
    }
  },
  methods: {
    
  }
}
</script>
