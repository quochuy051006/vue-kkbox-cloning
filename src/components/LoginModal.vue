<template>
  <div class="modal-overlay">
        <section class="login-card" aria-label="KKBOX Login - English">
          <div class="login-logo">KKBOX <span class="slogan">Listen, and Be Heard.</span></div>
          <form class="login-form" @submit.prevent="login">
            <div>
              <label for="email">Email</label>

              <input
                id="email"
                v-model="email"
                type="email"
                placeholder="name@example.com"
                :aria-invalid="!!emailError"
              >

              <div
                v-if="emailError"
                class="error"
                role="alert"
              >
                {{ emailError }}
              </div>
            </div>

            <div>
              <label for="password">Password</label>

              <input
                id="password"
                v-model="password"
                type="password"
                placeholder="Enter your password"
                :aria-invalid="!!passwordError"
              >

              <div
                v-if="passwordError"
                class="error"
                role="alert"
              >
                {{ passwordError }}
              </div>
            </div>

            <div class="login-cta">
              <button
                class="btn signup"
                type="submit"
              >
                Login
              </button>

              <button
                class="btn modal-close"
                type="button"
                @click="emit('close')"
              >
                Cancel
              </button>
            </div>
          </form>
      </section>
    </div>
</template>

<script setup>
import { ref } from 'vue'

  const emit = defineEmits([
    'close',
    'login-success'
  ])

  const email = ref('')
  const password = ref('')

  const emailError = ref('')
  const passwordError = ref('')

  function login() {
    emailError.value = ''
    passwordError.value = ''

    let hadError = false

    if (!email.value.trim()) {
      emailError.value = 'Please fill your email.'
      hadError = true
    }

    if (!password.value.trim()) {
      passwordError.value = 'Please fill your password.'
      hadError = true
    }

    if (hadError) return
    emit('login-success')
  }
</script>

<style scoped>
  .login-card{width:320px;background:#262626;padding:28px;border-radius:12px;box-shadow:0 18px 30px rgba(0,0,0,0.45);border:1px solid rgba(255,255,255,0.03)}
  .login-logo{font-size:32px;font-weight:800;color:#14c8ef;text-align:center}
  .login-logo .slogan{display:block;font-size:12px;font-weight:400;color:#bdbdbd;margin-top:6px}
  .login-form{margin-top:18px;display:flex;flex-direction:column;gap:12px}
  .login-form label{font-size:12px;color:#bdbdbd}
  .login-form input{padding:10px 12px;border-radius:8px;border:1px solid rgba(255,255,255,0.06);background:rgba(255,255,255,0.03);color:#fff}
  .login-form .error{color:#ff6b6b;font-size:12px;margin-top:6px}
  .login-form input[aria-invalid="true"]{border-color:#ff6b6b;box-shadow:0 0 0 4px rgba(255,107,107,0.06)}
  .login-cta{display:flex;flex-direction:column;gap:12px;margin-top:12px}
  .btn{display:inline-block;text-align:center;padding:12px 16px;border-radius:28px;border:0;cursor:pointer;font-weight:700}
  .btn.signup{background:#14c8ef;color:#012226}
  .btn.outline{background:transparent;border:1px solid rgba(20,200,239,0.6);color:#bfefff}
  .btn.modal-close{background:#bdbdbd;color:#012226;margin-top:6px;font-size:14px}
  .login-card.clone{transform:translateY(18px) scale(.99);opacity:.98}
  .modal-overlay{
    position:fixed;
    inset:0;
    display:flex;
    justify-content:center;
    align-items:center;
    background:rgba(0,0,0,.6);
    z-index:1000;
  }
  @media (max-width:880px){.login-card{width:100%;max-width:420px}}
</style>