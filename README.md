<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>💚 For Mom</title>

  <style>
    :root{
      /* Ramadan/Egypt vibe: emerald + gold + deep night */
      --night:#061a18;
      --night2:#0b2a26;
      --emerald:#0ea5a0;
      --emerald2:#0b7d79;
      --gold:#d9b35c;
      --gold2:#b88a2f;
      --cream:#fff6df;

      --card: rgba(255,255,255,0.92);
      --text:#0f172a;
      --muted: rgba(15,23,42,0.72);
      --ring: rgba(217,179,92,0.25);
      --shadow: 0 24px 70px rgba(0,0,0,0.35);
    }

    *{ box-sizing:border-box; font-family: system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif; }

    body{
      margin:0;
      min-height:100vh;
      display:grid;
      place-items:center;
      color: var(--text);

      /* Default background image if you upload background.jpg */
      background:
        radial-gradient(circle at 20% 15%, rgba(217,179,92,0.18), transparent 40%),
        radial-gradient(circle at 80% 25%, rgba(14,165,160,0.18), transparent 45%),
        radial-gradient(circle at 50% 90%, rgba(217,179,92,0.12), transparent 55%),
        linear-gradient(160deg, rgba(6,26,24,0.92), rgba(11,42,38,0.92)),
        url("background.jpg");
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
      overflow:hidden;
    }

    /* subtle animated pattern overlay (stars + lantern vibe) */
    .pattern{
      position:fixed;
      inset:0;
      pointer-events:none;
      opacity:0.28;
      mix-blend-mode: screen;
    }
    .pattern::before{
      content:"";
      position:absolute;
      inset:-60px;
      background-image:url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="140" height="140" viewBox="0 0 140 140"><text x="10" y="62" font-size="42">🌙</text><text x="78" y="110" font-size="40">✨</text></svg>');
      background-size: 140px 140px;
      animation: drift 26s linear infinite;
    }
    @keyframes drift{
      from{ transform: translate3d(0,0,0) rotate(0deg); }
      to{ transform: translate3d(-180px, -180px, 0) rotate(8deg); }
    }

    /* soft glass overlay to keep text readable on photos */
    .overlay{
      position:fixed;
      inset:0;
      background:
        radial-gradient(circle at 15% 20%, rgba(217,179,92,0.10), transparent 45%),
        radial-gradient(circle at 85% 25%, rgba(14,165,160,0.10), transparent 55%),
        rgba(255,255,255,0.08);
      pointer-events:none;
    }

    .card{
      width:min(820px, 94vw);
      background: var(--card);
      border: 1px solid rgba(217,179,92,0.22);
      border-radius: 28px;
      padding: 22px 20px;
      box-shadow: var(--shadow);
      text-align:center;
      backdrop-filter: blur(12px);
      position:relative;
    }

    .topRow{
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap:12px;
      flex-wrap:wrap;
      margin-bottom: 10px;
    }

    .badge{
      display:inline-flex;
      align-items:center;
      gap:10px;
      padding: 10px 14px;
      border-radius: 999px;
      background: rgba(217,179,92,0.10);
      border: 1px solid rgba(217,179,92,0.25);
      color: rgba(11,42,38,0.92);
      font-weight: 900;
      font-size: 13px;
      letter-spacing: 0.2px;
    }

    .bgBtn{
      display:inline-flex;
      align-items:center;
      gap:10px;
      padding: 10px 14px;
      border-radius: 999px;
      background: rgba(255,255,255,0.95);
      border: 1px solid rgba(14,165,160,0.20);
      color: rgba(11,42,38,0.92);
      font-weight: 900;
      font-size: 13px;
      cursor:pointer;
      box-shadow: 0 12px 26px rgba(0,0,0,0.10);
    }
    .bgBtn:focus-visible{
      outline:none;
      box-shadow: 0 0 0 6px var(--ring), 0 12px 26px rgba(0,0,0,0.12);
    }

    input[type="file"]{ display:none; }

    h1{
      margin: 10px 0 6px;
      font-size: clamp(26px, 4vw, 46px);
      letter-spacing: -0.6px;
      color: rgba(11,42,38,0.95);
    }

    .mom{
      display:inline-block;
      padding: 2px 12px;
      border-radius: 999px;
      background: rgba(14,165,160,0.12);
      border: 1px solid rgba(14,165,160,0.22);
      color: rgba(11,42,38,0.95);
      font-weight: 1000;
    }

    p{
      margin: 6px 0 14px;
      font-size: clamp(14px, 2vw, 18px);
      color: var(--muted);
      line-height: 1.45;
    }

    .subline{
      margin-top: 4px;
      font-size: 14px;
      color: rgba(15,23,42,0.62);
      font-weight: 700;
    }

    .divider{
      height:1px;
      background: linear-gradient(90deg, transparent, rgba(217,179,92,0.45), transparent);
      margin: 14px 0 14px;
    }

    .stage{
      margin-top: 10px;
      height: 300px;
      border-radius: 22px;
      background:
        radial-gradient(circle at 30% 30%, rgba(217,179,92,0.10), transparent 45%),
        linear-gradient(180deg, rgba(255,255,255,0.92), rgba(255,250,238,0.70));
      border: 1px dashed rgba(217,179,92,0.40);
      position: relative;
      overflow: hidden;
      display:flex;
      align-items:center;
      justify-content:center;
    }

    /* subtle ornament corners */
    .ornament{
      position:absolute;
      inset:0;
      pointer-events:none;
      opacity:0.55;
    }
    .ornament::before,
    .ornament::after{
      content:"";
      position:absolute;
      width: 180px;
      height: 180px;
      border-radius: 22px;
      border: 2px solid rgba(217,179,92,0.22);
      box-shadow: inset 0 0 0 2px rgba(14,165,160,0.10);
    }
    .ornament::before{ top:-90px; left:-90px; transform: rotate(12deg); }
    .ornament::after{ bottom:-90px; right:-90px; transform: rotate(-10deg); }

    .buttons{
      position:absolute;
      inset:0;
      display:flex;
      align-items:center;
      justify-content:center;
      gap: 14px;
      padding: 18px;
    }

    button{
      border:0;
      border-radius: 999px;
      padding: 14px 18px;
      font-size: 18px;
      font-weight: 950;
      cursor:pointer;
      box-shadow: 0 14px 30px rgba(0,0,0,0.16);
      user-select:none;
      touch-action: manipulation;
      transition: transform .10s ease;
    }
    button:active{ transform: scale(0.98); }

    #yesBtn{
      background: linear-gradient(180deg, var(--emerald), var(--emerald2));
      color:white;
      min-width: 160px;
    }

    #noBtn{
      background: linear-gradient(180deg, rgba(255,255,255,0.98), rgba(255,246,225,0.92));
      color: rgba(11,42,38,0.95);
      border: 1px solid rgba(217,179,92,0.35);
      min-width: 130px;

      position:absolute;
      left: 60%;
      top: 58%;
      transform: translate(-50%, -50%);
    }

    .success{
      display:none;
      margin-top: 14px;
      padding: 16px;
      border-radius: 18px;
      background: rgba(14,165,160,0.08);
      border: 1px solid rgba(14,165,160,0.18);
      color: rgba(11,42,38,0.95);
      font-weight: 950;
    }

    .dua{
      margin-top: 8px;
      font-size: 14px;
      color: rgba(15,23,42,0.70);
      font-weight: 700;
    }

    .tiny{
      margin-top: 10px;
      font-size: 13px;
      opacity: 0.78;
      color: rgba(15,23,42,0.70);
    }
  </style>
</head>

<body>
  <div class="pattern" aria-hidden="true"></div>
  <div class="overlay" aria-hidden="true"></div>

  <main class="card">
    <div class="topRow">
      <div class="badge">🌙✨ Ramadan / Egypt Style</div>

      <!-- Optional: choose a background image (temporary per device) -->
      <label class="bgBtn" for="bgInput" title="Choose a background photo">
        🖼️ Choose background
      </label>
      <input id="bgInput" type="file" accept="image/*" />
    </div>

    <h1>Dear <span class="mom">Mom</span> 💛</h1>
    <p class="subline">A little question from your son…</p>

    <div class="divider"></div>

    <p style="margin-top:0;"><strong>Am I the best son in the world?</strong></p>

    <section class="stage" id="stage">
      <div class="ornament" aria-hidden="true"></div>
      <div class="buttons">
        <button id="yesBtn" type="button">Yes 🤍</button>
        <button id="noBtn" type="button">No 🙈</button>
      </div>
    </section>

    <div class="success" id="successMsg">
      🥹💚 Thank you, Mom! You’re the best mother in the world.
      <div class="dua">May you always be happy and healthy ✨</div>
    </div>

    <div class="tiny">
      Tip: To set a permanent background, upload a file named <b>background.jpg</b> next to <b>index.html</b>.
    </div>
  </main>

  <script>
    const stage = document.getElementById("stage");
    const noBtn = document.getElementById("noBtn");
    const yesBtn = document.getElementById("yesBtn");
    const successMsg = document.getElementById("successMsg");
    const bgInput = document.getElementById("bgInput");

    let noDodges = 0;

    function clamp(n, min, max){ return Math.max(min, Math.min(max, n)); }

    function moveNoButton() {
      const pad = 10;
      const stageRect = stage.getBoundingClientRect();
      const btnRect = noBtn.getBoundingClientRect();

      const maxX = stageRect.width - btnRect.width - pad;
      const maxY = stageRect.height - btnRect.height - pad;

      const x = Math.random() * maxX + pad;
      const y = Math.random() * maxY + pad;

      noBtn.style.left = clamp(x, pad, maxX) + "px";
      noBtn.style.top  = clamp(y, pad, maxY) + "px";
      noBtn.style.transform = "translate(0, 0)";
    }

    function dodgeIfNearPointer(clientX, clientY) {
      const btnRect = noBtn.getBoundingClientRect();
      const cx = btnRect.left + btnRect.width / 2;
      const cy = btnRect.top + btnRect.height / 2;

      const dist = Math.hypot(clientX - cx, clientY - cy);
      const danger = 160 + Math.min(noDodges * 12, 260); // more "impossible" over time

      if (dist < danger) {
        noDodges++;
        moveNoButton();

        // gently grow YES as NO becomes impossible
        const scale = 1 + Math.min(noDodges * 0.05, 0.65);
        yesBtn.style.transform = `scale(${scale})`;
      }
    }

    // Desktop + mobile pointer dodge
    stage.addEventListener("mousemove", (e) => dodgeIfNearPointer(e.clientX, e.clientY));
    stage.addEventListener("pointermove", (e) => dodgeIfNearPointer(e.clientX, e.clientY));

    // If she tries anyway, teleport before it lands
    noBtn.addEventListener("pointerdown", (e) => { e.preventDefault(); noDodges++; moveNoButton(); });
    noBtn.addEventListener("click", (e) => { e.preventDefault(); noDodges++; moveNoButton(); });

    yesBtn.addEventListener("click", () => {
      successMsg.style.display = "block";
      stage.style.display = "none";
    });

    // Optional: let user choose a background image (temporary per device/session)
    bgInput.addEventListener("change", () => {
      const file = bgInput.files && bgInput.files[0];
      if (!file) return;

      const url = URL.createObjectURL(file);
      document.body.style.backgroundImage =
        `radial-gradient(circle at 20% 15%, rgba(217,179,92,0.18), transparent 40%),
         radial-gradient(circle at 80% 25%, rgba(14,165,160,0.18), transparent 45%),
         radial-gradient(circle at 50% 90%, rgba(217,179,92,0.12), transparent 55%),
         linear-gradient(160deg, rgba(6,26,24,0.92), rgba(11,42,38,0.92)),
         url("${url}")`;
      document.body.style.backgroundSize = "cover";
      document.body.style.backgroundPosition = "center";
      document.body.style.backgroundRepeat = "no-repeat";
    });

    // Start No inside the stage
    window.addEventListener("load", () => {
      noBtn.style.left = "62%";
      noBtn.style.top = "58%";
    });
  </script>
</body>
</html>

