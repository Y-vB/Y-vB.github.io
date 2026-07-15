# Y-vB.github.io
<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Comparatif des courtiers — 2026</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,400;0,9..144,600;1,9..144,500&family=Inter:wght@400;500;600&family=IBM+Plex+Mono:wght@400;500&display=swap');

:root{
  --paper: #EEF1E4;
  --paper-deep: #E1E7D3;
  --rule: #C6D0B7;
  --red-rule: #A13D2E;
  --ink: #1E2A20;
  --ink-soft: #4B594B;
  --green-deep: #2C4530;
  --green-mid: #4E7256;
  --gold: #B0801F;
  --white: #FBFAF4;
  --bad: #A13D2E;
  --good: #3E6A45;
}

*{box-sizing:border-box;}
html,body{margin:0;padding:0;}
body{
  background:var(--paper);
  background-image:
    repeating-linear-gradient(var(--paper) 0px, var(--paper) 27px, var(--rule) 28px);
  color:var(--ink);
  font-family:'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
  line-height:1.55;
  padding:0 0 60px;
}

@media (prefers-reduced-motion: reduce){
  *{transition:none !important; animation:none !important;}
}

.page{max-width:980px; margin:0 auto; padding:36px 20px 0;}

/* ---------- MASTHEAD ---------- */
.masthead{
  position:relative;
  background:var(--white);
  border:1px solid var(--rule);
  border-left:5px solid var(--red-rule);
  padding:34px 40px 30px;
  margin-bottom:28px;
  box-shadow:0 2px 0 rgba(30,42,32,0.05);
}
.tab-corner{
  position:absolute;
  top:-14px; right:28px;
  background:var(--red-rule);
  color:var(--white);
  font-family:'IBM Plex Mono', monospace;
  font-size:11px;
  letter-spacing:0.08em;
  padding:6px 14px;
  transform:rotate(1.5deg);
  box-shadow:0 3px 6px rgba(0,0,0,0.15);
}
.eyebrow{
  font-family:'IBM Plex Mono', monospace;
  font-size:12px;
  letter-spacing:0.16em;
  color:var(--gold);
  text-transform:uppercase;
  margin:0 0 10px;
}
h1{
  font-family:'Fraunces', Georgia, serif;
  font-size:clamp(30px, 5vw, 44px);
  font-weight:600;
  margin:0 0 12px;
  color:var(--green-deep);
  letter-spacing:-0.01em;
}
.subtitle{
  font-size:16px;
  color:var(--ink-soft);
  max-width:56ch;
  margin:0;
}

/* ---------- TABS ---------- */
.tabs{
  display:flex;
  gap:4px;
  overflow-x:auto;
  padding:0 4px;
  margin-bottom:0;
  scrollbar-width:thin;
}
.tab{
  font-family:'IBM Plex Mono', monospace;
  font-size:13px;
  white-space:nowrap;
  background:var(--paper-deep);
  color:var(--ink-soft);
  border:1px solid var(--rule);
  border-bottom:none;
  padding:11px 18px 13px;
  cursor:pointer;
  border-radius:8px 8px 0 0;
  position:relative;
  top:1px;
  transition:background 0.15s ease, color 0.15s ease;
}
.tab:hover{ background:#D8E0C8; color:var(--ink); }
.tab.active{
  background:var(--white);
  color:var(--green-deep);
  font-weight:600;
  border-color:var(--rule);
}
.tab.tab-profiles{
  margin-left:auto;
  color:var(--gold);
  border-color:var(--gold);
}
.tab.tab-profiles.active{ background:var(--white); }
.tab:focus-visible{ outline:2px solid var(--gold); outline-offset:2px; }

/* ---------- SHEET / CARD ---------- */
.sheet{
  background:var(--white);
  border:1px solid var(--rule);
  border-top:none;
  padding:0;
  box-shadow:0 3px 0 rgba(30,42,32,0.04);
}
.card{
  display:none;
  padding:36px 40px 40px;
  border-left:5px solid var(--red-rule);
  animation:fadeIn 0.2s ease;
}
.card.active{display:block;}
@keyframes fadeIn{ from{opacity:0;} to{opacity:1;} }

.card .eyebrow-row{
  display:flex;
  align-items:center;
  gap:12px;
  margin-bottom:6px;
}
.card h2{
  font-family:'Fraunces', Georgia, serif;
  font-size:30px;
  font-weight:600;
  margin:0 0 6px;
  color:var(--green-deep);
}
.badge{
  font-family:'IBM Plex Mono', monospace;
  font-size:11px;
  letter-spacing:0.06em;
  text-transform:uppercase;
  padding:4px 10px;
  border-radius:20px;
  border:1px solid var(--rule);
  color:var(--ink-soft);
}
.badge.high{ border-color:var(--good); color:var(--good); }
.badge.mid{ border-color:var(--gold); color:var(--gold); }

.resume{
  font-family:'Fraunces', Georgia, serif;
  font-style:italic;
  font-size:18px;
  color:var(--ink-soft);
  margin:14px 0 26px;
  padding-bottom:20px;
  border-bottom:1px dashed var(--rule);
}

.pros-cons{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:24px;
  margin-bottom:26px;
}
@media (max-width:640px){ .pros-cons{grid-template-columns:1fr;} }
.pc-col h3{
  font-family:'IBM Plex Mono', monospace;
  font-size:12px;
  letter-spacing:0.1em;
  text-transform:uppercase;
  margin:0 0 10px;
}
.pc-col.pros h3{ color:var(--good); }
.pc-col.cons h3{ color:var(--bad); }
.pc-col ul{ list-style:none; margin:0; padding:0; }
.pc-col li{
  position:relative;
  padding:0 0 10px 22px;
  font-size:14.5px;
}
.pc-col.pros li::before{ content:"✓"; position:absolute; left:0; color:var(--good); font-weight:600; }
.pc-col.cons li::before{ content:"✕"; position:absolute; left:0; color:var(--bad); font-weight:600; }

.row{
  display:grid;
  grid-template-columns:150px 1fr;
  gap:18px;
  padding:16px 0;
  border-top:1px solid var(--rule);
  font-size:14.5px;
}
@media (max-width:640px){ .row{grid-template-columns:1fr;} }
.row-label{
  font-family:'IBM Plex Mono', monospace;
  font-size:11.5px;
  letter-spacing:0.08em;
  text-transform:uppercase;
  color:var(--gold);
  padding-top:2px;
}

.profile-fit{
  margin-top:26px;
  background:var(--paper);
  border-left:3px solid var(--gold);
  padding:16px 20px;
  font-size:14.5px;
}
.profile-fit strong{
  display:block;
  font-family:'IBM Plex Mono', monospace;
  font-size:11px;
  letter-spacing:0.08em;
  text-transform:uppercase;
  color:var(--green-deep);
  margin-bottom:6px;
}

/* ---------- PROFILES TAB ---------- */
.profiles-intro{
  font-size:15px;
  color:var(--ink-soft);
  max-width:70ch;
  margin:14px 0 28px;
  padding-bottom:20px;
  border-bottom:1px dashed var(--rule);
}
.matrix{
  width:100%;
  border-collapse:collapse;
  font-size:13.5px;
}
.matrix th, .matrix td{
  border:1px solid var(--rule);
  padding:14px;
  vertical-align:top;
  text-align:left;
}
.matrix thead th{
  background:var(--green-deep);
  color:var(--white);
  font-family:'IBM Plex Mono', monospace;
  font-size:11.5px;
  letter-spacing:0.06em;
  text-transform:uppercase;
  font-weight:500;
}
.matrix tbody th{
  background:var(--paper-deep);
  font-family:'IBM Plex Mono', monospace;
  font-size:11.5px;
  letter-spacing:0.05em;
  text-transform:uppercase;
  color:var(--green-deep);
  width:150px;
}
.matrix td strong{ display:block; color:var(--green-deep); margin-bottom:5px; font-size:14px; }
.matrix-wrap{ overflow-x:auto; }
@media (max-width:720px){ .matrix{font-size:12.5px;} .matrix th, .matrix td{padding:10px;} }

.cross-note{
  margin-top:26px;
  background:var(--paper);
  border-left:3px solid var(--red-rule);
  padding:16px 20px;
  font-size:14.5px;
}
.cross-note strong{
  display:block;
  font-family:'IBM Plex Mono', monospace;
  font-size:11px;
  letter-spacing:0.08em;
  text-transform:uppercase;
  color:var(--red-rule);
  margin-bottom:6px;
}

/* ---------- FOOTER ---------- */
.fineprint{
  max-width:980px;
  margin:22px auto 0;
  padding:0 24px;
  font-size:12px;
  color:var(--ink-soft);
  font-family:'IBM Plex Mono', monospace;
  line-height:1.6;
}
</style>
</head>
<body>
<div class="page">

  <header class="masthead">
    <p class="eyebrow">Juillet 2026</p>
    <h1>Comparatif des courtiers</h1>
    <p class="subtitle">Huit plateformes d'investissement passées au crible, poste par poste - fiabilité, avantages, inconvénients, rentabilité, frais et outils disponibles. Un onglet par plateforme, un onglet comparatif selon le profil.</p>
  </header>

  <nav class="tabs" id="tabs">
    <button class="tab active" data-tab="tr">Trade Republic</button>
    <button class="tab" data-tab="ibkr">Interactive Brokers</button>
    <button class="tab" data-tab="degiro">DEGIRO</button>
    <button class="tab" data-tab="xtb">XTB</button>
    <button class="tab" data-tab="etoro">eToro</button>
    <button class="tab" data-tab="bourso">BoursoBank</button>
    <button class="tab" data-tab="fortuneo">Fortuneo</button>
    <button class="tab" data-tab="revolut">Revolut</button>
    <button class="tab tab-profiles" data-tab="profiles">Profils</button>
  </nav>

  <main class="sheet">

    <!-- TRADE REPUBLIC -->
    <section class="card active" id="tr">
      <div class="eyebrow-row"><span class="badge mid">Fiabilité correcte</span></div>
      <h2>Trade Republic</h2>
      <p class="resume">Le néo-courtier allemand devenu banque : simplicité radicale, 1 € par ordre, et depuis 2026 un PEA sans frais pensé pour l'investisseur passif en DCA.</p>

      <div class="pros-cons">
        <div class="pc-col pros">
          <h3>Avantages</h3>
          <ul>
            <li>1 € par ordre ponctuel, plans d'investissement programmés gratuits</li>
            <li>PEA sans frais sur les versements, plafond 150 000 €</li>
            <li>IBAN français, carte Visa avec 1 % de cashback réinvesti</li>
            <li>Rémunération du cash non investi (~2,25-3 %/an)</li>
            <li>Pas de frais de garde ni d'inactivité</li>
          </ul>
        </div>
        <div class="pc-col cons">
          <h3>Inconvénients</h3>
          <ul>
            <li>25 € par ligne pour un transfert de titres sortant</li>
            <li>Spread caché en plus du 1 € affiché</li>
            <li>Pas de fonds traditionnels, d'options ni de futures</li>
            <li>Service client historiquement faible (amélioré depuis avril 2026)</li>
          </ul>
        </div>
      </div>

      <div class="row">
        <div class="row-label">Fiabilité</div>
        <div>Entreprise d'investissement allemande régulée par la Bundesbank et la BaFin. Espèces chez SolarisBank, titres conservés chez HSBC. Depuis la fin du PFOF (30 juin 2026), Trade Republic exécute lui-même les ordres comme teneur de marché.</div>
      </div>
      <div class="row">
        <div class="row-label">Rentabilité</div>
        <div>L'outil ne rend rien rentable en soi : la performance dépend des ETF/actions choisis. Sa valeur ajoutée est de préserver le rendement net grâce à des frais très bas, surtout en investissement régulier.</div>
      </div>
      <div class="row">
        <div class="row-label">Frais</div>
        <div>1 € par ordre ponctuel · 0 € sur les plans programmés · 25 € par ligne en cas de transfert sortant.</div>
      </div>
      <div class="row">
        <div class="row-label">Outils</div>
        <div>Application mobile, nouvelle interface web (juillet 2026) avec Best Price et Direct Price, pas d'options ni de futures.</div>
      </div>

      <div class="profile-fit">
        <strong>Profil correspondant</strong>
        Idéal pour un petit à moyen budget (50-300 €/mois) qui veut investir en quelques minutes par mois, sans s'occuper de la gestion. Moins pertinent au-delà d'un patrimoine conséquent ou pour un usage actif exigeant.
      </div>
    </section>

    <!-- INTERACTIVE BROKERS -->
    <section class="card" id="ibkr">
      <div class="eyebrow-row"><span class="badge high">Fiabilité élevée</span></div>
      <h2>Interactive Brokers</h2>
      <p class="resume">Le courtier des professionnels : le plus complet et souvent le moins cher du marché, mais une plateforme pensée pour des utilisateurs déjà à l'aise avec la bourse.</p>

      <div class="pros-cons">
        <div class="pc-col pros">
          <h3>Avantages</h3>
          <ul>
            <li>Frais parmi les plus bas du marché, y compris pour les gros volumes</li>
            <li>Accès à 150+ marchés dans le monde (actions, options, futures, obligations, forex)</li>
            <li>PEA et CTO disponibles, transfert de titres entrant gratuit</li>
            <li>Rémunération du cash attractive en EUR et USD</li>
          </ul>
        </div>
        <div class="pc-col cons">
          <h3>Inconvénients</h3>
          <ul>
            <li>Interface (Trader Workstation) puissante mais intimidante pour un débutant</li>
            <li>Frais minimum par ordre qui pénalisent les petits montants (&lt;10 000 €)</li>
            <li>Pas d'IFU sur le CTO : déclaration fiscale française à faire soi-même</li>
            <li>Service client majoritairement anglophone, horaires limités</li>
          </ul>
        </div>
      </div>

      <div class="row">
        <div class="row-label">Fiabilité</div>
        <div>Fondé en 1977, coté au S&P 500 depuis août 2025. Les clients européens sont rattachés à Interactive Brokers Ireland Limited, régulée par la Banque centrale d'Irlande. Plus de 4,6 millions de clients, 820 Md$ d'actifs gérés.</div>
      </div>
      <div class="row">
        <div class="row-label">Rentabilité</div>
        <div>La structure tarifaire ne devient vraiment avantageuse qu'à partir d'un certain volume d'ordres. Pas conçu pour du DCA à 50-100 €/mois, mais très efficace pour un portefeuille conséquent ou diversifié à l'international.</div>
      </div>
      <div class="row">
        <div class="row-label">Frais</div>
        <div>Tarification fixe ou dégressive selon le volume mensuel ; par exemple environ 3 € pour acheter 1 000 € d'un ETF S&P 500. Retrait gratuit une fois par mois, puis 1 € par retrait SEPA supplémentaire.</div>
      </div>
      <div class="row">
        <div class="row-label">Outils</div>
        <div>Trader Workstation, IBKR Desktop/Mobile/WebTrader, API complète, plus de 100 types d'ordres, scanners de marché et outils de gestion du risque avancés.</div>
      </div>

      <div class="profile-fit">
        <strong>Profil correspondant</strong>
        Pensé pour l'investisseur autonome et expérimenté, avec un capital suffisant pour rentabiliser la structure de frais et le temps disponible pour apprivoiser la plateforme. Moins adapté à un débutant pressé ou à un tout petit portefeuille.
      </div>
    </section>

    <!-- DEGIRO -->
    <section class="card" id="degiro">
      <div class="eyebrow-row"><span class="badge high">Fiabilité élevée</span></div>
      <h2>DEGIRO</h2>
      <p class="resume">Le courtier néerlandais réputé pour ses frais parmi les plus bas d'Europe et son univers d'investissement très large — mais sans PEA.</p>

      <div class="pros-cons">
        <div class="pc-col pros">
          <h3>Avantages</h3>
          <ul>
            <li>Frais de courtage très bas (1-2 € + petite commission variable)</li>
            <li>Aucun frais de garde ni d'inactivité</li>
            <li>Sélection d'ETF accessibles sans frais de courtage</li>
            <li>Univers large : actions, ETF, obligations, options, futures, warrants</li>
          </ul>
        </div>
        <div class="pc-col cons">
          <h3>Inconvénients</h3>
          <ul>
            <li>Pas de PEA ni d'assurance-vie : uniquement un compte-titres ordinaire</li>
            <li>Pas de plan d'investissement automatisé (DCA)</li>
            <li>Pas d'IFU : déclaration fiscale française manuelle</li>
            <li>Ne rémunère pas les liquidités non investies</li>
            <li>10 € par ligne au-delà des 10 premières lignes transférées gratuitement</li>
          </ul>
        </div>
      </div>

      <div class="row">
        <div class="row-label">Fiabilité</div>
        <div>Membre du groupe allemand flatexDEGIRO Bank AG, régulé par la BaFin, avec une succursale néerlandaise supervisée par l'AFM et la DNB. Plus de 3,5 millions de clients, séparation stricte entre les actifs des clients et ceux de l'entreprise.</div>
      </div>
      <div class="row">
        <div class="row-label">Rentabilité</div>
        <div>Très efficace pour une gestion indicielle en direct sur un compte-titres, mais moins optimisé fiscalement qu'un PEA pour un résident français qui vise des ETF européens sur le long terme.</div>
      </div>
      <div class="row">
        <div class="row-label">Frais</div>
        <div>Environ 1-2 € par ordre selon la place boursière, plus une commission variable ; frais de change de 0,25 % ; 10 € par ligne transférée au-delà du seuil gratuit.</div>
      </div>
      <div class="row">
        <div class="row-label">Outils</div>
        <div>Plateforme web et mobile claire, ordres stop loss disponibles, pas de CFD ni de forex — donc pas orienté trading spéculatif de court terme.</div>
      </div>

      <div class="profile-fit">
        <strong>Profil correspondant</strong>
        Bon choix pour un investisseur autonome qui construit un portefeuille diversifié d'actions et d'ETF en compte-titres, à condition de ne pas avoir besoin d'un PEA ou d'automatisation complète.
      </div>
    </section>

    <!-- XTB -->
    <section class="card" id="xtb">
      <div class="eyebrow-row"><span class="badge mid">Fiabilité correcte</span></div>
      <h2>XTB</h2>
      <p class="resume">Courtier polonais coté en bourse, passé du tout-CFD au multi-actifs, avec un PEA lancé en 2025 à 0 % de commission jusqu'à 100 000 € de volume mensuel.</p>

      <div class="pros-cons">
        <div class="pc-col pros">
          <h3>Avantages</h3>
          <ul>
            <li>0 % de commission sur actions/ETF jusqu'à 100 000 €/mois (CTO et PEA)</li>
            <li>Aucun frais de garde, dépôt possible dès 1 €</li>
            <li>Service client francophone réactif, avec gestionnaire dédié</li>
            <li>Groupe coté en bourse, résultats financiers publics</li>
          </ul>
        </div>
        <div class="pc-col cons">
          <h3>Inconvénients</h3>
          <ul>
            <li>Pas de transfert de PEA entrant possible en 2026</li>
            <li>Pas de plan d'investissement programmé (DCA) automatisé</li>
            <li>Frais de change ~0,5 % hors euro</li>
            <li>Frais d'inactivité de 10 €/mois après 365 jours sans transaction</li>
            <li>Le "0 €" repose sur les revenus CFD/Forex du groupe, donc pas gravé dans le marbre</li>
          </ul>
        </div>
      </div>

      <div class="row">
        <div class="row-label">Fiabilité</div>
        <div>Coté à la Bourse de Varsovie depuis 2016, régulé par la KNF polonaise et contrôlé par l'AMF en France. Fonds ségrégués chez BNP Paribas. Protection investisseur plafonnée à 20 100 €, plus faible que chez Trade Republic ou DEGIRO.</div>
      </div>
      <div class="row">
        <div class="row-label">Rentabilité</div>
        <div>Mathématiquement optimal pour un premier PEA 100 % ETF en euros à petit ou moyen budget : sur 10 ans, l'absence de commission peut représenter une économie substantielle. Moins pertinent pour un patrimoine déjà installé ailleurs (pas de transfert entrant).</div>
      </div>
      <div class="row">
        <div class="row-label">Frais</div>
        <div>0 % jusqu'à 100 000 €/mois, puis 0,2 % (minimum 10 €) ; change ~0,5 % hors euro ; inactivité 10 €/mois après un an sans mouvement.</div>
      </div>
      <div class="row">
        <div class="row-label">Outils</div>
        <div>Plateforme propriétaire xStation 5 (web, desktop, mobile), eWallet et carte de débit associée ; pas d'obligations ni de produits dérivés sur le PEA.</div>
      </div>

      <div class="profile-fit">
        <strong>Profil correspondant</strong>
        Très pertinent pour ouvrir un premier PEA 100 % ETF avec un budget modeste, à condition de ne rien avoir à transférer et d'être discipliné sur des versements réguliers manuels.
      </div>
    </section>

    <!-- ETORO -->
    <section class="card" id="etoro">
      <div class="eyebrow-row"><span class="badge mid">Fiabilité correcte</span></div>
      <h2>eToro</h2>
      <p class="resume">Le pionnier du trading social : interface ludique, CopyTrading, et univers multi-actifs (actions, ETF, cryptos, CFD) — mais pas de PEA et un service client en retrait.</p>

      <div class="pros-cons">
        <div class="pc-col pros">
          <h3>Avantages</h3>
          <ul>
            <li>0 % de commission sur les actions et ETF au comptant</li>
            <li>CopyTrader : reproduire automatiquement les positions d'autres investisseurs</li>
            <li>Interface moderne et sociale, très accessible aux débutants</li>
            <li>Large gamme d'actifs : actions, ETF, cryptos, CFD, forex, matières premières</li>
            <li>Assurance-vie et PER disponibles pour l'optimisation fiscale long terme</li>
          </ul>
        </div>
        <div class="pc-col cons">
          <h3>Inconvénients</h3>
          <ul>
            <li>Pas de PEA</li>
            <li>Frais de retrait (~5 $) et frais de change (tout est en USD)</li>
            <li>Spreads sur les CFD, et 52-61 % des comptes CFD perdent de l'argent</li>
            <li>Service client identifié comme point faible récurrent</li>
            <li>Le CopyTrading n'est pas une garantie de performance</li>
          </ul>
        </div>
      </div>

      <div class="row">
        <div class="row-label">Fiabilité</div>
        <div>Fondé en 2007, régulé par la CySEC chypriote et la FCA britannique, enregistré PSAN auprès de l'AMF en France. Comptes ségrégués avec garanties sur les dépôts (100 000 €) et les titres (20 000 €). Note Trustpilot autour de 4,2-4,3/5, mais 21 % d'avis 1 étoile.</div>
      </div>
      <div class="row">
        <div class="row-label">Rentabilité</div>
        <div>La partie actions/ETF au comptant est la plus saine de l'offre. Le CopyTrading peut aider un débutant à observer des stratégies, mais n'élimine pas le risque ; les CFD, statistiquement, font perdre de l'argent à la majorité des utilisateurs.</div>
      </div>
      <div class="row">
        <div class="row-label">Frais</div>
        <div>0 € de commission sur actions/ETF au comptant ; ~5 $ par retrait ; frais de change ~0,5-1,5 % selon devise ; spreads variables sur les CFD.</div>
      </div>
      <div class="row">
        <div class="row-label">Outils</div>
        <div>Application et interface web modernes, graphiques TradingView intégrés, CopyPortfolios thématiques ; pas d'options ou de futures classiques (hors CFD).</div>
      </div>

      <div class="profile-fit">
        <strong>Profil correspondant</strong>
        Convient à un débutant curieux du trading social ou multi-actifs, à condition de rester sur les actions/ETF au comptant et de garder ses distances avec les CFD à effet de levier.
      </div>
    </section>

    <!-- BOURSOBANK -->
    <section class="card" id="bourso">
      <div class="eyebrow-row"><span class="badge high">Fiabilité élevée</span></div>
      <h2>BoursoBank</h2>
      <p class="resume">La banque en ligne française la plus utilisée : un écosystème complet (banque + bourse + assurance-vie) adossé à la Société Générale, au prix de frais de courtage moins compétitifs.</p>

      <div class="pros-cons">
        <div class="pc-col pros">
          <h3>Avantages</h3>
          <ul>
            <li>Écosystème complet : compte courant, PEA, CTO, assurance-vie, PER au même endroit</li>
            <li>Interface pédagogique, bien adaptée aux débutants</li>
            <li>Boursomarkets : ETF partenaires (iShares) à commission réduite au-delà de 500 €</li>
            <li>Garanties de protection des moyens de paiement incluses</li>
          </ul>
        </div>
        <div class="pc-col cons">
          <h3>Inconvénients</h3>
          <ul>
            <li>Frais de courtage plus élevés que les courtiers spécialisés</li>
            <li>Montant minimum d'ordre relevé (jusqu'à 500 € sur certains produits en 2026)</li>
            <li>Frais d'inactivité de 5,95 €/mois sur certaines formules</li>
            <li>Grille tarifaire qui évolue fréquemment</li>
          </ul>
        </div>
      </div>

      <div class="row">
        <div class="row-label">Fiabilité</div>
        <div>Filiale à 100 % de la Société Générale, régulée par l'ACPR et l'AMF. Plus de 8 millions de clients, infrastructure institutionnelle solide et rassurante.</div>
      </div>
      <div class="row">
        <div class="row-label">Rentabilité</div>
        <div>Pertinent si la centralisation bancaire compte plus que l'optimisation pure des frais de courtage. Pour un investisseur qui cherche avant tout à minimiser les frais, Fortuneo ou un courtier spécialisé feront mieux à stratégie équivalente.</div>
      </div>
      <div class="row">
        <div class="row-label">Frais</div>
        <div>Par exemple 9,98 à 33,30 € pour 2 ordres de 1 000 € sur le PEA (hors Boursomarkets) ; 5,95 €/mois d'inactivité selon la formule choisie.</div>
      </div>
      <div class="row">
        <div class="row-label">Outils</div>
        <div>Interface complète avec actualités et outils d'analyse intégrés, gestion profilée disponible sur le PEA, conseillers accessibles par téléphone.</div>
      </div>

      <div class="profile-fit">
        <strong>Profil correspondant</strong>
        Adapté à qui veut tout centraliser dans une seule banque (compte courant, PEA, assurance-vie) et accepte de payer un peu plus cher le confort et l'accompagnement.
      </div>
    </section>

    <!-- FORTUNEO -->
    <section class="card" id="fortuneo">
      <div class="eyebrow-row"><span class="badge high">Fiabilité élevée</span></div>
      <h2>Fortuneo</h2>
      <p class="resume">Banque en ligne du Crédit Mutuel Arkéa, référence pour un PEA à frais compétitifs et bien pensé pour l'investissement régulier en douceur.</p>

      <div class="pros-cons">
        <div class="pc-col pros">
          <h3>Avantages</h3>
          <ul>
            <li>1er ordre du mois gratuit si le montant est ≤ 500 €</li>
            <li>0,35 % par ordre ensuite, sans frais fixe</li>
            <li>Aucun frais de garde ni d'inactivité</li>
            <li>Gestion pilotée disponible sur le PEA (3 profils de risque)</li>
            <li>Nominatif administré gratuit</li>
          </ul>
        </div>
        <div class="pc-col cons">
          <h3>Inconvénients</h3>
          <ul>
            <li>Interface plus sobre, moins moderne que les néo-courtiers</li>
            <li>Pas de plan d'investissement automatisé façon Trade Republic</li>
            <li>Frais de change à surveiller (J+1 + 0,12 % depuis mars 2025)</li>
          </ul>
        </div>
      </div>

      <div class="row">
        <div class="row-label">Fiabilité</div>
        <div>Filiale du Crédit Mutuel Arkéa, régulée par l'ACPR et l'AMF. Plus de 1,4 million de clients, réputation stable dans la durée et grille tarifaire jugée plus prévisible que celle de certains concurrents.</div>
      </div>
      <div class="row">
        <div class="row-label">Rentabilité</div>
        <div>Très efficace pour un investisseur régulier à budget modéré (jusqu'à 500 €/mois sans frais), et reste compétitif sur les gros ordres via la formule Pro (0,10 % au-delà de 10 000 €).</div>
      </div>
      <div class="row">
        <div class="row-label">Frais</div>
        <div>Gratuit pour le 1er ordre du mois (≤ 500 €), puis 0,35 % par ordre (ou 0,10 % en formule Pro) ; pas de frais de garde ni d'inactivité.</div>
      </div>
      <div class="row">
        <div class="row-label">Outils</div>
        <div>Interface web et mobile classique, OPCVM disponibles (dont une sélection sans frais d'entrée), gestion pilotée sur PEA.</div>
      </div>

      <div class="profile-fit">
        <strong>Profil correspondant</strong>
        Excellent choix pour investir en douceur chaque mois dans un PEA, avec un bon équilibre frais/simplicité, sans dépendre d'un néo-courtier étranger.
      </div>
    </section>

    <!-- REVOLUT -->
    <section class="card" id="revolut">
      <div class="eyebrow-row"><span class="badge mid">Fiabilité correcte</span></div>
      <h2>Revolut</h2>
      <p class="resume">Néobanque multi-devises avec un volet investissement intégré : pratique pour tout centraliser dans une seule app, mais pas pensée en priorité pour l'investisseur français de long terme.</p>

      <div class="pros-cons">
        <div class="pc-col pros">
          <h3>Avantages</h3>
          <ul>
            <li>Investir dès 1 € en fractions d'actions et d'ETF</li>
            <li>Ordres gratuits inclus selon l'abonnement (1 à 10 par mois)</li>
            <li>Pas de frais de change sur les investissements en eux-mêmes</li>
            <li>Tout centralisé avec le compte courant et les cartes multidevises</li>
          </ul>
        </div>
        <div class="pc-col cons">
          <h3>Inconvénients</h3>
          <ul>
            <li>Pas de PEA : uniquement un compte-titres, flat tax de 30 % sans abattement</li>
            <li>Pas d'IFU français : calcul et déclaration des plus-values à faire soi-même</li>
            <li>Catalogue plus restreint qu'un courtier spécialisé (environ 150-500 ETF)</li>
            <li>Outils de gestion du risque basiques (pas de stop loss sur actions/ETF)</li>
          </ul>
        </div>
      </div>

      <div class="row">
        <div class="row-label">Fiabilité</div>
        <div>Les services d'investissement sont fournis par Revolut Securities Europe UAB, régulée par la Banque de Lituanie (MiFID II) ; les services bancaires relèvent d'une entité distincte, Revolut Bank UAB. Note Trustpilot autour de 4,2/5.</div>
      </div>
      <div class="row">
        <div class="row-label">Rentabilité</div>
        <div>Pratique pour débuter ou investir de petits montants ponctuels, mais pour une stratégie ETF de long terme, un PEA ouvert ailleurs sera fiscalement plus avantageux après 5 ans, à supports comparables.</div>
      </div>
      <div class="row">
        <div class="row-label">Frais</div>
        <div>Quota d'ordres gratuits selon l'abonnement (Standard : 1, Plus : 3, Premium : 5, Metal/Ultra : 10), puis environ 1 € ou 0,25 % (minimum 1 €) par ordre ; option Trading Pro à partir de 4,99 €/mois.</div>
      </div>
      <div class="row">
        <div class="row-label">Outils</div>
        <div>Application unique tout-en-un (paiements, cryptos, investissement), plans d'investissement automatisés disponibles ; pas de compte démo ni d'effet de levier sur actions/ETF.</div>
      </div>

      <div class="profile-fit">
        <strong>Profil correspondant</strong>
        Utile en complément d'un compte principal pour investir occasionnellement de petits montants depuis une app déjà installée, plutôt que comme outil unique d'une stratégie long terme.
      </div>
    </section>

    <!-- PROFILES -->
    <section class="card" id="profiles">
      <div class="eyebrow-row"><span class="badge mid">Grille de lecture</span></div>
      <h2>Selon votre profil</h2>
      <p class="profiles-intro">Deux critères pour orienter le choix : combien vous investissez (et à quelle fréquence), et combien de temps vous êtes prêt à y consacrer. Le tableau croise 3 profils financiers et 3 profils de temps, avec une recommandation d'outil par case.</p>

      <div class="matrix-wrap">
        <table class="matrix">
          <thead>
            <tr>
              <th>Profil financier ↓ / Temps →</th>
              <th>Quelques minutes/mois</th>
              <th>Quelques heures/mois</th>
              <th>Plusieurs heures/semaine</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <th>Petit capital<br>(&lt; 100 €/mois ou &lt; 5 000 €)</th>
              <td><strong>Trade Republic ou XTB</strong>PEA sans frais, DCA quasi gratuit, aucune gestion active nécessaire.</td>
              <td><strong>Fortuneo</strong>1er ordre gratuit chaque mois, un peu plus de choix pour arbitrer manuellement.</td>
              <td><strong>eToro (prudence)</strong>CopyTrading pour apprendre, mais rester sur les actions/ETF au comptant plutôt que les CFD.</td>
            </tr>
            <tr>
              <th>Capital intermédiaire<br>(quelques centaines à quelques milliers €/mois, 5-50 k€)</th>
              <td><strong>Trade Republic, XTB ou DEGIRO</strong>Automatisation ou univers large selon l'enveloppe recherchée (PEA vs CTO).</td>
              <td><strong>BoursoBank, Fortuneo ou DEGIRO</strong>Écosystème bancaire complet ou univers d'actifs plus large pour arbitrer.</td>
              <td><strong>DEGIRO ou Interactive Brokers</strong>Bascule progressive vers plus d'outils si la stratégie devient plus active.</td>
            </tr>
            <tr>
              <th>Capital important<br>(&gt; 50-100 k€, approche patrimoniale)</th>
              <td><strong>Fortuneo ou BoursoBank</strong>PEA établi + diversification d'enveloppes (assurance-vie) en complément.</td>
              <td><strong>Interactive Brokers</strong>PEA et CTO, frais dégressifs avantageux au volume, univers mondial.</td>
              <td><strong>Interactive Brokers</strong>Seul outil vraiment dimensionné : options, futures, 150+ marchés, outils professionnels.</td>
            </tr>
          </tbody>
        </table>
      </div>

      <div class="cross-note">
        <strong>Lecture croisée</strong>
        Le combo le plus favorable à un néo-courtier comme Trade Republic ou XTB reste petit-à-moyen budget associé à peu de temps disponible. Plus le capital ou le temps consacré augmente vers des besoins sophistiqués, plus il devient pertinent de regarder vers des courtiers plus complets (DEGIRO, Interactive Brokers) ou de combiner plusieurs outils, plutôt que de forcer un seul outil à couvrir un usage pour lequel il n'est pas taillé.
      </div>
    </section>

  </main>

  <p class="fineprint">Comparatif informatif basé sur des données publiques disponibles en juillet 2026 ; les grilles tarifaires et conditions évoluent régulièrement, à revérifier avant toute décision.</p>

</div>

<script>
  const tabs = document.querySelectorAll('.tab');
  const cards = document.querySelectorAll('.card');
  tabs.forEach(tab => {
    tab.addEventListener('click', () => {
      tabs.forEach(t => t.classList.remove('active'));
      cards.forEach(c => c.classList.remove('active'));
      tab.classList.add('active');
      document.getElementById(tab.dataset.tab).classList.add('active');
    });
  });
</script>
</body>
</html>
