<template>
  <q-page class="flex flex-center">
    <div class="auth-page">
      <div class="flex flex-center q-mb-lg">
        <img
          alt="Quasar logo"
          src="~assets/wellscape_logo.png"
          style="width: 200px; "
        >
      </div>
      <q-card class="auth-card shadow-0">
        <q-card-section class="q-pa-none">
          <div class="title">
            User Login
          </div>
          <q-form class="q-pt-md">
            <div class="q-gutter-y-lg">
              <div class="form-input">
                <q-input
                  ref="email"
                  outlined
                  v-model="form.email"
                  placeholder="Email Address"
                  hide-bottom-space
                  autocomplete="off"
                />
              </div>
              <div class="form-input">
                <q-input
                  ref="Password"
                  type="password"
                  outlined
                  v-model="form.password"
                  placeholder="Password"
                  hide-bottom-space
                  autocomplete="off"
                />
              </div>
              <div class="row">
                <div class="col-4">
                  <div class="form-input">
                    <q-checkbox v-model="form.remember" label="Remember me" />
                  </div>
                </div>
                <div class="col-8">
                  <q-btn class="auth-btn2 full-width text-underline" color="primary" flat to="/auth/forgot-password">
                    <u>Forgot Password?</u>
                  </q-btn>
                </div>
              </div>
              <div class="form-input">
                <q-btn class="login-btn" color="primary" label="Login"/>
              </div>
            </div>
          </q-form>
        </q-card-section>
        <q-card-section class="footer q-pb-md text-center">
          <div class="row">
            <div class="col-3 row items-center">
              <q-separator class="full-width" inset />
            </div>
            <div class="col-6 row justify-center">
              <div class="continue-label">Or Continue with</div>
            </div>
            <div class="col-3 row items-center">
              <q-separator class="full-width" inset />
            </div>
          </div>
          <div class="social-logins row justify-center q-gutter-x-md q-mt-md">
            <div class="col">
              <q-btn class="full-width" color="accent">
                <q-icon name="img:/GoogleIcon.svg" />
              </q-btn>
            </div>
            <div class="col">
              <q-btn class="full-width" color="accent">
                <q-icon name="img:/AppleIcon.svg" />
              </q-btn>
            </div>
            <div class="col">
              <q-btn class="full-width" color="accent">
                <q-icon name="img:/MicrosoftIcon.svg" />
              </q-btn>
            </div>
          </div>
          <div class="row q-px-lg ">
            <div class="col-7 row items-center footer-label justify-center">
              Don't have an account?
            </div>
            <div class="col-5 row justify-start">
              <q-btn class="auth-btn3 text-underline" color="primary" flat to="/auth/register">
                <u>Sign Up?</u>
              </q-btn>
            </div>
          </div>
        </q-card-section>
      </q-card>
    </div>
  </q-page>
</template>

<script setup>
import { ref, computed, onMounted } from "vue";
defineOptions({
  name: 'LoginPage'
});

const form = ref({
  email: '',
  password: '',
  remember: false,
})
</script>
