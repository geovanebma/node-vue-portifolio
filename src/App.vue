<template>
  <div id="app">
    <header class="site-header">
      <a class="brand" href="#inicio" aria-label="Ir para o início">
        <span class="brand-mark">GB</span>
        <span>Geovane Barbosa</span>
      </a>

      <button class="menu-toggle" type="button" aria-label="Abrir menu" @click="isNavVisible = !isNavVisible">
        <b-icon icon="list"></b-icon>
      </button>

      <nav :class="['main-nav', { 'is-visible': isNavVisible }]">
        <button type="button" @click="scrollToSection('inicio')">Início</button>
        <button type="button" @click="scrollToSection('sobre')">Sobre</button>
        <button type="button" @click="scrollToSection('projetos')">Projetos</button>
        <button type="button" @click="scrollToSection('skills')">Stack</button>
        <button type="button" @click="scrollToSection('contato')">Contato</button>
      </nav>
    </header>

    <main>
      <section id="inicio" class="hero-section">
        <div class="hero-copy">
          <p class="eyebrow">Engenheiro de Software Full Stack</p>
          <h1>Construo sistemas web claros, úteis e prontos para o mundo real.</h1>
          <p class="hero-text">
            Mais de 9 anos criando APIs, plataformas internas, páginas comerciais e produtos digitais com PHP,
            Laravel, Node.js, Vue, bancos de dados e integrações.
          </p>

          <div class="hero-actions">
            <a class="btn-primary" href="https://api.whatsapp.com/send/?phone=5511911807503&text=Ol%C3%A1%20Geovane%2C%20vi%20seu%20portf%C3%B3lio%20e%20gostaria%20de%20conversar." target="_blank" rel="noopener noreferrer">
              <b-icon icon="whatsapp"></b-icon>
              Chamar no WhatsApp
            </a>
            <a class="btn-secondary" href="https://github.com/geovanebma?tab=repositories" target="_blank" rel="noopener noreferrer">
              <b-icon icon="github"></b-icon>
              Ver GitHub
            </a>
          </div>

          <div class="hero-metrics" aria-label="Resumo profissional">
            <div>
              <strong>9+</strong>
              <span>anos de experiência</span>
            </div>
            <div>
              <strong>Full stack</strong>
              <span>frontend, backend e banco</span>
            </div>
            <div>
              <strong>SP</strong>
              <span>Carapicuíba, Brasil</span>
            </div>
          </div>
        </div>

        <div class="hero-visual" aria-hidden="true">
          <img src="./assets/programming-pana.png" alt="">
        </div>
      </section>

      <section id="sobre" class="content-band">
        <div class="section-heading">
          <p class="eyebrow">Sobre</p>
          <h2>Perfil técnico com visão de produto.</h2>
        </div>

        <div class="about-grid">
          <article class="about-card">
            <h3>O que eu entrego</h3>
            <p>
              Desenvolvimento de sistemas web, APIs REST, CRUDs, dashboards, páginas de conversão e integrações
              com foco em manutenção simples, experiência do usuário e resultado para o negócio.
            </p>
          </article>
          <article class="about-card">
            <h3>Como eu trabalho</h3>
            <p>
              Gosto de entender o problema antes de codar, organizar fluxos, separar responsabilidades e transformar
              requisitos soltos em telas e serviços que façam sentido no uso diário.
            </p>
          </article>
          <article class="about-card">
            <h3>Formação e evolução</h3>
            <p>
              Formação pela Universidade Paulista, cursos em UX Design, Java e AWS, além de prática constante com
              PHP, Laravel, Node.js, Vue, JavaScript e bancos de dados.
            </p>
          </article>
        </div>
      </section>

      <section id="projetos" class="content-band projects-section">
        <div class="section-heading">
          <p class="eyebrow">Projetos</p>
          <h2>Trabalhos e estudos que mostram repertório.</h2>
        </div>

        <div class="project-grid">
          <article v-for="project in projects" :key="project.title" class="project-card">
            <a :href="project.url" target="_blank" rel="noopener noreferrer">
              <img :src="project.image" :alt="project.title">
              <div class="project-content">
                <span>{{ project.type }}</span>
                <h3>{{ project.title }}</h3>
                <p>{{ project.description }}</p>
                <ul>
                  <li v-for="tag in project.tags" :key="tag">{{ tag }}</li>
                </ul>
              </div>
            </a>
          </article>
        </div>
      </section>

      <section id="skills" class="content-band skills-section">
        <div class="section-heading">
          <p class="eyebrow">Stack</p>
          <h2>Tecnologias para entregar de ponta a ponta.</h2>
        </div>

        <div class="skills-layout">
          <article v-for="group in skillGroups" :key="group.title" class="skill-panel">
            <h3>{{ group.title }}</h3>
            <p>{{ group.description }}</p>
            <div class="skill-tags">
              <span v-for="skill in group.items" :key="skill">{{ skill }}</span>
            </div>
          </article>
        </div>
      </section>

      <section class="content-band timeline-section">
        <div class="section-heading">
          <p class="eyebrow">Experiência</p>
          <h2>Do sistema interno ao produto publicado.</h2>
        </div>

        <div class="timeline">
          <div v-for="item in timeline" :key="item.title" class="timeline-item">
            <span>{{ item.period }}</span>
            <h3>{{ item.title }}</h3>
            <p>{{ item.description }}</p>
          </div>
        </div>
      </section>
    </main>

    <footer id="contato" class="site-footer">
      <div>
        <p class="eyebrow">Contato</p>
        <h2>Vamos construir algo útil?</h2>
        <p>Aberto a oportunidades, freelas e conversas sobre sistemas web, automações e produtos digitais.</p>
      </div>

      <div class="footer-links">
        <a href="https://github.com/geovanebma" target="_blank" rel="noopener noreferrer">
          <b-icon icon="github"></b-icon>
          GitHub
        </a>
        <a href="https://www.linkedin.com/in/programador-php-laravel-node-java-dev/" target="_blank" rel="noopener noreferrer">
          <b-icon icon="linkedin"></b-icon>
          LinkedIn
        </a>
        <a href="https://www.instagram.com/geovaneb_/" target="_blank" rel="noopener noreferrer">
          <b-icon icon="instagram"></b-icon>
          Instagram
        </a>
        <a href="https://api.whatsapp.com/send/?phone=5511911807503&text=Ol%C3%A1%20Geovane%2C%20vi%20seu%20portf%C3%B3lio%20e%20gostaria%20de%20conversar." target="_blank" rel="noopener noreferrer">
          <b-icon icon="whatsapp"></b-icon>
          WhatsApp
        </a>
      </div>

      <small>Copyright © 2026 | Geovane Barbosa</small>
    </footer>
  </div>
</template>

<script>
import vivoIntergrall from './assets/vivo_intergrall.png';
import vivoFidelizacao from './assets/vivo_fidelizacao.png';
import tokenAcesso from './assets/token_acesso.png';
import solutions from './assets/solutions.png';
import langvoice from './assets/langvoice.png';
import dictionary from './assets/dictionary.png';

export default {
  name: 'App',
  data() {
    return {
      isNavVisible: false,
      projects: [
        {
          title: 'LangVoice',
          type: 'Produto de estudos',
          description: 'Flashcards de idiomas com anotações e áudios para apoiar aprendizado de inglês e espanhol.',
          image: langvoice,
          url: 'https://github.com/geovanebma/langvoice',
          tags: ['JavaScript', 'PHP', 'UX'],
        },
        {
          title: 'Dictionary',
          type: 'Aplicação Laravel',
          description: 'Dicionário de inglês com base de 20 mil palavras, CRUD e organização de conteúdo de estudo.',
          image: dictionary,
          url: 'https://github.com/geovanebma/laravel-crud-dictionary',
          tags: ['Laravel', 'SQLite', 'Vue'],
        },
        {
          title: 'Vivo Fidelização',
          type: 'Landing page comercial',
          description: 'Página para aquisição e renovação de produtos Vivo com foco em jornada rápida de conversão.',
          image: vivoFidelizacao,
          url: 'https://www.intergrall.com.br/lp/vivo_fidelizacao/vivo_fidelizacao.php?mku=MKU5jWsdaIuX4nbRbAoE3lVEdolxCoep4zTZ7O79d5qEZDq0U5GTocAdujr7jGea1iIDbx8HDCto4IWwwxb44awwAnNbYsfuEksNQjznfmcLqAL8UsmTt7hmfX7aTILCdRcv7A10bMd41eyNcSvmRnLbP8Ul7wwxb44awwm3RD7C1nmokE1uh09ojULTDRJWtAV9hRbp0zutuXdDNG5Yg==',
          tags: ['PHP', 'Vue', 'Front-end'],
        },
        {
          title: 'Login Vivo Intergrall',
          type: 'Sistema web',
          description: 'Interface de login para operação de leads, com atenção a fluxo, acesso e clareza visual.',
          image: vivoIntergrall,
          url: 'https://www.intergrall.com.br//login/vivo/index.php',
          tags: ['HTML', 'CSS', 'PHP'],
        },
        {
          title: 'Elleve Solutions',
          type: 'Site institucional',
          description: 'Presença digital para consultoria, estruturada para apresentar serviços e facilitar contato.',
          image: solutions,
          url: 'https://ellevesolutions.com/',
          tags: ['UI', 'Bootstrap', 'Web'],
        },
        {
          title: 'Token de Acesso',
          type: 'Ferramenta interna',
          description: 'Fluxo de permissão para consumo de API e controle de acesso em ambiente operacional.',
          image: tokenAcesso,
          url: 'https://www.intergrall.com.br/callcenter/cc_login.php',
          tags: ['API', 'Segurança', 'Backend'],
        },
      ],
      skillGroups: [
        {
          title: 'Backend',
          description: 'Criação de APIs, autenticação, regras de negócio, integrações e persistência de dados.',
          items: ['PHP', 'Laravel', 'Node.js', 'Java', 'REST APIs', 'MVC'],
        },
        {
          title: 'Frontend',
          description: 'Interfaces responsivas para sistemas, landing pages e ferramentas internas.',
          items: ['Vue.js', 'JavaScript', 'HTML', 'CSS', 'Bootstrap', 'React'],
        },
        {
          title: 'Dados e cloud',
          description: 'Modelagem, consultas e armazenamento para aplicações web e mobile.',
          items: ['MySQL', 'SQL Server', 'SQLite', 'Firebase', 'AWS', 'PHPMyAdmin'],
        },
        {
          title: 'Produto e qualidade',
          description: 'Organização de fluxo, prototipação, versionamento e colaboração.',
          items: ['Git', 'GitHub', 'Figma', 'UX Design', 'APIs', 'Documentação'],
        },
      ],
      timeline: [
        {
          period: 'Atual',
          title: 'WL Outlet Home',
          description: 'Atuação em desenvolvimento de sistemas e soluções digitais com foco em operação e negócio.',
        },
        {
          period: '9+ anos',
          title: 'Desenvolvimento full stack',
          description: 'Experiência com PHP, Laravel, Node.js, Vue, JavaScript, bancos de dados e integrações web.',
        },
        {
          period: '2017 - 2020',
          title: 'Universidade Paulista',
          description: 'Formação acadêmica somada a cursos de UX Design, Java e AWS.',
        },
      ],
    };
  },
  methods: {
    scrollToSection(id) {
      const target = document.getElementById(id);

      if (!target) {
        return;
      }

      this.isNavVisible = false;
      target.scrollIntoView({ behavior: 'smooth', block: 'start' });
    },
  },
};
</script>
