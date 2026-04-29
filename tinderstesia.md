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

<div class="title-container">
  <div class="title-glass-card">
    <img src="/icon.png" class="title-icon" alt="Tinderstesia Logo">
    <h1 class="title-text">Tinderstesia</h1>
    <p class="title-subtitle">Una forma menos dolorosa de repartir casas</p>
    <div class="title-info">
      <p>Hospital Universitario Miguel Servet</p>
      <p style="margin-top: 1rem;">
        <a href="https://tinderstesia.vercel.app/" target="_blank" class="app-link">
          🚀 Acceder a tinderstesia.vercel.app
        </a>
      </p>
      <p class="tagline">Afinidades reales, decisiones humanas mejor informadas</p>
    </div>
  </div>
</div>

<!--
Abrir con calma: "Esto empezó como una broma porque se parece a Tinder, pero el problema que intenta ordenar es real". La idea no es vender tecnología: es reducir memoria, pasillos y ruido antes de decidir.
-->

---

<div class="quote-slide">
  <h2 v-click>
    "Tinderstesia convierte <span class="quote-highlight">preferencias dispersas</span> en una foto clara de <span class="quote-highlight">afinidades reales</span> entre profesionales y casas."
  </h2>
</div>

<!--
Mensaje de esta diapositiva: foto clara. La aplicación no decide por la jefatura; pone las preferencias en un formato comparable.
-->

---

# Tinderstesia en vivo

<div class="screenshot-card" v-click>
  <img src="/tinderstesia_landing.png" class="screenshot-img landing-screenshot" alt="Landing Page" style="width: 100%; object-fit: contain; border-radius: 12px;">
</div>

<p style="text-align: center; color: #64748b; font-size: 0.9rem;" v-click>
  Interfaz moderna y adaptada para escritorio y dispositivos móviles.
</p>

<!--
Aquí conviene enseñar que no es una idea abstracta: existe, se puede abrir y se entiende visualmente. Si falla internet, esta captura sostiene la explicación.
-->

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

<!--
Buscar asentimiento. Este es el dolor cotidiano: información suelta, impresiones parciales y decisiones con demasiada carga mental.
-->

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
  <p class="solution-footer" v-click style="margin-top: 0.8rem;">La app no manda: ordena la mesa antes de la reunión.</p>
</div>

<!--
Frase clave para bajar defensas: "No manda". Es apoyo a la decisión, no piloto automático.
-->

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

<!--
Presentarlo como un piloto de baja fricción. Lo importante es que todos contestan a las mismas preguntas y dejan una señal comparable.
-->

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

<!--
Nombrar las casas reales ayuda a que deje de sonar genérico. Es una herramienta pensada para este servicio, no una plantilla externa.
-->

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

<!--
Separar bien los permisos: el profesional ve lo suyo, el responsable ve su casa, la administración ve el mapa. Esto protege privacidad y mantiene la visión global donde toca.
-->

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

<!--
En esta demo, remarcar que el responsable no está "puntuando personas" de forma aislada: expresa el interés de su casa para una posible incorporación.
-->

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

<!--
Este es el momento de la broma de Tinder. Después aterrizarla: misma mecánica sencilla, pero aplicada a preferencias laborales internas.
-->

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

<!--
Explicar que no todos los "me interesa" pesan igual. La escala 0-10 separa un encaje clarísimo de un interés tibio o asimétrico.
-->

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

<p style="margin-top: 1.5rem; text-align: center; font-style: italic; color: #475569;" v-click>
  La decisión sigue siendo humana, pero llega con mejores datos sobre la mesa.
</p>

<!--
Esta es la diapositiva para tu jefe: menos ruido, más orden, misma responsabilidad final.
-->

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

<!--
Usar estos dos casos como conversación. Match fuerte no significa obligación; discrepancia no significa fracaso. Ambas cosas informan.
-->

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

<!--
Decir esto antes de que lo pregunten. No recoloca automáticamente, no impone resultados y no toca datos de pacientes.
-->

---

# Propuesta de Uso

<ul class="usage-list">
  <li v-click>Validar casas y responsables</li>
  <li v-click>Profesionales completan perfiles y valoran casas</li>
  <li v-click>Responsables valoran candidatos</li>
  <li v-click>Revisión del panel global de afinidades</li>
  <li v-click>Uso de resultados como apoyo para decidir</li>
</ul>

<!--
Proponerlo como prueba acotada. Si ayuda, se incorpora; si no ayuda, al menos habremos aprendido cómo están las preferencias reales.
-->

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

<!--
Si la audiencia no es técnica, pasar rápido por esta diapositiva. Sirve para transmitir que la V1 está hecha con una base seria y que el roadmap existe, no para entrar en arquitectura.
-->

---

<div class="closing-slide">
  <img src="/icon.png" class="closing-logo" alt="Tinderstesia Logo" v-click>
  <div class="closing-title" v-click>Tinderstesia</div>
  <h2 v-click style="font-size: 1.65rem; color: #1e293b;">Decisiones más claras, procesos más humanos.</h2>
  
  <p class="closing-subtitle" v-click style="max-width: 800px; color: #475569; font-size: 1.08rem; line-height: 1.45;">
    Escuchar a los profesionales e incorporar la visión de las casas para decidir con mejores datos.
  </p>

  <div class="closing-footer" v-click style="border-top: 1px solid #e2e8f0; color: #64748b; font-size: 0.95rem;">
    Hospital Universitario Miguel Servet<br>
    <span style="font-weight: 700; color: #1a5799;">Desarrollado por David Guallar</span>
  </div>
</div>

<!--
Cierre breve: "La gracia es el nombre; la utilidad es ordenar afinidades". Terminar recordando que la decisión sigue siendo nuestra.
-->

