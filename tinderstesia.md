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

# Tinderstesia

*Una plataforma de afinidades para la reubicación de anestesia*

<div class="pt-8 text-lg opacity-80">
Hospital Universitario Miguel Servet<br>
Desarrollado por David Guallar<br>
Afinidades reales, decisiones informadas
</div>

---

# El Problema

<div class="problem-card">
  <div class="problem-item" v-click>
    <span class="problem-icon">👤</span>
    <p><b>Preferencias dispersas</b><br>Difíciles de capturar y comparar</p>
  </div>
  <div class="problem-item" v-click>
    <span class="problem-icon">🏥</span>
    <p><b>Intereses no sistematizados</b><br>Las casas no expresan sus necesidades</p>
  </div>
  <div class="problem-item" v-click>
    <span class="problem-icon">💬</span>
    <p><b>Conversaciones informales</b><br>Decisiones dispersas, sin trazabilidad</p>
  </div>
  <div class="problem-item" v-click>
    <span class="problem-icon">📊</span>
    <p><b>Falta de transparencia</b><br>Proceso opaco y poco reproducible</p>
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
      <li>Gestiona usuarios y roles</li>
      <li>Gestiona casas</li>
      <li>Asigna jefaturas</li>
      <li>Ve panel global</li>
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

<div class="admin-panel">
  <h3>Herramientas de Análisis</h3>

  <div class="panel-sections">
    <div class="panel-section" v-click>
      <h4><span class="section-icon">📊</span> Estadísticas Globales</h4>
      <ul>
        <li>Total de pares evaluados</li>
        <li>Score promedio</li>
        <li>% de matches</li>
        <li>% de relaciones convergentes</li>
      </ul>
    </div>

    <div class="panel-section" v-click>
      <h4><span class="section-icon">🔍</span> Filtros y Búsqueda</h4>
      <ul>
        <li>Por usuario o casa</li>
        <li>Por rango de score</li>
        <li>Solo matches activos</li>
        <li>Solo valoradas por ambas partes</li>
      </ul>
    </div>

    <div class="panel-section" v-click>
      <h4><span class="section-icon">📈</span> Ordenación</h4>
      <ul>
        <li>Por score (mayor/menor)</li>
        <li>Por nombre usuario</li>
        <li>Por nombre casa</li>
      </ul>
    </div>
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
      <li>Registro y sincronización</li>
      <li>Gestión de roles</li>
      <li>Swipe bidireccional</li>
      <li>Matches automáticos</li>
      <li>Fuerza de vínculo</li>
      <li>Panel administrativo</li>
      <li>Fotos y perfiles</li>
      <li>Tests E2E</li>
    </ul>
  </div>

  <div class="roadmap-column future" v-click>
    <h3>🚀 Fuera de Alcance V1</h3>
    <ul>
      <li>Reasignación automática</li>
      <li>Optimización global</li>
      <li>Historial completo</li>
      <li>Matching de guardias</li>
      <li>Múltiples rondas</li>
      <li>Rate limiting avanzado</li>
      <li>Exportación CSV</li>
      <li>Comentarios privados</li>
    </ul>
  </div>
</div>

---

# Mensaje de Cierre

<div class="closing-slide">
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

<style>
/* Global styles with smooth transitions */
.slidev-layout {
  background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
  font-family: 'IBM Plex Sans', sans-serif;
  color: #1a1a1a;
  --uno: transition-all duration-500 ease-out;
}

h1, h2, h3, h4, h5, h6 {
  --uno: font-weight-700 transition-all duration-500;
}

/* v-click animations */
.slidev-vclick-target {
  transition: all 500ms cubic-bezier(0.34, 1.56, 0.64, 1);
}

.slidev-vclick-hidden {
  opacity: 0;
  transform: translateY(20px);
}

/* Problem slide */
.problem-card {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2rem;
  margin-top: 1.5rem;
}

.problem-item {
  background: white;
  padding: 1.5rem;
  border-radius: 16px;
  box-shadow: 0 4px 12px rgba(26, 87, 153, 0.1);
  display: flex;
  flex-direction: column;
  gap: 1rem;
  border-left: 6px solid #1a5799;
  transition: all 400ms cubic-bezier(0.34, 1.56, 0.64, 1);
}

.problem-item:hover {
  transform: translateY(-8px);
  box-shadow: 0 8px 24px rgba(26, 87, 153, 0.15);
}

.problem-icon {
  font-size: 2.8rem;
  display: block;
  line-height: 1;
}

.problem-item p {
  margin: 0;
  line-height: 1.6;
}

/* Solution slide */
.solution-card {
  background: white;
  padding: 2.5rem;
  border-radius: 16px;
  box-shadow: 0 6px 16px rgba(10, 126, 108, 0.1);
  border-left: 8px solid #0a7e6c;
  transition: all 400ms ease;
}

.solution-card h3 {
  color: #0a7e6c;
  margin: 0 0 1.2rem 0;
  font-size: 1.4rem;
}

.solution-list {
  list-style: none;
  padding: 0;
  margin: 1.8rem 0;
}

.solution-list li {
  margin: 1rem 0;
  padding-left: 2.5rem;
  position: relative;
  font-size: 1.05rem;
  line-height: 1.8;
}

.solution-list li:before {
  content: "✓";
  position: absolute;
  left: 0;
  color: #0a7e6c;
  font-weight: bold;
  font-size: 1.3rem;
}

.solution-footer {
  margin-top: 2rem;
  padding-top: 1.5rem;
  border-top: 2px solid #e9ecef;
  font-style: italic;
  opacity: 0.85;
  color: #666;
}

/* Houses grid */
.houses-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.5rem;
  margin-top: 2rem;
}

.house-card {
  background: white;
  padding: 2rem;
  border-radius: 14px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.06);
  font-size: 1rem;
  text-align: center;
  border-top: 5px solid #1a5799;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 0.8rem;
  min-height: 140px;
  transition: all 400ms cubic-bezier(0.34, 1.56, 0.64, 1);
  cursor: pointer;
}

.house-card:nth-child(2) { border-top-color: #0a7e6c; }
.house-card:nth-child(3) { border-top-color: #334155; }
.house-card:nth-child(4) { border-top-color: #1a5799; }
.house-card:nth-child(5) { border-top-color: #0a7e6c; }
.house-card:nth-child(6) { border-top-color: #334155; }
.house-card:nth-child(7) { border-top-color: #1a5799; }

.house-card:hover {
  transform: scale(1.08) translateY(-6px);
  box-shadow: 0 12px 24px rgba(0, 0, 0, 0.12);
}

.house-emoji {
  font-size: 2.2rem;
  display: block;
  line-height: 1;
}

/* Actors grid */
.actors-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
  margin-top: 2.5rem;
}

.actor-card {
  background: white;
  padding: 2rem;
  border-radius: 14px;
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.06);
  border-left: 7px solid;
  transition: all 400ms cubic-bezier(0.34, 1.56, 0.64, 1);
}

.actor-card.candidate { border-left-color: #1a5799; }
.actor-card.leader { border-left-color: #0a7e6c; }
.actor-card.admin { border-left-color: #334155; }

.actor-card:hover {
  transform: translateY(-12px);
  box-shadow: 0 12px 32px rgba(0, 0, 0, 0.1);
}

.actor-icon {
  font-size: 3rem;
  margin-bottom: 1rem;
  display: block;
  line-height: 1;
}

.actor-card h4 {
  margin: 0 0 0.7rem 0;
  color: #1a1a1a;
  font-size: 1.15rem;
}

.role-id {
  background: linear-gradient(135deg, #f0f0f0 0%, #e8e8e8 100%);
  padding: 0.4rem 0.8rem;
  border-radius: 6px;
  font-family: 'IBM Plex Mono', monospace;
  font-size: 0.8rem;
  margin: 0 0 1.2rem 0;
  border: 1px solid #e0e0e0;
}

.actor-card ul {
  list-style: none;
  padding: 0;
  margin: 0;
  font-size: 0.95rem;
  line-height: 2;
}

.actor-card li {
  transition: all 200ms ease;
}

.actor-card li:before {
  content: "→ ";
  color: inherit;
  margin-right: 0.5rem;
  opacity: 0.7;
  transition: all 200ms ease;
}

.actor-card:hover li:before {
  opacity: 1;
}

/* Swipe demo */
.swipe-demo {
  display: flex;
  flex-direction: column;
  gap: 2.5rem;
  margin-top: 2.5rem;
  align-items: center;
}

.swipe-card {
  background: white;
  border-radius: 18px;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.15);
  width: 100%;
  max-width: 520px;
  overflow: hidden;
  transition: all 400ms ease;
}

.swipe-card:hover {
  transform: scale(1.04);
  box-shadow: 0 12px 48px rgba(0, 0, 0, 0.2);
}

.card-header {
  background: linear-gradient(135deg, #1a5799 0%, #0a7e6c 100%);
  color: white;
  padding: 2rem;
  display: flex;
  gap: 1.5rem;
  align-items: center;
}

.card-stripe {
  width: 5px;
  height: 60px;
  background: white;
  border-radius: 3px;
  animation: pulse 2s ease-in-out infinite;
}

@keyframes pulse {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.6; }
}

.card-header h3 {
  margin: 0 0 0.5rem 0;
  font-size: 1.4rem;
  font-weight: 700;
}

.card-meta {
  margin: 0;
  opacity: 0.95;
  font-size: 0.95rem;
  font-weight: 300;
}

.card-body {
  padding: 2rem;
  line-height: 1.7;
  font-size: 1rem;
}

.card-body p {
  margin: 0 0 1rem 0;
  color: #444;
}

.card-body p:last-child {
  margin-bottom: 0;
}

.swipe-controls {
  text-align: center;
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
  transition: all 400ms ease;
}

.control-buttons {
  display: flex;
  gap: 2rem;
  justify-content: center;
}

.control-button {
  font-weight: 600;
  color: white;
  font-size: 1.1rem;
  padding: 0.8rem 1.5rem;
  border-radius: 8px;
  transition: all 300ms ease;
  cursor: pointer;
}

.control-button.left {
  background: linear-gradient(135deg, #1a5799 0%, #1a3a6b 100%);
}

.control-button.right {
  background: linear-gradient(135deg, #0a7e6c 0%, #066b54 100%);
}

.control-button:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
}

.intensity-slider {
  background: white;
  padding: 1rem 1.5rem;
  border-radius: 10px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.06);
  display: flex;
  flex-direction: column;
  gap: 0.8rem;
}

.intensity-slider span {
  font-size: 0.9rem;
  color: #666;
  font-weight: 500;
}

.slider-bar {
  height: 6px;
  background: linear-gradient(90deg, #1a5799 0%, #0a7e6c 100%);
  border-radius: 3px;
  position: relative;
}

.slider-bar:after {
  content: '';
  position: absolute;
  right: 0;
  top: 50%;
  transform: translateY(-50%);
  width: 16px;
  height: 16px;
  background: white;
  border: 3px solid #0a7e6c;
  border-radius: 50%;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

/* Match and bond section */
.match-section {
  background: white;
  padding: 2.5rem;
  border-radius: 16px;
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.06);
}

.match-section h3 {
  color: #1a5799;
  margin: 0 0 1.2rem 0;
  font-size: 1.25rem;
  font-weight: 700;
}

.match-section ul {
  list-style: none;
  padding: 0;
  margin: 0 0 2rem 0;
}

.match-section li {
  margin: 0.8rem 0;
  padding-left: 2rem;
  position: relative;
  font-size: 1.05rem;
  line-height: 1.6;
}

.match-section li:before {
  content: "•";
  position: absolute;
  left: 0;
  color: #0a7e6c;
  font-weight: bold;
  font-size: 1.2rem;
}

.bond-examples {
  margin-top: 2rem;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1.2rem;
}

.bond-row {
  background: linear-gradient(135deg, #f8f9fa 0%, #f0f1f3 100%);
  padding: 1.4rem;
  border-radius: 12px;
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
  border-left: 4px solid #0a7e6c;
  transition: all 300ms ease;
}

.bond-row:hover {
  transform: translateY(-4px);
  box-shadow: 0 4px 12px rgba(10, 126, 108, 0.1);
}

.bond-label {
  font-size: 0.85rem;
  color: #777;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.bond-value {
  font-weight: 700;
  color: #1a5799;
  font-size: 1.05rem;
}

/* Admin panel */
.admin-panel {
  background: white;
  padding: 2.5rem;
  border-radius: 16px;
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.06);
}

.admin-panel h3 {
  color: #334155;
  margin: 0 0 2rem 0;
  font-size: 1.3rem;
  font-weight: 700;
}

.panel-sections {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
}

.panel-section {
  transition: all 400ms ease;
}

.panel-section h4 {
  color: #1a5799;
  margin: 0 0 1.3rem 0;
  font-size: 1.05rem;
  font-weight: 700;
  display: flex;
  align-items: center;
  gap: 0.7rem;
}

.section-icon {
  font-size: 1.2rem;
  display: block;
}

.panel-section ul {
  list-style: none;
  padding: 0;
  margin: 0;
  font-size: 0.95rem;
  line-height: 2;
}

.panel-section li {
  transition: all 200ms ease;
  padding-left: 0.5rem;
}

.panel-section li:before {
  content: "◆ ";
  color: #0a7e6c;
  margin-right: 0.5rem;
  font-size: 0.8rem;
}

.panel-section:hover li {
  padding-left: 1rem;
}

/* Tech grid */
.tech-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1.8rem;
  margin-top: 2rem;
}

.tech-item {
  background: white;
  padding: 2rem;
  border-radius: 14px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.06);
  transition: all 400ms cubic-bezier(0.34, 1.56, 0.64, 1);
}

.tech-item:hover {
  transform: translateY(-8px);
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.1);
}

.tech-label {
  display: block;
  font-weight: 700;
  color: #334155;
  margin-bottom: 1.2rem;
  font-size: 0.95rem;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.tech-badges {
  display: flex;
  flex-wrap: wrap;
  gap: 0.7rem;
}

.badge {
  background: linear-gradient(135deg, #1a5799 0%, #0a7e6c 100%);
  color: white;
  padding: 0.5rem 1rem;
  border-radius: 20px;
  font-size: 0.8rem;
  font-weight: 600;
  transition: all 300ms ease;
  display: inline-block;
}

.badge:hover {
  transform: scale(1.08);
  box-shadow: 0 4px 12px rgba(26, 87, 153, 0.3);
}

/* Roadmap section */
.roadmap-section {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2.5rem;
  margin-top: 2.5rem;
}

.roadmap-column {
  background: white;
  padding: 2.5rem;
  border-radius: 16px;
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.06);
  border-left: 8px solid;
  transition: all 400ms cubic-bezier(0.34, 1.56, 0.64, 1);
}

.roadmap-column:hover {
  transform: translateY(-8px);
  box-shadow: 0 12px 32px rgba(0, 0, 0, 0.1);
}

.roadmap-column.v1 { border-left-color: #0a7e6c; }
.roadmap-column.v1 h3 { color: #0a7e6c; }

.roadmap-column.future { border-left-color: #ff6600; }
.roadmap-column.future h3 { color: #ff6600; }

.roadmap-column h3 {
  margin: 0 0 1.5rem 0;
  font-size: 1.2rem;
  font-weight: 700;
}

.roadmap-column ul {
  list-style: none;
  padding: 0;
  margin: 0;
  font-size: 0.95rem;
  line-height: 2.2;
}

.roadmap-column li {
  transition: all 200ms ease;
  padding-left: 0.5rem;
}

.roadmap-column li:before {
  content: "✓ ";
  color: inherit;
  margin-right: 0.5rem;
  opacity: 0.8;
  font-weight: bold;
}

.roadmap-column.future li:before { content: "→ "; }

.roadmap-column:hover li {
  padding-left: 1rem;
}

/* Closing slide */
.closing-slide {
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  min-height: 100%;
  gap: 2.5rem;
  padding: 4rem 2rem;
}

.closing-slide h2 {
  font-size: 2.2rem;
  color: #1a5799;
  margin: 0;
  line-height: 1.5;
  max-width: 900px;
  font-weight: 800;
}

.closing-subtitle {
  font-size: 1.2rem;
  color: #666;
  margin: 0;
  max-width: 800px;
  line-height: 1.8;
  font-weight: 500;
}

.closing-footer {
  margin-top: 2rem;
  font-size: 1rem;
  color: #999;
  border-top: 2px solid #ddd;
  padding-top: 2rem;
  font-weight: 500;
}
</style>
