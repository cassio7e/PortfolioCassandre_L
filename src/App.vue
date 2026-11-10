<template>
  <div class="app-wrapper" :class="{ 'dark-theme': isDark }">
    <!-- Fenêtre du navigateur virtuel -->
    <div class="browser-window">
      
      <!-- Barre supérieure : Boutons système + Onglets -->
      <header class="browser-top">
        <div class="window-controls">
          <span class="btn-circle red"></span>
          <span class="btn-circle yellow"></span>
          <span class="btn-circle green"></span>
        </div>

        <nav class="tabs-container">
          <button 
            v-for="section in sections" 
            :key="section.id"
            class="tab"
            :class="{ active: currentTab === section.id }"
            @click="currentTab = section.id"
          >
            <span class="tab-icon">{{ section.icon }}</span>
            <span class="tab-title">{{ section.title }}</span>
          </button>
        </nav>

        <div class="theme-toggle">
          <button @click="toggleTheme" class="btn-action" title="Changer le thème">
            {{ isDark ? '☀️ Clair' : '🌙 Sombre' }}
          </button>
        </div>
      </header>

      <!-- Barre d'adresse URL -->
      <section class="browser-address-bar">
        <div class="nav-arrows">
          <button class="arrow" disabled>❮</button>
          <button class="arrow" disabled>❯</button>
          <button class="arrow" @click="currentTab = 'cv'">⟳</button>
        </div>

        <div class="url-input">
          <span class="lock-icon">🔒</span>
          <span class="protocol">https://</span>
          <span class="domain">cassandre-lebouvier.dev/</span>
          <span class="path">{{ currentTab }}</span>
        </div>

        <div class="address-actions">
          <a href="/cv-cassandre-lebouvier.pdf" target="_blank" class="btn-print" title="Ouvrir mon CV">
            📄 Mon CV PDF
          </a>
        </div>
      </section>

      <!-- Corps de page : Affichage de l'onglet actif -->
      <main class="browser-content">
        <CvSection v-if="currentTab === 'cv'" />
        <ExperienceSection v-if="currentTab === 'experience'" />
        <SkillsSection v-if="currentTab === 'skills'" />
        <ProjectsSection v-if="currentTab === 'projects'" />
        <ContactSection v-if="currentTab === 'contact'" />
      </main>

    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import CvSection from './components/CvSection.vue'
import ExperienceSection from './components/ExperienceSection.vue'
import SkillsSection from './components/SkillsSection.vue'
import ProjectsSection from './components/ProjectsSection.vue'
import ContactSection from './components/ContactSection.vue'

const isDark = ref(true)
const currentTab = ref('cv')

const sections = [
  { id: 'cv', title: 'Mon Profil & CV', icon: '👤' },
  { id: 'experience', title: 'Expériences', icon: '💼' },
  { id: 'skills', title: 'Compétences', icon: '⚡' },
  { id: 'projects', title: 'Projets', icon: '🚀' },
  { id: 'contact', title: 'Contact', icon: '📫' }
]

const toggleTheme = () => {
  isDark.value = !isDark.value
}
</script>

<style scoped>
.app-wrapper {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px;
  background-color: #0f172a;
  transition: background 0.3s;
}

.app-wrapper:not(.dark-theme) {
  background-color: #e2e8f0;
}

/* Fenêtre de navigation */
.browser-window {
  width: 100%;
  max-width: 1100px;
  min-height: 800px;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.4);
  display: flex;
  flex-direction: column;
  background-color: var(--bg-content);
  color: var(--text-color);
  border: 1px solid var(--border-color);
}

/* Thème Sombre */
.dark-theme {
  --bg-top: #1e293b;
  --bg-address: #0f172a;
  --bg-content: #0f172a;
  --tab-active: #0f172a;
  --tab-inactive: #1e293b;
  --text-color: #f8fafc;
  --text-muted: #94a3b8;
  --border-color: #334155;
  --card-bg: #1e293b;
  --accent: #38bdf8;
}

/* Thème Clair */
.app-wrapper:not(.dark-theme) {
  --bg-top: #e2e8f0;
  --bg-address: #ffffff;
  --bg-content: #ffffff;
  --tab-active: #ffffff;
  --tab-inactive: #e2e8f0;
  --text-color: #0f172a;
  --text-muted: #64748b;
  --border-color: #cbd5e1;
  --card-bg: #f8fafc;
  --accent: #0284c7;
}

/* Barre du haut */
.browser-top {
  background-color: var(--bg-top);
  display: flex;
  align-items: center;
  padding: 10px 16px 0 16px;
  gap: 12px;
  border-bottom: 1px solid var(--border-color);
}

.window-controls {
  display: flex;
  gap: 8px;
  margin-bottom: 8px;
}

.btn-circle {
  width: 12px;
  height: 12px;
  border-radius: 50%;
}
.red { background-color: #ef4444; }
.yellow { background-color: #f59e0b; }
.green { background-color: #10b981; }

.tabs-container {
  display: flex;
  flex: 1;
  gap: 6px;
  overflow-x: auto;
}

.tab {
  background-color: var(--tab-inactive);
  color: var(--text-muted);
  border: none;
  padding: 8px 16px;
  border-radius: 8px 8px 0 0;
  font-size: 0.85rem;
  font-weight: 500;
  cursor: pointer;
  display: flex;
  align-items: center;
  gap: 6px;
  border-top: 2px solid transparent;
  transition: all 0.2s;
}

.tab.active {
  background-color: var(--tab-active);
  color: var(--text-color);
  border-top-color: var(--accent);
}

.theme-toggle {
  margin-bottom: 8px;
}

.btn-action {
  background: var(--card-bg);
  border: 1px solid var(--border-color);
  color: var(--text-color);
  padding: 6px 12px;
  border-radius: 6px;
  cursor: pointer;
  font-size: 0.8rem;
}

/* Barre d'URL */
.browser-address-bar {
  background-color: var(--bg-content);
  padding: 10px 16px;
  display: flex;
  align-items: center;
  gap: 12px;
  border-bottom: 1px solid var(--border-color);
}

.nav-arrows {
  display: flex;
  gap: 4px;
}

.arrow {
  background: transparent;
  border: none;
  color: var(--text-muted);
  cursor: pointer;
  font-size: 1rem;
  padding: 4px 8px;
}

.url-input {
  flex: 1;
  background-color: var(--bg-top);
  border: 1px solid var(--border-color);
  padding: 6px 12px;
  border-radius: 20px;
  font-family: monospace;
  font-size: 0.85rem;
  display: flex;
  align-items: center;
  gap: 6px;
}

.protocol { color: var(--text-muted); }
.domain { color: var(--text-color); font-weight: bold; }
.path { color: var(--accent); }

.btn-print {
  text-decoration: none;
  background-color: var(--accent);
  color: #fff;
  padding: 6px 12px;
  border-radius: 6px;
  font-size: 0.8rem;
  font-weight: 600;
  display: flex;
  align-items: center;
  gap: 6px;
}

/* Contenu */
.browser-content {
  flex: 1;
  padding: 30px;
  overflow-y: auto;
}
</style>