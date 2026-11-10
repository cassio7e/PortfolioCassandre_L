<template>
  <div class="section-container">
    <h2>🚀 Mes Projets</h2>
    <p class="subtitle">Sélection de projets académiques et personnels en cours d'intégration.</p>

    <div class="projects-grid">
      <!-- Emplacement prêt pour accueillir tes futurs projets -->
      <article class="project-card placeholder">
        <div class="card-status">À venir</div>
        <div class="project-icon">📂</div>
        <h3>Projet Réseau & Système #1</h3>
        <p>Mise en place d'infrastructure, configuration de services réseaux ou virtualisation.</p>
        <div class="tags">
          <span class="tag">Réseaux</span>
          <span class="tag">Linux</span>
        </div>
      </article>

      <article class="project-card placeholder">
        <div class="card-status">À venir</div>
        <div class="project-icon">💻</div>
        <h3>Projet Développement / Scripting</h3>
        <p>Automatisation de tâches système ou application web développée en cours.</p>
        <div class="tags">
          <span class="tag">Python</span>
          <span class="tag">Bash</span>
        </div>
      </article>

      <article class="project-card placeholder">
        <div class="card-status">En cours</div>
        <div class="project-icon">🌐</div>
        <h3>Portfolio Navigateur Web</h3>
        <p>Conception d'un portfolio interactif avec interface calquée sur Google Chrome / Firefox.</p>
        <div class="tags">
          <span class="tag">Vue.js</span>
          <span class="tag">CSS3</span>
        </div>
      </article>
    </div>
  </div>
</template>

<style scoped>
.section-container {
  max-width: 900px;
  margin: 0 auto;
}

h2 {
  margin-bottom: 6px;
}

.subtitle {
  color: var(--text-muted);
  margin-bottom: 24px;
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 18px;
}

.project-card {
  position: relative;
  background: var(--card-bg);
  border: 1px dashed var(--border-color);
  border-radius: 12px;
  padding: 20px;
  display: flex;
  flex-direction: column;
  gap: 12px;
  transition: transform 0.2s, border-color 0.2s;
}

.project-card:hover {
  transform: translateY(-3px);
  border-color: var(--accent);
}

.card-status {
  position: absolute;
  top: 14px;
  right: 14px;
  font-size: 0.75rem;
  background: var(--bg-hover);
  color: var(--accent);
  padding: 3px 8px;
  border-radius: 12px;
  font-weight: bold;
}

.project-icon {
  font-size: 2rem;
}

.project-card h3 {
  font-size: 1.1rem;
}

.project-card p {
  color: var(--text-muted);
  font-size: 0.9rem;
  line-height: 1.4;
  flex-grow: 1;
}

.tags {
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
}

.tag {
  background: var(--bg-hover);
  color: var(--text-color);
  font-size: 0.75rem;
  padding: 3px 8px;
  border-radius: 4px;
}
</style>