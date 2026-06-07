<template>
      <section class="hero" role="region" aria-label="Song hero">
        <div class="art">
          <img src="/download.jpg" alt="星辰大海 專輯封面" class="album-img">
        </div>
        <div class="hero-meta">
          <div class="kicker">歌曲</div>
          <h1 class="title">星辰大海</h1>
          <a href="#" class="artist" aria-label="artist page">黃霄雲</a>

          <div class="ctas">
            <button id="previewBtn" class="btn primary" aria-pressed="false" @click="emit('open-login')">試聽</button>
            <button class="btn outline" @click="emit('open-login')">聽全曲</button>
            <button id="shareBtn" class="icon share" aria-haspopup="dialog" aria-controls="shareModal" @click="emit('open-login')">↗</button>
          </div>
        </div>
      </section>
</template>

<script setup>
const emit = defineEmits(['open-login'])
</script>

<style scoped>
  .hero {
      display: flex;
      gap: 28px;
      align-items: center;
      padding: 28px 18px;
      background: #fff;
      margin-top: 18px;
      border-radius: 4px
  }

  .art {
      width: 180px;
      height: 180px;
      background: #DADADA;
      border-radius: 6px
  }

  .hero-meta {
      flex: 1
  }

  .kicker {
      font-size: 13px;
      color: var(--muted)
  }

  .title {
      margin: 6px 0 4px;
      font-size: 28px
  }

  .artist {
      display: inline-block;
      color: var(--text);
      text-decoration: none;
      margin-bottom: 12px
  }

  .ctas {
      display: flex;
      gap: 12px;
      align-items: center;
      margin-top: 12px
  }

  .btn {
      padding: 10px 16px;
      border-radius: 20px;
      border: 1px solid transparent;
      cursor: pointer
  }

  .btn.primary {
      background: var(--accent);
      color: #fff
  }

  .btn.outline {
      background: #fff;
      border: 1px solid #ddd
  }

  .icon {
      background: transparent;
      border: 0;
      cursor: pointer
  }

  .art {
      width: 180px;
      height: 180px;
      background: linear-gradient(135deg, #cfc6ff 0%, #ffd1dc 60%);
      border-radius: 6px;
      box-shadow: 0 6px 18px rgba(0, 0, 0, 0.06);
      display: flex;
      align-items: center;
      justify-content: center;
      color: #fff;
      font-weight: 700
  }
</style>