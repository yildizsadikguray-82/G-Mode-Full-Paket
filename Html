<!doctype html>
<html lang="tr">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <meta name="theme-color" content="#000000" />
  <title>G-MODE • CORE SINGLE FILE • Ultra Prime</title>

  <style>
    :root{
      --bg:#02040a;
      --fg:#d7e3ff;
      --muted:rgba(215,227,255,.65);
      --glass:rgba(255,255,255,.06);
      --stroke:rgba(255,255,255,.12);
      --ok:rgba(0,255,180,.9);
      --warn:rgba(255,210,0,.9);
      --bad:rgba(255,60,120,.9);
      --shadow: 0 12px 40px rgba(0,0,0,.45);
      --r:18px;
    }
    *{box-sizing:border-box;margin:0;padding:0}
    html,body{height:100%;background:var(--bg);color:var(--fg);font-family:ui-sans-serif,-apple-system,BlinkMacSystemFont,"SF Pro Display","SF Pro Text",Roboto,Arial}
    a{color:inherit}
    .app{height:100%;display:grid;grid-template-rows:auto 1fr auto;gap:12px;padding:14px;max-width:980px;margin:0 auto}
    header, footer{
      background:linear-gradient(180deg, rgba(255,255,255,.06), rgba(255,255,255,.03));
      border:1px solid var(--stroke);
      border-radius:var(--r);
      box-shadow:var(--shadow);
      padding:12px 12px;
      backdrop-filter: blur(10px);
    }
    header{
      display:flex;align-items:center;justify-content:space-between;gap:12px;flex-wrap:wrap
    }
    .brand{display:flex;flex-direction:column;gap:2px}
    .brand .t{font-weight:800;letter-spacing:.6px}
    .brand .s{font-size:12px;color:var(--muted)}
    .row{display:flex;gap:8px;flex-wrap:wrap;align-items:center;justify-content:flex-end}
    .btn{
      border:1px solid var(--stroke);
      background:rgba(255,255,255,.06);
      color:var(--fg);
      border-radius:14px;
      padding:10px 12px;
      font-weight:700;
      cursor:pointer;
      transition:transform .12s ease, background .12s ease;
      user-select:none;
    }
    .btn:active{transform:scale(.98)}
    .btn.primary{background:rgba(0,255,180,.10);border-color:rgba(0,255,180,.25)}
    .btn.danger{background:rgba(255,60,120,.10);border-color:rgba(255,60,120,.25)}
    .btn.ghost{background:transparent}
    .pill{
      font-size:12px;
      padding:6px 10px;
      border-radius:999px;
      border:1px solid var(--stroke);
      background:rgba(255,255,255,.04);
      color:var(--muted);
    }

    main{
      position:relative;
      border-radius:var(--r);
      overflow:hidden;
      border:1px solid rgba(255,255,255,.10);
      box-shadow:var(--shadow);
      background:
        radial-gradient(1100px 900px at 10% 10%, rgba(0,255,180,.14), transparent 55%),
        radial-gradient(900px 700px at 90% 40%, rgba(140,80,255,.14), transparent 60%),
        radial-gradient(800px 700px at 40% 100%, rgba(255,60,120,.10), transparent 55%),
        #02040a;
      min-height:420px;
    }

    /* HUD */
    .hud{
      position:absolute;inset:12px;
      display:grid;
      grid-template-columns: 1fr;
      grid-template-rows:auto 1fr auto;
      gap:10px;
      pointer-events:none;
    }
    .hud-top,.hud-bot{
      display:flex;align-items:center;justify-content:space-between;gap:8px;flex-wrap:wrap;
    }
    .hud-card{
      pointer-events:none;
      border:1px solid var(--stroke);
      background:rgba(0,0,0,.28);
      border-radius:16px;
      padding:10px 12px;
      backdrop-filter: blur(8px);
    }
    .kv{display:flex;gap:10px;align-items:baseline;flex-wrap:wrap}
    .k{font-size:12px;color:var(--muted)}
    .v{font-size:13px;font-weight:800}

    /* Center stage */
    .stage{
      position:absolute;inset:0;
      display:flex;align-items:center;justify-content:center;
      padding:18px;
    }
    .core{
      width:min(640px, 100%);
      border-radius:22px;
      border:1px solid rgba(255,255,255,.12);
      background:linear-gradient(180deg, rgba(255,255,255,.06), rgba(0,0,0,.25));
      box-shadow: 0 20px 60px rgba(0,0,0,.55);
      padding:18px;
      backdrop-filter: blur(12px);
    }
    .core h1{font-size:22px;letter-spacing:.4px}
    .core p{margin-top:8px;color:var(--muted);line-height:1.35}
    .grid{
      margin-top:14px;
      display:grid;
      grid-template-columns:1fr;
      gap:10px;
    }
    .panel{
      border-radius:18px;
      border:1px solid var(--stroke);
      background:rgba(255,255,255,.04);
      padding:12px;
    }
    .panel-title{display:flex;align-items:center;justify-content:space-between;gap:10px}
    .panel-title b{letter-spacing:.4px}
    .mono{font-family:ui-monospace,SFMono-Regular,Menlo,Monaco,Consolas,monospace}
    .log{
      margin-top:10px;
      height:160px;
      overflow:auto;
      border-radius:14px;
      border:1px solid rgba(255,255,255,.10);
      background:rgba(0,0,0,.35);
      padding:10px;
      font-size:12px;
      color:rgba(215,227,255,.78);
      line-height:1.35;
    }

    /* Motion layer (visual engine) */
    canvas#viz{
      position:absolute; inset:0;
      width:100%; height:100%;
      opacity:.85;
    }

    footer{
      display:flex;align-items:center;justify-content:space-between;gap:10px;flex-wrap:wrap
    }
    .small{font-size:12px;color:var(--muted);line-height:1.3}
  </style>
</head>

<body>
  <div class="app">
    <header>
      <div class="brand">
        <div class="t">G-MODE • CORE</div>
        <div class="s">Tek tık • Chrome’da çalışır • Akış/Sistem/Reels iskeleti</div>
      </div>

      <div class="row">
        <span class="pill" id="pillState">STATE: OFF</span>
        <button class="btn primary" id="btnBoot">BOOT</button>
        <button class="btn" id="btnFlow">FLOW</button>
        <button class="btn" id="btnReels">REELS</button>
        <button class="btn" id="btnSystem">SYSTEM</button>
        <button class="btn danger" id="btnReset">RESET</button>
        <button class="btn ghost" id="btnMute">SOUND: ON</button>
      </div>
    </header>

    <main>
      <canvas id="viz" aria-hidden="true"></canvas>

      <div class="hud">
        <div class="hud-top">
          <div class="hud-card kv">
            <span class="k">Mode</span><span class="v" id="hudMode">—</span>
            <span class="k">Polarity</span><span class="v" id="hudPol">±</span>
            <span class="k">Tempo</span><span class="v" id="hudTempo">1.00x</span>
          </div>
          <div class="hud-card kv">
            <span class="k">Security</span><span class="v" id="hudSec">HARDENED</span>
            <span class="k">Session</span><span class="v mono" id="hudSession">—</span>
          </div>
        </div>

        <div></div>

        <div class="hud-bot">
          <div class="hud-card kv">
            <span class="k">Input</span><span class="v" id="hudInput">IDLE</span>
            <span class="k">Signal</span><span class="v" id="hudSignal">STABLE</span>
          </div>
          <div class="hud-card kv">
            <span class="k">Save</span><span class="v" id="hudSave">LOCAL</span>
            <span class="k">Telemetry</span><span class="v" id="hudTel">ON</span>
          </div>
        </div>
      </div>

      <div class="stage">
        <div class="core">
          <h1 id="title">G-MODE Boot Core</h1>
          <p id="subtitle">Bu tek dosya: durum makinesi + görsel motor + ses motoru + log + mod geçişi. Eski parçaları buraya slot’layacaksın.</p>

          <div class="grid">
            <div class="panel">
              <div class="panel-title">
                <b>CORE PANEL</b>
                <span class="pill mono" id="coreClock">00:00:00</span>
              </div>
              <div class="small" style="margin-top:8px" id="coreDesc">
                Modlar: <b>FLOW</b> (akış), <b>REELS</b> (teaser), <b>SYSTEM</b> (çekirdek). RESET zinciri sıfırlar, BOOT başlatır.
              </div>
              <div class="log mono" id="log"></div>
            </div>

            <div class="panel">
              <div class="panel-title">
                <b>CTA / GELİR SLOT</b>
                <span class="pill">placeholder</span>
              </div>
              <div class="small" style="margin-top:8px">
                Buraya “tek link” (site, ödeme, yönlendirme) mantığını bağlarsın.
                Bu iskelet <b>ödeme/IBAN</b> saklamaz; güvenlik için para tarafı dış sistemde olur.
              </div>
            </div>
          </div>

        </div>
      </div>
    </main>

    <footer>
      <div class="small">
        <b>Not:</b> Bu yapı offline çalışır. Log/ayarlar localStorage’dadır. İstersen PWA manifest/service worker sonra eklenir.
      </div>
      <div class="row">
        <button class="btn" id="btnExport">EXPORT LOG</button>
        <button class="btn" id="btnClear">CLEAR DATA</button>
      </div>
    </footer>
  </div>

  <script>
    /***********************
     * G-MODE CORE ISKELET *
     ***********************/

    // ---- Utilities
    const $ = (id) => document.getElementById(id);
    const nowISO = () => new Date().toISOString();
    const clamp = (v,min,max)=>Math.max(min,Math.min(max,v));
    const rand = (a,b)=>a+Math.random()*(b-a);

    // ---- Persistent store (local only)
    const STORE_KEY = "GMODE_CORE_SINGLE_FILE_V1";
    const store = {
      load(){
        try{ return JSON.parse(localStorage.getItem(STORE_KEY) || "{}"); }
        catch{ return {}; }
      },
      save(data){
        localStorage.setItem(STORE_KEY, JSON.stringify(data));
      },
      clear(){
        localStorage.removeItem(STORE_KEY);
      }
    };

    // ---- Core state machine
    const STATE = {
      OFF:"OFF",
      BOOTING:"BOOTING",
      RUNNING:"RUNNING",
      SHUTDOWN:"SHUTDOWN",
    };

    const MODE = {
      SYSTEM:"SYSTEM",
      FLOW:"FLOW",
      REELS:"REELS"
    };

    const core = {
      state: STATE.OFF,
      mode: MODE.SYSTEM,
      muted: false,
      polarity: 1,          // +1 / -1
      tempo: 1.0,           // 0.5..2.0
      sessionId: "",
      lastInput: "IDLE",
      signal: "STABLE",
      telemetry: true,
      secure: true,
      log: [],
      bootAt: 0,
      data: store.load(),
    };

    function newSession(){
      // kısa, offline session id
      const s = Math.random().toString(16).slice(2,10).toUpperCase();
      core.sessionId = "GM-" + s;
    }

    function writeLog(msg, level="INFO"){
      const line = `[${new Date().toLocaleTimeString()}] ${level}: ${msg}`;
      core.log.push(line);
      if (core.log.length > 400) core.log.shift();
      $("log").textContent = core.log.join("\n");
      $("log").scrollTop = $("log").scrollHeight;
      if (core.telemetry) {
        // local “telemetry”: son durumları kaydet
        core.data.last = { t: nowISO(), state: core.state, mode: core.mode, tempo: core.tempo, polarity: core.polarity };
        store.save(core.data);
      }
    }

    function setState(next){
      core.state = next;
      $("pillState").textContent = "STATE: " + next;
      $("hudSession").textContent = core.sessionId || "—";
      writeLog(`STATE -> ${next}`);
    }

    function setMode(next){
      core.mode = next;
      $("hudMode").textContent = next;
      $("title").textContent = `G-MODE • ${next}`;
      const desc = {
        SYSTEM:"Çekirdek panel: güvenlik, reset, kayıt, temel motorlar.",
        FLOW:"Akış modu: artı-eksi, gece-gündüz, acı-tatlı gibi karşıtlıkları tek zincirde sürer.",
        REELS:"Reels/Teaser: daha sinematik tempo, daha agresif pulse; içerik slot’ları hazır."
      }[next] || "";
      $("subtitle").textContent = desc;
      writeLog(`MODE -> ${next}`);
    }

    function togglePolarity(){
      core.polarity *= -1;
      $("hudPol").textContent = core.polarity > 0 ? "+" : "−";
      writeLog(`POLARITY -> ${core.polarity > 0 ? "PLUS" : "MINUS"}`);
    }

    function setTempo(v){
      core.tempo = clamp(v, 0.50, 2.00);
      $("hudTempo").textContent = core.tempo.toFixed(2) + "x";
      writeLog(`TEMPO -> ${core.tempo.toFixed(2)}x`);
    }

    // ---- “Security hardening” (client-side realism)
    // Not: Tarayıcıda %100 güvenlik yok. Ama “kolay bozulmasın/hacklenmesin” diye:
    // 1) dış script yok, 2) local data minimal, 3) eval yok, 4) kritik veri tutmuyoruz.
    function harden(){
      core.secure = true;
      $("hudSec").textContent = "HARDENED";
      writeLog("HARDEN: no-externals, no-eval, minimal-storage");
      // DevTools engelleme gibi şeyler sahte güvenlik; yapmıyoruz.
    }

    // ---- Sound engine (safe, simple)
    // WebAudio: kısa pulse/ambient (mute var)
    let audioCtx = null;
    let masterGain = null;

    function ensureAudio(){
      if (core.muted) return;
      if (!audioCtx){
        audioCtx = new (window.AudioContext || window.webkitAudioContext)();
        masterGain = audioCtx.createGain();
        masterGain.gain.value = 0.18;
        masterGain.connect(audioCtx.destination);
      }
      if (audioCtx.state === "suspended") audioCtx.resume();
    }

    function beep(freq=220, dur=0.08){
      if (core.muted) return;
      ensureAudio();
      if (!audioCtx) return;
      const o = audioCtx.createOscillator();
      const g = audioCtx.createGain();
      o.type = "sine";
      o.frequency.value = freq;
      g.gain.value = 0.0001;
      o.connect(g);
      g.connect(masterGain);

      const t = audioCtx.currentTime;
      g.gain.setValueAtTime(0.0001, t);
      g.gain.exponentialRampToValueAtTime(0.14, t + 0.01);
      g.gain.exponentialRampToValueAtTime(0.0001, t + dur);

      o.start(t);
      o.stop(t + dur + 0.02);
    }

    function bootSound(){
      beep(220,0.06); setTimeout(()=>beep(330,0.06),80);
      setTimeout(()=>beep(440,0.08),170);
    }
    function resetSound(){
      beep(520,0.06); setTimeout(()=>beep(260,0.08),90);
      setTimeout(()=>beep(130,0.10),190);
    }

    // ---- Visual engine (canvas pulse/spiral-ish)
    const canvas = $("viz");
    const ctx = canvas.getContext("2d", { alpha:true });
    let W=0,H=0, t0=performance.now();

    function resize(){
      const dpr = Math.max(1, Math.min(2, window.devicePixelRatio || 1));
      W = canvas.clientWidth; H = canvas.clientHeight;
      canvas.width = Math.floor(W*dpr);
      canvas.height = Math.floor(H*dpr);
      ctx.setTransform(dpr,0,0,dpr,0,0);
    }
    window.addEventListener("resize", resize);

    function draw(){
      const t = (performance.now() - t0)/1000;
      ctx.clearRect(0,0,W,H);

      // pulse strength by mode
      const m = core.mode;
      const base = m===MODE.REELS ? 1.25 : m===MODE.FLOW ? 1.05 : 0.9;
      const tempo = core.tempo;
      const pol = core.polarity;

      // soft background haze
      for(let i=0;i<6;i++){
        const r = (Math.sin(t*0.5 + i)*0.5+0.5)*220 + 120;
        const x = (Math.sin(t*0.22 + i*1.7)*0.5+0.5)*W;
        const y = (Math.cos(t*0.18 + i*2.1)*0.5+0.5)*H;
        ctx.globalAlpha = 0.08 * base;
        ctx.beginPath();
        ctx.arc(x,y,r,0,Math.PI*2);
        ctx.fill();
      }

      // ring pulse
      const cx=W/2, cy=H/2;
      const rings = 7;
      for(let k=1;k<=rings;k++){
        const phase = t*tempo*0.9 + k*0.65*pol;
        const rr = (Math.sin(phase)*0.5+0.5);
        const rad = k*48 + rr*42*base;
        ctx.globalAlpha = 0.07 + rr*0.06;
        ctx.lineWidth = 1.25;
        ctx.beginPath();
        ctx.arc(cx,cy, rad, 0, Math.PI*2);
        ctx.stroke();
      }

      // “spiral-ish” strokes
      const strokes = 180;
      ctx.globalAlpha = 0.06 * base;
      ctx.lineWidth = 1;
      for(let i=0;i<strokes;i++){
        const a = (i/strokes)*Math.PI*2 + t*0.5*tempo*pol;
        const r = (i/strokes)*Math.min(W,H)*0.48 + 14*Math.sin(t*1.2 + i*0.07);
        const x = cx + Math.cos(a)*r;
        const y = cy + Math.sin(a)*r;
        ctx.beginPath();
        ctx.moveTo(cx,cy);
        ctx.lineTo(x,y);
        ctx.stroke();
      }

      requestAnimationFrame(draw);
    }

    // ---- Boot / Reset / Shutdown flows
    async function boot(){
      if (core.state !== STATE.OFF) return;
      newSession();
      harden();
      setState(STATE.BOOTING);
      core.bootAt = Date.now();
      $("hudInput").textContent = "BOOT";
      writeLog("BOOT SEQUENCE: init engines, load store, apply defaults");
      bootSound();

      // restore any stored prefs
      const saved = core.data?.prefs || {};
      if (typeof saved.tempo === "number") setTempo(saved.tempo);
      if (typeof saved.polarity === "number") {
        core.polarity = saved.polarity;
        $("hudPol").textContent = core.polarity > 0 ? "+" : "−";
      }
      if (typeof saved.mode === "string") setMode(saved.mode);

      // fake “health checks”
      await wait(420);
      core.signal = "STABLE";
      $("hudSignal").textContent = "STABLE";
      writeLog("HEALTH: ok • signal stable • storage ok");

      setState(STATE.RUNNING);
      $("hudInput").textContent = "IDLE";
      writeLog("RUNNING: ready");
    }

    function wait(ms){ return new Promise(r=>setTimeout(r,ms)); }

    function reset(){
      // “Kopan zincir kendini yenilesin”
      $("hudInput").textContent = "RESET";
      writeLog("RESET: chain refresh, normalize, clear volatile state", "WARN");
      resetSound();

      core.signal = "STABLE";
      $("hudSignal").textContent = "STABLE";
      // reset transient values
      setTempo(1.0);
      if (core.polarity < 0) togglePolarity(); // normalize to PLUS
      setMode(MODE.SYSTEM);

      // persist prefs
      core.data.prefs = { tempo: core.tempo, polarity: core.polarity, mode: core.mode };
      store.save(core.data);

      $("hudInput").textContent = "IDLE";
      writeLog("RESET DONE");
    }

    function shutdown(){
      if (core.state === STATE.OFF) return;
      setState(STATE.SHUTDOWN);
      $("hudInput").textContent = "SHUTDOWN";
      writeLog("SHUTDOWN: save prefs, stop telemetry (local), audio suspend");
      core.data.prefs = { tempo: core.tempo, polarity: core.polarity, mode: core.mode };
      store.save(core.data);

      if (audioCtx && audioCtx.state === "running") audioCtx.suspend();
      setTimeout(()=>{
        setState(STATE.OFF);
        $("hudInput").textContent = "IDLE";
        $("hudMode").textContent = "—";
        $("hudSession").textContent = "—";
        $("title").textContent = "G-MODE Boot Core";
        $("subtitle").textContent = "BOOT ile başlat. FLOW/REELS/SYSTEM modları hazır.";
      }, 260);
    }

    // ---- Export log
    function exportLog(){
      const blob = new Blob([core.log.join("\n")], { type:"text/plain;charset=utf-8" });
      const url = URL.createObjectURL(blob);
      const a = document.createElement("a");
      a.href = url;
      a.download = `G-MODE_LOG_${core.sessionId || "NOSESSION"}.txt`;
      a.click();
      URL.revokeObjectURL(url);
      writeLog("EXPORT: log downloaded");
    }

    // ---- Clear local data
    function clearData(){
      store.clear();
      core.data = {};
      writeLog("LOCAL DATA CLEARED", "WARN");
    }

    // ---- Input bindings
    $("btnBoot").addEventListener("click", boot);
    $("btnReset").addEventListener("click", reset);
    $("btnFlow").addEventListener("click", ()=>{
      if (core.state !== STATE.RUNNING) return writeLog("Not running. BOOT first.", "WARN");
      setMode(MODE.FLOW);
      togglePolarity();
      setTempo(1.10);
      core.data.prefs = { tempo: core.tempo, polarity: core.polarity, mode: core.mode };
      store.save(core.data);
      beep(300,0.05);
    });
    $("btnReels").addEventListener("click", ()=>{
      if (core.state !== STATE.RUNNING) return writeLog("Not running. BOOT first.", "WARN");
      setMode(MODE.REELS);
      setTempo(1.35);
      beep(420,0.06);
      core.data.prefs = { tempo: core.tempo, polarity: core.polarity, mode: core.mode };
      store.save(core.data);
    });
    $("btnSystem").addEventListener("click", ()=>{
      if (core.state !== STATE.RUNNING) return writeLog("Not running. BOOT first.", "WARN");
      setMode(MODE.SYSTEM);
      setTempo(1.00);
      beep(220,0.05);
      core.data.prefs = { tempo: core.tempo, polarity: core.polarity, mode: core.mode };
      store.save(core.data);
    });

    $("btnMute").addEventListener("click", ()=>{
      core.muted = !core.muted;
      $("btnMute").textContent = "SOUND: " + (core.muted ? "OFF" : "ON");
      writeLog("SOUND -> " + (core.muted ? "MUTED" : "ON"));
      if (!core.muted) beep(260,0.04);
      if (core.muted && audioCtx && audioCtx.state==="running") audioCtx.suspend();
    });

    $("btnExport").addEventListener("click", exportLog);
    $("btnClear").addEventListener("click", clearData);

    // Optional: double tap header to shutdown
    document.querySelector("header").addEventListener("dblclick", shutdown);

    // ---- Clock
    setInterval(()=>{
      const d=new Date();
      $("coreClock").textContent = d.toLocaleTimeString();
    }, 250);

    // ---- Init
    resize();
    $("hudMode").textContent = "—";
    $("hudPol").textContent = "±";
    $("hudTempo").textContent = core.tempo.toFixed(2) + "x";
    $("hudSession").textContent = "—";
    $("hudSignal").textContent = core.signal;
    $("hudSave").textContent = "LOCAL";
    $("hudTel").textContent = core.telemetry ? "ON" : "OFF";
    $("hudSec").textContent = "—";
    writeLog("READY: click BOOT");
    requestAnimationFrame(draw);

    // Mobile friendly: resume audio on first touch (if not muted)
    window.addEventListener("pointerdown", ()=>{
      core.lastInput = "POINTER";
      $("hudInput").textContent = "POINTER";
      setTimeout(()=>$("hudInput").textContent="IDLE", 220);
      if (!core.muted) ensureAudio();
    }, {passive:true});
  </script>
</body>
</html>
