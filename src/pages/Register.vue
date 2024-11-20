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
            User Sign Up
          </div>
          <q-form class="q-pt-md">
            <div class="q-gutter-y-md">
              <div class="form-input">
                <q-input
                  ref="full_name"
                  outlined
                  v-model="form.full_name"
                  placeholder="Full Name"
                  hide-bottom-space
                />
              </div>
              <div class="form-input">
                <q-input
                  ref="email"
                  outlined
                  v-model="form.email"
                  placeholder="Work email Address"
                  hide-bottom-space
                />
              </div>
              <div class="row">
                <div class="col-6 q-px-xs">
                  <div class="form-input">
                    <q-input
                      ref="company"
                      outlined
                      v-model="form.company"
                      placeholder="Company"
                      hide-bottom-space
                    />
                  </div>
                </div>
                <div class="col-6 q-px-xs">
                  <div class="form-input">
                    <q-input
                      ref="country"
                      outlined
                      v-model="form.country"
                      placeholder="Country"
                      hide-bottom-space
                    />
                  </div>
                </div>
              </div>
              <div class="form-input">
                <q-btn class="login-btn" color="primary" label="Signup"/>
              </div>
            </div>
          </q-form>
        </q-card-section>
        <q-card-section class="q-mt-lg q-pb-md text-center">
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
          <div class="row q-mt-xl footer q-px-lg ">
            <div class="col-8 row items-center footer-label justify-center">
              Already have an account?
            </div>
            <div class="col-4 row justify-start">
              <q-btn class="auth-btn3 text-underline" color="dark" flat to="/auth/login">
                <u>Login</u>
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
  name: 'RegisterPage'
});

const form = ref({
  full_name: '',
  email: '',
  company: '',
  country: '',
})
</script>
