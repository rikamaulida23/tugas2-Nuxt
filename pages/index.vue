<template>
  <div>
    <Header />
    <div class="content">
      <ResepList :resepList="resepData" />
    </div>
    <Footer />
  </div>
</template>

<script>
import Header from '~/components/Header.vue';
import Footer from '~/components/Footer.vue';
import ResepList from '~/components/ResepList.vue'; // Impor komponen ResepList

export default {
  components: {
    Header,
    Footer,
    ResepList
  },
  data() {
    return {
      resepData: [
        {
          id: 1,
          title: 'Meal Planning',
          description: 'perencanaan menu makan baik keluarga atau pribadi dalam jangka waktu tertentu yang terdiri dari sarapan, makan siang, snack, dan makan malam..',
          image: 'https://media.istockphoto.com/id/1317219837/id/foto/huevos-rancheros-adalah-sarapan-ranchero-eggs-meksiko-dengan-pico-de-gallo-dan-guacamole.jpg?s=1024x1024&w=is&k=20&c=TIy1r-dhZqKbf7J_0LNEOIufgfWRaFKLuJznZ0p9aTo='
        },
        {
          id: 2,
          title: 'Resep Makanan',
          description: 'instruksi yang menjelaskan cara menyiapkan atau membuat sesuatu, terutama hidangan makanan yang disiapkan..',
          image: 'https://media.istockphoto.com/id/1282548028/id/foto/burger-makanan-laut-segar-yang-sehat-dengan-fillet-ikan-bayam-dan-telur-latar-belakang-abu-abu.jpg?s=1024x1024&w=is&k=20&c=JZN8_vCEACAmo84QAT8sW40BvzxZRyG8ZPhXrr34HnM='
        },
        
      ]
    };
  }
};
</script>

<style>
.content {
  padding: 20px;
}
</style>