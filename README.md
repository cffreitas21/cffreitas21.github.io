# cffreitas21.github.io
<!doctype html>
<html lang="pt-PT">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Carlos Freitas — Portefólio</title>
  <meta name="description" content="Portefólio pessoal de Carlos Freitas: sobre, soft skills, projetos e contactos." />

  <style>
    :root{
      --bg: #0b1220;
      --panel: rgba(255,255,255,.06);
      --panel2: rgba(255,255,255,.08);
      --text: rgba(255,255,255,.92);
      --muted: rgba(255,255,255,.72);
      --line: rgba(255,255,255,.12);
      --accent: #7c5cff;
      --accent2: #22c55e;
      --shadow: 0 20px 60px rgba(0,0,0,.35);
      --radius: 18px;
      --max: 1120px;
    }

    *{ box-sizing: border-box; }
    html,body{ height: 100%; }
    body{
      margin: 0;
      font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Arial, "Noto Sans", "Helvetica Neue", sans-serif;
      background:
        radial-gradient(1200px 700px at 10% 5%, rgba(124,92,255,.25), transparent 60%),
        radial-gradient(900px 600px at 90% 15%, rgba(34,197,94,.16), transparent 55%),
        radial-gradient(800px 600px at 50% 110%, rgba(255,255,255,.08), transparent 55%),
        var(--bg);
      color: var(--text);
    }

    a{ color: inherit; text-decoration: none; }
    a:hover{ text-decoration: underline; }

    /* Layout */
    .container{
      width: min(var(--max), calc(100% - 40px));
      margin: 0 auto;
    }
    .section{
      padding: 64px 0;
    }
    .intro{
      padding: 72px 0 24px;
    }

    /* Simple header nav */
    header{
      position: sticky;
      top: 0;
      z-index: 10;
      backdrop-filter: blur(10px);
      background: rgba(11,18,32,.55);
      border-bottom: 1px solid var(--line);
    }
    .nav{
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 14px 0;
      gap: 16px;
    }
    .brand{
      display: flex;
      align-items: center;
      gap: 10px;
      font-weight: 700;
      letter-spacing: .2px;
    }
    .dot{
      width: 10px; height: 10px; border-radius: 999px;
      background: var(--accent);
      box-shadow: 0 0 0 4px rgba(124,92,255,.15);
    }
    .nav a.link{
      color: var(--muted);
      font-weight: 600;
      font-size: 14px;
      padding: 10px 12px;
      border-radius: 999px;
    }
    .nav a.link:hover{
      background: rgba(255,255,255,.06);
      color: var(--text);
      text-decoration: none;
    }
    .nav-right{ display: flex; align-items: center; gap: 6px; flex-wrap: wrap; }

    /* Typography */
    h1,h2,h3{ margin: 0 0 10px; }
    h1{
      font-size: clamp(28px, 4vw, 44px);
      line-height: 1.1;
      letter-spacing: -0.02em;
    }
    h2{
      font-size: clamp(22px, 2.6vw, 30px);
      letter-spacing: -0.01em;
    }
    p{ margin: 0; color: var(--muted); line-height: 1.7; }
    .lead{ font-size: 16px; max-width: 70ch; }

    .eyebrow{
      display: inline-block;
      font-size: 12px;
      letter-spacing: .14em;
      text-transform: uppercase;
      color: rgba(255,255,255,.68);
      margin-bottom: 10px;
      padding: 6px 10px;
      border-radius: 999px;
      border: 1px solid var(--line);
      background: rgba(255,255,255,.04);
    }

    /* Cards and grids */
    .hero{
      display: grid;
      grid-template-columns: 1.2fr .8fr;
      gap: 22px;
      align-items: stretch;
    }
    .panel{
      background: linear-gradient(180deg, rgba(255,255,255,.07), rgba(255,255,255,.04));
      border: 1px solid var(--line);
      border-radius: var(--radius);
      padding: 22px;
      box-shadow: var(--shadow);
    }
    .panel.soft{
      box-shadow: none;
      background: rgba(255,255,255,.05);
    }

    .quick-facts{
      display: grid;
      gap: 10px;
      margin-top: 12px;
    }
    .fact{
      padding: 12px 14px;
      border-radius: 14px;
      background: rgba(255,255,255,.04);
      border: 1px solid var(--line);
      color: rgba(255,255,255,.86);
      font-size: 14px;
      display: flex;
      justify-content: space-between;
      gap: 10px;
    }
    .fact span{ color: rgba(255,255,255,.65); }

    .section-header{
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 18px;
      align-items: end;
      margin-bottom: 18px;
    }
    .section-header p{ max-width: 70ch; }

    .skills-grid{
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 16px;
      margin-top: 14px;
    }
    .card-block{
      background: rgba(255,255,255,.05);
      border: 1px solid var(--line);
      border-radius: var(--radius);
      padding: 18px;
    }
    ul{
      margin: 12px 0 0;
      padding-left: 18px;
      color: rgba(255,255,255,.78);
      line-height: 1.7;
    }
    li{ margin: 6px 0; }

    /* Projects */
    .project-grid{
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 16px;
      margin-top: 18px;
    }
    .project-card{
      background: rgba(255,255,255,.05);
      border: 1px solid var(--line);
      border-radius: var(--radius);
      padding: 18px;
      display: grid;
      gap: 10px;
      transition: transform .15s ease, border-color .15s ease, background .15s ease;
    }
    .project-card:hover{
      transform: translateY(-2px);
      border-color: rgba(124,92,255,.35);
      background: rgba(255,255,255,.06);
    }
    .project-type{
      font-size: 12px;
      letter-spacing: .12em;
      text-transform: uppercase;
      color: rgba(255,255,255,.70);
      margin: 0;
    }
    .project-meta{
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 12px;
      flex-wrap: wrap;
      padding-top: 6px;
      border-top: 1px solid var(--line);
      margin-top: 4px;
    }
    .project-meta span{
      color: rgba(255,255,255,.74);
      font-size: 13px;
    }
    .project-meta a{
      font-weight: 700;
      color: rgba(255,255,255,.92);
      border-bottom: 1px dashed rgba(255,255,255,.25);
      padding-bottom: 2px;
    }
    .project-meta a:hover{
      text-decoration: none;
      border-bottom-color: rgba(124,92,255,.7);
    }

    /* Contact */
    .contact-card{
      padding: 22px;
      display: grid;
      grid-template-columns: 1.2fr .8fr;
      gap: 18px;
      align-items: start;
    }
    .contact-card ul{
      list-style: none;
      padding: 0;
      margin: 0;
      display: grid;
      gap: 10px;
    }
    .contact-card li{
      display: grid;
      gap: 4px;
      padding: 12px 14px;
      border: 1px solid var(--line);
      border-radius: 14px;
      background: rgba(255,255,255,.04);
    }
    .contact-card li span{
      font-size: 12px;
      letter-spacing: .1em;
      text-transform: uppercase;
      color: rgba(255,255,255,.62);
    }
    .contact-card li a{
      color: rgba(255,255,255,.90);
      font-weight: 650;
      word-break: break-word;
    }

    footer{
      padding: 28px 0 40px;
      border-top: 1px solid var(--line);
      color: rgba(255,255,255,.55);
      font-size: 13px;
    }

    /* Responsive */
    @media (max-width: 900px){
      .hero, .section-header, .contact-card{ grid-template-columns: 1fr; }
      .project-grid{ grid-template-columns: 1fr; }
    }
  </style>
</head>

<body>
  <header>
    <div class="container nav">
      <div class="brand">
        <span class="dot" aria-hidden="true"></span>
        <span>Carlos Freitas</span>
      </div>
      <nav class="nav-right" aria-label="Navegação principal">
        <a class="link" href="#sobre">Sobre</a>
        <a class="link" href="#skills-hobbies">Soft skills</a>
        <a class="link" href="#projetos">Projetos</a>
        <a class="link" href="#contactos">Contactos</a>
      </nav>
    </div>
  </header>

  <main>
    <!-- SOBRE -->
    <section class="container intro" id="sobre">
      <div class="hero">
        <div class="panel">
          <p class="eyebrow">Sobre mim</p>
          <h1>Primeiro-Sargento da Força Aérea Portuguesa<br/>e estudante de Engenharia Informática</h1>
          <p class="lead">
            Sou militar há cerca de 10 anos e atualmente desempenho funções como inspetor de produção em eletricidade e instrumentos de avião,
            com foco na manutenção de helicópteros AW119 Koala. Paralelamente, frequento a Licenciatura em Engenharia Informática.
          </p>

          <div class="quick-facts" aria-label="Factos rápidos">
            <div class="fact"><strong>Função</strong><span>Inspetor de produção (Eletricidade &amp; Instrumentos)</span></div>
            <div class="fact"><strong>Área</strong><span>Manutenção aeronáutica (AW119 Koala)</span></div>
            <div class="fact"><strong>Idiomas</strong><span>Português • Espanhol • Inglês</span></div>
            <div class="fact"><strong>Formação</strong><span>Engenharia Informática (a decorrer)</span></div>
          </div>
        </div>

        <aside class="panel soft" aria-label="Resumo rápido">
          <p class="eyebrow">Destaque</p>
          <h2>O que faço melhor</h2>
          <p>
            Diagnóstico e resolução de avarias elétricas, inspeção de manutenções programadas e tarefas técnicas em sistemas e instrumentos
            (incluindo atualizações e afinações em aviônica).
          </p>
          <div style="height: 12px"></div>
          <p>
            <strong style="color: rgba(255,255,255,.88)">Objetivo do portefólio:</strong>
            juntar experiência técnica, disciplina operacional e evolução académica, com projetos (placeholder) para mostrar o que tenho desenvolvido.
          </p>
        </aside>
      </div>
    </section>

    <!-- SOFT SKILLS & HOBBIES -->
    <section class="section skills-hobbies" id="skills-hobbies">
      <div class="container section-header">
        <div>
          <p class="eyebrow">Mais sobre mim</p>
          <h2>Soft skills &amp; interesses</h2>
        </div>
        <p>
          Para além da parte técnica, valorizo capacidades comportamentais, trabalho em equipa e evolução contínua.
          (Ajusta esta secção para refletir a tua realidade atual.)
        </p>
      </div>

      <div class="container skills-grid">
        <div class="card-block">
          <h3>Soft skills</h3>
          <ul>
            <li>Rigor e atenção ao detalhe (ambiente operacional)</li>
            <li>Responsabilidade e cumprimento de procedimentos</li>
            <li>Comunicação clara em equipas técnicas</li>
            <li>Gestão de prioridades e trabalho sob pressão</li>
            <li>Resolução de problemas e troubleshooting</li>
            <li>Aprendizagem contínua (formação + prática)</li>
          </ul>
        </div>

        <div class="card-block">
          <h3>Hobbies e interesses</h3>
          <ul>
            <li><!-- TODO: troca pelo teu hobby --> Ex.: treino físico / desporto</li>
            <li><!-- TODO --> Ex.: tecnologia e ferramentas de desenvolvimento</li>
            <li><!-- TODO --> Ex.: projetos académicos</li>
            <li><!-- TODO --> Ex.: leitura / música / viagens</li>
          </ul>
        </div>
      </div>
    </section>

    <!-- PROJETOS (PLACEHOLDERS) -->
    <section class="section projects" id="projetos">
      <div class="container section-header">
        <div>
          <p class="eyebrow">Projetos em destaque</p>
          <h2>O que tenho construído</h2>
        </div>
        <p>
          Aqui ficam placeholders para os teus projetos (académicos, pessoais ou ligados a automação/IT).
          Substitui os textos, tecnologias e links quando tiveres os repositórios prontos.
        </p>
      </div>

      <div class="container project-grid">
        <!-- PROJETO 1 -->
        <article class="project-card">
          <p class="project-type">Projeto #1</p>
          <h3><!-- TODO: título --> Nome do projeto (placeholder)</h3>
          <p>
            <!-- TODO: descrição -->
            Descrição curta do projeto: o problema que resolves, o que implementaste e o resultado obtido.
          </p>
          <div class="project-meta">
            <span><!-- TODO: stack --> Tecnologias: Ex.: Python • Docker • API</span>
            <a href="#" target="_blank" rel="noopener noreferrer" aria-label="Ver projeto">
              Ver projeto →
            </a>
          </div>
        </article>

        <!-- PROJETO 2 -->
        <article class="project-card">
          <p class="project-type">Projeto #2</p>
          <h3>Nome do projeto (placeholder)</h3>
          <p>
            Descrição curta do projeto: objetivo, principais funcionalidades e o teu contributo.
          </p>
          <div class="project-meta">
            <span>Tecnologias: Ex.: Java • Spring • PostgreSQL</span>
            <a href="#" target="_blank" rel="noopener noreferrer">Ver projeto →</a>
          </div>
        </article>

        <!-- PROJETO 3 -->
        <article class="project-card">
          <p class="project-type">Projeto #3</p>
          <h3>Nome do projeto (placeholder)</h3>
          <p>
            Descrição curta do projeto: o que aprendeste e como validaste (testes, métricas, demo).
          </p>
          <div class="project-meta">
            <span>Tecnologias: Ex.: React • Node • MongoDB</span>
            <a href="#" target="_blank" rel="noopener noreferrer">Ver projeto →</a>
          </div>
        </article>

        <!-- PROJETO 4 -->
        <article class="project-card">
          <p class="project-type">Projeto #4</p>
          <h3>Nome do projeto (placeholder)</h3>
          <p>
            Descrição curta do projeto: integração, automação, scripts, CI/CD, etc.
          </p>
          <div class="project-meta">
            <span>Tecnologias: Ex.: Bash • GitHub Actions • Linux</span>
            <a href="#" target="_blank" rel="noopener noreferrer">Ver projeto →</a>
          </div>
        </article>
      </div>
    </section>

    <!-- CONTACTOS -->
    <section class="container section">
      <div class="panel contact-card" id="contactos">
        <div>
          <p class="eyebrow">Contactos</p>
          <h2>Vamos conversar?</h2>
          <p>
            Para oportunidades, colaborações ou dúvidas, contacta-me pelos meios abaixo.
          </p>
          <div style="height: 12px"></div>
          <p style="color: rgba(255,255,255,.72); font-size: 14px;">
            <!-- TODO: opcional -->
            (Opcional) Podes adicionar aqui a tua disponibilidade, zona geográfica ou preferências de contacto.
          </p>
        </div>

        <ul aria-label="Lista de contactos">
          <li>
            <span>Email</span>
            <a href="mailto:carlosfreitas-21@hotmail.com">carlosfreitas-21@hotmail.com</a>
          </li>

          <li>
            <span>Telefone</span>
            <a href="tel:+351912812538">+351 912 812 538</a>
          </li>

          <li>
            <span>LinkedIn</span>
            <!-- TODO: mete o teu link real -->
            <a href="#" target="_blank" rel="noopener noreferrer">https://www.linkedin.com/in/SEU-PERFIL</a>
          </li>

          <li>
            <span>GitHub</span>
            <!-- TODO: mete o teu link real -->
            <a href="#" target="_blank" rel="noopener noreferrer">https://github.com/SEU-USER</a>
          </li>
        </ul>
      </div>
    </section>
  </main>

  <footer>
    <div class="container">
      © <span id="year"></span> Carlos Freitas — Portefólio.
    </div>
  </footer>

  <script>
    document.getElementById("year").textContent = new Date().getFullYear();
  </script>
</body>
</html>
