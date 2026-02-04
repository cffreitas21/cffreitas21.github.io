<!doctype html>
<html lang="pt-PT">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Carlos Freitas — Portefólio</title>
  <meta name="description" content="Portefólio pessoal de Carlos Freitas: sobre, soft skills, projetos e contactos." />

  <style>
    @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap');

    :root{
      --bg-dark: #050a14;
      --bg-card: #0f1621;
      --bg-elevated: #1a2332;
      --text-primary: #e8eef7;
      --text-secondary: #9ba3b4;
      --text-muted: #6b7280;
      --border: #1e293b;
      --accent-primary: #3b82f6;
      --accent-secondary: #10b981;
      --accent-purple: #8b5cf6;
      --accent-orange: #f59e0b;
      --gradient-1: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
      --gradient-2: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
      --gradient-3: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
      --gradient-4: linear-gradient(135deg, #43e97b 0%, #38f9d7 100%);
    }

    *{ 
      box-sizing: border-box; 
      margin: 0;
      padding: 0;
    }
    
    html{ 
      scroll-behavior: smooth;
      scroll-padding-top: 80px;
    }
    
    body{
      font-family: 'Inter', system-ui, -apple-system, sans-serif;
      background: var(--bg-dark);
      color: var(--text-primary);
      line-height: 1.6;
      overflow-x: hidden;
    }

    /* Background Effects */
    body::before {
      content: '';
      position: fixed;
      top: -50%;
      right: -50%;
      width: 200%;
      height: 200%;
      background: 
        radial-gradient(circle at 20% 30%, rgba(59, 130, 246, 0.15) 0%, transparent 40%),
        radial-gradient(circle at 80% 20%, rgba(139, 92, 246, 0.12) 0%, transparent 40%),
        radial-gradient(circle at 40% 80%, rgba(16, 185, 129, 0.1) 0%, transparent 40%);
      z-index: -1;
      animation: float 20s ease-in-out infinite;
    }

    @keyframes float {
      0%, 100% { transform: translate(0, 0) rotate(0deg); }
      33% { transform: translate(30px, -30px) rotate(5deg); }
      66% { transform: translate(-20px, 20px) rotate(-5deg); }
    }

    /* Header */
    .header{
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      z-index: 1000;
      backdrop-filter: blur(20px) saturate(180%);
      background: rgba(5, 10, 20, 0.8);
      border-bottom: 1px solid var(--border);
      transition: all 0.3s ease;
    }

    .header-container{
      max-width: 1400px;
      margin: 0 auto;
      padding: 20px 40px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo{
      font-size: 20px;
      font-weight: 700;
      background: linear-gradient(135deg, var(--accent-primary), var(--accent-purple));
      -webkit-background-clip: text;
      background-clip: text;
      -webkit-text-fill-color: transparent;
      letter-spacing: -0.5px;
    }

    .nav-links{
      display: flex;
      gap: 8px;
      list-style: none;
    }

    .nav-links a{
      color: var(--text-secondary);
      text-decoration: none;
      padding: 8px 16px;
      border-radius: 8px;
      font-size: 14px;
      font-weight: 500;
      transition: all 0.2s ease;
    }

    .nav-links a:hover{
      color: var(--text-primary);
      background: var(--bg-elevated);
    }

    /* Hero Section */
    .hero{
      padding: 140px 40px 80px;
      max-width: 1400px;
      margin: 0 auto;
    }

    .hero-content{
      display: grid;
      grid-template-columns: 1.2fr 0.8fr;
      gap: 60px;
      align-items: center;
    }

    .hero-text{
      animation: fadeInUp 0.8s ease;
    }

    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .badge{
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: var(--bg-elevated);
      border: 1px solid var(--border);
      padding: 8px 16px;
      border-radius: 100px;
      font-size: 13px;
      font-weight: 600;
      color: var(--text-secondary);
      margin-bottom: 24px;
    }

    .badge-dot{
      width: 8px;
      height: 8px;
      background: var(--accent-secondary);
      border-radius: 50%;
      animation: pulse 2s infinite;
    }

    @keyframes pulse {
      0%, 100% { opacity: 1; }
      50% { opacity: 0.5; }
    }

    h1{
      font-size: clamp(36px, 5vw, 64px);
      font-weight: 800;
      line-height: 1.1;
      margin-bottom: 24px;
      letter-spacing: -1px;
    }

    .gradient-text{
      background: linear-gradient(135deg, var(--accent-primary), var(--accent-purple));
      -webkit-background-clip: text;
      background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    .hero-description{
      font-size: 18px;
      color: var(--text-secondary);
      margin-bottom: 32px;
      line-height: 1.8;
      max-width: 600px;
    }

    .cta-buttons{
      display: flex;
      gap: 16px;
      flex-wrap: wrap;
    }

    .btn{
      padding: 14px 28px;
      border-radius: 12px;
      font-weight: 600;
      font-size: 15px;
      text-decoration: none;
      display: inline-flex;
      align-items: center;
      gap: 8px;
      transition: all 0.3s ease;
      border: none;
      cursor: pointer;
    }

    .btn-primary{
      background: var(--accent-primary);
      color: white;
      box-shadow: 0 4px 14px rgba(59, 130, 246, 0.4);
    }

    .btn-primary:hover{
      transform: translateY(-2px);
      box-shadow: 0 6px 20px rgba(59, 130, 246, 0.5);
    }

    .btn-secondary{
      background: var(--bg-elevated);
      color: var(--text-primary);
      border: 1px solid var(--border);
    }

    .btn-secondary:hover{
      background: var(--bg-card);
      border-color: var(--accent-primary);
    }

    /* Hero Card */
    .hero-card{
      background: var(--bg-card);
      border: 1px solid var(--border);
      border-radius: 24px;
      padding: 32px;
      position: relative;
      overflow: hidden;
    }

    .hero-card::before{
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 4px;
      background: var(--gradient-1);
    }

    .info-item{
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 16px 0;
      border-bottom: 1px solid var(--border);
    }

    .info-item:last-child{
      border-bottom: none;
    }

    .info-label{
      font-size: 14px;
      color: var(--text-muted);
      font-weight: 500;
    }

    .info-value{
      font-size: 14px;
      color: var(--text-primary);
      font-weight: 600;
      text-align: right;
    }

    /* Section */
    section{
      padding: 80px 40px;
      max-width: 1400px;
      margin: 0 auto;
    }

    .section-header{
      text-align: center;
      max-width: 700px;
      margin: 0 auto 60px;
    }

    .section-tag{
      display: inline-block;
      color: var(--accent-primary);
      font-size: 14px;
      font-weight: 700;
      letter-spacing: 2px;
      text-transform: uppercase;
      margin-bottom: 16px;
    }

    h2{
      font-size: clamp(32px, 4vw, 48px);
      font-weight: 800;
      margin-bottom: 16px;
      letter-spacing: -0.5px;
    }

    .section-description{
      font-size: 17px;
      color: var(--text-secondary);
      line-height: 1.7;
    }

    /* Skills Grid */
    .skills-grid{
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 24px;
    }

    .skill-card{
      background: var(--bg-card);
      border: 1px solid var(--border);
      border-radius: 20px;
      padding: 32px;
      transition: all 0.3s ease;
      position: relative;
      overflow: hidden;
    }

    .skill-card::before{
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: var(--gradient-1);
      opacity: 0;
      transition: opacity 0.3s ease;
    }

    .skill-card:hover{
      transform: translateY(-4px);
      border-color: var(--accent-primary);
    }

    .skill-card:hover::before{
      opacity: 0.05;
    }

    .skill-card h3{
      font-size: 22px;
      margin-bottom: 20px;
      position: relative;
      z-index: 1;
    }

    .skill-card ul{
      list-style: none;
      position: relative;
      z-index: 1;
    }

    .skill-card li{
      padding: 12px 0 12px 28px;
      color: var(--text-secondary);
      position: relative;
      font-size: 15px;
    }

    .skill-card li::before{
      content: '→';
      position: absolute;
      left: 0;
      color: var(--accent-primary);
      font-weight: 700;
    }

    /* Projects */
    .projects-grid{
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(340px, 1fr));
      gap: 28px;
    }

    .project-card{
      background: var(--bg-card);
      border: 1px solid var(--border);
      border-radius: 20px;
      padding: 28px;
      transition: all 0.4s ease;
      position: relative;
      overflow: hidden;
      cursor: pointer;
    }

    .project-card::after{
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: linear-gradient(135deg, rgba(59, 130, 246, 0.1), rgba(139, 92, 246, 0.1));
      opacity: 0;
      transition: opacity 0.4s ease;
    }

    .project-card:hover{
      transform: translateY(-8px);
      border-color: var(--accent-primary);
      box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
    }

    .project-card:hover::after{
      opacity: 1;
    }

    .project-number{
      display: inline-block;
      background: var(--bg-elevated);
      color: var(--text-muted);
      font-size: 12px;
      font-weight: 700;
      padding: 6px 12px;
      border-radius: 8px;
      margin-bottom: 16px;
      position: relative;
      z-index: 1;
    }

    .project-card h3{
      font-size: 22px;
      margin-bottom: 12px;
      position: relative;
      z-index: 1;
    }

    .project-card p{
      color: var(--text-secondary);
      margin-bottom: 20px;
      line-height: 1.7;
      position: relative;
      z-index: 1;
    }

    .project-footer{
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding-top: 20px;
      border-top: 1px solid var(--border);
      position: relative;
      z-index: 1;
    }

    .tech-tags{
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      font-size: 12px;
      color: var(--text-muted);
    }

    .project-link{
      color: var(--accent-primary);
      text-decoration: none;
      font-weight: 600;
      font-size: 14px;
      display: flex;
      align-items: center;
      gap: 6px;
      transition: gap 0.3s ease;
    }

    .project-link:hover{
      gap: 10px;
    }

    /* Contact */
    .contact-section{
      background: var(--bg-card);
      border: 1px solid var(--border);
      border-radius: 32px;
      padding: 60px;
      position: relative;
      overflow: hidden;
    }

    .contact-section::before{
      content: '';
      position: absolute;
      top: -50%;
      right: -50%;
      width: 100%;
      height: 100%;
      background: radial-gradient(circle, rgba(59, 130, 246, 0.15), transparent 60%);
    }

    .contact-grid{
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 60px;
      align-items: start;
      position: relative;
      z-index: 1;
    }

    .contact-info h2{
      margin-bottom: 16px;
    }

    .contact-list{
      list-style: none;
      display: grid;
      gap: 20px;
      margin-top: 40px;
    }

    .contact-item{
      background: var(--bg-elevated);
      border: 1px solid var(--border);
      border-radius: 16px;
      padding: 20px;
      transition: all 0.3s ease;
    }

    .contact-item:hover{
      background: var(--bg-dark);
      border-color: var(--accent-primary);
    }

    .contact-label{
      font-size: 12px;
      text-transform: uppercase;
      letter-spacing: 1px;
      color: var(--text-muted);
      margin-bottom: 8px;
      font-weight: 600;
    }

    .contact-value{
      color: var(--text-primary);
      font-size: 16px;
      font-weight: 600;
    }

    .contact-value a{
      color: inherit;
      text-decoration: none;
      transition: color 0.3s ease;
    }

    .contact-value a:hover{
      color: var(--accent-primary);
    }

    /* Footer */
    footer{
      padding: 40px;
      text-align: center;
      border-top: 1px solid var(--border);
      color: var(--text-muted);
      font-size: 14px;
    }

    /* Responsive */
    @media (max-width: 1024px){
      .hero-content,
      .contact-grid{
        grid-template-columns: 1fr;
        gap: 40px;
      }

      .header-container{
        padding: 16px 24px;
      }

      section{
        padding: 60px 24px;
      }

      .hero{
        padding: 120px 24px 60px;
      }

      .contact-section{
        padding: 40px 28px;
      }
    }

    @media (max-width: 768px){
      .nav-links{
        gap: 4px;
      }

      .nav-links a{
        padding: 8px 12px;
        font-size: 13px;
      }

      h1{
        font-size: 36px;
      }

      h2{
        font-size: 28px;
      }

      .cta-buttons{
        flex-direction: column;
      }

      .btn{
        justify-content: center;
      }

      .projects-grid{
        grid-template-columns: 1fr;
      }

      .skills-grid{
        grid-template-columns: 1fr;
      }
    }

    /* Smooth animations */
    .fade-in{
      opacity: 0;
      animation: fadeIn 0.8s ease forwards;
    }

    @keyframes fadeIn {
      to {
        opacity: 1;
      }
    }
  </style>
</head>

<body>
  <!-- Header -->
  <header class="header">
    <div class="header-container">
      <div class="logo">CF</div>
      <nav>
        <ul class="nav-links">
          <li><a href="#sobre">Sobre</a></li>
          <li><a href="#skills">Competências</a></li>
          <li><a href="#projetos">Projetos</a></li>
          <li><a href="#contactos">Contactos</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <!-- Hero Section -->
  <section class="hero" id="sobre">
    <div class="hero-content">
      <div class="hero-text">
      
        <h1>
          Primeiro-Sargento e<br/>
          <span class="gradient-text">Engenheiro Informático</span>
        </h1>
        
        <p class="hero-description">
          Militar da Força Aérea Portuguesa há 10 anos, atualmente como inspetor de produção em eletricidade e instrumentos de avião. 
          Especializado em manutenção de helicópteros AW119 Koala e estudante de Engenharia Informática.
        </p>
        
        <div class="cta-buttons">
          <a href="#projetos" class="btn btn-primary">
            Ver projetos
            <svg width="16" height="16" viewBox="0 0 16 16" fill="none">
              <path d="M6 3L11 8L6 13" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
            </svg>
          </a>
          <a href="#contactos" class="btn btn-secondary">Entrar em contacto</a>
        </div>
      </div>

      <div class="hero-card">
        <div class="info-item">
          <span class="info-label">Função</span>
          <span class="info-value">Inspetor de Produção</span>
        </div>
        <div class="info-item">
          <span class="info-label">Especialização</span>
          <span class="info-value">Eletricidade & Instrumentos</span>
        </div>
        <div class="info-item">
          <span class="info-label">Aeronave</span>
          <span class="info-value">AW119 Koala</span>
        </div>
        <div class="info-item">
          <span class="info-label">Idiomas</span>
          <span class="info-value">PT • ES • EN</span>
        </div>
        <div class="info-item">
          <span class="info-label">Formação</span>
          <span class="info-value">Eng. Informática</span>
        </div>
        <div class="info-item">
          <span class="info-label">Experiência</span>
          <span class="info-value">+10 anos FAP</span>
        </div>
      </div>
    </div>
  </section>

  <!-- Skills Section -->
  <section id="skills">
    <div class="section-header">
      <span class="section-tag">Competências</span>
      <h2>Conhecimentos Técnicos & Competências</h2>
      <p class="section-description">
        Combinação de experiência técnica operacional, disciplina militar e evolução contínua na área da tecnologia.
      </p>
    </div>

    <div class="skills-grid">
      <div class="skill-card">
        <h3>💻 Linguagens de Programação</h3>
        <ul>
          <li>Python</li>
          <li>Java</li>
          <li>JavaScript</li>
          <li>SQL</li>
        </ul>
      </div>

      <div class="skill-card">
        <h3>🌐 Frameworks & Tecnologias Web</h3>
        <ul>
          <li>React</li>
          <li>Laravel</li>
          <li>ASP.NET</li>
          <li>Desenvolvimento Web Full-Stack</li>
        </ul>
      </div>

      <div class="skill-card">
        <h3>📱 Desenvolvimento Mobile & Sistemas</h3>
        <ul>
          <li>Programação Android</li>
          <li>Sistemas Operativos</li>
          <li>Redes de Computadores</li>
          <li>Arquitetura de Sistemas</li>
        </ul>
      </div>

      <div class="skill-card">
        <h3>⚡ Eletricidade & Eletrónica</h3>
        <ul>
          <li>Conhecimentos aprofundados de eletricidade e eletrónica</li>
          <li>Desmontagem e montagem de equipamentos eletrónicos</li>
          <li>Reparação de aparelhos eletrónicos</li>
          <li>Diagnóstico de avarias elétricas</li>
          <li>Inspeção e manutenção de sistemas elétricos</li>
        </ul>
      </div>

      <div class="skill-card">
        <h3>� Liderança & Gestão</h3>
        <ul>
          <li>Liderança de equipas de manutenção aeronáutica</li>
          <li>Coordenação de trabalhos técnicos complexos</li>
          <li>Supervisão e inspeção de qualidade (QA)</li>
          <li>Gestão de recursos humanos e materiais</li>
          <li>Tomada de decisão em ambientes críticos</li>
        </ul>
      </div>

      <div class="skill-card">
        <h3>�💼 Competências Profissionais</h3>
        <ul>
          <li>Rigor e atenção ao detalhe em ambiente operacional</li>
          <li>Responsabilidade e cumprimento de procedimentos</li>
          <li>Comunicação clara em equipas técnicas</li>
          <li>Gestão de prioridades e trabalho sob pressão</li>
          <li>Resolução de problemas e troubleshooting</li>
        </ul>
      </div>

      <div class="skill-card">
        <h3>🎯 Desenvolvimento Pessoal</h3>
        <ul>
          <li>Aprendizagem contínua (formação + prática)</li>
          <li>Adaptação a novas tecnologias</li>
          <li>Autodisciplina e organização</li>
          <li>Pensamento analítico e crítico</li>
          <li>Compromisso com a excelência</li>
        </ul>
      </div>

      <div class="skill-card">
        <h3>🚀 Interesses & Hobbies</h3>
        <ul>
          <li>Tecnologia e desenvolvimento de software</li>
          <li>Automação e otimização de processos</li>
          <li>Projetos académicos e pessoais</li>
          <li>Futebol e desporto</li>
          <li>Treino físico</li>
          <li>Gaming</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- Projects Section -->
  <section id="projetos">
    <div class="section-header">
      <span class="section-tag">Portfolio</span>
      <h2>Projetos em Destaque</h2>
      <p class="section-description">
        Seleção de projetos académicos e pessoais que demonstram as minhas capacidades técnicas e evolução contínua.
      </p>
    </div>

    <div class="projects-grid">
      <!-- Projeto 1 -->
      <article class="project-card">
        <span class="project-number">PROJETO #01</span>
        <h3>Nome do Projeto</h3>
        <p>
          Descrição breve do projeto: problema identificado, solução implementada e resultados obtidos. 
          Inclui detalhes sobre o processo de desenvolvimento.
        </p>
        <div class="project-footer">
          <div class="tech-tags">Python • Docker • API</div>
          <a href="#" class="project-link">
            Ver projeto
            <svg width="14" height="14" viewBox="0 0 16 16" fill="none">
              <path d="M6 3L11 8L6 13" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
            </svg>
          </a>
        </div>
      </article>

      <!-- Projeto 2 -->
      <article class="project-card">
        <span class="project-number">PROJETO #02</span>
        <h3>Nome do Projeto</h3>
        <p>
          Descrição do objetivo principal, funcionalidades implementadas e o contributo técnico. 
          Destaque para desafios superados e aprendizagens.
        </p>
        <div class="project-footer">
          <div class="tech-tags">Java • Spring • PostgreSQL</div>
          <a href="#" class="project-link">
            Ver projeto
            <svg width="14" height="14" viewBox="0 0 16 16" fill="none">
              <path d="M6 3L11 8L6 13" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
            </svg>
          </a>
        </div>
      </article>

      <!-- Projeto 3 -->
      <article class="project-card">
        <span class="project-number">PROJETO #03</span>
        <h3>Nome do Projeto</h3>
        <p>
          Descrição das tecnologias utilizadas, processo de validação (testes, métricas) 
          e principais aprendizagens durante o desenvolvimento.
        </p>
        <div class="project-footer">
          <div class="tech-tags">React • Node • MongoDB</div>
          <a href="#" class="project-link">
            Ver projeto
            <svg width="14" height="14" viewBox="0 0 16 16" fill="none">
              <path d="M6 3L11 8L6 13" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
            </svg>
          </a>
        </div>
      </article>

      <!-- Projeto 4 -->
      <article class="project-card">
        <span class="project-number">PROJETO #04</span>
        <h3>Nome do Projeto</h3>
        <p>
          Projeto focado em automação, integração contínua ou desenvolvimento de scripts. 
          Descrição do impacto e eficiência alcançada.
        </p>
        <div class="project-footer">
          <div class="tech-tags">Bash • GitHub Actions • Linux</div>
          <a href="#" class="project-link">
            Ver projeto
            <svg width="14" height="14" viewBox="0 0 16 16" fill="none">
              <path d="M6 3L11 8L6 13" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
            </svg>
          </a>
        </div>
      </article>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contactos">
    <div class="contact-section">
      <div class="contact-grid">
        <div class="contact-info">
          <span class="section-tag">Contactos</span>
          <h2>Vamos conversar?</h2>
          <p class="section-description">
            Estou disponível para discutir oportunidades, colaborações ou projetos. 
            Entre em contacto através dos meios abaixo.
          </p>
        </div>

        <ul class="contact-list">
          <li class="contact-item">
            <div class="contact-label">Email</div>
            <div class="contact-value">
              <a href="mailto:carlosfreitas-21@hotmail.com">carlosfreitas-21@hotmail.com</a>
            </div>
          </li>

          <li class="contact-item">
            <div class="contact-label">Telefone</div>
            <div class="contact-value">
              <a href="tel:+351912812538">+351 912 812 538</a>
            </div>
          </li>

          <li class="contact-item">
            <div class="contact-label">LinkedIn</div>
            <div class="contact-value">
              <a href="#" target="_blank" rel="noopener noreferrer">linkedin.com/in/carlos-freitas</a>
            </div>
          </li>

          <li class="contact-item">
            <div class="contact-label">GitHub</div>
            <div class="contact-value">
              <a href="#" target="_blank" rel="noopener noreferrer">github.com/carlosfreitas</a>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    <p>© <span id="year"></span> Carlos Freitas. Todos os direitos reservados.</p>
  </footer>

  <script>
    // Update year
    document.getElementById('year').textContent = new Date().getFullYear();

    // Smooth scroll for navigation links
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function (e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        if (target) {
          target.scrollIntoView({ behavior: 'smooth' });
        }
      });
    });

    // Header background on scroll
    const header = document.querySelector('.header');
    window.addEventListener('scroll', () => {
      if (window.scrollY > 100) {
        header.style.background = 'rgba(5, 10, 20, 0.95)';
      } else {
        header.style.background = 'rgba(5, 10, 20, 0.8)';
      }
    });
  </script>
</body>
</html>
