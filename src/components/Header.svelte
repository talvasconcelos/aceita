<header class="hero-section">
  <div class="hero container grid-lg">
    <div class="hero-content">
      <div class="hero-text">
        <h1>Adopção, Educação e Informação sobre Bitcoin</h1>
        <p>
          Acreditamos numa economia local, baseada em Bitcoin, que potencie
          novas oportunidades à comunidade
        </p>
        <div class="hero-buttons">
          <a href="/porque-bitcoin" class="btn btn-primary">Saber Mais</a>
          <a href="/encontros" class="btn btn-primary">Encontrar Eventos</a>
        </div>
      </div>
      <div class="hero-visual">
        <img src="../../images/hero_bitcoin.svg" alt="Comunidade conectada" />
      </div>
    </div>
  </div>
</header>

<style>
  .hero-section {
    background: linear-gradient(135deg, #f8fafc 0%, #e2e8f0 100%);
    padding: 6rem 0;
    overflow: hidden;
  }

  .hero-content {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    align-items: center;
  }

  .hero-text {
    max-width: 600px;
  }

  .hero-text h1 {
    font-size: 3.5rem;
    line-height: 1.2;
    font-weight: 700;
    color: #1a202c;
    margin-bottom: 1.5rem;
    letter-spacing: -0.02em;
  }

  .hero-text p {
    font-size: 1.25rem;
    line-height: 1.6;
    color: #4a5568;
    margin-bottom: 2rem;
  }

  .hero-buttons {
    display: flex;
    gap: 1rem;
  }

  .btn {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    padding: 0.875rem 1.5rem;
    border-radius: 8px;
    font-weight: 500;
    font-size: 1.125rem;
    transition: all 0.2s ease;
    text-decoration: none;
  }

  .btn-primary {
    background-color: #2563eb;
    color: white;
    border: 2px solid #2563eb;
  }

  .btn-primary:hover {
    background-color: #1d4ed8;
    border-color: #1d4ed8;
    transform: translateY(-2px);
  }

  .btn-outline {
    background-color: transparent;
    color: #2563eb;
    border: 2px solid #2563eb;
  }

  .btn-outline:hover {
    background-color: #2563eb;
    color: white;
    transform: translateY(-2px);
  }

  .hero-visual {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .hero-visual img {
    width: 100%;
    max-width: 500px;
    height: auto;
    animation: float 6s ease-in-out infinite;
  }

  @keyframes float {
    0% {
      transform: translateY(0px);
    }
    50% {
      transform: translateY(-20px);
    }
    100% {
      transform: translateY(0px);
    }
  }

  @media (max-width: 1024px) {
    .hero-section {
      padding: 4rem 0;
    }

    .hero-text h1 {
      font-size: 2.75rem;
    }

    .hero-text p {
      font-size: 1.125rem;
    }
  }

  @media (max-width: 768px) {
    .hero-content {
      grid-template-columns: 1fr;
      gap: 3rem;
      text-align: center;
    }

    .hero-text {
      margin: 0 auto;
    }

    .hero-buttons {
      justify-content: center;
    }

    .hero-visual {
      order: -1;
    }

    .hero-visual img {
      max-width: 400px;
    }
  }

  @media (max-width: 640px) {
    .hero-section {
      padding: 3rem 0;
    }

    .hero-text h1 {
      font-size: 2rem;
    }

    .hero-text p {
      font-size: 1rem;
    }

    .hero-buttons {
      flex-direction: column;
    }

    .btn {
      width: 100%;
    }

    .hero-visual img {
      max-width: 300px;
    }
  }
</style>
