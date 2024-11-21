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
            Password Reset
          </div>
          <div class="sub-title">
            We received a request to reset the password for your account. To proceed, please click the link below:
            <div>
              <q-btn class="reset-password-link" flat padding="sm" to="/auth/reset-password">
                [Reset Password Link]
              </q-btn>
            </div>
            <div>
              If you didn't request this change, you can ignore this email. Your password will remain unchanged.
              For security reasons, this link will expire in [time frame, e.g., 30 minutes].
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
  name: 'PasswordReset'
});

const form = ref({
  email: '',
  password: '',
  remember: false,
})
</script>
