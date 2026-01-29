<template>
  <div class="landing">
    

    <header class="hero">
      <div class="container">
        <h1>Bienvenido a FormsVue</h1>
        <p>La mejor plataforma para gestionar tus formularios</p>
        <BaseButton to="/login" variant="accent">Comienza Ahora</BaseButton>
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
/* Navbar moved to component */

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

/* CTA handled by BaseButton (variant=accent) */

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
/* Footer moved to component */

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
