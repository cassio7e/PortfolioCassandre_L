<template>
  <div class="section-container">
    <h2>📫 Me Contacter</h2>
    <p class="subtitle">N'hésitez pas à me contacter pour une opportunité d'alternance ou pour échanger.</p>

    <div class="contact-cards">
      <a href="mailto:lebouviercassandre@gmail.com" class="contact-card">
        <span class="icon">✉️</span>
        <div>
          <h3>Email</h3>
          <p>lebouviercassandre@gmail.com</p>
        </div>
      </a>

      <a href="https://github.com/cassio7e" target="_blank" rel="noopener noreferrer" class="contact-card">
        <span class="icon">💻</span>
        <div>
          <h3>GitHub</h3>
          <p>github.com/cassio7e</p>
        </div>
      </a>

      <a href="https://linkedin.com/in/cassandre-lebouvier-4283aa38b" target="_blank" rel="noopener noreferrer" class="contact-card">
        <span class="icon">🔗</span>
        <div>
          <h3>LinkedIn</h3>
          <p>Cassandre LEBOUVIER</p>
        </div>
      </a>
    </div>
  </div>
</template>

<style scoped>
.section-container { 
  max-width: 700px; 
  margin: 0 auto; 
  text-align: center; 
}

h2 { 
  margin-bottom: 8px; 
}

.subtitle { 
  color: var(--text-muted); 
  margin-bottom: 30px; 
}

.contact-cards { 
  display: flex; 
  flex-direction: column; 
  gap: 16px; 
}

.contact-card {
  display: flex; 
  align-items: center; 
  gap: 20px;
  background: var(--card-bg); 
  border: 1px solid var(--border-color);
  padding: 16px 24px; 
  border-radius: 10px; 
  text-decoration: none;
  color: var(--text-color); 
  transition: transform 0.2s, border-color 0.2s;
  text-align: left;
}

.contact-card:hover {
  transform: translateY(-2px);
  border-color: var(--accent);
}

.icon { 
  font-size: 1.8rem; 
}

.contact-card h3 { 
  font-size: 1rem; 
  margin-bottom: 2px; 
}

.contact-card p { 
  color: var(--accent); 
  font-size: 0.9rem; 
}
</style>