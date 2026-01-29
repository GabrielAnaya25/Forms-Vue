<template>
  <nav class="navbar">
    <div class="container">
      <div class="logo">FormsVue</div>
      <BaseButton to="/login" variant="ghost" class="login-btn">Iniciar Sesión</BaseButton>
    </div>
  </nav>
</template>

<script setup>
import BaseButton from './BaseButton.vue'
</script>

<style scoped>
.navbar {
  background: var(--card-bg);
  padding: 1rem 0;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.06);
  position: sticky;
  top: 0;
  z-index: 100;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  font-size: 1.5rem;
  font-weight: 700;
  color: var(--color-primary);
}

.login-btn {
  color: var(--color-primary);
}

.login-btn:hover {
  color: var(--color-primary-dark);
}
</style>
