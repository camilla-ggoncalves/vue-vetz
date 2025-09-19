<template>
  <div class="about-page">
    <h1>ℹ️ Sobre Nós</h1>
    
    <div class="about-content">
      <div class="company-info">
        <h2>🚀 Nossa Missão</h2>
        <p>
          Somos uma empresa dedicada a criar soluções tecnológicas inovadoras 
          que simplificam a vida das pessoas e impulsionam o crescimento dos negócios.
        </p>
      </div>

      <div class="stats-grid">
        <div class="stat-card">
          <div class="stat-number">{{ stats.years }}</div>
          <div class="stat-label">Anos de Experiência</div>
        </div>
        <div class="stat-card">
          <div class="stat-number">{{ stats.projects }}</div>
          <div class="stat-label">Projetos Concluídos</div>
        </div>
        <div class="stat-card">
          <div class="stat-number">{{ stats.clients }}</div>
          <div class="stat-label">Clientes Satisfeitos</div>
        </div>
      </div>

      <div class="team-section">
        <h2>👥 Nossa Equipe</h2>
        <div class="team-grid">
          <div v-for="member in team" :key="member.id" class="team-member">
            <div class="member-avatar">{{ member.emoji }}</div>
            <h3>{{ member.name }}</h3>
            <p class="member-role">{{ member.role }}</p>
          </div>
        </div>
      </div>

      <div class="values-section">
        <h2>💡 Nossos Valores</h2>
        <div class="values-list">
          <div v-for="value in values" :key="value.id" class="value-item">
            <span class="value-icon">{{ value.icon }}</span>
            <div>
              <h4>{{ value.title }}</h4>
              <p>{{ value.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const stats = ref({
  years: 5,
  projects: 150,
  clients: 89
})

const team = ref([
  { id: 1, name: 'Isadora', role: 'CEO & Fundadora', },
  { id: 2, name: 'Carlos Santos', role: 'CTO', emoji: '👨‍💻' },
  { id: 3, name: 'Maria Costa', role: 'Designer UX/UI', emoji: '👩‍🎨' },
  { id: 4, name: 'Ana Silva', role: 'CEO & Fundadora', emoji: '👩‍💼' },
  { id: 5, name: 'João Oliveira', role: 'Desenvolvedor Senior', emoji: '👨‍💻' }
  
])

const values = ref([
  {
    id: 1,
    icon: '🎯',
    title: 'Foco no Cliente',
    description: 'Colocamos as necessidades dos nossos clientes em primeiro lugar'
  },
  {
    id: 2,
    icon: '⚡',
    title: 'Inovação',
    description: 'Buscamos constantemente novas tecnologias e soluções'
  },
  {
    id: 3,
    icon: '🤝',
    title: 'Colaboração',
    description: 'Trabalhamos em equipe para alcançar os melhores resultados'
  },
  {
    id: 4,
    icon: '🌟',
    title: 'Excelência',
    description: 'Comprometidos com a qualidade em tudo que fazemos'
  }
])
</script>

<style scoped>
.about-page {
  max-width: 800px;
  margin: 0 auto;
}

.about-content {
  text-align: left;
}

.company-info {
  background-color: #f8f9fa;
  padding: 25px;
  border-radius: 8px;
  margin-bottom: 30px;
}

.company-info h2 {
  color: #495057;
  margin-bottom: 15px;
}

.stats-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  gap: 20px;
  margin-bottom: 40px;
}

.stat-card {
  background-color: white;
  border: 2px solid #007bff;
  border-radius: 8px;
  padding: 20px;
  text-align: center;
}

.stat-number {
  font-size: 2.5rem;
  font-weight: bold;
  color: #007bff;
}

.stat-label {
  color: #6c757d;
  font-size: 0.9rem;
  margin-top: 5px;
}

.team-section {
  margin-bottom: 40px;
}

.team-section h2 {
  color: #495057;
  margin-bottom: 20px;
}

.team-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  gap: 20px;
}

.team-member {
  background-color: white;
  border: 1px solid #dee2e6;
  border-radius: 8px;
  padding: 20px;
  text-align: center;
}

.member-avatar {
  font-size: 3rem;
  margin-bottom: 10px;
}

.member-photo {
  width: 120px;
  height: 120px;
  object-fit: cover;
  border-radius: 50%;
  margin-bottom: 10px;
  border: 2px solid #bdbdbd;
  display: block;
  margin-left: auto;
  margin-right: auto;
}

.team-member h3 {
  color: #495057;
  margin-bottom: 5px;
}

.member-role {
  color: #6c757d;
  font-size: 0.9rem;
}

.values-section h2 {
  color: #495057;
  margin-bottom: 20px;
}

.values-list {
  display: grid;
  gap: 15px;
}

.value-item {
  display: flex;
  align-items: flex-start;
  background-color: #f8f9fa;
  padding: 20px;
  border-radius: 8px;
  border-left: 4px solid #007bff;
}

.value-icon {
  font-size: 2rem;
  margin-right: 15px;
}

.value-item h4 {
  color: #495057;
  margin-bottom: 5px;
}

.value-item p {
  color: #6c757d;
  margin: 0;
}
</style>
