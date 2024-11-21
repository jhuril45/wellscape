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
            Reset Password
          </div>
          <q-form class="q-pt-md">
            <div class="q-gutter-y-lg">
              <div class="form-input">
                <q-input
                  ref="password"
                  type="password"
                  outlined
                  v-model="form.password"
                  placeholder="New Password"
                  hide-bottom-space
                  autocomplete="off"
                />
              </div>
              <div class="form-input">
                <q-input
                  ref="confirm_password"
                  type="password"
                  outlined
                  v-model="form.confirm_password"
                  placeholder="Confirm Password"
                  hide-bottom-space
                  autocomplete="off"
                />
              </div>
              <div class="form-input">
                <q-btn class="login-btn" color="primary" label="Submit"/>
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
  name: 'ResetPassword'
});

const form = ref({
  email: '',
  password: '',
  confirm_password: '',
  remember: false,
})
</script>
