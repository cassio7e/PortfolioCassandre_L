<template>
  <div class="section-container">
    <div class="cv-header">
      <div>
        <h2>Cassandre LEBOUVIER</h2>
        <p class="subtitle">Étudiante en 2ème année de Bachelor (CPI) • Spécialisation Systèmes & Réseaux</p>
        <p class="location">📍 Île-de-France</p>
      </div>

      <div class="cv-actions">
        <!-- Tu pourras déposer ton PDF dans le dossier public/ avec ce nom -->
        <a href="/CV_Cassandre_LEBOUVIER.pdf" download class="btn-print">
          📄 Télécharger mon CV (PDF)
        </a>
      </div>
    </div>

    <div class="cv-content">
      <section class="cv-block">
        <h3>🎯 Profil & Objectif</h3>
        <p>
          Actuellement en 2ème année de cycle préparatoire intégré (CPI 2) chez <strong>Sup de Vinci</strong>, 
          je prépare ma spécialisation en <strong>Systèmes et Réseaux</strong> pour ma 3ème année. 
          Curieuse, rigoureuse et dotée d'une forte détermination à aller au bout de chaque projet, 
          je recherche activement des opportunités pour mettre en pratique mes acquis techniques.
        </p>
      </section>

      <section class="cv-block">
        <h3>🎓 Formation</h3>
        <div class="edu-item">
          <div class="edu-header">
            <strong>Bachelor Cycle Préparatoire Intégré (CPI 1 & 2)</strong>
            <span>En cours (Spécialisation Systèmes & Réseaux en 3ème année)</span>
          </div>
          <p class="school">Sup de Vinci — École d'informatique</p>
        </div>

        <div class="edu-item">
          <div class="edu-header">
            <strong>Baccalauréat Général</strong>
            <span>Mention Assez Bien</span>
          </div>
          <p class="school">Spécialités : Sciences de la Vie et de la Terre (SVT) & Physique-Chimie</p>
        </div>
      </section>

      <section class="cv-block">
        <h3>🌍 Certifications & Langues</h3>
        <p><strong>Anglais :</strong> Niveau C2 attesté par l'Éducation Nationale (Préparation du TOEFL prévue pour 2027)</p>
        <p><strong>Français :</strong> Langue maternelle</p>
      </section>
    </div>
  </div>
</template>

<style scoped>
.section-container {
  max-width: 850px;
  margin: 0 auto;
}

.cv-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  flex-wrap: wrap;
  gap: 16px;
  padding-bottom: 20px;
  border-bottom: 1px solid var(--border-color);
  margin-bottom: 24px;
}

h2 {
  font-size: 1.8rem;
  margin-bottom: 4px;
}

.subtitle {
  color: var(--accent);
  font-weight: 500;
  margin-bottom: 4px;
}

.location {
  color: var(--text-muted);
  font-size: 0.9rem;
}

.btn-print {
  display: inline-block;
  background: var(--accent);
  color: #fff;
  padding: 10px 18px;
  border-radius: 8px;
  text-decoration: none;
  font-weight: 600;
  font-size: 0.9rem;
  transition: opacity 0.2s;
}

.btn-print:hover {
  opacity: 0.9;
}

.cv-content {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.cv-block {
  background: var(--card-bg);
  border: 1px solid var(--border-color);
  border-radius: 12px;
  padding: 20px;
}

.cv-block h3 {
  font-size: 1.15rem;
  margin-bottom: 12px;
  color: var(--accent);
}

.cv-block p {
  font-size: 0.92rem;
  line-height: 1.5;
}

.edu-item {
  margin-bottom: 12px;
}

.edu-header {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 8px;
  font-size: 0.95rem;
}

.school {
  color: var(--text-muted);
  font-size: 0.88rem;
  margin-top: 2px;
}
</style>