<template>      
      <section class="details">
        <aside class="left">
          <div class="album-block">
            <h3>出自專輯</h3>
            <a href="#">星辰大海</a>
            <div class="date">2021/01/15</div>
          </div>

          <div class="tracks">
            <h4>專輯曲目</h4>
            <ol>
              <li>星辰大海</li>
              <li>星辰大海 - 伴奏</li>
            </ol>
          </div>
        </aside>

        <article class="right">
          <div class="credits">
            <strong>作詞 / 作曲 / 編曲</strong>
            <p>瞿子千、劉濤、溫莨 等</p>
          </div>

          <div class="lyrics">
            <h4>歌詞</h4>
            <div id="lyricsContent" class="lyrics-content collapsed" aria-hidden="false">
              <p>我願變成一顆恆星<br>守護海底的蜂鳴<br>It's my dream it's magic<br>照亮你的心<br>To your eyes 有多遠的距離</p>

              <p>穿過人海 別停下來<br>趁現在還有期待<br>...</p>
            </div>
            <div class="lyrics-controls">
              <button id="toggleLyrics" class="btn outline" aria-expanded="false" aria-controls="lyricsContent" @click="emit('open-login')">顯示更多</button>
            </div>
          </div>
        </article>
      </section>
</template>

<script setup>
const emit = defineEmits(['open-login'])
</script>

<style scoped>
  .details {
    display: flex;
    gap: 56px;
    padding: 28px 18px;
    margin-top: 18px;
  }

  .right {
    flex: 1;
  }
  .left {
    width: 280px;
  }
  .album-block a {
    display: block;
    color: var(--text);
    font-weight: 600;
  }
  .tracks ol {
    padding-left: 18px;
  }
  .credits {
    margin-bottom: 16px;
  }
  .lyrics p {
    line-height: 1.8;
    color: var(--muted);
  }
</style>