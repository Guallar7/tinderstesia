---
theme: default
colorSchema: light
fonts:
  sans: 'IBM Plex Sans'
  mono: 'IBM Plex Mono'
  provider: google
title: Tinderstesia
info: |
  Una plataforma interna para la reubicación de personal de anestesia
  Hospital Universitario Miguel Servet
  David Guallar
transition: fade
clicksPerSlide: 999
---

<style>
/* Global styles with smooth transitions */
.slidev-layout {
  background: linear-gradient(135deg, #ffffff 0%, #f1f5f9 100%);
  font-family: 'IBM Plex Sans', sans-serif;
  color: #1e293b;
  transition: all 500ms ease-out;
  padding: 1.5rem 2.5rem !important;
}

.slidev-layout h1 {
  font-size: 1.8rem !important;
  margin-bottom: 0.8rem !important;
}

/* Horizontal Video Layout */
.horizontal-video-container {
  display: grid;
  grid-template-columns: 1fr 1.5fr;
  gap: 2rem;
  align-items: center;
  height: 80%;
}

/* Slide 1 Redesign: Premium Glassmorphism */
.title-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100%;
  width: 100%;
  text-align: center;
  padding: 0;
  background: radial-gradient(circle at top right, rgba(26, 87, 153, 0.05), transparent),
              radial-gradient(circle at bottom left, rgba(10, 126, 108, 0.05), transparent);
  position: absolute;
  top: 0;
  left: 0;
}

.title-glass-card {
  background: rgba(255, 255, 255, 0.7);
  backdrop-filter: blur(12px);
  -webkit-backdrop-filter: blur(12px);
  padding: 3rem;
  border-radius: 24px;
  border: 1px solid rgba(255, 255, 255, 0.8);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.08);
  max-width: 800px;
  width: 90%;
  margin: 0 auto;
  animation: fadeInDown 0.8s cubic-bezier(0.2, 0.8, 0.2, 1);
}

@keyframes fadeInDown {
  from { opacity: 0; transform: translateY(-20px); }
  to { opacity: 1; transform: translateY(0); }
}

.title-icon {
  width: 120px !important;
  height: 120px !important;
  margin: 0 auto 1.5rem auto !important;
  display: block;
  filter: drop-shadow(0 10px 20px rgba(26, 87, 153, 0.2));
  animation: float 6s ease-in-out infinite;
}

@keyframes float {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-10px); }
}

.title-text {
  font-size: 3.8rem !important;
  font-weight: 800 !important;
  background: linear-gradient(135deg, #1a5799 0%, #0a7e6c 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  margin-bottom: 0.5rem !important;
  letter-spacing: -1px;
}

.title-subtitle {
  font-size: 1.3rem;
  color: #475569;
  margin-bottom: 2rem;
  font-weight: 500;
  line-height: 1.3;
}

.title-info {
  border-top: 1px solid rgba(0, 0, 0, 0.08);
  padding-top: 1.5rem;
  color: #64748b;
  font-size: 0.9rem;
  line-height: 1.5;
}

.tagline {
  color: #1a5799;
  font-weight: 700;
  margin-top: 0.8rem;
  letter-spacing: 1px;
  text-transform: uppercase;
  font-size: 0.8rem;
}

/* Typography Helpers */
h1, h2, h3, h4, h5, h6 {
  font-weight: 700;
}

/* v-click animations */
.slidev-vclick-target {
  transition: all 500ms cubic-bezier(0.34, 1.56, 0.64, 1);
}

.slidev-vclick-hidden {
  opacity: 0;
  transform: translateY(15px);
}

/* Problem slide: 2x2 Grid Fix */
.problem-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1.2rem;
  margin-top: 1.5rem;
}

.problem-item {
  background: white;
  padding: 1.2rem;
  border-radius: 14px;
  box-shadow: 0 4px 12px rgba(26, 87, 153, 0.05);
  display: flex;
  gap: 1.2rem;
  align-items: flex-start;
  border-left: 5px solid #1a5799;
  transition: all 300ms ease;
}

.problem-item:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 24px rgba(26, 87, 153, 0.12);
}

.problem-icon {
  font-size: 2.2rem;
  flex-shrink: 0;
}

.problem-text p {
  margin: 0;
  line-height: 1.6;
  font-size: 0.95rem;
}

/* Solution slide: Tightening Spacing */
.solution-card {
  background: white;
  padding: 2rem;
  border-radius: 16px;
  box-shadow: 0 4px 20px rgba(10, 126, 108, 0.06);
  border-left: 6px solid #0a7e6c;
  max-width: 95%;
  margin: 0 auto;
}

.solution-card h3 {
  color: #0a7e6c;
  margin: 0 0 1rem 0;
  font-size: 1.4rem;
}

.solution-list {
  list-style: none;
  padding: 0;
  margin: 1.2rem 0;
}

.solution-list li {
  margin: 0.8rem 0;
  padding-left: 2rem;
  position: relative;
  font-size: 1.05rem;
  line-height: 1.5;
}

.solution-list li:before {
  content: "✓";
  position: absolute;
  left: 0;
  color: #0a7e6c;
  font-weight: 900;
}

.solution-footer {
  margin-top: 1.5rem;
  padding-top: 1.2rem;
  border-top: 1px solid #f1f5f9;
  font-style: italic;
  color: #64748b;
  font-size: 0.95rem;
}

/* Houses grid */
.houses-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1rem;
  margin-top: 1rem;
}

.house-card {
  background: white;
  padding: 1.2rem;
  border-radius: 16px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.04);
  text-align: center;
  border-top: 4px solid #1a5799;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.8rem;
  transition: all 400ms cubic-bezier(0.34, 1.56, 0.64, 1);
}

.house-card:nth-child(even) { border-top-color: #0a7e6c; }

.house-card:hover {
  transform: scale(1.05) translateY(-5px);
  box-shadow: 0 12px 24px rgba(0, 0, 0, 0.1);
}

.house-emoji {
  font-size: 2.5rem;
}

/* Actors grid: Overflow Fix */
.actors-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.2rem;
  margin-top: 1rem;
}

.actor-card {
  background: white;
  padding: 1.2rem;
  border-radius: 16px;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.05);
  border-top: 5px solid;
  transition: all 300ms ease;
  display: flex;
  flex-direction: column;
}

.actor-card.candidate { border-top-color: #1a5799; }
.actor-card.leader { border-top-color: #0a7e6c; }
.actor-card.admin { border-top-color: #334155; }

.actor-icon {
  font-size: 2.5rem;
  margin-bottom: 0.8rem;
}

.actor-card h4 {
  margin: 0 0 0.5rem 0;
  font-size: 1.1rem;
}

.role-id {
  background: #f8fafc;
  padding: 0.3rem 0.6rem;
  border-radius: 6px;
  font-family: 'IBM Plex Mono', monospace;
  font-size: 0.7rem;
  margin-bottom: 1rem;
  border: 1px solid #e2e8f0;
  display: inline-block;
  align-self: flex-start;
}

.actor-card ul {
  list-style: none;
  padding: 0;
  margin: 0;
  font-size: 0.85rem;
  line-height: 1.6;
}

.actor-card li:before {
  content: "→ ";
  color: #1a5799;
  margin-right: 0.4rem;
  font-weight: bold;
}

/* Swipe demo */
.swipe-demo {
  display: flex;
  flex-direction: column;
  gap: 2rem;
  margin-top: 1.5rem;
  align-items: center;
}

.swipe-card {
  background: white;
  border-radius: 20px;
  box-shadow: 0 10px 40px rgba(0, 0, 0, 0.12);
  width: 100%;
  max-width: 480px;
  overflow: hidden;
}

.card-header {
  background: linear-gradient(135deg, #1a5799 0%, #0a7e6c 100%);
  color: white;
  padding: 1.5rem 2rem;
  display: flex;
  gap: 1.5rem;
  align-items: center;
}

.card-stripe {
  width: 4px;
  height: 50px;
  background: white;
  border-radius: 2px;
}

.card-body {
  padding: 1.5rem 2rem;
  font-size: 1.05rem;
}

.swipe-controls {
  display: flex;
  flex-direction: column;
  gap: 1.2rem;
  width: 100%;
  max-width: 400px;
}

.control-buttons {
  display: flex;
  gap: 1.5rem;
  justify-content: center;
}

.control-button {
  padding: 0.7rem 1.5rem;
  border-radius: 12px;
  font-weight: 700;
  color: white;
}

.control-button.left { background: #1a5799; }
.control-button.right { background: #0a7e6c; }

.intensity-slider {
  background: #f8fafc;
  padding: 0.8rem 1.2rem;
  border-radius: 12px;
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

.slider-bar {
  height: 8px;
  background: linear-gradient(90deg, #1a5799 0%, #0a7e6c 100%);
  border-radius: 4px;
  position: relative;
}

.slider-bar:after {
  content: '';
  position: absolute;
  right: 15%;
  top: 50%;
  transform: translateY(-50%);
  width: 18px;
  height: 18px;
  background: white;
  border: 4px solid #0a7e6c;
  border-radius: 50%;
  box-shadow: 0 2px 8px rgba(0,0,0,0.2);
}

/* Roadmap section: Size Optimization */
.roadmap-section {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1.5rem;
  margin-top: 1rem;
}

.roadmap-column {
  background: white;
  padding: 1.5rem;
  border-radius: 16px;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.05);
  border-left: 6px solid;
}

.roadmap-column.v1 { border-left-color: #0a7e6c; }
.roadmap-column.future { border-left-color: #f59e0b; }

.roadmap-column h3 {
  margin: 0 0 1rem 0;
  font-size: 1.2rem;
}

.roadmap-column ul {
  list-style: none;
  padding: 0;
  margin: 0;
  font-size: 0.85rem;
  line-height: 1.8;
}

.roadmap-column li:before {
  content: "• ";
  color: inherit;
  font-weight: bold;
}

/* Closing slide */
.closing-slide {
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100%;
  width: 100%;
  gap: 2rem;
  position: absolute;
  top: 0;
  left: 0;
}

/* Disclaimer / What it doesn't do */
.disclaimer-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1rem;
  margin-top: 1.5rem;
}

.disclaimer-item {
  background: #fef2f2;
  border-left: 4px solid #ef4444;
  padding: 1rem;
  border-radius: 8px;
  display: flex;
  gap: 0.8rem;
  align-items: center;
  font-size: 0.9rem;
  color: #991b1b;
}

/* Screenshot styling */
.screenshot-card {
  background: white;
  padding: 0.3rem;
  border-radius: 12px;
  box-shadow: 0 10px 30px rgba(0,0,0,0.1);
  border: 1px solid #e2e8f0;
  max-width: 100%;
  margin: 0.5rem auto;
}

.screenshot-img {
  width: 100%;
  border-radius: 8px;
  display: block;
  object-fit: contain;
}

/* Usage Proposal */
.usage-list {
  counter-reset: usage-counter;
  list-style: none;
  padding: 0;
  margin-top: 1.5rem;
}

.usage-list li {
  counter-increment: usage-counter;
  background: white;
  margin-bottom: 1rem;
  padding: 1rem 1.5rem;
  border-radius: 12px;
  display: flex;
  align-items: center;
  gap: 1.5rem;
  box-shadow: 0 2px 8px rgba(0,0,0,0.03);
}

.usage-list li::before {
  content: counter(usage-counter);
  background: #0a7e6c;
  color: white;
  width: 32px;
  height: 32px;
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 800;
  flex-shrink: 0;
}

/* Quote Slide: High Impact */
.quote-slide {
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 4rem;
  background: radial-gradient(circle at center, rgba(26, 87, 153, 0.03), transparent);
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
}

.quote-slide h2 {
  font-size: 2.8rem;
  line-height: 1.4;
  font-weight: 700;
  color: #1e293b;
  max-width: 900px;
}

.quote-highlight {
  color: #1a5799;
  font-weight: 800;
}

/* Onboarding Steps */
.onboarding-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.5rem;
  margin-top: 2rem;
}

.step-card {
  background: white;
  padding: 1.5rem;
  border-radius: 16px;
  box-shadow: 0 4px 12px rgba(0,0,0,0.04);
  text-align: center;
  position: relative;
  border: 1px solid #f1f5f9;
}

.step-number {
  position: absolute;
  top: -15px;
  left: 50%;
  transform: translateX(-50%);
  background: #1a5799;
  color: white;
  width: 30px;
  height: 30px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 800;
  font-size: 0.9rem;
}

.step-card h4 { margin: 1rem 0 0.5rem 0; }
.step-card p { font-size: 0.85rem; color: #64748b; margin: 0; }

/* Enhanced Link and Logo styles */
.app-link {
  display: inline-block;
  padding: 0.4rem 1rem;
  background: linear-gradient(135deg, rgba(26, 87, 153, 0.1) 0%, rgba(10, 126, 108, 0.1) 100%);
  border: 1px solid rgba(26, 87, 153, 0.2);
  border-radius: 100px;
  color: #1a5799 !important;
  font-weight: 700;
  text-decoration: none;
  transition: all 300ms ease;
  margin-top: 0.5rem;
}

.app-link:hover {
  background: linear-gradient(135deg, rgba(26, 87, 153, 0.2) 0%, rgba(10, 126, 108, 0.2) 100%);
  transform: translateY(-2px);
  box-shadow: 0 5px 15px rgba(26, 87, 153, 0.1);
}

.closing-logo {
  width: 120px;
  height: 120px;
  margin-bottom: 0.5rem;
  filter: drop-shadow(0 10px 20px rgba(0,0,0,0.1));
  animation: subtle-float 4s ease-in-out infinite;
}

@keyframes subtle-float {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-12px); }
}

.closing-title {
  font-size: 3.5rem;
  font-weight: 900;
  background: linear-gradient(135deg, #1a5799 0%, #0a7e6c 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  margin-bottom: 1.5rem;
  letter-spacing: -1px;
}
</style>

<div class="title-container">
  <div class="title-glass-card">
    <img src="/icon.png" class="title-icon" alt="Tinderstesia Logo">
    <h1 class="title-text">Tinderstesia</h1>
    <p class="title-subtitle">Propuesta para el Servicio de Anestesia</p>
    <div class="title-info">
      <p>Hospital Universitario Miguel Servet</p>
      <p style="margin-top: 1rem;">
        <a href="https://tinderstesia.vercel.app/" target="_blank" class="app-link">
          🚀 Acceder a tinderstesia.vercel.app
        </a>
      </p>
      <p class="tagline">Afinidades reales, decisiones informadas</p>
    </div>
  </div>
</div>

---

<div class="quote-slide">
  <h2 v-click>
    "Tinderstesia convierte <span class="quote-highlight">preferencias dispersas</span> en una visión clara de <span class="quote-highlight">afinidades reales</span> entre profesionales y unidades."
  </h2>
</div>

---

# Tinderstesia en vivo

<div class="screenshot-card" v-click>
  <img src="/tinderstesia_landing.png" class="screenshot-img" alt="Landing Page" style="max-height: 500px; width: 100%; object-fit: contain; border-radius: 12px;">
</div>

<p style="text-align: center; color: #64748b; font-size: 0.9rem;" v-click>
  Interfaz moderna y adaptada para escritorio y dispositivos móviles.
</p>

---

# ¿Qué problema resuelve?

<div class="problem-grid">
  <div class="problem-item" v-click>
    <span class="problem-icon">💬</span>
    <div class="problem-text">
      <p><b>Conversaciones informales</b><br>Información repartida y no registrada</p>
    </div>
  </div>
  <div class="problem-item" v-click>
    <span class="problem-icon">👁️</span>
    <div class="problem-text">
      <p><b>Percepciones parciales</b><br>Dificultad para ver la foto global</p>
    </div>
  </div>
  <div class="problem-item" v-click>
    <span class="problem-icon">⚖️</span>
    <div class="problem-text">
      <p><b>Dificultad de comparación</b><br>Candidatos y casas sin base homogénea</p>
    </div>
  </div>
  <div class="problem-item" v-click>
    <span class="problem-icon">⚠️</span>
    <div class="problem-text">
      <p><b>Información incompleta</b><br>Riesgo en la toma de decisiones</p>
    </div>
  </div>
</div>

---

# ¿Para qué sirve?

<div class="solution-card">
  <h3 v-click>Apoyar decisiones de reubicación</h3>
  <p v-click>Centraliza la captura de intereses para identificar:</p>
  
  <ul class="solution-list">
    <li v-click>Preferencias de los <b>profesionales</b></li>
    <li v-click>Interés de las <b>casas</b> por candidatos</li>
    <li v-click>Intensidad real y <b>coincidencias</b> bidireccionales</li>
    <li v-click>Afinidades fuertes vs. discrepancias</li>
  </ul>

  <p class="solution-footer" v-click>No sustituye el criterio de la administración. <b>Lo complementa con datos claros.</b></p>
</div>

---

# Onboarding: Empezar a usarla

<div class="onboarding-grid">
  <div class="step-card" v-click>
    <div class="step-number">1</div>
    <div class="actor-icon">🔑</div>
    <h4>Crear Cuenta</h4>
    <div class="screenshot-card" style="margin-top: 0.5rem; max-width: 100%;">
       <img src="/tinderstesia_signup.png" class="screenshot-img" style="height: 80px; object-fit: cover;">
    </div>
    <p>Acceso simple y creación de perfil personal</p>
  </div>
  <div class="step-card" v-click>
    <div class="step-number">2</div>
    <div class="actor-icon">📝</div>
    <h4>Configurar Perfil</h4>
    <div class="screenshot-card" style="margin-top: 0.5rem; max-width: 100%;">
       <img src="/tinderstesia_signin.png" class="screenshot-img" style="height: 80px; object-fit: cover;">
    </div>
    <p>Casa actual, guardias e información laboral</p>
  </div>
  <div class="step-card" v-click>
    <div class="step-number">3</div>
    <div class="actor-icon">🎮</div>
    <h4>Jugar</h4>
    <p>Valorar las casas en el panel de swipe</p>
  </div>
</div>

<p style="margin-top: 2rem; text-align: center; color: #64748b;" v-click>
  Un proceso rápido, visual y guiado para todos los profesionales.
</p>

---

# Las 7 Casas Incluidas

<div class="houses-grid">
  <div class="house-card" v-click.scale>
    <span class="house-emoji">🏥</span>
    <span>General</span>
  </div>
  <div class="house-card" v-click.scale>
    <span class="house-emoji">👨‍👩‍👧‍👦</span>
    <span>Mater</span>
  </div>
  <div class="house-card" v-click.scale>
    <span class="house-emoji">👶</span>
    <span>Infantil</span>
  </div>
  <div class="house-card" v-click.scale>
    <span class="house-emoji">❤️</span>
    <span>Cardiotorácica</span>
  </div>
  <div class="house-card" v-click.scale>
    <span class="house-emoji">🧬</span>
    <span>REA</span>
  </div>
  <div class="house-card" v-click.scale>
    <span class="house-emoji">💊</span>
    <span>CSI</span>
  </div>
  <div class="house-card" v-click.scale>
    <span class="house-emoji">🩺</span>
    <span>Dolor</span>
  </div>
</div>

---

# Qué ve cada perfil

<div class="actors-grid">
  <div class="actor-card candidate" v-click>
    <div class="actor-icon">👤</div>
    <h4>Profesional</h4>
    <div class="screenshot-card" style="margin: 0.5rem 0;">
       <img src="/user_view.png" class="screenshot-img" style="height: 100px; object-fit: cover;">
    </div>
    <ul>
      <li>Configura su perfil laboral</li>
      <li>Valora casas (swipe)</li>
      <li>Ve sus propios matches</li>
    </ul>
  </div>

  <div class="actor-card leader" v-click>
    <div class="actor-icon">👔</div>
    <h4>Responsable Casa</h4>
    <div class="screenshot-card" style="margin: 0.5rem 0;">
       <img src="/boss_view.png" class="screenshot-img" style="height: 100px; object-fit: cover;">
    </div>
    <ul>
      <li>Valora candidatos</li>
      <li>Ve matches de su casa</li>
      <li>Revisa info de candidatos</li>
    </ul>
  </div>

  <div class="actor-card admin" v-click>
    <div class="actor-icon">⚙️</div>
    <h4>Administración</h4>
    <div class="screenshot-card" style="margin: 0.5rem 0;">
       <img src="/admin_view.png" class="screenshot-img" style="height: 100px; object-fit: cover;">
    </div>
    <ul>
      <li>Visión global del panel</li>
      <li>Consulta fuerza de afinidad</li>
      <li>Detecta discrepancias</li>
    </ul>
  </div>
</div>

---

# Vista del Responsable

<div class="horizontal-video-container">
  <div v-click>
    <p style="font-size: 1.1rem; color: #475569; line-height: 1.6;">
      El responsable actúa en nombre de su casa para valorar a los candidatos y gestionar afinidades.
    </p>
    <ul style="margin-top: 1rem; color: #64748b; font-size: 0.9rem;">
      <li>Valora candidatos en tiempo real</li>
      <li>Ve matches consolidados de su casa</li>
      <li>Acceso a perfiles detallados</li>
    </ul>
  </div>
  <div class="screenshot-card" v-click style="padding: 0; overflow: hidden; border: none; box-shadow: 0 20px 50px rgba(0,0,0,0.2); background: #000;">
    <video 
      src="/videos/tinderapp-boss.webm" 
      controls 
      class="screenshot-img" 
      style="width: 100%; max-height: 420px; object-fit: contain; display: block;"
    ></video>
  </div>
</div>

---

# El Juego: Valoración Bidireccional

<div class="horizontal-video-container">
  <div v-click>
    <p style="font-size: 1.1rem; color: #475569; line-height: 1.6;">
      Interacción fluida de "swipe" para decidir preferencias con intensidad ajustable.
    </p>
    <ul style="margin-top: 1rem; color: #64748b; font-size: 0.9rem;">
      <li>Flujo de acceso seguro</li>
      <li>Valoración de intensidad (0-10)</li>
      <li>Matches inmediatos bidireccionales</li>
    </ul>
  </div>
  <div class="screenshot-card" v-click style="padding: 0; overflow: hidden; border: none; box-shadow: 0 20px 50px rgba(0,0,0,0.2); background: #000;">
    <video 
      src="/videos/tinderapp-user.webm" 
      controls 
      class="screenshot-img" 
      style="width: 100%; max-height: 420px; object-fit: contain; display: block;"
    ></video>
  </div>
</div>

---

# Fuerza de Afinidad (0-10)

<div class="match-section">
  <p v-click>Combina el interés de ambas partes para priorizar:</p>

  <div class="bond-examples">
    <div class="bond-row" v-click>
      <span class="bond-label">Candidato 10 + Casa 10</span>
      <span class="bond-value">🔥 10 — Coincidencia Máxima</span>
    </div>
    <div class="bond-row" v-click>
      <span class="bond-label">Candidato 8 + Casa 6</span>
      <span class="bond-value">✨ 7 — Interés Fuerte</span>
    </div>
    <div class="bond-row" v-click>
      <span class="bond-label">Candidato 5 + Casa 9</span>
      <span class="bond-value">⚡ 7 — Asimetría (Interés mutuo)</span>
    </div>
    <div class="bond-row" v-click>
      <span class="bond-label">Candidato 4 + Casa 0</span>
      <span class="bond-value">⚠️ 2 — Discrepancia Útil</span>
    </div>
  </div>

  <div class="solution-card" style="margin-top: 1.5rem;" v-click>
    <p style="margin: 0; font-size: 0.9rem;"><b>Match:</b> Ocurre cuando AMBAS partes marcan "Me interesa". La fuerza de afinidad ayuda a ordenar las opciones.</p>
  </div>
</div>

---

# ¿Qué aporta a la Dirección?

<div class="problem-grid">
  <div class="problem-item" v-click>
    <span class="problem-icon">📊</span>
    <div class="problem-text">
      <p><b>Visión rápida</b><br>Fotografía instantánea del interés real</p>
    </div>
  </div>
  <div class="problem-item" v-click>
    <span class="problem-icon">📑</span>
    <div class="problem-text">
      <p><b>Información estructurada</b><br>Datos homogéneos y comparables</p>
    </div>
  </div>
  <div class="problem-item" v-click>
    <span class="problem-icon">📉</span>
    <div class="problem-text">
      <p><b>Menos ruido</b><br>Reduce impresiones subjetivas</p>
    </div>
  </div>
  <div class="problem-item" v-click>
    <span class="problem-icon">✨</span>
    <div class="problem-text">
      <p><b>Transparencia</b><br>Proceso trazable y reproducible</p>
    </div>
  </div>
</div>

---

# Ejemplo Sencillo

<div class="roadmap-section">
  <div class="roadmap-column v1" v-click>
    <h3>Caso A: Match Fuerte</h3>
    <p>Profesional → Mucho interés por REA</p>
    <p>REA → Mucho interés por Profesional</p>
    <div class="tagline" style="color: #0a7e6c;">Opción clara de reubicación</div>
  </div>

  <div class="roadmap-column future" v-click style="border-left-color: #f59e0b;">
    <h3>Caso B: Afinidades Débiles</h3>
    <p>Profesional → Interés por Mater</p>
    <p>Mater → No muestra interés</p>
    <div class="tagline" style="color: #f59e0b;">Información útil, no es prioridad</div>
  </div>
</div>

---

# ¿Qué NO hace Tinderstesia?

<div class="disclaimer-grid">
  <div class="disclaimer-item" v-click>
    <span>❌</span> No sustituye la decisión final
  </div>
  <div class="disclaimer-item" v-click>
    <span>❌</span> No recoloca automáticamente
  </div>
  <div class="disclaimer-item" v-click>
    <span>❌</span> No trata datos de pacientes
  </div>
  <div class="disclaimer-item" v-click>
    <span>❌</span> No impone resultados
  </div>
</div>

<p style="margin-top: 2rem; text-align: center; font-style: italic;" v-click>
  Es una herramienta de <b>apoyo</b> a la decisión humana.
</p>

---

# Propuesta de Uso

<ul class="usage-list">
  <li v-click>Validar casas y responsables</li>
  <li v-click>Profesionales completan perfiles y valoran casas</li>
  <li v-click>Responsables valoran candidatos</li>
  <li v-click>Revisión del panel global de afinidades</li>
  <li v-click>Uso de resultados como apoyo para decidir</li>
</ul>

---

# Stack Técnico & Roadmap

<div class="tech-grid" style="transform: scale(0.85); margin-top: -1rem;">
  <div class="tech-item" v-click>
    <div class="tech-label">Next.js 16 + React 19</div>
  </div>
  <div class="tech-item" v-click>
    <div class="tech-label">Prisma 7 + PostgreSQL</div>
  </div>
  <div class="tech-item" v-click>
    <div class="tech-label">Clerk + Roles</div>
  </div>
  <div class="tech-item" v-click>
    <div class="tech-label">Vitest + Playwright</div>
  </div>
</div>

<div class="roadmap-section" style="margin-top: 1rem; transform: scale(0.9);">
  <div class="roadmap-column v1" v-click>
    <h3>✅ V1 Cubierta</h3>
    <p>Swipe, Matches, Roles, Panel Admin</p>
  </div>
  <div class="roadmap-column future" v-click>
    <h3>🚀 Futuro</h3>
    <p>Reasignación auto, Historial, Exportación CSV</p>
  </div>
</div>

---

<div class="closing-slide">
  <img src="/icon.png" class="closing-logo" alt="Tinderstesia Logo" v-click>
  <div class="closing-title" v-click>Tinderstesia</div>
  <h2 v-click style="font-size: 1.8rem; color: #1e293b; margin-bottom: 1rem;">Decisiones más claras, procesos más humanos.</h2>
  
  <p class="closing-subtitle" v-click style="max-width: 800px; color: #475569; font-size: 1.2rem; line-height: 1.6; margin-bottom: 3rem;">
    Escuchar a los profesionales e incorporar la visión de las casas para decidir con mejores datos.
  </p>

  <div class="closing-footer" v-click style="border-top: 1px solid #e2e8f0; padding-top: 2rem; color: #64748b; font-size: 1rem;">
    Hospital Universitario Miguel Servet<br>
    <span style="font-weight: 700; color: #1a5799;">Desarrollado por David Guallar</span>
  </div>
</div>

