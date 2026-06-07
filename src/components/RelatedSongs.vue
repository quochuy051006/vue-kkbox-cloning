<script setup>
const emit = defineEmits(['open-login'])

const songs = [
  '/500x500.jpg',
  '/500x500 (1).jpg',
  '/500x500 (2).jpg',
  '/download (1).jpg'
]
</script>

<template>
      <section class="related">
        <h3>相關歌曲</h3>
        <div class="card-grid">
            <div class="card">
              <a href="#"><img src="/500x500.jpg" alt="相關歌曲 1" @click.prevent="emit('open-login')"></a>
            </div>
            <div class="card">
              <a href="#"><img src="/500x500 (1).jpg" alt="相關歌曲 2" @click.prevent="emit('open-login')"></a>
            </div>
            <div class="card">
              <a href="#"><img src="/500x500 (2).jpg" alt="相關歌曲 3" @click.prevent="emit('open-login')"></a>
            </div>
            <div class="card">
              <a href="#"><img src="/download (1).jpg" alt="相關歌曲 4" @click.prevent="emit('open-login')"></a>
            </div>
        </div>
      </section>
</template>

<style scoped>
  .related {
      margin-top: 30px;
  }

  .card-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 16px;
  }

  .card {
      overflow: hidden;
      border-radius: 8px;
  }

  .card img {
      width: 100%;
      height: 200px;
      object-fit: cover;
      display: block;
  }
</style>