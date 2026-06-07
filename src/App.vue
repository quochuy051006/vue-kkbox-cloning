<template>
  <Header @open-login="showLogin = true" />
  <Hero @open-login="showLogin = true" />
  <SongInfo @open-login="showLogin = true" />
  <RelatedSongs @open-login="showLogin = true" />
  <Footer />
  <LoginModal
    v-if="showLogin"
    @close="showLogin = false"
    @login-success="handleLoginSuccess"
  />
  <SuccessModal
  v-if="showSuccess"
  @close="showSuccess = false"
  />
</template>

<script setup>
import { ref } from 'vue'
import Header from './components/Header.vue'
import Hero from './components/Hero.vue'
import SongInfo from './components/SongInfo.vue'
import RelatedSongs from './components/RelatedSongs.vue'
import Footer from './components/Footer.vue'

import LoginModal from './components/LoginModal.vue'
import SuccessModal from './components/SuccessModal.vue'

  const showLogin = ref(false)
  const showSuccess = ref(false)

  function handleLoginSuccess() {
    showLogin.value = false
    showSuccess.value = true
  }
</script>