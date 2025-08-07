<section class="podcast-section">
  <div class="container grid-lg">
    <header class="section-header">
      <h2>Podcast</h2>
      <div class="subtitle">
        <p>Episódios semanais, ao vivo</p>
      </div>
    </header>
    <div class="podcast-player">
      <iframe
        title="podcast"
        src="https://open.spotify.com/embed/show/2jG7A87jvC6DEAI7k1jSuE?utm_source=generator&t=0"
        width="100%"
        height="152"
        frameBorder="0"
        allowfullscreen=""
        allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"
      />
    </div>
  </div>
</section>

<style>
  .podcast-section {
    padding: 6rem 0;
    background: linear-gradient(135deg, var(--bg-light) 0%, #f8fafc 100%);
  }

  .section-header {
    text-align: center;
    margin-bottom: 3rem;
  }

  h2 {
    font-size: 2.4rem;
    font-weight: bold;
    color: #1a202c;
    margin-bottom: 1rem;
    letter-spacing: -0.02em;
  }

  .subtitle {
    font-size: 1.2rem;
    color: var(--secondary-color);
    line-height: 1.6;
  }

  .podcast-player {
    max-width: 800px;
    margin: 0 auto;
    background: white;
    border-radius: 12px;
    padding: 1.5rem;
    box-shadow:
      0 4px 6px -1px rgba(0, 0, 0, 0.1),
      0 2px 4px -1px rgba(0, 0, 0, 0.06);
  }

  iframe {
    border-radius: 8px;
  }

  @media (max-width: 768px) {
    .podcast-section {
      padding: 4rem 0;
    }

    h2 {
      font-size: 2rem;
    }

    .subtitle {
      font-size: 1.1rem;
    }

    .podcast-player {
      padding: 1rem;
    }
  }
</style>
