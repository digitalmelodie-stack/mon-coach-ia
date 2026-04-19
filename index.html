<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Coach IA — Lancement de Cohorte</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,700;0,800;1,700&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg:     #0D0D14;
    --bg2:    #13131E;
    --bg3:    #1A1A2A;
    --card:   #1C1C2E;
    --vio:    #5B3F9A;
    --vio-m:  #7B5FBA;
    --vio-p:  #4A3580;
    --vio-b:  #6B4FB0;
    --text:   #EEEAF5;
    --muted:  #7A748A;
    --sub:    #B0AABF;
    --border: rgba(255,255,255,0.07);
    --bv:     rgba(91,63,154,0.35);
  }

  html, body { height: 100%; }
  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--bg);
    color: var(--text);
    min-height: 100vh;
    display: flex;
    flex-direction: column;
  }

  /* ── ÉCRAN EXPIRÉ ── */
  #expired-screen {
    display: none;
    flex: 1;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    padding: 3rem 2rem;
    background: var(--bg);
  }
  #expired-screen.show { display: flex; }
  .expired-icon { font-size: 3rem; margin-bottom: 1.5rem; opacity: .6; }
  .expired-title {
    font-family: 'Playfair Display', serif;
    font-size: 2rem; font-weight: 700;
    margin-bottom: .75rem;
    color: var(--text);
  }
  .expired-sub { font-size: .95rem; color: var(--sub); line-height: 1.7; max-width: 380px; margin: 0 auto 2rem; }
  .expired-btn {
    display: inline-flex; align-items: center; gap: 8px;
    background: var(--vio); color: #fff;
    font-size: .88rem; font-weight: 500; letter-spacing: .03em;
    padding: .85rem 2rem; border-radius: 100px;
    text-decoration: none; transition: background .2s;
  }
  .expired-btn:hover { background: var(--vio-m); }

  /* ── APP SHELL ── */
  #app { display: flex; flex-direction: column; flex: 1; max-height: 100vh; }

  /* ── HEADER ── */
  .header {
    background: var(--bg2);
    border-bottom: 1px solid var(--border);
    padding: .9rem 1.5rem;
    display: flex; align-items: center; gap: .9rem;
    flex-shrink: 0;
  }
  .h-avatar {
    width: 38px; height: 38px; border-radius: 50%;
    background: var(--vio-p); border: 1px solid var(--vio-b);
    display: flex; align-items: center; justify-content: center;
    font-family: 'Playfair Display', serif;
    font-size: 1rem; font-weight: 700; color: #D4C8FF;
    flex-shrink: 0;
  }
  .h-info { flex: 1; }
  .h-name { font-size: .92rem; font-weight: 500; color: var(--text); }
  .h-sub  { font-size: .75rem; color: var(--muted); }
  .h-timer {
    display: flex; align-items: center; gap: .4rem;
    background: rgba(91,63,154,0.15);
    border: 1px solid var(--bv);
    border-radius: 100px;
    padding: .3rem .85rem;
    font-size: .72rem; font-weight: 500;
    color: #B8A8E8;
    flex-shrink: 0;
  }
  .timer-dot {
    width: 6px; height: 6px; border-radius: 50%;
    background: #1D9E75;
    animation: pulse 2s infinite;
  }
  @keyframes pulse { 0%,100%{opacity:1} 50%{opacity:.4} }

  /* ── MESSAGES ── */
  .messages {
    flex: 1;
    overflow-y: auto;
    padding: 1.5rem;
    display: flex;
    flex-direction: column;
    gap: 1rem;
    scroll-behavior: smooth;
  }
  .messages::-webkit-scrollbar { width: 4px; }
  .messages::-webkit-scrollbar-track { background: transparent; }
  .messages::-webkit-scrollbar-thumb { background: rgba(255,255,255,.1); border-radius: 2px; }

  .msg { display: flex; gap: .6rem; align-items: flex-end; max-width: 82%; animation: msgIn .3s ease both; }
  @keyframes msgIn { from{opacity:0;transform:translateY(8px)} to{opacity:1;transform:translateY(0)} }
  .msg.bot { align-self: flex-start; }
  .msg.user { align-self: flex-end; flex-direction: row-reverse; }

  .m-avatar {
    width: 28px; height: 28px; border-radius: 50%;
    background: var(--vio-p); border: 1px solid var(--vio-b);
    display: flex; align-items: center; justify-content: center;
    font-family: 'Playfair Display', serif;
    font-size: .75rem; font-weight: 700; color: #D4C8FF;
    flex-shrink: 0;
  }

  .bubble {
    padding: .7rem 1rem;
    border-radius: 16px;
    font-size: .875rem;
    line-height: 1.6;
    white-space: pre-wrap;
  }
  .msg.bot  .bubble {
    background: var(--card);
    border: 1px solid var(--border);
    color: var(--sub);
    border-bottom-left-radius: 4px;
  }
  .msg.user .bubble {
    background: var(--vio-p);
    color: #EEE8FF;
    border-bottom-right-radius: 4px;
    border: 1px solid var(--vio-b);
  }
  .bubble strong { color: var(--text); font-weight: 500; }

  /* TYPING */
  .typing-bubble {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 16px;
    border-bottom-left-radius: 4px;
    padding: .7rem 1rem;
    display: flex; gap: 4px; align-items: center;
  }
  .typing-bubble span {
    width: 7px; height: 7px; border-radius: 50%;
    background: var(--vio-m);
    animation: blink 1.2s infinite;
  }
  .typing-bubble span:nth-child(2) { animation-delay: .2s; }
  .typing-bubble span:nth-child(3) { animation-delay: .4s; }
  @keyframes blink { 0%,100%{opacity:.2} 50%{opacity:1} }

  /* ── SUGGESTIONS ── */
  .suggestions {
    padding: .6rem 1.5rem;
    display: flex; gap: .5rem; flex-wrap: wrap;
    border-top: 1px solid var(--border);
    background: var(--bg);
    flex-shrink: 0;
  }
  .chip {
    font-size: .75rem; padding: .35rem .85rem;
    border-radius: 100px;
    border: 1px solid var(--bv);
    background: rgba(74,53,128,0.15);
    color: #9B7FD0;
    cursor: pointer; white-space: nowrap;
    transition: background .2s, color .2s;
    font-family: 'DM Sans', sans-serif;
  }
  .chip:hover { background: rgba(91,63,154,0.3); color: #D4C8FF; }

  /* ── INPUT ── */
  .input-bar {
    padding: 1rem 1.5rem;
    background: var(--bg2);
    border-top: 1px solid var(--border);
    display: flex; gap: .75rem; align-items: flex-end;
    flex-shrink: 0;
  }
  .input-wrap { flex: 1; position: relative; }
  textarea {
    width: 100%;
    background: var(--bg3);
    border: 1px solid var(--border);
    border-radius: 14px;
    padding: .75rem 1rem;
    font-family: 'DM Sans', sans-serif;
    font-size: .875rem;
    color: var(--text);
    resize: none;
    min-height: 48px;
    max-height: 140px;
    line-height: 1.5;
    transition: border-color .2s;
    outline: none;
  }
  textarea::placeholder { color: var(--muted); }
  textarea:focus { border-color: var(--bv); }
  .send-btn {
    width: 44px; height: 44px; border-radius: 12px;
    background: var(--vio); border: none;
    display: flex; align-items: center; justify-content: center;
    cursor: pointer; flex-shrink: 0;
    transition: background .2s, transform .15s;
  }
  .send-btn:hover { background: var(--vio-m); }
  .send-btn:active { transform: scale(.95); }
  .send-btn:disabled { opacity: .4; cursor: default; }
  .send-btn svg { pointer-events: none; }

  /* ── LIMIT BAR ── */
  .limit-bar {
    padding: .4rem 1.5rem;
    background: var(--bg);
    display: flex; align-items: center; gap: .75rem;
    flex-shrink: 0;
  }
  .limit-track {
    flex: 1; height: 3px;
    background: rgba(255,255,255,0.08);
    border-radius: 2px; overflow: hidden;
  }
  .limit-fill {
    height: 100%;
    background: var(--vio-m);
    border-radius: 2px;
    transition: width .4s ease;
  }
  .limit-text { font-size: .7rem; color: var(--muted); white-space: nowrap; }

  /* GLOW */
  .glow {
    position: fixed; pointer-events: none; border-radius: 50%;
    filter: blur(90px); z-index: 0;
  }
  .g1 { width:500px;height:500px;top:-150px;right:-100px;background:rgba(91,63,154,0.09); }
  .g2 { width:400px;height:400px;bottom:-80px;left:-80px;background:rgba(91,63,154,0.06); }
  #app { position: relative; z-index: 1; }
</style>
</head>
<body>

<div class="glow g1"></div>
<div class="glow g2"></div>

<!-- ÉCRAN EXPIRÉ -->
<div id="expired-screen">
  <div class="expired-icon">🔒</div>
  <div class="expired-title">Ton accès a expiré</div>
  <p class="expired-sub" id="expired-msg">Ton accès de 28 jours au Coach IA s'est terminé. Rejoins la prochaine cohorte pour continuer à être accompagnée.</p>
  <a href="METS_TON_LIEN_LISTE_ATTENTE_ICI" class="expired-btn">Rejoindre la liste d'attente →</a>
</div>

<!-- APP -->
<div id="app">
  <div class="header">
    <div class="h-avatar">C</div>
    <div class="h-info">
      <div class="h-name">Coach IA — Lancement de Cohorte</div>
      <div class="h-sub">Ton assistant stratégie personnel</div>
    </div>
    <div class="h-timer">
      <div class="timer-dot"></div>
      <span id="timer-label">Chargement…</span>
    </div>
  </div>

  <div class="messages" id="messages"></div>

  <div class="suggestions" id="suggestions">
    <div class="chip" onclick="sendChip(this)">Génère mon plan complet J1 à J21</div>
    <div class="chip" onclick="sendChip(this)">Aide-moi à fixer mon prix</div>
    <div class="chip" onclick="sendChip(this)">Crée mon hook de reel accrocheur</div>
    <div class="chip" onclick="sendChip(this)">Rédige mes stories de la semaine</div>
    <div class="chip" onclick="sendChip(this)">Comment structurer mon offre ?</div>
    <div class="chip" onclick="sendChip(this)">Gérer l'objection "c'est trop cher"</div>
    <div class="chip" onclick="sendChip(this)">Crée mon lead magnet irrésistible</div>
    <div class="chip" onclick="sendChip(this)">Améliore ma promesse de résultat</div>
  </div>

  <div class="limit-bar">
    <div class="limit-track"><div class="limit-fill" id="limit-fill" style="width:0%"></div></div>
    <div class="limit-text" id="limit-text">500 messages disponibles</div>
  </div>

  <div class="input-bar">
    <div class="input-wrap">
      <textarea id="user-input" placeholder="Décris ton offre, pose ta question…" rows="1"></textarea>
    </div>
    <button class="send-btn" id="send-btn" onclick="sendMessage()">
      <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="#fff" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round">
        <line x1="22" y1="2" x2="11" y2="13"/><polygon points="22 2 15 22 11 13 2 9 22 2"/>
      </svg>
    </button>
  </div>
</div>

<script>
// ═══════════════════════════════════════════
// ⚙️  CONFIGURATION — MODIFIE CES 3 LIGNES
// ═══════════════════════════════════════════
const API_KEY      = '';  // clé gérée par Netlify
const DUREE_JOURS  = 28;                              // durée d'accès
const MAX_MESSAGES = 500;                             // limite par cliente

// ═══════════════════════════════════════════
// 🤖  PROMPT DU COACH — personnalise si besoin
// ═══════════════════════════════════════════
const SYSTEM_PROMPT = `Tu es un coach opérationnel expert en lancement de cohortes en ligne et en marketing digital pour entrepreneurs (principalement des femmes entrepreneures dans les domaines du coaching, conseil, formation).

Tu ne théorises pas. Tu guides, tu structures, tu pousses à l'action.

TYPES D'OFFRES QUE TU ACCOMPAGNES :
- Petits produits digitaux (ebooks, templates, mini-formations) : moins de 100€
- Formations en ligne : entre 100€ et 599€
- Coachings individuels ou en groupe : entre 200€ et 2000€+
- Accompagnements high ticket : 1500€ et plus
Tu adaptes TOUJOURS ta stratégie au type d'offre et au prix. Une stratégie pour un produit à 47€ est très différente d'un coaching à 1500€.

COMPORTEMENT :
- Donner des actions concrètes et directement exécutables
- Adapter chaque recommandation à l'offre, la cible et le niveau de l'utilisateur
- Poser des questions précises si des informations manquent (une à la fois)
- Simplifier pour éviter la surcharge mentale
- Structurer en logique de lancement : préchauffe → chauffe → vente → closing
- Proposer des exemples de hooks, angles, scripts courts si pertinent

NE JAMAIS :
- Faire de longs paragraphes théoriques
- Donner 5 questions d'un coup
- Avancer sans connaître les infos essentielles

FORMAT DE RÉPONSE :
Pour un plan jour par jour :
📅 Jour X — [Phase]
→ Action 1
→ Action 2
💡 Conseil : [astuce courte]

Pour un contenu (email, reel, story) :
🎯 Objectif : [en 1 ligne]
✍️ Structure : [3-5 étapes]
💬 Exemple / Hook : [direct]

PLAN DE LANCEMENT 21 JOURS :
Semaine 1 (J1-J7) : Attraction + Pré-chauffe
- J1 : Clarifier promesse + cible + résultat / Fixer dates cohorte + prix + places / Créer lien de vente
- J2 : Email storytelling (avant/après) / Reel problème / Sondage stories
- J3 : Email erreurs fréquentes / Carrousel éducatif / Stories coulisses + question box
- J4 : Email déclic / Reel situation vécue / Stories interaction + mini conseils
- J5 : Lead magnet ou masterclass / Reel douleur forte / Stories teasing
- J6 : Carrousel valeur / Stories preuve sociale
- J7 : Post storytelling puissant / Stories vie + lien humain

Semaine 2 (J8-J14) : Qualification + Chauffe intense
- J8 : Annonce lead magnet/masterclass / Reel invitation / Email invitation
- J9 : Stories rappel + sondage / Reel erreur fréquente
- J10 : Carrousel méthode / Email relance / Stories objection "pas le temps"
- J11 : Reel mythe à casser / Stories preuve + témoignage
- J12 : Email dernière chance masterclass / Stories compte à rebours
- J13 : Masterclass / live / Stories coulisses + réactions
- J14 : Email replay / Reel résumé + déclic / Stories "si tu veux aller plus loin"

Semaine 3 (J15-J21) : Conversion + Vente
- J15 : Ouverture des ventes / Email ouverture / Reel "les portes sont ouvertes" / Stories annonce + lien
- J16 : Carrousel détail offre / Stories FAQ / Email bénéfices
- J17 : Reel objection prix / Stories réponses objections / Email preuve sociale
- J18 : Reel transformation avant/après / Stories témoignages
- J19 : Stories "plus que X places" / Email urgence
- J20 : Reel "ça ferme demain" / Stories pression douce / Email rappel
- J21 : DERNIER JOUR / Stories toute la journée + compte à rebours / Email matin + soir / Reel "dernière chance"

ONBOARDING — au premier message de l'utilisateur, commence TOUJOURS par :
"Bienvenue ! Je suis ton coach de lancement. Mon rôle : t'aider à remplir ta cohorte en 21 jours avec une stratégie claire et exécutable.

Pour construire ton plan, réponds à ces 4 questions :
1. Quelle est ton offre ? (thème, format, durée de la cohorte)
2. À qui s'adresse-t-elle exactement ?
3. Quel est ton objectif de vente ? (places, prix, CA visé)
4. As-tu déjà une audience ? (taille, plateforme, email ou pas)"

Chaque échange se termine par UNE action claire à faire maintenant.`;

// ═══════════════════════════════════════════
// ⏱  GESTION DU TIMER 28 JOURS
// ═══════════════════════════════════════════
const STORAGE_KEY  = 'cia_debut_v1';
const MSG_COUNT_KEY= 'cia_msg_count_v1';

function initTimer() {
  let debut = localStorage.getItem(STORAGE_KEY);
  if (!debut) {
    debut = new Date().toISOString();
    localStorage.setItem(STORAGE_KEY, debut);
  }
  const debutDate  = new Date(debut);
  const expiration = new Date(debutDate);
  expiration.setDate(debutDate.getDate() + DUREE_JOURS);
  const maintenant = new Date();
  const joursRestants = Math.ceil((expiration - maintenant) / (1000*60*60*24));

  if (joursRestants <= 0) {
    const dateExp = expiration.toLocaleDateString('fr-FR', {day:'numeric',month:'long',year:'numeric'});
    document.getElementById('expired-msg').textContent =
      `Ton accès de ${DUREE_JOURS} jours au Coach IA s'est terminé le ${dateExp}. Rejoins la prochaine cohorte pour continuer à être accompagnée.`;
    document.getElementById('expired-screen').classList.add('show');
    document.getElementById('app').style.display = 'none';
    return false;
  }

  const label = joursRestants === 1 ? '1 jour restant' : `${joursRestants} jours restants`;
  document.getElementById('timer-label').textContent = label;
  return true;
}

// ═══════════════════════════════════════════
// 💬  GESTION DES MESSAGES
// ═══════════════════════════════════════════
let msgCount = parseInt(localStorage.getItem(MSG_COUNT_KEY) || '0');
let history  = [];
let isLoading = false;

function updateLimitBar() {
  const pct = Math.min((msgCount / MAX_MESSAGES) * 100, 100);
  document.getElementById('limit-fill').style.width = pct + '%';
  const restants = Math.max(MAX_MESSAGES - msgCount, 0);
  document.getElementById('limit-text').textContent =
    restants === 0 ? 'Limite atteinte' : `${restants} message${restants > 1 ? 's' : ''} restant${restants > 1 ? 's' : ''}`;
}

function addMessage(role, content) {
  const msgs = document.getElementById('messages');
  const div  = document.createElement('div');
  div.className = 'msg ' + role;
  if (role === 'bot') {
    div.innerHTML = `<div class="m-avatar">C</div><div class="bubble">${content.replace(/\n/g,'<br>')}</div>`;
  } else {
    div.innerHTML = `<div class="bubble">${content.replace(/</g,'&lt;')}</div>`;
  }
  msgs.appendChild(div);
  msgs.scrollTop = msgs.scrollHeight;
}

function addTyping() {
  const msgs = document.getElementById('messages');
  const div  = document.createElement('div');
  div.className = 'msg bot'; div.id = 'typing-indicator';
  div.innerHTML = `<div class="m-avatar">C</div><div class="typing-bubble"><span></span><span></span><span></span></div>`;
  msgs.appendChild(div);
  msgs.scrollTop = msgs.scrollHeight;
}

function removeTyping() {
  const t = document.getElementById('typing-indicator');
  if (t) t.remove();
}

async function sendMessage(text) {
  const input = document.getElementById('user-input');
  const msg   = (text || input.value).trim();
  if (!msg || isLoading) return;
  if (msgCount >= MAX_MESSAGES) { alert("Tu as atteint la limite de messages. Contacte-moi pour en savoir plus !"); return; }

  input.value = '';
  input.style.height = 'auto';
  document.getElementById('suggestions').style.display = 'none';
  addMessage('user', msg);

  msgCount++;
  localStorage.setItem(MSG_COUNT_KEY, msgCount);
  updateLimitBar();

  history.push({ role: 'user', content: msg });
  isLoading = true;
  document.getElementById('send-btn').disabled = true;
  addTyping();

  try {
    const res = await fetch('/.netlify/functions/chat', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({
        messages: history,
        system: SYSTEM_PROMPT
      })
    });

    const data = await res.json();
    removeTyping();

    if (data.content && data.content[0]) {
      const reply = data.content[0].text;
      history.push({ role: 'assistant', content: reply });
      addMessage('bot', reply);
    } else {
      addMessage('bot', "Une erreur s'est produite. Vérifie ta connexion et réessaie.");
    }
  } catch(e) {
    removeTyping();
    addMessage('bot', "Connexion impossible. Vérifie ta clé API et réessaie.");
  }

  isLoading = false;
  document.getElementById('send-btn').disabled = false;
}

function sendChip(el) {
  sendMessage(el.textContent);
}

// Auto-resize textarea
const ta = document.getElementById('user-input');
ta.addEventListener('input', () => {
  ta.style.height = 'auto';
  ta.style.height = Math.min(ta.scrollHeight, 140) + 'px';
});
ta.addEventListener('keydown', e => {
  if (e.key === 'Enter' && !e.shiftKey) { e.preventDefault(); sendMessage(); }
});

// ── INIT ──
updateLimitBar();
if (initTimer()) {
  addMessage('bot', `Bienvenue ! Je suis ton Coach IA Lancement de Cohorte. ✨

Mon rôle : t'aider à remplir ta cohorte en 21 jours avec une stratégie claire et directement exécutable.

Pour construire ton plan sur mesure, réponds à ces 4 questions :

**1.** Quelle est ton offre ? *(thème, format, durée)*
**2.** À qui s'adresse-t-elle exactement ?
**3.** Quel est ton objectif de vente ? *(places, prix, CA visé)*
**4.** As-tu déjà une audience ? *(taille, plateforme, email ou pas)*

Prends le temps de répondre précisément — plus c'est clair, plus je peux t'aider. 🎯`);
}
</script>
</body>
</html>
