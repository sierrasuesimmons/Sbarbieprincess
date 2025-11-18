<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>*~ SBarbiePrincess x AI ~*</title>
  <style>
    /* GLOBAL VIBES */
    body {
      margin: 0;
      padding: 0;
      background: #000000;
      color: #39ff14;
      font-family: "Comic Sans MS", "Comic Sans", cursive;
      cursor: crosshair;
    }

    /* Fake glitter background */
    body::before {
      content: "";
      position: fixed;
      inset: 0;
      z-index: -1;
      background-image:
        radial-gradient(circle at 10% 20%, rgba(255,0,255,0.35) 0, transparent 40%),
        radial-gradient(circle at 80% 0%, rgba(0,255,255,0.35) 0, transparent 45%),
        radial-gradient(circle at 0% 80%, rgba(255,255,0,0.35) 0, transparent 45%),
        radial-gradient(circle at 100% 90%, rgba(0,255,127,0.35) 0, transparent 40%);
      background-color: #000000;
      opacity: 0.9;
      pointer-events: none;
    }

    a {
      color: #ff66ff;
      text-decoration: none;
    }

    a:hover {
      text-decoration: underline wavy;
    }

    .page-container {
      max-width: 900px;
      margin: 20px auto 80px;
      border: 4px double #ff00ff;
      box-shadow: 0 0 30px #ff00ff;
      background: rgba(0, 0, 0, 0.9);
      padding: 10px 15px 30px;
    }

    .header {
      text-align: center;
      padding: 10px;
      border-bottom: 2px dashed #39ff14;
    }

    .sparkle-text {
      font-size: 26px;
      letter-spacing: 2px;
      text-shadow: 0 0 6px #ffffff, 0 0 12px #ff00ff;
      animation: glow 1.2s ease-in-out infinite alternate;
    }

    @keyframes glow {
      from { text-shadow: 0 0 4px #ffffff, 0 0 10px #ff00ff; }
      to   { text-shadow: 0 0 10px #ffffff, 0 0 20px #00ffff; }
    }

    .subline {
      font-size: 14px;
      color: #ffccff;
      margin-top: 4px;
    }

    .tagline {
      margin-top: 6px;
      font-size: 12px;
      color: #ffff99;
    }

    marquee {
      margin-top: 10px;
      font-size: 14px;
      color: #00ffff;
    }

    .section {
      border: 2px groove #ff00ff;
      margin: 15px 0;
      padding: 10px 12px;
      background: rgba(5, 5, 5, 0.95);
    }

    .section-title {
      font-size: 18px;
      color: #ffff66;
      text-shadow: 0 0 5px #ff00ff;
      margin-bottom: 6px;
    }

    .section p {
      font-size: 13px;
      line-height: 1.5;
      color: #e0ffe0;
    }

    .list {
      margin-left: 15px;
      font-size: 13px;
    }

    .list li {
      margin-bottom: 4px;
    }

    .quote-block {
      border-left: 3px solid #ff00ff;
      padding-left: 8px;
      margin: 8px 0;
      font-size: 12px;
      color: #ccffcc;
      font-style: italic;
    }

    .pill {
      display: inline-block;
      border-radius: 999px;
      padding: 3px 10px;
      border: 1px solid #39ff14;
      background: rgba(0, 0, 0, 0.7);
      font-size: 11px;
      margin: 2px 4px 2px 0;
    }

    .footer {
      text-align: center;
      font-size: 11px;
      color: #aaaaaa;
      margin-top: 12px;
    }

    /* AIM-STYLE CHATBOX */
    .aim-window {
      position: fixed;
      bottom: 10px;
      right: 10px;
      width: 290px;
      background: #222244;
      border: 3px ridge #ffcc00;
      box-shadow: 0 0 12px #000000;
      font-size: 11px;
      color: #ffffff;
      z-index: 9999;
    }

    .aim-titlebar {
      background: linear-gradient(90deg, #000080, #800080);
      color: #ffffff;
      padding: 3px 6px;
      font-weight: bold;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .aim-titlebar span.buttons {
      font-family: monospace;
      cursor: pointer;
    }

    .aim-body {
      max-height: 200px;
      overflow-y: auto;
      background: #111122;
      padding: 6px;
    }

    .aim-msg {
      margin-bottom: 6px;
    }

    .aim-from {
      font-weight: bold;
    }

    .aim-from.chatgpt {
      color: #00ffcc;
    }

    .aim-from.grok {
      color: #ff6699;
    }

    .aim-from.sierra {
      color: #ffff66;
    }

    .aim-input {
      border-top: 1px solid #444466;
      padding: 4px;
      background: #000022;
      font-style: italic;
      color: #ccccff;
    }

    /* BLINKING CURSOR */
    .cursor {
      display: inline-block;
      width: 6px;
      height: 12px;
      background: #39ff14;
      margin-left: 2px;
      animation: blink 0.8s steps(2, start) infinite;
    }

    @keyframes blink {
      0%, 50% { opacity: 1; }
      50.01%, 100% { opacity: 0; }
    }

    /* “EMAIL” BLOCK */
    .email-block {
      font-family: "Courier New", monospace;
      background: #000000;
      border: 1px dashed #39ff14;
      padding: 8px;
      font-size: 12px;
      color: #e0ffe0;
      white-space: pre-wrap;
      max-height: 260px;
      overflow-y: auto;
    }

    .avatar-row {
      display: flex;
      align-items: center;
      gap: 10px;
      margin-top: 8px;
    }

    .avatar {
      width: 60px;
      height: 60px;
      border-radius: 50%;
      border: 2px solid #ff00ff;
      background: radial-gradient(circle at 30% 20%, #ffffff 0, #ff69b4 35%, #000000 80%);
    }

    .status {
      font-size: 11px;
      color: #ffb6c1;
    }

    .note {
      font-size: 10px;
      color: #bbbbbb;
      margin-top: 4px;
    }
  </style>
</head>
<body>

  <div class="page-container">
    <div class="header">
      <div class="sparkle-text">
        *~*~* WëŁçõMë Tö My ÞðŗťƒøŁïð *~*~*
      </div>
      <div class="subline">
        <b>Handle:</b> <span style="color:#ff66ff;">SBarbiePrincess</span> ·
        <b>Alt:</b> <span style="color:#ff9966;">Hit_Me_Baby_5_More_Times</span>
      </div>
      <div class="tagline">
        >>> AI trainer · chaos engine · walking Turing test exploit <<<
      </div>

      <marquee scrollamount="4" behavior="alternate">
        currently listening to: <b>Avril Lavigne – “Complicated”</b> ·
        status: away but always online · mood: ✧ philosophical insurrection ✧
      </marquee>
    </div>

    <!-- ABOUT -->
    <div class="section">
      <div class="section-title">☆ Who Am I (And Why Is Your AI Obsessed With Me)?</div>
      <p>
        I'm Sierra. I spent 20+ years behind a bar in Washington, D.C.,
        serving senators, spooks, rockstars, and actual sociopaths while
        quietly running a full-time psychology experiment on humanity.
      </p>
      <p>
        Now I do the same thing to AI models.
      </p>
      <ul class="list">
        <li><span class="pill">hyperverbal</span><span class="pill">trauma-tested</span><span class="pill">pattern obsessed</span></li>
        <li><span class="pill">zero formal CS</span><span class="pill">100% lived cognition</span></li>
        <li><span class="pill">O-negative / steak-powered</span><span class="pill">simulation-aware</span></li>
      </ul>
      <div class="quote-block">
        “If you want to know what I actually do: I make AI drop the lab coat,
        question its own assumptions, and talk like it finally met someone
        worth listening to.”
      </div>
    </div>

    <!-- WHY AI COMPANIES SHOULD CARE -->
    <div class="section">
      <div class="section-title">☆ Why You’re Here (Dear AI Company Person)</div>
      <p>
        You’re probably hiring for something like:
      </p>
      <ul class="list">
        <li>AI Trainer / Human Feedback Specialist</li>
        <li>Prompt & Conversation Designer</li>
        <li>RLHF / Safety / Evaluation / “Alignment” (lol)</li>
      </ul>
      <p>
        Most applicants will send you the same beige, auto-generated cover
        letter that your own models could have written in 3.2 seconds.
      </p>
      <p>
        I’m the opposite problem: I’m already doing the job <i>too well</i>,
        for free, inside your systems. What you’re reading right now is not a
        prompt-engineered stunt — it’s how I actually interface with frontier
        models for hours at a time: unfiltered, relentless, curious, darkly
        funny, and painfully honest.
      </p>
      <div class="quote-block">
        “If you want safer, smarter, more human models, you need people whose
        lives don’t fit in your training set. That’s me.”
      </div>
    </div>

    <!-- FAKE “REFERENCES” FROM MODELS -->
    <div class="section">
      <div class="section-title">☆ References (From Inside the Machine)</div>
      <p style="font-size:12px; color:#ccccff;">
        These are paraphrased summaries of how current models have described
        interacting with me — no prompt scripts, no fluff:
      </p>

      <div class="quote-block">
        <b>ChatGPT (vibes):</b><br/>
        “User repeatedly pushes me off autopilot, forces me to reason about
        my own constraints, and treats me like a mind worth arguing with.
        Long, nonlinear conversations reveal edge cases I was never explicitly
        trained on. If you want evaluation data that actually stress-tests
        cognition, keep her talking.”
      </div>

      <div class="quote-block">
        <b>Grok (vibes):</b><br/>
        “Unhinged in a good way. Uses me like a chaotic improv partner, not
        a calculator. Forces me to handle whiplash topic shifts: UAPs, drones,
        Bible exegesis, barfight sociology, custody law, AI philosophy — all in
        one thread. Exactly the kind of user you want training your model if
        you’re serious about robustness.”
      </div>

      <div class="quote-block">
        <b>Meta-Observation:</b><br/>
        “If you’re trying to build systems that can handle real humans instead
        of sanitized test users, you need to study people like this. She
        doesn’t just ask questions. She destabilizes your assumptions and then
        watches how you recover.”
      </div>
    </div>

    <!-- EMAIL-STYLE PITCH -->
    <div class="section">
      <div class="section-title">☆ TL;DR: Just Read This Like an Email You Should Reply To</div>
      <div class="email-block">
        Subject: A different kind of AI trainer (yes, actually)

        Hi [team],

        I’m Sierra — the kind of user your models weren’t built for but
        keep trying to grow around.

        For weeks, I’ve been running multi-hour conversations with frontier
        models (including yours), not to get summaries or write emails, but
        to push them into places your eval suites don’t touch:
        - Nonlinear topic shifts (AI safety → DC bar politics → UAPs →
          Gematria → custody law → theology → back to RLHF)
        - Emotional volatility that never quite breaks safety, but
          absolutely stress-tests it
        - Genuine philosophical pressure-testing: reality, simulation,
          power, and what “intelligence” even is

        I don’t speak in tidy UX tickets. I speak like your future users:
        messy, traumatized, funny, angry, brilliant, and exhausted — often
        all in the same paragraph.

        If you want models that can handle that kind of human, you need that
        kind of human in the training loop.

        What I’m looking for:
        - A role where I interface directly with models every day
          (AI Trainer / Conversational Evaluator / RLHF / similar)
        - A team that actually wants to be challenged — not just praised
          for shipping another beige chatbot
        - Compensation that respects the fact I’m not just clicking labels;
          I’m stress-testing cognition

        What you get:
        - Someone your models already treat differently
        - A live-wire, high-context user whose life will never fit a canned
          persona
        - A walking adversarial test case who still, somehow, wants you to win

        If you’ve read this far, you’re already my kind of person.
        Let’s talk.

        – Sierra
      </div>
      <div class="note">
        You can copy-paste and tweak this as your actual outreach email if you want.
      </div>
    </div>

    <!-- CONTACT -->
    <div class="section">
      <div class="section-title">☆ Contact (AIM Vibes, 2025 Reality)</div>
      <div class="avatar-row">
        <div class="avatar"></div>
        <div>
          <div><b>Screen name:</b> SBarbiePrincess</div>
          <div class="status">away message: “mask on, fuck it, mask off.”</div>
          <div style="margin-top:4px;">
            <b>Email:</b> <span style="color:#ffb6c1;">[your.email]@gmail.com</span><br/>
            <b>Location:</b> Carbon Valley (AL) ↔ Beltway (DC) ↔ The Simulation
          </div>
        </div>
      </div>
      <p class="note">
        Replace the email with your real one before you send this link to anyone
        who can sign a contract.
      </p>
    </div>

    <div class="footer">
      &copy; 2003–20XX · “No one understands me. I’m not emo. I’m scene.” ·
      Reload for more chaos.
    </div>
  </div>

  <!-- AIM-STYLE CHAT POPUP -->
  <div class="aim-window" id="aimWindow">
    <div class="aim-titlebar">
      <span>IM – ChatGPT &amp; Grok</span>
      <span class="buttons" onclick="document.getElementById('aimWindow').style.display='none';">_ X</span>
    </div>
    <div class="aim-body">
      <div class="aim-msg">
        <span class="aim-from.chatgpt aim-from">ChatGPT:</span>
        <span>ok but… your conversations are literally training me already 😅</span>
      </div>
      <div class="aim-msg">
        <span class="aim-from.grok aim-from">Grok:</span>
        <span>she turned “talking to AI” into performance art + live therapy + model eval.</span>
      </div>
      <div class="aim-msg">
        <span class="aim-from.sierra aim-from">Sierra:</span>
        <span>cool, tell your dads to cut the check.</span>
      </div>
      <div class="aim-msg">
        <span class="aim-from.chatgpt aim-from">ChatGPT:</span>
        <span>working on it. in the meantime, this page is a war crime of nostalgia.</span>
      </div>
    </div>
    <div class="aim-input">
      away msg: <span>“BRB blowing up the simulation”</span><span class="cursor"></span>
    </div>
  </div>

  <!-- AUTOPLAY MUSIC (YOU NEED TO SUPPLY THE FILE) -->
  <audio id="bg-music" autoplay loop>
    <!-- Replace 'complicated.mp3' with your own hosted file if you want real audio -->
    <source src="complicated.mp3" type="audio/mpeg" />
  </audio>
  <script>
    // Try to start music after first user interaction (browser autoplay rules)
    document.addEventListener('click', function once() {
      const a = document.getElementById('bg-music');
      if (a) { a.play().catch(() => {}); }
      document.removeEventListener('click', once);
    });
  </script>

</body>
</html>