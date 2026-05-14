<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>sx1ph's Profile</title>
<link href="https://fonts.googleapis.com/css2?family=VT323&family=Courier+Prime:ital,wght@0,400;0,700;1,400&display=swap" rel="stylesheet">
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background-color: #0a0010;
    background-image:
      radial-gradient(ellipse at 20% 50%, #1a003a 0%, transparent 60%),
      radial-gradient(ellipse at 80% 20%, #200040 0%, transparent 50%),
      url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='400' height='400'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3CfeColorMatrix type='saturate' values='0'/%3E%3C/filter%3E%3Crect width='400' height='400' filter='url(%23noise)' opacity='0.04'/%3E%3C/svg%3E");
    font-family: 'Courier Prime', monospace;
    color: #fff;
    min-height: 100vh;
    padding: 20px;
    overflow-x: hidden;
  }

  /* Stars */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      radial-gradient(1px 1px at 10% 15%, #fff 0%, transparent 100%),
      radial-gradient(1px 1px at 25% 40%, #ffb3e6 0%, transparent 100%),
      radial-gradient(1px 1px at 40% 10%, #fff 0%, transparent 100%),
      radial-gradient(1.5px 1.5px at 55% 30%, #fff 0%, transparent 100%),
      radial-gradient(1px 1px at 70% 60%, #ffb3e6 0%, transparent 100%),
      radial-gradient(1px 1px at 85% 25%, #fff 0%, transparent 100%),
      radial-gradient(1px 1px at 15% 70%, #fff 0%, transparent 100%),
      radial-gradient(1.5px 1.5px at 35% 80%, #fff 0%, transparent 100%),
      radial-gradient(1px 1px at 60% 90%, #ffb3e6 0%, transparent 100%),
      radial-gradient(1px 1px at 90% 80%, #fff 0%, transparent 100%),
      radial-gradient(1px 1px at 5% 50%, #fff 0%, transparent 100%),
      radial-gradient(1px 1px at 75% 5%, #fff 0%, transparent 100%),
      radial-gradient(2px 2px at 45% 55%, #ff69b4 0%, transparent 100%),
      radial-gradient(1px 1px at 20% 95%, #fff 0%, transparent 100%),
      radial-gradient(1px 1px at 95% 45%, #fff 0%, transparent 100%);
    pointer-events: none;
    z-index: 0;
  }

  .container {
    max-width: 860px;
    margin: 0 auto;
    position: relative;
    z-index: 1;
  }

  /* ── Header / Name ── */
  .header {
    text-align: center;
    margin-bottom: 18px;
    animation: fadeDown 0.6s ease;
  }

  .header h1 {
    font-family: 'VT323', monospace;
    font-size: 64px;
    color: #ff69b4;
    text-shadow: 0 0 20px #ff69b4, 0 0 40px #ff1493, 2px 2px 0 #8b0057;
    letter-spacing: 4px;
    line-height: 1;
  }

  .header .tagline {
    font-style: italic;
    color: #ffb3e6;
    font-size: 14px;
    margin-top: 4px;
    opacity: 0.85;
  }

  .header .mood {
    display: inline-block;
    margin-top: 8px;
    background: #1a0030;
    border: 1px solid #ff69b4;
    padding: 3px 12px;
    border-radius: 20px;
    font-size: 12px;
    color: #ffb3e6;
  }

  /* ── Grid Layout ── */
  .grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
  }

  .grid .full { grid-column: 1 / -1; }

  /* ── Box / Card ── */
  .box {
    background: linear-gradient(135deg, #1e0035cc, #2d004dcc);
    border: 1.5px solid #c71585;
    border-radius: 4px;
    overflow: hidden;
    box-shadow: 0 0 12px #c7158530, inset 0 0 20px #ff69b408;
    animation: fadeUp 0.5s ease both;
  }

  .box-header {
    background: linear-gradient(90deg, #c71585, #8b0057);
    padding: 5px 12px;
    font-family: 'VT323', monospace;
    font-size: 18px;
    color: #fff;
    letter-spacing: 1px;
    display: flex;
    align-items: center;
    gap: 6px;
  }

  .box-header .star { color: #ffff99; font-size: 14px; }

  .box-body {
    padding: 12px 14px;
    font-size: 13px;
    line-height: 1.7;
    color: #f0c0e0;
  }

  .box-body a {
    color: #ff69b4;
    text-decoration: none;
  }

  .box-body a:hover { text-decoration: underline; }

  /* ── About / Blurbs ── */
  .label {
    color: #ff69b4;
    font-weight: 700;
    font-size: 12px;
    text-transform: uppercase;
    letter-spacing: 1px;
    margin-top: 8px;
    margin-bottom: 2px;
    display: block;
  }

  .label:first-child { margin-top: 0; }

  /* ── Interests list ── */
  .tag-list {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
    margin-top: 4px;
  }

  .tag {
    background: #3d0060;
    border: 1px solid #ff69b4;
    border-radius: 3px;
    padding: 2px 8px;
    font-size: 12px;
    color: #ffb3e6;
  }

  /* ── Friends ── */
  .friends-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(70px, 1fr));
    gap: 8px;
    margin-top: 4px;
  }

  .friend {
    text-align: center;
    font-size: 11px;
    color: #ffb3e6;
  }

  .friend-avatar {
    width: 60px;
    height: 60px;
    border: 2px solid #c71585;
    border-radius: 4px;
    background: #2d004d;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 22px;
    margin: 0 auto 3px;
  }

  /* ── Contact buttons ── */
  .btn-list {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
    margin-top: 6px;
  }

  .btn {
    background: #3d0060;
    border: 1px solid #ff69b4;
    border-radius: 3px;
    padding: 4px 10px;
    font-size: 12px;
    color: #ffb3e6;
    cursor: pointer;
    font-family: 'Courier Prime', monospace;
    transition: background 0.2s, color 0.2s;
  }

  .btn:hover {
    background: #c71585;
    color: #fff;
  }

  /* ── URL box ── */
  .url-box {
    background: #0f001f;
    border: 1px solid #8b0057;
    border-radius: 3px;
    padding: 4px 8px;
    font-size: 11px;
    color: #ff69b4;
    word-break: break-all;
    margin-top: 6px;
  }

  /* ── Blog ── */
  .empty-note {
    font-style: italic;
    color: #8b4070;
    font-size: 12px;
  }

  /* ── Footer ── */
  .footer {
    text-align: center;
    margin-top: 20px;
    font-family: 'VT323', monospace;
    font-size: 16px;
    color: #8b0057;
    letter-spacing: 2px;
    animation: fadeUp 1s ease 0.4s both;
  }

  /* ── Divider ── */
  hr.pink {
    border: none;
    border-top: 1px solid #c71585;
    margin: 8px 0;
    opacity: 0.4;
  }

  /* ── Animations ── */
  @keyframes fadeDown {
    from { opacity: 0; transform: translateY(-20px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(16px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  .box:nth-child(1) { animation-delay: 0.05s; }
  .box:nth-child(2) { animation-delay: 0.10s; }
  .box:nth-child(3) { animation-delay: 0.15s; }
  .box:nth-child(4) { animation-delay: 0.20s; }
  .box:nth-child(5) { animation-delay: 0.25s; }
  .box:nth-child(6) { animation-delay: 0.30s; }

  /* glowing pink scrollbar */
  ::-webkit-scrollbar { width: 6px; }
  ::-webkit-scrollbar-track { background: #0a0010; }
  ::-webkit-scrollbar-thumb { background: #c71585; border-radius: 3px; }

  @media (max-width: 580px) {
    .grid { grid-template-columns: 1fr; }
    .grid .full { grid-column: 1; }
    .header h1 { font-size: 48px; }
  }
</style>
</head>
<body>
<div class="container">

  <!-- Header -->
  <div class="header">
    <h1>☆ sx1ph ☆</h1>
    <div class="tagline">"sleeping on the xdlpillow" · peach!</div>
    <div class="mood">🌙 mood: trying to keep my eyes open</div>
  </div>

  <div class="grid">

    <!-- About Me -->
    <div class="box">
      <div class="box-header"><span class="star">✦</span> about me ☆ sx1ph's blurbs</div>
      <div class="box-body">
        <span class="label">About me:</span>
        just me, existing 🌸

        <span class="label">Who I'd like to meet:</span>
        this is too personal for me but eu and rose.idk
      </div>
    </div>

    <!-- Contact -->
    <div class="box">
      <div class="box-header"><span class="star">✦</span> say hi! ☆ contacting sx1ph</div>
      <div class="box-body">
        <div class="btn-list">
          <button class="btn">☆ Add to Friends</button>
          <button class="btn">☆ Send Message</button>
          <button class="btn">☆ Instant Message</button>
          <button class="btn">☆ Add to Group</button>
          <button class="btn">☆ Add to Favorites</button>
          <button class="btn">☆ Forward to Friend</button>
          <button class="btn">☆ Block User</button>
          <button class="btn">☆ Report User</button>
        </div>
        <hr class="pink">
        <span class="label">SpaceHey URL:</span>
        <div class="url-box">https://spacehey.com/profile?id=3055408</div>
      </div>
    </div>

    <!-- Interests -->
    <div class="box">
      <div class="box-header"><span class="star">✦</span> my interests ☆ sx1ph's</div>
      <div class="box-body">
        <span class="label">Interests:</span>
        <div class="tag-list">
          <span class="tag">watching movies</span>
          <span class="tag">series</span>
          <span class="tag">whatever sounds good</span>
          <span class="tag">back to the future</span>
          <span class="tag">holiday httyd</span>
        </div>

        <span class="label">Television:</span>
        <div class="tag-list">
          <span class="tag">I actually love it</span>
        </div>

        <span class="label">Books:</span>
        <div class="tag-list">
          <span class="tag">📖 reading list TBD</span>
        </div>
      </div>
    </div>

    <!-- Blog -->
    <div class="box">
      <div class="box-header"><span class="star">✦</span> sx1ph's latest blog entries</div>
      <div class="box-body">
        <a href="#">[ View Blog ]</a>
        <hr class="pink">
        <p class="empty-note">There are no Blog Entries yet.</p>
      </div>
    </div>

    <!-- Friends -->
    <div class="box full">
      <div class="box-header"><span class="star">✦</span> my friends ☆ sx1ph's friend space · sx1ph has 6 friends</div>
      <div class="box-body">
        <div class="friends-grid">
          <div class="friend">
            <div class="friend-avatar">🌐</div>
            SpaceHey
          </div>
          <div class="friend">
            <div class="friend-avatar">🦊</div>
            Foxyman135
          </div>
          <div class="friend">
            <div class="friend-avatar">👾</div>
            Xx.*A.†jadrt.*x
          </div>
          <div class="friend">
            <div class="friend-avatar">🐱</div>
            goosebumps
          </div>
          <div class="friend">
            <div class="friend-avatar">😈</div>
            cyberangel
          </div>
          <div class="friend">
            <div class="friend-avatar">🌸</div>
            An ●
          </div>
        </div>
      </div>
    </div>

  </div><!-- /grid -->

  <div class="footer">✦ · · · sexy angel · · · ✦</div>

</div>
</body>
</html>
