<template>
  <div class="section-container">
    <h2>⚡ Compétences & Soft Skills</h2>
    <p class="subtitle">Aperçu de mes acquis techniques et de mes compétences relationnelles.</p>

    <div class="skills-grid">
      <!-- Hard Skills -->
      <div class="skills-card">
        <h3>🛠️ Compétences Techniques (Hard Skills)</h3>
        <p class="card-desc">Bases acquises en cycle préparatoire Sup de Vinci & cursus Systèmes et Réseaux :</p>
        <ul class="skills-list">
          <li><strong>Systèmes :</strong> Linux (commandes de base, gestion utilisateurs, droits), Windows Server</li>
          <li><strong>Réseaux :</strong> Adressage IP, masque sous-réseau, modèles OSI / TCP-IP, routage de base</li>
          <li><strong>Développement & Scripting :</strong> Algorithmique, HTML5 / CSS3, notions de scripts d'automatisation</li>
          <li><strong>Outils & Environnement :</strong> Git, GitHub, virtualisation (VirtualBox / VMware)</li>
        </ul>
      </div>

      <!-- Soft Skills -->
      <div class="skills-card">
        <h3>💡 Qualités Personnelles (Soft Skills)</h3>
        <p class="card-desc">Aptitudes relationnelles et professionnelles développées en formation et en poste :</p>
        <ul class="skills-list">
          <li><strong>Travail en équipe :</strong> Capacité à collaborer efficacement lors de projets de groupe ou en entreprise.</li>
          <li><strong>Curiosité intellectuelle :</strong> Volonté constante d'apprendre de nouvelles technologies et protocoles.</li>
          <li><strong>Persévérance & Détermination :</strong> Désir d'aller au bout des projets et de résoudre les problèmes complexes.</li>
          <li><strong>Relation client & Écoute :</strong> Patience, gestion du stress et sens de l'accueil client (expérience Carrefour).</li>
        </ul>
      </div>

      <!-- Langues -->
      <div class="skills-card full-width">
        <h3>🌍 Langues</h3>
        <div class="languages">
          <div class="lang-item">
            <span class="lang-name">Français</span>
            <span class="lang-level">Langue maternelle</span>
          </div>
          <div class="lang-item">
            <span class="lang-name">Anglais</span>
            <span class="lang-level highlight">Niveau C2 (Attestation Éducation Nationale) • Préparation TOEFL (2027)</span>
          </div>
        </div>
      </div>
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

.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  gap: 20px;
}

.skills-card {
  background: var(--card-bg);
  border: 1px solid var(--border-color);
  border-radius: 12px;
  padding: 22px;
  display: flex;
  flex-direction: column;
}

.skills-card.full-width {
  grid-column: 1 / -1;
}

.skills-card h3 {
  font-size: 1.15rem;
  margin-bottom: 8px;
  color: var(--accent);
}

.card-desc {
  font-size: 0.9rem;
  color: var(--text-muted);
  margin-bottom: 14px;
}

.skills-list {
  list-style: none;
  padding: 0;
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.skills-list li {
  font-size: 0.92rem;
  line-height: 1.45;
}

.skills-list strong {
  color: var(--text-color);
}

.languages {
  display: flex;
  flex-direction: column;
  gap: 12px;
  margin-top: 6px;
}

.lang-item {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: var(--bg-hover);
  padding: 10px 14px;
  border-radius: 8px;
  flex-wrap: wrap;
  gap: 8px;
}

.lang-name {
  font-weight: 600;
}

.lang-level {
  font-size: 0.88rem;
  color: var(--text-muted);
}

.lang-level.highlight {
  color: var(--accent);
  font-weight: 500;
}
</style>