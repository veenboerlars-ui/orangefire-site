<html lang="nl"><head>
  <meta charset="UTF-8">
  <title>Rhein Fire – Orange Fire Fanpage voor Nederlandse Fans</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <style>
    :root {
      --bg-dark: #050610;
      --bg-card: #111321;
      --accent: #ff5a1f;
      --accent-soft: rgba(255, 90, 31, 0.18);
      --accent-alt: #ffb347;
      --text-main: #f5f5f7;
      --text-muted: #a5a7b5;
      --border-subtle: #27293a;
      --radius-xl: 18px;
      --shadow-soft: 0 18px 45px rgba(0, 0, 0, 0.45);
      --font-main: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: var(--font-main);
      background: radial-gradient(circle at top, #181b3a 0, #050610 60%);
      color: var(--text-main);
      line-height: 1.6;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    /* Top nav */
    .top-nav {
      position: sticky;
      top: 0;
      z-index: 20;
      backdrop-filter: blur(18px);
      background: linear-gradient(to bottom, rgba(5,6,16,0.97), rgba(5,6,16,0.9), transparent);
      border-bottom: 1px solid rgba(255,255,255,0.06);
    }

    .top-nav-inner {
      max-width: 1120px;
      margin: 0 auto;
      padding: 10px 16px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 10px;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .brand-badge {
      width: 32px;
      height: 32px;
      border-radius: 10px;
      background: radial-gradient(circle at 30% 0, #ffe7c2 0, #ff5a1f 45%, #3b0f0a 100%);
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 0 16px rgba(255, 90, 31, 0.7);
      font-weight: 700;
      font-size: 17px;
    }

    .brand-text {
      font-size: 14px;
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      color: var(--text-muted);
    }

    .nav-links {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      justify-content: flex-end;
    }

    .nav-link {
      font-size: 13px;
      padding: 6px 10px;
      border-radius: 999px;
      border: 1px solid transparent;
      color: var(--text-muted);
      cursor: pointer;
      transition: 0.2s ease;
    }

    .nav-link:hover {
      border-color: rgba(255,255,255,0.18);
      color: var(--text-main);
      background: rgba(255,255,255,0.03);
    }

    @media (max-width: 720px) {
      .top-nav-inner {
        flex-direction: column;
        align-items: flex-start;
      }
    }

    .page {
      max-width: 1120px;
      margin: 0 auto;
      padding: 80px 16px 40px;
    }

    /* Hero */
    .hero {
      display: grid;
      grid-template-columns: minmax(0,1.5fr) minmax(0,1.1fr);
      gap: 26px;
      align-items: center;
      margin-bottom: 40px;
    }

    @media (max-width: 860px) {
      .hero {
        grid-template-columns: 1fr;
      }
    }

    .hero-kicker {
      font-size: 11px;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      color: var(--accent-alt);
      margin-bottom: 8px;
    }

    .hero-title {
      font-size: clamp(26px, 4vw, 34px);
      font-weight: 700;
      margin-bottom: 8px;
    }

    .hero-highlight {
      background: linear-gradient(115deg, #ff5a1f, #ffb347);
      -webkit-background-clip: text;
      color: transparent;
    }

    .hero-subtitle {
      font-size: 14px;
      color: var(--text-muted);
      max-width: 540px;
      margin-bottom: 18px;
    }

    .hero-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-bottom: 18px;
    }

    .tag {
      font-size: 11px;
      padding: 6px 10px;
      border-radius: 999px;
      border: 1px solid rgba(255,255,255,0.16);
      text-transform: uppercase;
      letter-spacing: 0.12em;
      color: var(--text-muted);
    }

    .tag--accent {
      border-color: rgba(255,90,31,0.8);
      background: rgba(255,90,31,0.15);
      color: var(--accent-alt);
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
    }

    .btn {
      border-radius: 999px;
      border: none;
      font-size: 13px;
      padding: 9px 14px;
      cursor: pointer;
      display: inline-flex;
      align-items: center;
      gap: 6px;
      transition: 0.2s ease;
    }

    .btn-primary {
      background: linear-gradient(130deg,#ff5a1f,#ffb347);
      color: #050610;
      font-weight: 600;
      box-shadow: 0 12px 32px rgba(255,90,31,0.6);
    }

    .btn-primary:hover {
      transform: translateY(-1px);
      box-shadow: 0 18px 40px rgba(255,90,31,0.8);
    }

    .btn-ghost {
      background: transparent;
      border: 1px solid rgba(255,255,255,0.26);
      color: var(--text-main);
    }

    .btn-ghost:hover {
      background: rgba(255,255,255,0.04);
    }

    .hero-card {
      background: radial-gradient(circle at top, #262847 0, #111321 55%);
      border-radius: var(--radius-xl);
      border: 1px solid rgba(255,255,255,0.08);
      padding: 18px 18px 14px;
      box-shadow: var(--shadow-soft);
      font-size: 13px;
    }

    .hero-card h2 {
      font-size: 13px;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      color: var(--text-muted);
      margin-bottom: 10px;
    }

    /* Generic sections */
    .section {
      margin-bottom: 32px;
    }

    .section-header {
      margin-bottom: 8px;
    }

    .section-kicker {
      font-size: 11px;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      color: var(--text-muted);
      margin-bottom: 2px;
    }

    .section-title {
      font-size: 18px;
      font-weight: 600;
    }

    .section-sub {
      font-size: 13px;
      color: var(--text-muted);
    }

    .section p {
      font-size: 13px;
      color: #d5d6e4;
      margin-top: 6px;
    }

    /* Image blocks */
    .image-block {
      margin: 20px 0 26px;
      border-radius: 18px;
      overflow: hidden;
      border: 1px solid rgba(255,255,255,0.08);
      box-shadow: 0 16px 40px rgba(0,0,0,0.5);
    }

    .image-block img {
      display: block;
      width: 100%;
      height: auto;
    }

    .image-caption {
      font-size: 12px;
      padding: 8px 12px 10px;
      background: rgba(5,6,16,0.9);
      color: var(--text-muted);
    }

    /* Cards & grids */
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px,1fr));
      gap: 14px;
      margin-top: 12px;
    }

    .card {
      background: rgba(9,10,23,0.96);
      border-radius: 14px;
      border: 1px solid var(--border-subtle);
      padding: 11px 12px 10px;
      font-size: 13px;
      transition: 0.2s ease;
    }

    .card:hover {
      border-color: rgba(255,90,31,0.6);
      box-shadow: 0 14px 32px rgba(255,90,31,0.25);
      transform: translateY(-1px);
    }

    .card h3, .card h4 {
      margin-bottom: 4px;
      font-size: 14px;
    }

    .pill {
      display: inline-block;
      margin-bottom: 4px;
      font-size: 10px;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      padding: 3px 7px;
      border-radius: 999px;
      background: var(--accent-soft);
      color: var(--accent-alt);
      border: 1px solid rgba(255,90,31,0.82);
    }

    /* Steps */
    .steps {
      counter-reset: step;
      list-style: none;
      margin-top: 10px;
    }

    .steps li {
      position: relative;
      padding-left: 30px;
      margin-bottom: 8px;
      font-size: 13px;
    }

    .steps li::before {
      counter-increment: step;
      content: counter(step);
      position: absolute;
      left: 0;
      top: 2px;
      width: 20px;
      height: 20px;
      border-radius: 50%;
      background: var(--accent-soft);
      color: var(--accent-alt);
      font-size: 11px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: 600;
    }

    /* FAQ */
    .faq-item {
      background: rgba(9,10,23,0.96);
      border-radius: 14px;
      border: 1px solid var(--border-subtle);
      margin-bottom: 8px;
      overflow: hidden;
    }

    .faq-question {
      padding: 10px 12px;
      cursor: pointer;
      font-size: 13px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .faq-question span {
      margin-right: 8px;
    }

    .faq-toggle {
      font-size: 16px;
      color: var(--accent-alt);
      transition: transform 0.2s ease;
    }

    .faq-answer {
      max-height: 0;
      overflow: hidden;
      padding: 0 12px;
      font-size: 13px;
      color: #d5d6e4;
      transition: max-height 0.25s ease, padding-bottom 0.25s ease;
    }

    .faq-item.open .faq-answer {
      max-height: 200px;
      padding-bottom: 10px;
    }

    .faq-item.open .faq-toggle {
      transform: rotate(45deg);
    }

    /* CTA strip */
    .cta-strip {
      margin-top: 28px;
      padding: 14px 16px;
      border-radius: 18px;
      background: linear-gradient(120deg, rgba(255,90,31,0.16), rgba(255,180,71,0.12));
      border: 1px solid rgba(255,90,31,0.7);
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      align-items: center;
      justify-content: space-between;
      font-size: 13px;
    }

    .cta-strip span { max-width: 640px; }

    /* Sponsors & form */
    .sponsor-bar {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      gap: 10px;
      margin: 10px 0 14px;
    }

    .sponsor-label {
      font-size: 11px;
      text-transform: uppercase;
      letter-spacing: 0.18em;
      color: var(--text-muted);
    }

    .sponsor-logos {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      align-items: center;
    }

    .sponsor-logos img {
      height: 40px;
      border-radius: 6px;
      background: #008ecc;
    }

    .form-card form {
      margin-top: 10px;
      display: grid;
      gap: 8px;
    }

    .form-row {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
    }

    .form-row > div {
      flex: 1 1 140px;
    }

    label {
      display: block;
      font-size: 11px;
      margin-bottom: 3px;
      color: var(--text-muted);
    }

    input[type="text"],
    input[type="email"],
    select,
    textarea {
      width: 100%;
      padding: 7px 9px;
      border-radius: 9px;
      border: 1px solid var(--border-subtle);
      background: #070816;
      color: var(--text-main);
      font-size: 13px;
      outline: none;
    }

    textarea {
      min-height: 60px;
      resize: vertical;
    }

    input[type="checkbox"] {
      margin-right: 6px;
    }

    .form-small {
      font-size: 11px;
      color: var(--text-muted);
    }

    .form-success {
      margin-top: 6px;
      font-size: 12px;
      color: var(--accent-alt);
      display: none;
    }

    .form-success.visible {
      display: block;
    }
  </style>
</head>
<body>
  <header class="top-nav">
    <div class="top-nav-inner">
      <div class="brand">
        <div class="brand-badge">RF</div>
        <div class="brand-text">Orange Fire · NL Fans</div>
      </div>
      <nav class="nav-links">
        <a class="nav-link" href="#wat">Wat is Orange Fire?</a>
        <a class="nav-link" href="#wanneer">Wanneer &amp; Waar</a>
        <a class="nav-link" href="#reis">Reis vanuit NL</a>
        <a class="nav-link" href="#tickets">Tickets</a>
        <a class="nav-link" href="#flag">Flag football</a>
        <a class="nav-link" href="#faq">FAQ</a>
      </nav>
    </div>
  </header>

  <main class="page">
    <!-- Hero -->
    <section class="hero" id="top">
      <div>
        <div class="hero-kicker">Speciale actie voor Nederlandse fans</div>
        <h1 class="hero-title">
          Rhein Fire <span class="hero-highlight">Orange Fire</span>
        </h1>
        <p class="hero-subtitle">
          Een unieke wedstrijddag in Düsseldorf, speciaal voor Nederlandse fans. 
          Samen met de bus, in één fanvak, vol vuurwerk, hits en touchdowns.
        </p>
        <div class="hero-tags">
          <span class="tag tag--accent">Dutch Fan Block</span>
          <span class="tag">Bus + Ticket combi</span>
          <span class="tag">American football beleving</span>
        </div>
        <div class="hero-actions">
          <a href="#tickets" class="btn btn-primary">Reserveer jouw plek</a>
          <a href="#wat" class="btn btn-ghost">Meer over Orange Fire</a>
        </div>
      </div>
      <aside class="hero-card">
        <h2>Orange Fire in het kort</h2>
        <p>
          <strong>Voor wie?</strong> Voor iedereen in Nederland die een keer 
          <em>live American football</em> wil meemaken – met vrienden, familie of teamgenoten.
        </p>
        <p style="margin-top:8px;">
          <strong>Wat?</strong> Een speciale Rhein Fire-wedstrijd met een 
          <em>Dutch Fan Block</em>, gezamenlijke busreis, Nederlandse info en extra fan-activiteiten.
        </p>
        <p style="margin-top:8px;">
          <strong>Hoe?</strong> Jij boekt een Bus + Ticket combi, stapt in ergens in Nederland en 
          stapt in Düsseldorf direct in de Orange Fire-sfeer.
        </p>
      </aside>
    </section>

    <!-- Image 1 -->
    <div class="image-block">
      <img src="https://images.pexels.com/photos/1618200/pexels-photo-1618200.jpeg" alt="American football spelers in actie">
      <div class="image-caption">
        Volle tribunes, helm op, muziek hard – Orange Fire brengt Nederlandse fans rechtstreeks in het hart van de ELF.
      </div>
    </div>

    <!-- Wat -->
    <section class="section" id="wat">
      <div class="section-header">
        <div class="section-kicker">1 · Wat</div>
        <h2 class="section-title">Wat is de Orange Fire-campagne?</h2>
        <p class="section-sub">Een gameday-beleving speciaal voor fans uit Nederland.</p>
      </div>
      <p>
        Orange Fire is een speciale wedstrijddag van Rhein Fire in Düsseldorf waarbij 
        <strong>Nederlandse fans centraal</strong> staan. Denk aan:
      </p>
      <ul class="steps">
        <li>Een eigen <strong>Dutch Fan Block</strong> in het stadion, zodat je samen met andere Nederlanders zit.</li>
        <li>Een <strong>Bus + Ticket combi</strong>, zodat je niet zelf hoeft te rijden of te puzzelen met OV.</li>
        <li>Extra aandacht voor <strong>muziek, entertainment en fan-beleving</strong> rond de wedstrijd.</li>
      </ul>
      <p>
        Je hoeft geen American football-expert te zijn. Het belangrijkste is dat je zin hebt in een dag 
        vol sport, sfeer en vuurwerk net over de grens.
      </p>
    </section>

    <!-- Wanneer & Waar -->
    <section class="section" id="wanneer">
      <div class="section-header">
        <div class="section-kicker">2 · Wanneer &amp; Waar</div>
        <h2 class="section-title">American football op rijafstand van Nederland</h2>
        <p class="section-sub">De exacte datum kan later ingevuld worden.</p>
      </div>
      <div class="grid">
        <div class="card">
          <span class="pill">Datum &amp; tijd</span>
          <h3>Orange Fire Gameday</h3>
          <p>
            Datum: <strong>[Datum volgt / in te vullen]</strong><br>
            Kick-off: <strong>[Tijd volgt]</strong><br>
            Stadion open: ruim vóór de wedstrijd voor muziek, food &amp; drinks.
          </p>
        </div>
        <div class="card">
          <span class="pill">Locatie</span>
          <h3>Düsseldorf, Duitsland</h3>
          <p>
            Speelstad: <strong>Düsseldorf</strong><br>
            Stadion: <strong>[Stadionnaam]</strong><br>
            Goed bereikbaar vanuit Nederland met de bus of auto, net over de grens.
          </p>
        </div>
      </div>
    </section>

    <!-- Image 2 -->
    <div class="image-block">
      <img src="https://images.pexels.com/photos/1618269/pexels-photo-1618269.jpeg" alt="Fans in het stadion">
      <div class="image-caption">
        In het Dutch Fan Block beleef je de wedstrijd samen – juichen, high-fives en touchdown-dansjes inbegrepen.
      </div>
    </div>

    <!-- Reis vanuit NL -->
    <section class="section" id="reis">
      <div class="section-header">
        <div class="section-kicker">3 · Reis</div>
        <h2 class="section-title">Reis vanuit Nederland</h2>
        <p class="section-sub">Gemak, sfeer en geen stress over parkeren.</p>
      </div>
      <div class="card">
        <span class="pill">Zo werkt het</span>
        <h3>Bus + Ticket combi</h3>
        <ol class="steps">
          <li><strong>Boek jouw combi</strong> – via de speciale Orange Fire-link ontvang je één pakket: busreis + wedstrijdticket.</li>
          <li><strong>Stap in in Nederland</strong> – op een opstapplaats in (bijv.) Randstad, oosten of zuiden van het land.</li>
          <li><strong>Reis samen</strong> – muziek, voorbeschouwingen en sfeer aan boord met andere Nederlandse fans.</li>
          <li><strong>Stap uit bij het stadion</strong> – geen gedoe met parkeren of route zoeken.</li>
          <li><strong>Na afloop weer terug</strong> – bus brengt je veilig naar dezelfde opstapplaats in Nederland.</li>
        </ol>
        <p>
          Je kunt ook op eigen gelegenheid reizen. In dat geval kun je alleen een ticket voor het Dutch Fan Block boeken.
        </p>
      </div>
    </section>

    <!-- Image 3 -->
    <div class="image-block">
      <img src="https://images.pexels.com/photos/1618260/pexels-photo-1618260.jpeg" alt="Quarterback die gooit">
      <div class="image-caption">
        Touchdowns, field goals en big plays – perfect om met vrienden of teamgenoten een keer live te ervaren.
      </div>
    </div>

    <!-- Tickets -->
    <section class="section" id="tickets">
      <div class="section-header">
        <div class="section-kicker">4 · Tickets</div>
        <h2 class="section-title">Tickets &amp; fanvak</h2>
        <p class="section-sub">Kies hoe jij de Orange Fire-dag wilt beleven.</p>
      </div>
      <div class="grid">
        <div class="card">
          <span class="pill">Aanbevolen</span>
          <h3>Bus + Ticket combi</h3>
          <p>
            ✔ Retour busreis vanuit NL<br>
            ✔ Toegang tot het <strong>Dutch Fan Block</strong><br>
            ✔ Nederlandse info vooraf (mail/WhatsApp)<br>
            ✔ Perfect voor vriendengroepen, teams of familie
          </p>
          <p style="margin-top:6px;">
            <em>Prijs en bestel-link kunnen hier worden toegevoegd.</em>
          </p>
        </div>
        <div class="card">
          <span class="pill">Eigen vervoer</span>
          <h3>Alleen ticket</h3>
          <p>
            ✔ Ticket voor het Dutch Fan Block<br>
            ✔ Ideaal als je zelf met de auto of trein komt<br>
            ✔ Je zit alsnog tussen de Nederlandse fans
          </p>
        </div>
      </div>

      <div style="margin-top:14px;">
        <a href="#" class="btn btn-primary">Ik wil op de hoogte blijven</a>
        <span style="font-size:12px; color:var(--text-muted); margin-left:8px;">
          (Voeg hier later een echte link of formulier toe.)
        </span>
      </div>
    </section>

    <!-- Flag football sign-up -->
    <section class="section" id="flag">
      <div class="section-header">
        <div class="section-kicker">5 · Flag football</div>
        <h2 class="section-title">Meld je aan voor Flag Football-toernooien</h2>
        <p class="section-sub">Toernooien in Nederland rondom Orange Fire – zonder contact, mét spektakel.</p>
      </div>

      <div class="sponsor-bar">
        <span class="sponsor-label">Gesponsord door</span>
        <div class="sponsor-logos">
          <img src="https://1000logos.net/wp-content/uploads/2021/05/Coolblue-logo.png" alt="Coolblue logo">
          <img src="https://1000logos.net/wp-content/uploads/2021/05/Decathlon-logo.png" alt="Decathlon logo">
        </div>
      </div>

      <div class="card form-card">
        <span class="pill">Aanmelden</span>
        <h3>Schrijf je in voor een flag football-toernooi</h3>
        <p>
          Vul hieronder je gegevens in als je mee wilt doen aan een van de flag football-toernooien 
          gekoppeld aan de Orange Fire-campagne. Ideaal voor vriendengroepen, sportteams en schoolsquads.
        </p>

        <form id="flag-form">
          <div class="form-row">
            <div>
              <label for="naam">Naam</label>
              <input type="text" id="naam" name="naam" required>
            </div>
            <div>
              <label for="email">E-mailadres</label>
              <input type="email" id="email" name="email" required>
            </div>
          </div>

          <div class="form-row">
            <div>
              <label for="team">Team / vereniging (optioneel)</label>
              <input type="text" id="team" name="team">
            </div>
            <div>
              <label for="niveau">Niveau</label>
              <select id="niveau" name="niveau" required>
                <option value="" disabled selected>Kies je niveau</option>
                <option>Beginner</option>
                <option>Recreatief</option>
                <option>Ervaren</option>
              </select>
            </div>
          </div>

          <div>
            <label for="locatie">Voorkeurslocatie in NL</label>
            <input type="text" id="locatie" name="locatie" placeholder="Bijv. Randstad, oosten, zuiden">
          </div>

          <div>
            <label for="opmerking">Opmerkingen (bijv. aantal spelers, leeftijdsgroep)</label>
            <textarea id="opmerking" name="opmerking"></textarea>
          </div>

          <div>
            <label class="form-small">
              <input type="checkbox" id="toestemming" required>
              Ik ga akkoord dat mijn gegevens worden gebruikt om mij te informeren over de toernooien.
            </label>
          </div>

          <button type="submit" class="btn btn-primary">Aanmelden voor toernooi</button>
          <p id="flag-success" class="form-success" aria-live="polite"></p>
        </form>
      </div>
    </section>

    <!-- FAQ -->
    <section class="section" id="faq">
      <div class="section-header">
        <div class="section-kicker">6 · FAQ</div>
        <h2 class="section-title">Veelgestelde vragen</h2>
        <p class="section-sub">Handige info voor jouw Orange Fire-trip.</p>
      </div>

      <div class="faq-item">
        <div class="faq-question">
          <span>Moet ik al veel van American football weten?</span>
          <span class="faq-toggle">+</span>
        </div>
        <div class="faq-answer">
          <p>
            Nee hoor. Je krijgt basisuitleg in het vak en op de schermen wordt veel toegelicht. 
            De sfeer, muziek en het spektakel maken het sowieso de moeite waard.
          </p>
        </div>
      </div>

      <div class="faq-item">
        <div class="faq-question">
          <span>Kan ik ook met mijn sportteam komen?</span>
          <span class="faq-toggle">+</span>
        </div>
        <div class="faq-answer">
          <p>
            Zeker, dit is juist ideaal als teamuitje. Je kunt als team plaatsen in het Dutch Fan Block reserveren 
            en samen met de bus reizen. Bij grotere groepen kan er in overleg vaak iets extra’s geregeld worden.
          </p>
        </div>
      </div>

      <div class="faq-item">
        <div class="faq-question">
          <span>Vanaf waar vertrekt de bus in Nederland?</span>
          <span class="faq-toggle">+</span>
        </div>
        <div class="faq-answer">
          <p>
            De exacte opstapplaatsen worden later bekendgemaakt (bijvoorbeeld Randstad, oosten en zuiden van het land). 
            Na je inschrijving ontvang je alle details per mail.
          </p>
        </div>
      </div>

      <div class="faq-item">
        <div class="faq-question">
          <span>Is er eten en drinken in het stadion?</span>
          <span class="faq-toggle">+</span>
        </div>
        <div class="faq-answer">
          <p>
            Ja, in en rond het stadion zijn meerdere foodstands en bars. 
            Je kunt ter plekke eten en drinken kopen, net als bij een voetbalstadion.
          </p>
        </div>
      </div>
    </section>

    <!-- CTA strip -->
    <section class="cta-strip">
      <span>
        Orange Fire is dé kans om American football op topniveau live te beleven – samen met andere Nederlandse fans.
        Houd deze pagina in de gaten voor definitieve datum, prijzen en boekingslinks.
      </span>
      <a href="#top" class="btn btn-ghost">Terug naar boven</a>
    </section>
  </main>

  <script>
    // FAQ toggle
    document.querySelectorAll('.faq-item').forEach(item => {
      item.querySelector('.faq-question').addEventListener('click', () => {
        item.classList.toggle('open');
      });
    });

    // Flag football form handler (front-end demo)
    const flagForm = document.getElementById('flag-form');
    if (flagForm) {
      flagForm.addEventListener('submit', (event) => {
        event.preventDefault();
        const successEl = document.getElementById('flag-success');
        if (successEl) {
          successEl.textContent = 'Bedankt voor je aanmelding! We nemen contact met je op over de toernooien.';
          successEl.classList.add('visible');
        }
        flagForm.reset();
      });
    }
  </script>


</body></html>
