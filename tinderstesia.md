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
  width: 140px !important;
  height: 140px !important;
  margin: 0 auto 2rem auto !important;
  display: block;
  filter: drop-shadow(0 10px 20px rgba(26, 87, 153, 0.2));
  animation: float 6s ease-in-out infinite;
}

@keyframes float {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-15px); }
}

.title-text {
  font-size: 4.5rem !important;
  font-weight: 800 !important;
  background: linear-gradient(135deg, #1a5799 0%, #0a7e6c 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  margin-bottom: 0.8rem !important;
  letter-spacing: -1px;
}

.title-subtitle {
  font-size: 1.5rem;
  color: #475569;
  margin-bottom: 2.5rem;
  font-weight: 500;
  line-height: 1.4;
}

.title-info {
  border-top: 1px solid rgba(0, 0, 0, 0.08);
  padding-top: 2rem;
  color: #64748b;
  font-size: 1rem;
  line-height: 1.6;
}

.tagline {
  color: #1a5799;
  font-weight: 700;
  margin-top: 1rem;
  letter-spacing: 2px;
  text-transform: uppercase;
  font-size: 0.85rem;
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

.closing-title {
  font-size: 1.2rem;
  text-transform: uppercase;
  letter-spacing: 3px;
  color: #64748b;
  margin-bottom: 1rem;
  font-weight: 700;
}

.closing-slide h2 {
  font-size: 2.5rem;
  background: linear-gradient(135deg, #1a5799 0%, #0a7e6c 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  max-width: 90%;
  line-height: 1.3;
}

.closing-subtitle {
  font-size: 1.3rem;
  color: #475569;
  max-width: 80%;
}

.closing-footer {
  margin-top: 2rem;
  color: #94a3b8;
  font-size: 1rem;
  border-top: 1px solid #e2e8f0;
  padding-top: 2rem;
}
</style>

<div class="title-container">
  <div class="title-glass-card">
    <img src="/icon.png" class="title-icon" alt="Tinderstesia Logo">
    <h1 class="title-text">Tinderstesia</h1>
    <p class="title-subtitle">Una plataforma de afinidades para la reubicación de anestesia</p>
    <div class="title-info">
      <p>Hospital Universitario Miguel Servet</p>
      <p>Desarrollado por David Guallar</p>
      <p class="tagline">Afinidades reales, decisiones informadas</p>
    </div>
  </div>
</div>

---

# El Problema

<div class="problem-grid">
  <div class="problem-item" v-click>
    <span class="problem-icon">👤</span>
    <div class="problem-text">
      <p><b>Preferencias dispersas</b><br>Difíciles de capturar y comparar</p>
    </div>
  </div>
  <div class="problem-item" v-click>
    <span class="problem-icon">🏥</span>
    <div class="problem-text">
      <p><b>Intereses no sistematizados</b><br>Las casas no expresan sus necesidades</p>
    </div>
  </div>
  <div class="problem-item" v-click>
    <span class="problem-icon">💬</span>
    <div class="problem-text">
      <p><b>Conversaciones informales</b><br>Decisiones dispersas, sin trazabilidad</p>
    </div>
  </div>
  <div class="problem-item" v-click>
    <span class="problem-icon">📊</span>
    <div class="problem-text">
      <p><b>Falta de transparencia</b><br>Proceso opaco y poco reproducible</p>
    </div>
  </div>
</div>

---

# La Solución

<div class="solution-card">
  <h3 v-click>Un sistema ordenado de afinidades</h3>
  <p v-click>Tinderstesia centraliza la captura bidireccional de preferencias:</p>
  
  <ul class="solution-list">
    <li v-click>Los candidatos valoran casas mediante un interfaz tipo <b>swipe</b></li>
    <li v-click>Las casas responden valorando candidatos</li>
    <li v-click>El sistema calcula la <b>fuerza de vínculo</b> entre ambas partes</li>
    <li v-click>La administración dispone de información <b>estructurada</b> para tomar decisiones</li>
  </ul>

  <p class="solution-footer" v-click>La decisión final sigue siendo humana. Los datos la hacen más informada, transparente y reproducible.</p>
</div>

---

# Las 7 Casas

<div class="houses-grid">
  <div class="house-card" v-click.scale>
    <span class="house-emoji">🏥</span>
    <span>General</span>
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
  <div class="house-card" v-click.scale>
    <span class="house-emoji">👨‍👩‍👧‍👦</span>
    <span>Mater</span>
  </div>
</div>

---

# Los Actores y sus Roles

<div class="actors-grid">
  <div class="actor-card candidate" v-click>
    <div class="actor-icon">👤</div>
    <h4>Candidato</h4>
    <p class="role-id"><code>normal_user</code></p>
    <ul>
      <li>Valora casas activas</li>
      <li>Ve sus propios matches</li>
      <li>Completa su perfil laboral</li>
      <li>Sube fotos de perfil</li>
    </ul>
  </div>

  <div class="actor-card leader" v-click>
    <div class="actor-icon">👔</div>
    <h4>Jefe de Casa</h4>
    <p class="role-id"><code>section_leader</code></p>
    <ul>
      <li>Valora candidatos</li>
      <li>Ve matches de su casa</li>
      <li>Edita info de su casa</li>
      <li>Sube fotos de la casa</li>
    </ul>
  </div>

  <div class="actor-card admin" v-click>
    <div class="actor-icon">⚙️</div>
    <h4>Administración</h4>
    <p class="role-id"><code>admin</code></p>
    <ul>
      <li>Gestiona usuarios</li>
      <li>Gestiona casas</li>
      <li>Asigna jefaturas</li>
      <li>Panel global</li>
    </ul>
  </div>
</div>

---
clicks: 1
---

# El Juego: Swipe de Casas

<div class="swipe-demo">
  <div class="swipe-card">
    <div class="card-header">
      <div class="card-stripe"></div>
      <div>
        <h3>General</h3>
        <p class="card-meta">Casa de Anestesia General</p>
      </div>
    </div>
    <div class="card-body">
      <p>Responsable: Dra. García López</p>
      <p>Equipos disponibles, urgencias frecuentes, rotación completa</p>
      <Typewriter v-if="$clicks >= 1" text="¿Te interesa esta casa?" />
    </div>
  </div>

  <div class="swipe-controls" v-click>
    <div class="control-buttons">
      <div class="control-button left">← Paso</div>
      <div class="control-button right">Me interesa →</div>
    </div>
    <div class="intensity-slider">
      <span>Intensidad: 0-10</span>
      <div class="slider-bar"></div>
    </div>
  </div>
</div>

---

# Match y Fuerza de Vínculo

<div class="match-section">
  <h3>¿Cuándo existe un Match?</h3>
  <p>Cuando hay <b>doble interés</b>:</p>
  <ul>
    <li v-click>Candidato marca "Me interesa" en una casa <b>AND</b></li>
    <li v-click>Esa casa marca "Me interesa" en el candidato</li>
  </ul>

  <h3 style="margin-top: 2rem;">La Fuerza de Vínculo (0-10)</h3>
  <p v-click>Combina las intensidades de ambas partes:</p>

  <div class="bond-examples">
    <div class="bond-row" v-click>
      <span class="bond-label">Candidato 10 + Casa 10</span>
      <span class="bond-value">🔥 10 — Vínculo máximo</span>
    </div>
    <div class="bond-row" v-click>
      <span class="bond-label">Candidato 8 + Casa 6</span>
      <span class="bond-value">✨ 7 — Fuerte pero asimétrico</span>
    </div>
    <div class="bond-row" v-click>
      <span class="bond-label">Candidato 5 + Casa 9</span>
      <span class="bond-value">⚡ 7 — Interés mutuo, débil de una parte</span>
    </div>
    <div class="bond-row" v-click>
      <span class="bond-label">Candidato 4 + Casa 8</span>
      <span class="bond-value">⚠️ 6 — Divergencia, útil para análisis</span>
    </div>
  </div>
</div>

---

# Panel de Fuerza de Vínculo

<div class="admin-panel-container">

<div class="panel-section" v-click>

#### 📊 Estadísticas Globales

- Total de pares evaluados
- Score promedio
- % de matches
- % de relaciones convergentes

</div>

<div class="panel-section" v-click>

#### 🔍 Filtros y Búsqueda

- Por usuario o casa
- Por rango de score
- Solo matches activos
- Solo valoradas por ambas partes

</div>

<div class="panel-section" v-click>

#### 📈 Ordenación

- Por score (mayor/menor)
- Por nombre usuario
- Por nombre casa

</div>

</div>

---

# Stack Técnico

<div class="tech-grid">
  <div class="tech-item" v-click>
    <div class="tech-label">Frontend</div>
    <div class="tech-badges">
      <span class="badge">Next.js 16</span>
      <span class="badge">React 19</span>
      <span class="badge">Tailwind CSS 4</span>
    </div>
  </div>

  <div class="tech-item" v-click>
    <div class="tech-label">Backend</div>
    <div class="tech-badges">
      <span class="badge">Next.js API Routes</span>
      <span class="badge">Server Actions</span>
      <span class="badge">Prisma 7</span>
    </div>
  </div>

  <div class="tech-item" v-click>
    <div class="tech-label">Base de Datos</div>
    <div class="tech-badges">
      <span class="badge">PostgreSQL</span>
      <span class="badge">Railway</span>
    </div>
  </div>

  <div class="tech-item" v-click>
    <div class="tech-label">Autenticación</div>
    <div class="tech-badges">
      <span class="badge">Clerk</span>
      <span class="badge">Auth con Roles</span>
    </div>
  </div>

  <div class="tech-item" v-click>
    <div class="tech-label">Almacenamiento</div>
    <div class="tech-badges">
      <span class="badge">Railway Storage</span>
      <span class="badge">URLs Firmadas</span>
    </div>
  </div>

  <div class="tech-item" v-click>
    <div class="tech-label">Validación y Testing</div>
    <div class="tech-badges">
      <span class="badge">Zod</span>
      <span class="badge">Vitest</span>
      <span class="badge">Playwright</span>
    </div>
  </div>
</div>

---

# Estado Actual vs. Roadmap

<div class="roadmap-section">
  <div class="roadmap-column v1" v-click>
    <h3>✅ V1 Cubierta</h3>
    <ul>
      <li>Registro y roles</li>
      <li>Swipe bidireccional</li>
      <li>Matches automáticos</li>
      <li>Fuerza de vínculo</li>
      <li>Panel administrativo</li>
      <li>Fotos y perfiles</li>
      <li>Tests E2E</li>
    </ul>
  </div>

  <div class="roadmap-column future" v-click>
    <h3>🚀 Roadmap</h3>
    <ul>
      <li>Reasignación auto</li>
      <li>Optimización global</li>
      <li>Historial completo</li>
      <li>Matching guardias</li>
      <li>Múltiples rondas</li>
      <li>Rate limiting</li>
      <li>Exportación CSV</li>
    </ul>
  </div>
</div>

---

<div class="closing-slide">
  <div class="closing-title">Mensaje de Cierre</div>
  <h2 v-click>Tinderstesia convierte un proceso potencialmente subjetivo y disperso en un sistema ordenado de afinidades.</h2>
  
  <p class="closing-subtitle" v-click>
    No automatiza decisiones. No sustituye el criterio humano.
  </p>
  
  <p class="closing-subtitle" v-click>
    Lo que hace es hacerlo más informado, transparente y reproducible.
  </p>

  <div class="closing-footer" v-click>
    Hospital Universitario Miguel Servet<br>
    Desarrollado por David Guallar
  </div>
</div>

