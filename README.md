<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Conlux Brasil - Consultoria e Análise Financeira</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; scroll-behavior: smooth; }

    body {
      font-family: Arial, sans-serif;
      background: #000;
      color: #fff;
      position: relative;
      overflow-x: hidden;
    }

    #particles-js {
      position: fixed;
      width: 100%;
      height: 100%;
      z-index: -2;
      top: 0; left: 0;
      background: #000;
    }

    #bg-video {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      object-fit: cover;
      z-index: -1;
      opacity: 0.1;
    }

    header {
      background-color: #111;
      padding: 20px 30px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-bottom: 2px solid #d4af37;
    }

    .logo {
      display: flex;
      align-items: center;
      font-size: 24px;
      color: #d4af37;
      font-weight: bold;
      text-shadow: 2px 2px 5px #d4af37;
    }

    .logo img {
      height: 100px;
      margin-right: 15px;
      filter: drop-shadow(0 0 5px #d4af37);
    }

    .cta {
      background: linear-gradient(90deg, #d4af37, #b8860b);
      color: #000;
      padding: 12px 24px;
      border-radius: 30px;
      font-weight: bold;
      text-decoration: none;
      cursor: pointer;
      animation: pulse 2s infinite;
      box-shadow: 0 0 10px #d4af37;
    }

    @keyframes pulse {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.05); }
    }

    .hero {
      padding: 60px 20px;
      text-align: center;
      animation: fadeIn 1.5s ease-in;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(30px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .hero h1 {
      font-size: 32px;
      color: #d4af37;
      margin-bottom: 25px;
    }

    .hero p {
      font-size: 18px;
      color: #ccc;
      margin-bottom: 15px;
    }

    .timeline {
      display: flex;
      flex-direction: column;
      max-width: 800px;
      margin: 60px auto;
    }

    .timeline-step {
      background-color: #111;
      border-left: 4px solid #d4af37;
      padding: 20px;
      margin-bottom: 20px;
      position: relative;
    }

    .timeline-step::before {
      content: "";
      width: 14px;
      height: 14px;
      background-color: #d4af37;
      border-radius: 50%;
      position: absolute;
      left: -9px;
      top: 24px;
    }

    .timeline-step i {
      margin-right: 10px;
      color: #d4af37;
    }

    .cards {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
      margin: 60px auto;
    }

    .card {
      width: 200px;
      height: 240px;
      background: #111;
      border-radius: 12px;
      text-align: center;
      padding: 20px;
      transition: transform 0.3s ease, box-shadow 0.3s;
    }

    .card i {
      font-size: 36px;
      color: #d4af37;
      margin-bottom: 15px;
    }

    .card:hover {
      transform: scale(1.05);
      box-shadow: 0 0 20px #d4af37;
    }

    .counter-section {
      text-align: center;
      margin: 60px auto;
    }

    .counter i {
      font-size: 28px;
      color: #d4af37;
      margin-bottom: 10px;
    }

    .counter {
      font-size: 28px;
      font-weight: bold;
      color: #d4af37;
      margin-top: 5px;
    }

    .grafico-section {
      max-width: 800px;
      margin: 60px auto;
      background-color: #111;
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 0 15px #d4af37;
    }

    .whatsapp-section {
      text-align: center;
      padding: 60px 20px;
      background-color: #111;
    }

    .whatsapp-section h2 {
      color: #d4af37;
      margin-bottom: 20px;
    }

    .btn-enviar {
      background: linear-gradient(90deg, #25D366, #128C7E);
      color: #fff;
      padding: 14px 28px;
      font-weight: bold;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      font-size: 16px;
      text-decoration: none;
      box-shadow: 0 0 10px #25D366;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }

    .btn-enviar:hover {
      transform: scale(1.05);
      box-shadow: 0 0 20px #25D366;
    }

    iframe {
      width: 100%;
      height: 300px;
      border: 0;
    }

    .footer {
      background: #111;
      color: #fff;
      padding: 40px 20px;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      gap: 20px;
    }

    .footer-column {
      flex: 1;
      min-width: 200px;
    }

    .footer-column h4 {
      color: #d4af37;
      margin-bottom: 15px;
    }

    .footer-column p {
      color: #ccc;
      font-size: 14px;
    }
  </style>
</head>
<body>
  <div id="particles-js"></div>
  <video autoplay muted loop id="bg-video">
    <source src="https://www.videvo.net/videvo_files/converted/2017_11/preview/171007_Business_01_720p.mp429116.webm" type="video/webm">
  </video>

  <header>
    <div class="logo">
      <img src="logo-caf.png" alt="CAF Logo">
      Consultoria e Análise Financeira
    </div>
    <a class="cta" href="#whatsapp-contato">Fale Conosco</a>
  </header>

  <section class="hero">
    <h1>Transforme sua vida financeira com apoio especializado</h1>
    <p>Oferecemos orientação personalizada para quem busca recuperar sua reputação no mercado e tomar decisões financeiras com segurança.</p>
  </section>

  <section class="timeline">
    <div class="timeline-step"><i class="fab fa-whatsapp"></i> Clique no WhatsApp</div>
    <div class="timeline-step"><i class="fas fa-user-friends"></i> Converse com um especialista</div>
    <div class="timeline-step"><i class="fas fa-file-upload"></i> Envie seus documentos com segurança</div>
    <div class="timeline-step"><i class="fas fa-check-circle"></i> Receba a solução ideal para o seu caso</div>
  </section>

  <section class="cards">
    <div class="card"><i class="fas fa-id-card"></i><div>Consulta CPF e CNPJ</div></div>
    <div class="card"><i class="fas fa-chart-bar"></i><div>Acompanhamento do Score</div></div>
    <div class="card"><i class="fas fa-handshake"></i><div>Negociação de Dívidas</div></div>
    <div class="card"><i class="fas fa-file-signature"></i><div>Assessoria Jurídica</div></div>
  </section>

  <section class="counter-section">
    <div><i class="fas fa-users"></i><div class="counter">+3500 Clientes Atendidos</div></div>
    <div><i class="fas fa-briefcase"></i><div class="counter">+5 Anos de Experiência</div></div>
    <div><i class="fas fa-building"></i><div class="counter">+1200 Empresas Ajudadas</div></div>
  </section>

  <section class="grafico-section">
    <canvas id="scoreChart"></canvas>
  </section>

  <section>
    <iframe src="https://www.google.com/maps/embed?pb=!1m14!1m12!1m3!1d12677238.692980943!2d-49.8799464!3d-14.2394248!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!5e0!3m2!1spt-BR!2sbr!4v1720000000000" allowfullscreen loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
  </section>

  <section class="whatsapp-section" id="whatsapp-contato">
    <h2>Clique no botão abaixo e fale com um de nossos atendentes via WhatsApp</h2>
    <a class="btn-enviar" href="https://wa.me/5581989888797" target="_blank">Falar com um Atendente</a>
  </section>

  <footer class="footer">
    <div class="footer-column">
      <h4>Contato</h4>
      <p><i class="fab fa-whatsapp"></i> 81 99898-8797</p>
      <p><i class="fas fa-envelope"></i> conluxbrasil@gmail.com</p>
    </div>
    <div class="footer-column">
      <h4>Endereço</h4>
      <p><i class="fas fa-map-marker-alt"></i> Recife, Pernambuco - Brasil</p>
    </div>
    <div class="footer-column">
      <h4>Sobre</h4>
      <p>Especialistas em recuperação de crédito, contabilidade e consultoria financeira para CPF e CNPJ.</p>
    </div>
  </footer>

  <script src="https://cdn.jsdelivr.net/npm/particles.js@2.0.0/particles.min.js"></script>
  <script>
    particlesJS('particles-js', {
      particles: {
        number: { value: 80, density: { enable: true, value_area: 800 } },
        color: { value: "#d4af37" },
        shape: { type: "circle" },
        opacity: { value: 0.5 },
        size: { value: 3, random: true },
        line_linked: { enable: true, distance: 150, color: "#d4af37", opacity: 0.4, width: 1 },
        move: { enable: true, speed: 2 }
      },
      interactivity: {
        events: {
          onhover: { enable: true, mode: "grab" },
          onclick: { enable: true, mode: "push" },
          resize: true
        },
        modes: {
          grab: { distance: 140, line_linked: { opacity: 1 } },
          push: { particles_nb: 4 }
        }
      },
      retina_detect: true
    });
  </script>

  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
  <script>
    const ctx = document.getElementById('scoreChart').getContext('2d');
    new Chart(ctx, {
      type: 'line',
      data: {
        labels: ['Jan', 'Fev', 'Mar', 'Abr', 'Mai', 'Jun'],
        datasets: [{
          label: 'Evolução do Score',
          data: [400, 520, 610, 690, 740, 800],
          borderColor: '#d4af37',
          backgroundColor: 'rgba(212,175,55,0.2)',
          borderWidth: 2,
          tension: 0.3,
          fill: true,
          pointBackgroundColor: '#fff'
        }]
      },
      options: {
        scales: {
          y: { beginAtZero: false, ticks: { color: '#fff' } },
          x: { ticks: { color: '#fff' } }
        },
        plugins: {
          legend: { labels: { color: '#fff' } }
        }
      }
    });
  </script>

  <script type="text/javascript">
    var Tawk_API=Tawk_API||{}, Tawk_LoadStart=new Date();
    (function(){
      var s1=document.createElement("script"),s0=document.getElementsByTagName("script")[0];
      s1.async=true;
      s1.src='https://embed.tawk.to/6866aab5ea734d190e48b9cc/1iv8gllr0';
      s1.charset='UTF-8';
      s1.setAttribute('crossorigin','*');
      s0.parentNode.insertBefore(s1,s0);
    })();
  </script>
</body>
</html>
