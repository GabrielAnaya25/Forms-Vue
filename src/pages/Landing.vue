<template>
  <div class="landing">
    <nav class="navbar">
      <div class="container">
        <div class="logo">FormsVue</div>
        <router-link to="/login" class="login-btn">Iniciar Sesión</router-link>
      </div>
    </nav>

    <header class="hero">
      <div class="container">
        <h1>Bienvenido a FormsVue</h1>
        <p>La mejor plataforma para gestionar tus formularios</p>
        <router-link to="/login" class="cta-btn">Comienza Ahora</router-link>
      </div>
    </header>

    <section class="features">
      <div class="container">
        <h2>Características</h2>
        <div class="features-grid">
          <div class="feature-card">
            <div class="feature-icon">
              <ClipboardList :size="48" />
            </div>
            <h3>Formularios Dinámicos</h3>
            <p>Crea formularios personalizados sin necesidad de código</p>
          </div>
          <div class="feature-card">
            <div class="feature-icon">
              <Shield :size="48" />
            </div>
            <h3>Seguro</h3>
            <p>Tus datos están protegidos con encriptación</p>
          </div>
          <div class="feature-card">
            <div class="feature-icon">
              <Zap :size="48" />
            </div>
            <h3>Rápido</h3>
            <p>Rendimiento optimizado para la mejor experiencia</p>
          </div>
          <div class="feature-card">
            <div class="feature-icon">
              <BarChart3 :size="48" />
            </div>
            <h3>Análisis</h3>
            <p>Visualiza estadísticas y reportes en tiempo real</p>
          </div>
        </div>
      </div>
    </section>

    <footer class="footer">
      <div class="container">
        <p>&copy; 2026 FormsVue. Todos los derechos reservados.</p>
      </div>
    </footer>
  </div>
</template>

<script setup>
import { ClipboardList, Shield, Zap, BarChart3 } from 'lucide-vue-next'
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.landing {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  color: var(--text-dark);
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

/* Navbar */
.navbar {
  background: #fff;
  padding: 1rem 0;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  position: sticky;
  top: 0;
  z-index: 100;
}

.navbar .container {
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
  text-decoration: none;
  font-weight: 600;
  transition: color 0.3s;
}

.login-btn:hover {
  color: var(--color-primary-dark);
}

/* Hero Section */
.hero {
  background: linear-gradient(135deg, var(--color-primary) 0%, var(--color-primary-dark) 100%);
  color: var(--text-light);
  padding: 100px 0;
  text-align: center;
}

.hero h1 {
  font-size: 3rem;
  margin-bottom: 1rem;
}

.hero p {
  font-size: 1.2rem;
  margin-bottom: 2rem;
  opacity: 0.9;
}

.cta-btn {
  display: inline-block;
  background: var(--color-accent);
  color: var(--color-primary-dark);
  padding: 12px 40px;
  border-radius: 50px;
  text-decoration: none;
  font-weight: 600;
  transition: transform 0.3s, box-shadow 0.3s;
}

.cta-btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
  background: var(--color-accent-600);
}

/* Features Section */
.features {
  padding: 80px 0;
  background: var(--bg-muted);
}

.features h2 {
  text-align: center;
  font-size: 2.5rem;
  margin-bottom: 3rem;
  color: var(--text-dark);
}

.features-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
}

.feature-card {
  background: var(--card-bg);
  padding: 2rem;
  border-radius: 10px;
  text-align: center;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s, box-shadow 0.3s;
}

.feature-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 12px rgba(0, 0, 0, 0.15);
}

.feature-icon {
  font-size: 3rem;
  margin-bottom: 1rem;
}

.feature-card h3 {
  margin-bottom: 0.5rem;
  color: var(--color-primary);
}

.feature-icon {
  color: var(--color-primary);
}

.feature-card p {
  color: var(--muted);
  font-size: 0.95rem;
}

/* Footer */
.footer {
  background: var(--footer-bg);
  color: var(--text-light);
  text-align: center;
  padding: 2rem 0;
}

/* Responsive */
@media (max-width: 768px) {
  .hero h1 {
    font-size: 2rem;
  }

  .hero p {
    font-size: 1rem;
  }

  .features h2 {
    font-size: 1.8rem;
  }
}
</style>
