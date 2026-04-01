<!DOCTYPE html>

<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Harmonix — Conditions d'utilisation</title>
  <link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;700;800&family=JetBrains+Mono:wght@300;400&display=swap" rel="stylesheet"/>
  <style>
    :root {
      --bg: #050a0e;
      --surface: #0b1520;
      --accent: #00e5ff;
      --accent2: #7b2fff;
      --text: #c8d8e8;
      --muted: #4a6070;
      --border: #1a2a3a;
    }
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; }
    body {
      background: var(--bg);
      color: var(--text);
      font-family: 'JetBrains Mono', monospace;
      font-size: 14px;
      line-height: 1.8;
      min-height: 100vh;
      overflow-x: hidden;
    }

```
/* Grid background */
body::before {
  content: '';
  position: fixed;
  inset: 0;
  background-image:
    linear-gradient(var(--border) 1px, transparent 1px),
    linear-gradient(90deg, var(--border) 1px, transparent 1px);
  background-size: 40px 40px;
  opacity: 0.4;
  z-index: 0;
  pointer-events: none;
}

/* Glow orbs */
body::after {
  content: '';
  position: fixed;
  top: -200px; left: -200px;
  width: 600px; height: 600px;
  border-radius: 50%;
  background: radial-gradient(circle, rgba(0,229,255,0.06) 0%, transparent 70%);
  z-index: 0;
  pointer-events: none;
}

.container {
  position: relative;
  z-index: 1;
  max-width: 860px;
  margin: 0 auto;
  padding: 60px 24px 100px;
}

/* Header */
header {
  border-bottom: 1px solid var(--border);
  padding-bottom: 40px;
  margin-bottom: 60px;
}

.logo {
  font-family: 'Syne', sans-serif;
  font-size: 13px;
  font-weight: 700;
  letter-spacing: 0.3em;
  text-transform: uppercase;
  color: var(--accent);
  margin-bottom: 32px;
  display: flex;
  align-items: center;
  gap: 10px;
}
.logo::before {
  content: '';
  display: inline-block;
  width: 8px; height: 8px;
  background: var(--accent);
  border-radius: 50%;
  box-shadow: 0 0 10px var(--accent);
  animation: pulse 2s infinite;
}
@keyframes pulse {
  0%, 100% { opacity: 1; transform: scale(1); }
  50% { opacity: 0.5; transform: scale(0.8); }
}

h1 {
  font-family: 'Syne', sans-serif;
  font-size: clamp(32px, 6vw, 56px);
  font-weight: 800;
  line-height: 1.1;
  color: #fff;
  margin-bottom: 16px;
}
h1 span {
  color: var(--accent);
  text-shadow: 0 0 30px rgba(0,229,255,0.4);
}

.meta {
  color: var(--muted);
  font-size: 12px;
  letter-spacing: 0.1em;
}

/* Sections */
section {
  margin-bottom: 48px;
  padding: 32px;
  background: var(--surface);
  border: 1px solid var(--border);
  border-left: 3px solid var(--accent);
  position: relative;
  animation: fadeIn 0.5s ease both;
}
section:nth-child(even) { border-left-color: var(--accent2); }

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(12px); }
  to { opacity: 1; transform: translateY(0); }
}

.section-num {
  position: absolute;
  top: 16px; right: 20px;
  font-family: 'Syne', sans-serif;
  font-size: 48px;
  font-weight: 800;
  color: rgba(255,255,255,0.03);
  line-height: 1;
  pointer-events: none;
}

h2 {
  font-family: 'Syne', sans-serif;
  font-size: 16px;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.2em;
  color: #fff;
  margin-bottom: 16px;
  display: flex;
  align-items: center;
  gap: 10px;
}
h2::before {
  content: '//';
  color: var(--accent);
  font-size: 14px;
}
section:nth-child(even) h2::before { color: var(--accent2); }

p { color: var(--text); margin-bottom: 12px; }
p:last-child { margin-bottom: 0; }

ul {
  list-style: none;
  padding: 0;
}
ul li {
  padding: 6px 0 6px 20px;
  position: relative;
  color: var(--text);
}
ul li::before {
  content: '→';
  position: absolute;
  left: 0;
  color: var(--accent);
}

/* Contact */
.contact-card {
  background: linear-gradient(135deg, rgba(0,229,255,0.05), rgba(123,47,255,0.05));
  border: 1px solid var(--border);
  padding: 24px 32px;
  margin-top: 60px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 16px;
  flex-wrap: wrap;
}
.contact-card .label {
  font-family: 'Syne', sans-serif;
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--muted);
  margin-bottom: 6px;
}
.contact-card a {
  color: var(--accent);
  text-decoration: none;
  font-size: 15px;
}
.contact-card a:hover { text-decoration: underline; }

footer {
  text-align: center;
  color: var(--muted);
  font-size: 11px;
  letter-spacing: 0.1em;
  margin-top: 60px;
  padding-top: 24px;
  border-top: 1px solid var(--border);
}
```

  </style>
</head>
<body>
<div class="container">
  <header>
    <div class="logo">Harmonix OSINT</div>
    <h1>Conditions<br/><span>d'utilisation</span></h1>
    <p class="meta">Dernière mise à jour : 01 avril 2025 &nbsp;·&nbsp; Version 1.0</p>
  </header>

  <section style="animation-delay:0.05s">
    <div class="section-num">01</div>
    <h2>Présentation</h2>
    <p>Harmonix est un assistant d'investigation OSINT (Open Source Intelligence) développé à des fins éducatives, de recherche en cybersécurité et d'analyse de données publiques. En utilisant ce service, vous acceptez les présentes conditions d'utilisation dans leur intégralité.</p>
  </section>

  <section style="animation-delay:0.1s">
    <div class="section-num">02</div>
    <h2>Utilisation autorisée</h2>
    <p>Vous êtes autorisé à utiliser Harmonix uniquement dans les cadres suivants :</p>
    <ul>
      <li>Recherche académique et éducative en cybersécurité</li>
      <li>Analyse de données accessibles publiquement (OSINT légal)</li>
      <li>Tests de sécurité sur des systèmes dont vous êtes propriétaire ou pour lesquels vous avez une autorisation écrite</li>
      <li>Projets personnels non commerciaux respectant les lois en vigueur</li>
    </ul>
  </section>

  <section style="animation-delay:0.15s">
    <div class="section-num">03</div>
    <h2>Utilisations interdites</h2>
    <p>Il est strictement interdit d'utiliser Harmonix pour :</p>
    <ul>
      <li>Collecter des données personnelles sans consentement explicite</li>
      <li>Harceler, surveiller ou porter atteinte à la vie privée d'individus</li>
      <li>Toute activité illégale selon les lois de votre pays de résidence</li>
      <li>Contourner des mesures de sécurité ou accéder à des systèmes non autorisés</li>
      <li>Revendre, redistribuer ou exploiter commercialement les résultats sans accord préalable</li>
    </ul>
  </section>

  <section style="animation-delay:0.2s">
    <div class="section-num">04</div>
    <h2>Données & API tierces</h2>
    <p>Harmonix peut interagir avec des APIs tierces (TikTok, Google, Hunter.io, IPinfo, etc.) dont vous acceptez également les conditions d'utilisation respectives. Harmonix n'est pas responsable des données fournies par ces services.</p>
    <p>Les données récupérées via ces intégrations sont utilisées uniquement dans le cadre de la requête en cours et ne sont pas stockées de manière permanente sans votre consentement explicite.</p>
  </section>

  <section style="animation-delay:0.25s">
    <div class="section-num">05</div>
    <h2>Responsabilité</h2>
    <p>Harmonix est fourni "tel quel", sans garantie d'aucune sorte. L'utilisateur est seul responsable de l'usage qu'il fait des informations obtenues via le service. Le développeur décline toute responsabilité en cas d'utilisation abusive, illégale ou dommageable.</p>
  </section>

  <section style="animation-delay:0.3s">
    <div class="section-num">06</div>
    <h2>Modifications</h2>
    <p>Ces conditions peuvent être modifiées à tout moment. La date de dernière mise à jour sera toujours indiquée en haut de cette page. La poursuite de l'utilisation du service après modification vaut acceptation des nouvelles conditions.</p>
  </section>

  <div class="contact-card">
    <div>
      <div class="label">Contact</div>
      <a href="mailto:presleyngombolo@gmail.com">presleyngombolo@gmail.com</a>
    </div>
    <div>
      <div class="label">Développeur</div>
      <a href="https://github.com/Presleyngombolo-stack" target="_blank">Presleyngombolo-stack</a>
    </div>
  </div>

  <footer>
    &copy; 2025 Harmonix OSINT · Dakar, Sénégal · Tous droits réservés
  </footer>
</div>
</body>
</html>

<!DOCTYPE html>

<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Harmonix — Politique de confidentialité</title>
  <link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;700;800&family=JetBrains+Mono:wght@300;400&display=swap" rel="stylesheet"/>
  <style>
    :root {
      --bg: #050a0e;
      --surface: #0b1520;
      --accent: #7b2fff;
      --accent2: #00e5ff;
      --text: #c8d8e8;
      --muted: #4a6070;
      --border: #1a2a3a;
    }
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; }
    body {
      background: var(--bg);
      color: var(--text);
      font-family: 'JetBrains Mono', monospace;
      font-size: 14px;
      line-height: 1.8;
      min-height: 100vh;
      overflow-x: hidden;
    }
    body::before {
      content: '';
      position: fixed;
      inset: 0;
      background-image:
        linear-gradient(var(--border) 1px, transparent 1px),
        linear-gradient(90deg, var(--border) 1px, transparent 1px);
      background-size: 40px 40px;
      opacity: 0.4;
      z-index: 0;
      pointer-events: none;
    }
    body::after {
      content: '';
      position: fixed;
      bottom: -200px; right: -200px;
      width: 600px; height: 600px;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(123,47,255,0.06) 0%, transparent 70%);
      z-index: 0;
      pointer-events: none;
    }
    .container {
      position: relative;
      z-index: 1;
      max-width: 860px;
      margin: 0 auto;
      padding: 60px 24px 100px;
    }
    header {
      border-bottom: 1px solid var(--border);
      padding-bottom: 40px;
      margin-bottom: 60px;
    }
    .logo {
      font-family: 'Syne', sans-serif;
      font-size: 13px;
      font-weight: 700;
      letter-spacing: 0.3em;
      text-transform: uppercase;
      color: var(--accent);
      margin-bottom: 32px;
      display: flex;
      align-items: center;
      gap: 10px;
    }
    .logo::before {
      content: '';
      display: inline-block;
      width: 8px; height: 8px;
      background: var(--accent);
      border-radius: 50%;
      box-shadow: 0 0 10px var(--accent);
      animation: pulse 2s infinite;
    }
    @keyframes pulse {
      0%, 100% { opacity: 1; transform: scale(1); }
      50% { opacity: 0.5; transform: scale(0.8); }
    }
    h1 {
      font-family: 'Syne', sans-serif;
      font-size: clamp(32px, 6vw, 56px);
      font-weight: 800;
      line-height: 1.1;
      color: #fff;
      margin-bottom: 16px;
    }
    h1 span {
      color: var(--accent);
      text-shadow: 0 0 30px rgba(123,47,255,0.5);
    }
    .meta {
      color: var(--muted);
      font-size: 12px;
      letter-spacing: 0.1em;
    }
    section {
      margin-bottom: 48px;
      padding: 32px;
      background: var(--surface);
      border: 1px solid var(--border);
      border-left: 3px solid var(--accent);
      position: relative;
      animation: fadeIn 0.5s ease both;
    }
    section:nth-child(even) { border-left-color: var(--accent2); }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(12px); }
      to { opacity: 1; transform: translateY(0); }
    }
    .section-num {
      position: absolute;
      top: 16px; right: 20px;
      font-family: 'Syne', sans-serif;
      font-size: 48px;
      font-weight: 800;
      color: rgba(255,255,255,0.03);
      line-height: 1;
      pointer-events: none;
    }
    h2 {
      font-family: 'Syne', sans-serif;
      font-size: 16px;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.2em;
      color: #fff;
      margin-bottom: 16px;
      display: flex;
      align-items: center;
      gap: 10px;
    }
    h2::before {
      content: '//';
      color: var(--accent);
      font-size: 14px;
    }
    section:nth-child(even) h2::before { color: var(--accent2); }
    p { color: var(--text); margin-bottom: 12px; }
    p:last-child { margin-bottom: 0; }
    ul { list-style: none; padding: 0; }
    ul li {
      padding: 6px 0 6px 20px;
      position: relative;
      color: var(--text);
    }
    ul li::before {
      content: '→';
      position: absolute;
      left: 0;
      color: var(--accent);
    }

```
/* Highlight box */
.highlight {
  background: rgba(123,47,255,0.08);
  border: 1px solid rgba(123,47,255,0.2);
  padding: 16px 20px;
  margin-top: 12px;
  font-size: 13px;
  color: #a0b4c8;
}

.contact-card {
  background: linear-gradient(135deg, rgba(123,47,255,0.05), rgba(0,229,255,0.05));
  border: 1px solid var(--border);
  padding: 24px 32px;
  margin-top: 60px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 16px;
  flex-wrap: wrap;
}
.contact-card .label {
  font-family: 'Syne', sans-serif;
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--muted);
  margin-bottom: 6px;
}
.contact-card a {
  color: var(--accent);
  text-decoration: none;
  font-size: 15px;
}
.contact-card a:hover { text-decoration: underline; }
footer {
  text-align: center;
  color: var(--muted);
  font-size: 11px;
  letter-spacing: 0.1em;
  margin-top: 60px;
  padding-top: 24px;
  border-top: 1px solid var(--border);
}
```

  </style>
</head>
<body>
<div class="container">
  <header>
    <div class="logo">Harmonix OSINT</div>
    <h1>Politique de<br/><span>confidentialité</span></h1>
    <p class="meta">Dernière mise à jour : 01 avril 2025 &nbsp;·&nbsp; Version 1.0</p>
  </header>

  <section style="animation-delay:0.05s">
    <div class="section-num">01</div>
    <h2>Engagement général</h2>
    <p>Harmonix respecte la vie privée de ses utilisateurs. Cette politique décrit quelles données sont collectées, comment elles sont utilisées, et comment vous pouvez exercer vos droits. Nous nous engageons à ne jamais vendre ni partager vos données personnelles à des tiers sans votre consentement explicite.</p>
  </section>

  <section style="animation-delay:0.1s">
    <div class="section-num">02</div>
    <h2>Données collectées</h2>
    <p>Harmonix peut collecter les types de données suivants dans le cadre de son fonctionnement :</p>
    <ul>
      <li>Requêtes de recherche soumises volontairement par l'utilisateur</li>
      <li>Données techniques de session (adresse IP, type de navigateur) à des fins de sécurité</li>
      <li>Informations publiques récupérées via APIs tierces suite à vos requêtes</li>
      <li>Données de compte si vous créez un profil utilisateur</li>
    </ul>
    <div class="highlight">
      ℹ️ Aucune donnée biométrique, aucun contenu privé ni aucune information sensible n'est collectée sans votre accord explicite.
    </div>
  </section>

  <section style="animation-delay:0.15s">
    <div class="section-num">03</div>
    <h2>Intégration TikTok</h2>
    <p>Dans le cadre de l'intégration avec l'API TikTok, Harmonix peut accéder aux données publiques de profils TikTok conformément aux <a href="https://developers.tiktok.com/terms" target="_blank" style="color:var(--accent2)">conditions d'utilisation TikTok for Developers</a>.</p>
    <ul>
      <li>Seules les données publiques accessibles via l'API officielle TikTok sont traitées</li>
      <li>Aucun token d'accès personnel n'est stocké sans chiffrement</li>
      <li>Les données TikTok ne sont pas partagées avec d'autres services</li>
      <li>L'utilisateur peut révoquer l'accès à tout moment</li>
    </ul>
  </section>

  <section style="animation-delay:0.2s">
    <div class="section-num">04</div>
    <h2>Utilisation des données</h2>
    <p>Les données collectées sont utilisées exclusivement pour :</p>
    <ul>
      <li>Fournir les résultats de recherche demandés</li>
      <li>Améliorer les performances et la pertinence du service</li>
      <li>Assurer la sécurité et prévenir les abus</li>
      <li>Générer des rapports d'analyse demandés par l'utilisateur</li>
    </ul>
  </section>

  <section style="animation-delay:0.25s">
    <div class="section-num">05</div>
    <h2>Conservation & suppression</h2>
    <p>Les données de session sont supprimées automatiquement à la fin de la session ou au maximum après 30 jours. Les données de compte sont conservées tant que le compte est actif et supprimées dans les 30 jours suivant une demande de suppression.</p>
    <p>Vous pouvez demander la suppression de vos données à tout moment en nous contactant à l'adresse indiquée ci-dessous.</p>
  </section>

  <section style="animation-delay:0.3s">
    <div class="section-num">06</div>
    <h2>Vos droits</h2>
    <p>Conformément aux principes de protection des données personnelles, vous disposez des droits suivants :</p>
    <ul>
      <li>Droit d'accès à vos données personnelles</li>
      <li>Droit de rectification des données inexactes</li>
      <li>Droit à l'effacement ("droit à l'oubli")</li>
      <li>Droit d'opposition au traitement de vos données</li>
      <li>Droit à la portabilité de vos données</li>
    </ul>
  </section>

  <section style="animation-delay:0.35s">
    <div class="section-num">07</div>
    <h2>Cookies & tracking</h2>
    <p>Harmonix utilise un minimum de cookies techniques indispensables au fonctionnement du service. Aucun cookie publicitaire ou de tracking comportemental n'est déposé sans votre consentement. Vous pouvez configurer votre navigateur pour refuser les cookies à tout moment.</p>
  </section>

  <div class="contact-card">
    <div>
      <div class="label">Contact DPO</div>
      <a href="mailto:presleyngombolo@gmail.com">presleyngombolo@gmail.com</a>
    </div>
    <div>
      <div class="label">Développeur</div>
      <a href="https://github.com/Presleyngombolo-stack" target="_blank">Presleyngombolo-stack</a>
    </div>
    <div>
      <div class="label">Localisation</div>
      <span style="color:var(--text)">Dakar, Sénégal</span>
    </div>
  </div>

  <footer>
    &copy; 2025 Harmonix OSINT · Politique de confidentialité · Tous droits réservés
  </footer>
</div>
</body>
</html>
