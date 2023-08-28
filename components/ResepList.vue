<template>
  <div class="resep-list">
    <div v-for="resep in resepList" :key="resep.id" class="resep-item">
      <img :src="resep.image" alt="Gambar Resep" class="resep-image" />
      <h3 class="resep-title">{{ resep.title }}</h3>
      <p class="resep-description">{{ resep.description }}</p>
      <div class="button-container">
        <button @click="editResep(resep.id)" class="edit-button">Edit</button>
        <button @click="hapusResep(resep.id)" class="hapus-button">Hapus</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    resepList: Array // Properti yang berisi daftar resep
  }
};
</script>

<style scoped>
  .resep-list {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
  }

  .resep-item {
    border: 1px solid #ccc;
    padding: 20px;
  }

  .resep-image {
    max-width: 100%;
    height: auto;
  }

  .resep-title {
    font-size: 1.2rem;
    margin-top: 10px;
  }

  .resep-description {
    margin-top: 5px;
  }

  .edit-button,
.hapus-button {
  padding: 5px 10px;
  margin-right: 10px;
  cursor: pointer;
  background-color: #007bff;
  color: #fff;
  border: none;
  border-radius: 3px;
}

.hapus-button {
  background-color: #dc3545;
}
</style>