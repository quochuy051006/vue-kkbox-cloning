<template>
  <div class="success-modal-overlay">
    <div class="success-modal">
      <button
        class="success-modal-close"
        @click="emit('close')"
      >
        ✕
      </button>

      <div class="success-modal-content">
        Objective Complete! Thanks for the credentials.
        Don't worry, I'll only use your account to play
        Baby Shark on repeat 24/7. Stay vigilant next time! 🦈😈
      </div>

      <div class="success-modal-actions">
        <button
          class="btn signup"
          @click="emit('close')"
        >
          OK
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
const emit = defineEmits(['close']);

</script>

<style scoped>
  .success-modal-overlay{
    position: fixed;
    inset: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    background: rgba(0,0,0,0.6);
    z-index: 1000;
  }

  .success-modal{
    background: #262626;
    color: #fff;
    padding: 20px;
    border-radius: 12px;
    width: min(560px, 94%);
    box-shadow: 0 20px 40px rgba(0,0,0,0.6);
    border: 1px solid rgba(255,255,255,0.04);
    position: relative;
  }

  .success-modal-content{
    font-size: 15px;
    color: #e6f9ff;
    line-height: 1.5;
    margin-top: 10px;
  }

  .success-modal-actions{
    margin-top: 18px;
    display: flex;
    justify-content: flex-end;
  }

  .success-modal-close{
    position: absolute;
    top: 10px;
    right: 10px;
    background: transparent;
    color: #bdbdbd;
    border: 0;
    font-size: 20px;
    cursor: pointer;
  }

  .btn.signup{
    background: #14c8ef;
    color: #012226;
    border: 0;
    border-radius: 28px;
    padding: 10px 20px;
    cursor: pointer;
    font-weight: 700;
  }

  @media (max-width:480px){
    .success-modal{
      padding: 14px;
    }
  }
</style>