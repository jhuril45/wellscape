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
            Forgot Password?
          </div>
          <div class="sub-title">
            Please enter the email address associated with your account to proceed.
          </div>
          <q-form class="">
            <div >
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
              <div class="q-mt-lg form-input">
                <q-btn class="login-btn" color="primary" label="Submit" to="/auth/password-reset"/>
              </div>
            </div>
          </q-form>
        </q-card-section>
      </q-card>
    </div>
  </q-page>
</template>

<script setup>
import { ref, computed, onMounted } from "vue";
defineOptions({
  name: 'ForgotPassword'
});

const form = ref({
  email: '',
  password: '',
  remember: false,
})
</script>
