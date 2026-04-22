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
  <div class="problem-item">
    <span class="problem-icon">👤</span>
    <p><b>Preferencias dispersas</b><br>Difíciles de capturar y comparar</p>
  </div>
  <div class="problem-item">
    <span class="problem-icon">🏥</span>
    <p><b>Intereses no sistematizados</b><br>Las casas no expresan sus necesidades</p>
  </div>
  <div class="problem-item">
    <span class="problem-icon">💬</span>
    <p><b>Conversaciones informales</b><br>Decisiones dispersas, sin trazabilidad</p>
  </div>
  <div class="problem-item">
    <span class="problem-icon">📊</span>
    <p><b>Falta de transparencia</b><br>Proceso opaco y poco reproducible</p>
  </div>
</div>

---

# La Solución

<div class="solution-card">
  <h3>Un sistema ordenado de afinidades</h3>
  <p>Tinderstesia centraliza la captura bidireccional de preferencias:</p>
  
  <ul class="solution-list">
    <li>Los candidatos valoran casas mediante un interfaz tipo <b>swipe</b></li>
    <li>Las casas responden valorando candidatos</li>
    <li>El sistema calcula la <b>fuerza de vínculo</b> entre ambas partes</li>
    <li>La administración dispone de información <b>estructurada</b> para tomar decisiones</li>
  </ul>

  <p class="solution-footer">La decisión final sigue siendo humana. Los datos la hacen más informada, transparente y reproducible.</p>
</div>

---

# Las 7 Casas

<div class="houses-grid">
  <div class="house-card">🏥 General</div>
  <div class="house-card">👶 Infantil</div>
  <div class="house-card">❤️ Cardiotorácica</div>
  <div class="house-card">🧬 REA</div>
  <div class="house-card">💊 CSI</div>
  <div class="house-card">🩺 Dolor</div>
  <div class="house-card">👨‍👩‍👧‍👦 Mater</div>
</div>

---

# Los Actores y sus Roles

<div class="actors-grid">
  <div class="actor-card candidate">
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

  <div class="actor-card leader">
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

  <div class="actor-card admin">
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
      <h3>General</h3>
      <p class="card-meta">Casa de Anestesia General</p>
    </div>
    <div class="card-body">
      <p>Responsable: Dra. García López</p>
      <p>Equipos disponibles, urgencias frecuentes, rotación completa</p>
      <Typewriter v-if="$clicks >= 1" text="¿Te interesa esta casa?" />
    </div>
  </div>

  <div class="swipe-controls">
    <div class="control-item">← Paso</div>
    <div class="control-bar">
      <span>Intensidad: 0-10</span>
    </div>
    <div class="control-item">Me interesa →</div>
  </div>
</div>

---

# Match y Fuerza de Vínculo

<div class="match-section">
  <h3>¿Cuándo existe un Match?</h3>
  <p>Cuando hay <b>doble interés</b>:</p>
  <ul>
    <li>Candidato marca "Me interesa" en una casa <b>AND</b></li>
    <li>Esa casa marca "Me interesa" en el candidato</li>
  </ul>

  <h3 style="margin-top: 2rem;">La Fuerza de Vínculo (0-10)</h3>
  <p>Combina las intensidades de ambas partes:</p>

  <div class="bond-examples">
    <div class="bond-row">
      <span class="bond-label">Candidato 10 + Casa 10</span>
      <span class="bond-value">🔥 10 — Vínculo máximo</span>
    </div>
    <div class="bond-row">
      <span class="bond-label">Candidato 8 + Casa 6</span>
      <span class="bond-value">✨ 7 — Fuerte pero asimétrico</span>
    </div>
    <div class="bond-row">
      <span class="bond-label">Candidato 5 + Casa 9</span>
      <span class="bond-value">⚡ 7 — Interés mutuo, pero débil de una parte</span>
    </div>
    <div class="bond-row">
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
    <div class="panel-section">
      <h4>📊 Estadísticas Globales</h4>
      <ul>
        <li>Total de pares evaluados</li>
        <li>Score promedio</li>
        <li>% de matches</li>
        <li>% de relaciones convergentes</li>
      </ul>
    </div>

    <div class="panel-section">
      <h4>🔍 Filtros y Búsqueda</h4>
      <ul>
        <li>Por usuario o casa</li>
        <li>Por rango de score</li>
        <li>Solo matches activos</li>
        <li>Solo valoradas por ambas partes</li>
      </ul>
    </div>

    <div class="panel-section">
      <h4>📈 Ordenación</h4>
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
  <div class="tech-item">
    <div class="tech-label">Frontend</div>
    <div class="tech-badges">
      <span class="badge">Next.js 16</span>
      <span class="badge">React 19</span>
      <span class="badge">Tailwind CSS 4</span>
    </div>
  </div>

  <div class="tech-item">
    <div class="tech-label">Backend</div>
    <div class="tech-badges">
      <span class="badge">Next.js API Routes</span>
      <span class="badge">Server Actions</span>
      <span class="badge">Prisma 7</span>
    </div>
  </div>

  <div class="tech-item">
    <div class="tech-label">Base de Datos</div>
    <div class="tech-badges">
      <span class="badge">PostgreSQL</span>
      <span class="badge">Railway</span>
    </div>
  </div>

  <div class="tech-item">
    <div class="tech-label">Autenticación</div>
    <div class="tech-badges">
      <span class="badge">Clerk</span>
      <span class="badge">Auth con Roles</span>
    </div>
  </div>

  <div class="tech-item">
    <div class="tech-label">Almacenamiento</div>
    <div class="tech-badges">
      <span class="badge">Railway Storage</span>
      <span class="badge">URLs Firmadas</span>
    </div>
  </div>

  <div class="tech-item">
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
  <div class="roadmap-column v1">
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

  <div class="roadmap-column future">
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
  <h2>Tinderstesia convierte un proceso potencialmente subjetivo y disperso en un sistema ordenado de afinidades.</h2>
  
  <p class="closing-subtitle">
    No automatiza decisiones. No sustituye el criterio humano.
  </p>
  
  <p class="closing-subtitle">
    Lo que hace es hacerlo más informado, transparente y reproducible.
  </p>

  <div class="closing-footer">
    Hospital Universitario Miguel Servet<br>
    Desarrollado por David Guallar
  </div>
</div>

<style>
/* Global styles */
.slidev-layout {
  background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
  font-family: 'IBM Plex Sans', sans-serif;
  color: #1a1a1a;
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
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
  display: flex;
  flex-direction: column;
  gap: 1rem;
  border-left: 4px solid #1a5799;
}

.problem-icon {
  font-size: 2.5rem;
  display: block;
}

.problem-item p {
  margin: 0;
  line-height: 1.5;
}

/* Solution slide */
.solution-card {
  background: white;
  padding: 2rem;
  border-radius: 12px;
  box-shadow: 0 2px 12px rgba(0, 0, 0, 0.1);
  border-left: 6px solid #0a7e6c;
}

.solution-card h3 {
  color: #0a7e6c;
  margin: 0 0 1rem 0;
}

.solution-list {
  list-style: none;
  padding: 0;
  margin: 1.5rem 0;
}

.solution-list li {
  margin: 0.8rem 0;
  padding-left: 2rem;
  position: relative;
}

.solution-list li:before {
  content: "✓";
  position: absolute;
  left: 0;
  color: #0a7e6c;
  font-weight: bold;
}

.solution-footer {
  margin-top: 1.5rem;
  padding-top: 1.5rem;
  border-top: 1px solid #eee;
  font-style: italic;
  opacity: 0.85;
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
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
  font-size: 1.2rem;
  text-align: center;
  border-top: 4px solid #1a5799;
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 120px;
}

.house-card:nth-child(2) { border-top-color: #0a7e6c; }
.house-card:nth-child(3) { border-top-color: #334155; }
.house-card:nth-child(4) { border-top-color: #1a5799; }
.house-card:nth-child(5) { border-top-color: #0a7e6c; }
.house-card:nth-child(6) { border-top-color: #334155; }
.house-card:nth-child(7) { border-top-color: #1a5799; }

/* Actors grid */
.actors-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.5rem;
  margin-top: 2rem;
}

.actor-card {
  background: white;
  padding: 1.5rem;
  border-radius: 12px;
  box-shadow: 0 2px 12px rgba(0, 0, 0, 0.08);
  border-left: 6px solid;
}

.actor-card.candidate {
  border-left-color: #1a5799;
}

.actor-card.leader {
  border-left-color: #0a7e6c;
}

.actor-card.admin {
  border-left-color: #334155;
}

.actor-icon {
  font-size: 2.5rem;
  margin-bottom: 1rem;
}

.actor-card h4 {
  margin: 0 0 0.5rem 0;
  color: #1a1a1a;
}

.role-id {
  background: #f0f0f0;
  padding: 0.3rem 0.6rem;
  border-radius: 4px;
  font-family: 'IBM Plex Mono', monospace;
  font-size: 0.85rem;
  margin: 0 0 1rem 0;
}

.actor-card ul {
  list-style: none;
  padding: 0;
  margin: 0;
  font-size: 0.9rem;
  line-height: 1.8;
}

.actor-card li:before {
  content: "→ ";
  color: inherit;
  margin-right: 0.3rem;
  opacity: 0.7;
}

/* Swipe demo */
.swipe-demo {
  display: flex;
  flex-direction: column;
  gap: 2rem;
  margin-top: 2rem;
  align-items: center;
}

.swipe-card {
  background: white;
  border-radius: 12px;
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.12);
  width: 100%;
  max-width: 500px;
  overflow: hidden;
}

.card-header {
  background: linear-gradient(135deg, #1a5799 0%, #0a7e6c 100%);
  color: white;
  padding: 1.5rem;
  display: flex;
  gap: 1rem;
}

.card-stripe {
  width: 4px;
  background: white;
  border-radius: 2px;
}

.card-header h3 {
  margin: 0 0 0.3rem 0;
  font-size: 1.3rem;
}

.card-meta {
  margin: 0;
  opacity: 0.9;
  font-size: 0.9rem;
}

.card-body {
  padding: 1.5rem;
  line-height: 1.6;
}

.card-body p {
  margin: 0 0 0.8rem 0;
}

.card-body p:last-child {
  margin-bottom: 0;
}

.swipe-controls {
  text-align: center;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.control-item {
  font-weight: 600;
  color: #334155;
  font-size: 1.1rem;
}

.control-bar {
  background: white;
  padding: 0.8rem 1.5rem;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
}

/* Match and bond section */
.match-section {
  background: white;
  padding: 2rem;
  border-radius: 12px;
  box-shadow: 0 2px 12px rgba(0, 0, 0, 0.08);
}

.match-section h3 {
  color: #1a5799;
  margin: 0 0 1rem 0;
}

.match-section ul {
  list-style: none;
  padding: 0;
  margin: 0 0 1.5rem 0;
}

.match-section li {
  margin: 0.5rem 0;
  padding-left: 1.5rem;
  position: relative;
}

.match-section li:before {
  content: "•";
  position: absolute;
  left: 0;
  color: #0a7e6c;
  font-weight: bold;
}

.bond-examples {
  margin-top: 1.5rem;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1rem;
}

.bond-row {
  background: #f8f9fa;
  padding: 1rem;
  border-radius: 8px;
  display: flex;
  flex-direction: column;
  gap: 0.3rem;
}

.bond-label {
  font-size: 0.85rem;
  color: #666;
  font-weight: 500;
}

.bond-value {
  font-weight: 600;
  color: #1a5799;
}

/* Admin panel */
.admin-panel {
  background: white;
  padding: 2rem;
  border-radius: 12px;
  box-shadow: 0 2px 12px rgba(0, 0, 0, 0.08);
}

.admin-panel h3 {
  color: #334155;
  margin: 0 0 1.5rem 0;
}

.panel-sections {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.5rem;
}

.panel-section h4 {
  color: #1a5799;
  margin: 0 0 1rem 0;
  font-size: 1rem;
}

.panel-section ul {
  list-style: none;
  padding: 0;
  margin: 0;
  font-size: 0.9rem;
  line-height: 1.8;
}

.panel-section li:before {
  content: "◆ ";
  color: #0a7e6c;
  margin-right: 0.5rem;
}

/* Tech grid */
.tech-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1.5rem;
  margin-top: 1.5rem;
}

.tech-item {
  background: white;
  padding: 1.5rem;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
}

.tech-label {
  display: block;
  font-weight: 600;
  color: #334155;
  margin-bottom: 1rem;
  font-size: 0.9rem;
}

.tech-badges {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.badge {
  background: linear-gradient(135deg, #1a5799 0%, #0a7e6c 100%);
  color: white;
  padding: 0.4rem 0.8rem;
  border-radius: 20px;
  font-size: 0.75rem;
  font-weight: 500;
}

/* Roadmap section */
.roadmap-section {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2rem;
  margin-top: 2rem;
}

.roadmap-column {
  background: white;
  padding: 1.5rem;
  border-radius: 12px;
  box-shadow: 0 2px 12px rgba(0, 0, 0, 0.08);
  border-left: 6px solid;
}

.roadmap-column.v1 {
  border-left-color: #0a7e6c;
}

.roadmap-column.v1 h3 {
  color: #0a7e6c;
}

.roadmap-column.future {
  border-left-color: #ff6600;
}

.roadmap-column.future h3 {
  color: #ff6600;
}

.roadmap-column h3 {
  margin: 0 0 1rem 0;
}

.roadmap-column ul {
  list-style: none;
  padding: 0;
  margin: 0;
  font-size: 0.9rem;
  line-height: 2;
}

.roadmap-column li:before {
  content: "✓ ";
  color: inherit;
  margin-right: 0.5rem;
  opacity: 0.8;
}

.roadmap-column.future li:before {
  content: "→ ";
}

/* Closing slide */
.closing-slide {
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  min-height: 100%;
  gap: 2rem;
  padding: 2rem;
}

.closing-slide h2 {
  font-size: 2rem;
  color: #1a5799;
  margin: 0;
  line-height: 1.4;
  max-width: 900px;
}

.closing-subtitle {
  font-size: 1.1rem;
  color: #666;
  margin: 0;
  max-width: 800px;
  line-height: 1.6;
}

.closing-footer {
  margin-top: 2rem;
  font-size: 0.9rem;
  color: #999;
  border-top: 1px solid #ddd;
  padding-top: 1.5rem;
}
</style>
