<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sai Tuition Centre – Foundation Maths</title>
<link href="https://fonts.googleapis.com/css2?family=Baloo+2:wght@400;600;700;800;900&family=Nunito:wght@400;600;700;800&display=swap" rel="stylesheet">
<style>
  :root {
    --navy: #0d1b4b;
    --blue: #1a3a9e;
    --sky: #3b82f6;
    --gold: #f59e0b;
    --amber: #fbbf24;
    --orange: #f97316;
    --green: #10b981;
    --pink: #ec4899;
    --light: #f0f6ff;
    --white: #ffffff;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    font-family: 'Nunito', sans-serif;
    background: #050d2e;
    color: var(--white);
    overflow-x: hidden;
    min-height: 100vh;
  }

  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background:
      radial-gradient(1px 1px at 10% 15%, rgba(255,255,255,.6) 0%, transparent 100%),
      radial-gradient(1px 1px at 25% 40%, rgba(255,255,255,.5) 0%, transparent 100%),
      radial-gradient(1px 1px at 60% 10%, rgba(255,255,255,.7) 0%, transparent 100%),
      radial-gradient(1px 1px at 80% 55%, rgba(255,255,255,.4) 0%, transparent 100%),
      radial-gradient(1px 1px at 45% 70%, rgba(255,255,255,.5) 0%, transparent 100%),
      radial-gradient(1px 1px at 90% 30%, rgba(255,255,255,.6) 0%, transparent 100%),
      radial-gradient(1.5px 1.5px at 35% 85%, rgba(255,255,255,.4) 0%, transparent 100%),
      radial-gradient(1px 1px at 70% 80%, rgba(255,255,255,.5) 0%, transparent 100%),
      linear-gradient(180deg, #050d2e 0%, #0d1b4b 50%, #0a2060 100%);
    pointer-events: none;
    z-index: 0;
  }

  .page-wrap { position: relative; z-index: 1; }

  /* HERO */
  .hero {
    text-align: center;
    padding: 56px 20px 36px;
    position: relative;
    overflow: hidden;
  }

  .float-icons { position: absolute; top:0; left:0; right:0; bottom:0; pointer-events:none; overflow:hidden; }
  .fi { position:absolute; font-size:28px; opacity:.2; animation: float-drift linear infinite; }
  @keyframes float-drift {
    0%   { transform:translateY(0) rotate(0deg); opacity:.2; }
    50%  { opacity:.3; }
    100% { transform:translateY(-100px) rotate(25deg); opacity:0; }
  }

  .badge {
    display: inline-block;
    background: linear-gradient(135deg, var(--gold), var(--orange));
    color: var(--navy);
    font-family: 'Baloo 2', cursive;
    font-weight: 800;
    font-size: 13px;
    letter-spacing: .08em;
    text-transform: uppercase;
    padding: 7px 20px;
    border-radius: 999px;
    margin-bottom: 20px;
    box-shadow: 0 4px 20px rgba(245,158,11,.5);
    animation: pulse-glow 2.4s ease-in-out infinite;
  }
  @keyframes pulse-glow {
    0%,100% { box-shadow:0 4px 20px rgba(245,158,11,.5); }
    50%      { box-shadow:0 4px 36px rgba(245,158,11,.9); }
  }

  .hero-org {
    font-family: 'Baloo 2', cursive;
    font-size: 14px;
    font-weight: 700;
    letter-spacing: .28em;
    text-transform: uppercase;
    color: var(--sky);
    margin-bottom: 10px;
  }

  .hero-title {
    font-family: 'Baloo 2', cursive;
    font-size: clamp(44px, 11vw, 82px);
    font-weight: 900;
    line-height: 1.0;
    background: linear-gradient(135deg, #fff 0%, var(--amber) 55%, var(--orange) 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    margin-bottom: 8px;
    animation: slide-in-down .7s cubic-bezier(.22,1,.36,1) both;
  }

  .hero-subtitle {
    font-family: 'Baloo 2', cursive;
    font-size: clamp(17px, 4vw, 24px);
    font-weight: 700;
    color: var(--sky);
    margin-bottom: 28px;
    animation: slide-in-down .85s .1s cubic-bezier(.22,1,.36,1) both;
  }

  @keyframes slide-in-down {
    from { opacity:0; transform:translateY(-24px); }
    to   { opacity:1; transform:translateY(0); }
  }

  .stats-row {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    justify-content: center;
    margin-bottom: 0;
    animation: fade-up .9s .2s both;
  }
  @keyframes fade-up {
    from { opacity:0; transform:translateY(22px); }
    to   { opacity:1; transform:translateY(0); }
  }
  .stat-pill {
    background: rgba(255,255,255,.1);
    border: 1.5px solid rgba(255,255,255,.16);
    backdrop-filter: blur(6px);
    border-radius: 999px;
    padding: 8px 18px;
    font-size: 13px;
    font-weight: 700;
    display: flex;
    align-items: center;
    gap: 7px;
    transition: transform .2s, background .2s;
  }
  .stat-pill:hover { transform:translateY(-3px); background:rgba(255,255,255,.16); }

  /* SECTIONS */
  .section { max-width: 760px; margin: 0 auto; padding: 36px 16px 0; }

  .card {
    background: rgba(255,255,255,.06);
    border: 1.5px solid rgba(255,255,255,.12);
    border-radius: 24px;
    padding: 28px 24px;
    backdrop-filter: blur(10px);
    margin-bottom: 24px;
    animation: fade-up .8s .3s both;
  }

  .card-title {
    font-family: 'Baloo 2', cursive;
    font-size: 22px;
    font-weight: 800;
    margin-bottom: 20px;
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .highlight-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
  }
  @media(max-width:480px){ .highlight-grid { grid-template-columns:1fr; } }

  .highlight-item {
    background: linear-gradient(135deg, rgba(59,130,246,.16), rgba(16,185,129,.1));
    border: 1px solid rgba(59,130,246,.22);
    border-radius: 14px;
    padding: 14px 16px;
    display: flex;
    align-items: flex-start;
    gap: 10px;
    transition: transform .2s, border-color .2s;
  }
  .highlight-item:hover { transform:translateY(-3px); border-color:rgba(59,130,246,.5); }
  .hi-icon { font-size: 22px; flex-shrink:0; margin-top:1px; }
  .hi-text { font-size: 14px; font-weight: 700; line-height: 1.35; }

  /* PRICE */
  .price-banner {
    background: linear-gradient(135deg, var(--gold) 0%, var(--orange) 100%);
    border-radius: 22px;
    padding: 26px 24px;
    text-align: center;
    margin-bottom: 24px;
    animation: fade-up .8s .4s both;
    position: relative;
    overflow: hidden;
  }
  .price-banner::before {
    content:'🎉'; font-size:90px;
    position:absolute; opacity:.1; top:-12px; right:-12px; pointer-events:none;
  }
  .price-label { font-size:12px; font-weight:800; text-transform:uppercase; letter-spacing:.1em; color:var(--navy); margin-bottom:4px; }
  .price-amount { font-family:'Baloo 2',cursive; font-size:56px; font-weight:900; color:var(--navy); line-height:1; }
  .price-note { font-size:13px; font-weight:700; color:rgba(13,27,75,.7); margin-top:4px; }
  .seats-pill {
    display:inline-block; background:var(--navy); color:var(--amber);
    font-size:12px; font-weight:800; padding:5px 14px; border-radius:999px;
    margin-top:14px; letter-spacing:.06em; text-transform:uppercase;
  }

  /* FORM */
  .form-card {
    background: linear-gradient(160deg, rgba(255,255,255,.09) 0%, rgba(59,130,246,.07) 100%);
    border: 1.5px solid rgba(255,255,255,.14);
    border-radius: 28px;
    padding: 32px 24px;
    backdrop-filter: blur(14px);
    animation: fade-up .8s .5s both;
    margin-bottom: 30px;
  }
  .form-title {
    font-family:'Baloo 2',cursive; font-size:26px; font-weight:900;
    text-align:center; margin-bottom:6px;
    background:linear-gradient(90deg, var(--sky), var(--amber));
    -webkit-background-clip:text; -webkit-text-fill-color:transparent; background-clip:text;
  }
  .form-subtitle { text-align:center; font-size:13px; color:rgba(255,255,255,.55); margin-bottom:24px; }

  .form-grid { display:grid; grid-template-columns:1fr 1fr; gap:14px; }
  @media(max-width:520px){ .form-grid { grid-template-columns:1fr; } }

  .form-group { display:flex; flex-direction:column; gap:6px; }
  .form-group.full { grid-column: 1/-1; }

  label {
    font-size:12px; font-weight:700; text-transform:uppercase;
    letter-spacing:.07em; color:rgba(255,255,255,.65);
    display:flex; align-items:center; gap:5px;
  }

  input, select, textarea {
    background:rgba(255,255,255,.08);
    border:1.5px solid rgba(255,255,255,.14);
    border-radius:12px;
    padding:13px 16px;
    font-family:'Nunito',sans-serif;
    font-size:15px; font-weight:600;
    color:#fff; outline:none; width:100%;
    transition: border-color .2s, background .2s, box-shadow .2s;
  }
  input::placeholder, textarea::placeholder { color:rgba(255,255,255,.3); }
  input:focus, select:focus, textarea:focus {
    border-color:var(--sky);
    background:rgba(59,130,246,.12);
    box-shadow:0 0 0 3px rgba(59,130,246,.18);
  }
  select option { background:#0d1b4b; color:#fff; }
  textarea { resize:vertical; min-height:90px; }

  .checkbox-group { display:flex; flex-direction:column; gap:10px; margin-top:4px; }
  .checkbox-row {
    display:flex; align-items:center; gap:10px;
    cursor:pointer; font-size:14px; font-weight:600;
    text-transform:none; letter-spacing:0; color:#fff;
  }
  .checkbox-row input[type="checkbox"] {
    width:18px; height:18px; accent-color:var(--sky); cursor:pointer; flex-shrink:0;
  }

  .submit-btn {
    width:100%; padding:17px; border:none; border-radius:16px;
    background:linear-gradient(135deg, var(--sky) 0%, #2563eb 100%);
    color:#fff; font-family:'Baloo 2',cursive; font-size:20px; font-weight:800;
    cursor:pointer; margin-top:20px; letter-spacing:.04em;
    box-shadow:0 8px 32px rgba(59,130,246,.45);
    transition:transform .2s, box-shadow .2s;
  }
  .submit-btn:hover { transform:translateY(-2px); box-shadow:0 12px 40px rgba(59,130,246,.6); }
  .submit-btn:active { transform:translateY(1px); }

  .error-msg { color:#fc8181; font-size:12px; font-weight:700; margin-top:4px; display:none; }

  /* SUCCESS */
  .success-msg {
    display:none; text-align:center; padding:28px 16px;
    animation:pop-in .5s cubic-bezier(.22,1,.36,1) both;
  }
  @keyframes pop-in {
    from { opacity:0; transform:scale(.85); }
    to   { opacity:1; transform:scale(1); }
  }
  .success-msg .big-emoji { font-size:64px; margin-bottom:14px; }
  .success-msg h3 {
    font-family:'Baloo 2',cursive; font-size:28px; font-weight:900; margin-bottom:10px;
    background:linear-gradient(90deg,var(--green),var(--sky));
    -webkit-background-clip:text; -webkit-text-fill-color:transparent; background-clip:text;
  }
  .success-msg p { color:rgba(255,255,255,.7); font-size:15px; line-height:1.7; }
  .success-msg .ref {
    display:inline-block; margin-top:16px;
    background:rgba(255,255,255,.08); border-radius:12px;
    padding:10px 20px; font-size:14px; font-weight:700; color:var(--amber);
  }

  /* CONTACT */
  .contact-strip { max-width:760px; margin:0 auto 56px; padding:0 16px; animation:fade-up .8s .6s both; }
  .contact-card {
    background:linear-gradient(135deg,var(--blue) 0%,#0f2d80 100%);
    border-radius:20px; padding:22px 24px;
    display:flex; align-items:center; justify-content:space-between;
    flex-wrap:wrap; gap:14px; border:1px solid rgba(255,255,255,.12);
  }
  .contact-info { display:flex; flex-direction:column; gap:4px; }
  .contact-info .ci-name { font-family:'Baloo 2',cursive; font-size:18px; font-weight:800; }
  .contact-info .ci-phone { font-size:22px; font-weight:800; color:var(--amber); }
  .contact-info .ci-note { font-size:12px; color:rgba(255,255,255,.55); }
  .call-btn {
    background:linear-gradient(135deg,var(--gold),var(--orange));
    color:var(--navy); font-family:'Baloo 2',cursive;
    font-size:16px; font-weight:800;
    padding:12px 26px; border-radius:14px;
    text-decoration:none;
    box-shadow:0 4px 20px rgba(245,158,11,.4);
    transition:transform .2s, box-shadow .2s; white-space:nowrap;
  }
  .call-btn:hover { transform:translateY(-2px); box-shadow:0 8px 28px rgba(245,158,11,.6); }

  .divider { text-align:center; font-size:20px; letter-spacing:8px; color:rgba(255,255,255,.12); margin:8px 0 0; }
</style>
</head>
<body>
<div class="page-wrap">

  <!-- HERO -->
  <section class="hero">
    <div class="float-icons">
      <div class="fi" style="left:6%;top:20%;animation-duration:7s;animation-delay:0s;">📐</div>
      <div class="fi" style="left:88%;top:14%;animation-duration:9s;animation-delay:2s;">➕</div>
      <div class="fi" style="left:14%;top:72%;animation-duration:11s;animation-delay:1s;">🔢</div>
      <div class="fi" style="left:82%;top:62%;animation-duration:8s;animation-delay:3s;">📏</div>
      <div class="fi" style="left:50%;top:78%;animation-duration:10s;animation-delay:.5s;">✖️</div>
      <div class="fi" style="left:40%;top:6%;animation-duration:12s;animation-delay:1.5s;">🧮</div>
      <div class="fi" style="left:72%;top:38%;animation-duration:9.5s;animation-delay:4s;">÷</div>
    </div>

    <div class="badge">📘 May 2026 Batch · Limited Seats!</div>
    <div class="hero-org">🎓 Sai Tuition Centre</div>
    <h1 class="hero-title">Foundation<br>Maths</h1>
    <div class="hero-subtitle">Grade 6 – 8 &nbsp;·&nbsp; Build Strong Maths Skills This May!</div>

    <div class="stats-row">
      <div class="stat-pill">📅 4 Days / Week</div>
      <div class="stat-pill">⏱️ 1 Hour / Day</div>
      <div class="stat-pill">💻 Online via Zoom / Meet</div>
      <div class="stat-pill">📚 4 Hours / Week Total</div>
      <div class="stat-pill">🚀 Starting May 2026</div>
    </div>
  </section>

  <div class="divider">· · · · ·</div>

  <!-- HIGHLIGHTS + PRICE + FORM -->
  <section class="section">

    <div class="card">
      <div class="card-title">✨ What You'll Learn</div>
      <div class="highlight-grid">
        <div class="highlight-item"><div class="hi-icon">💡</div><div class="hi-text">Strong Basics &amp; Concept Clarity</div></div>
        <div class="highlight-item"><div class="hi-icon">🧠</div><div class="hi-text">Vedic Maths Techniques</div></div>
        <div class="highlight-item"><div class="hi-icon">⚡</div><div class="hi-text">Quick Square Number Tricks</div></div>
        <div class="highlight-item"><div class="hi-icon">🔥</div><div class="hi-text">Fast Calculation Methods</div></div>
        <div class="highlight-item"><div class="hi-icon">📝</div><div class="hi-text">Weekly Tests &amp; Practice</div></div>
        <div class="highlight-item"><div class="hi-icon">🎯</div><div class="hi-text">Expert Guidance &amp; Doubt Clearing</div></div>
      </div>
    </div>

    <div class="price-banner">
      <div class="price-label">Course Fee per Student</div>
      <div class="price-amount">₹1500</div>
      <div class="price-note">One-time payment · All study material included</div>
      <div class="seats-pill">🔥 Limited Seats — Register Now!</div>
    </div>

    <!-- REGISTRATION FORM -->
    <div class="form-card">
      <div class="form-title">📝 Register Your Child</div>
      <div class="form-subtitle">Fill in the details below — we'll confirm your seat within 24 hours!</div>

      <div id="reg-form">
        <div class="form-grid">

          <div class="form-group">
            <label>👤 Student Name *</label>
            <input type="text" id="f-student" placeholder="Full name">
            <div class="error-msg" id="err-student">Please enter the student's name.</div>
          </div>

          <div class="form-group">
            <label>🎓 Grade / Class *</label>
            <select id="f-grade">
              <option value="" disabled selected>Select grade</option>
              <option value="6">Grade 6</option>
              <option value="7">Grade 7</option>
              <option value="8">Grade 8</option>
            </select>
            <div class="error-msg" id="err-grade">Please select a grade.</div>
          </div>

          <div class="form-group">
            <label>📞 Parent's Phone *</label>
            <input type="tel" id="f-phone" placeholder="+91 XXXXX XXXXX">
            <div class="error-msg" id="err-phone">Please enter a valid phone number.</div>
          </div>

          <div class="form-group">
            <label>📧 Email (Optional)</label>
            <input type="email" id="f-email" placeholder="you@example.com">
          </div>

          <div class="form-group">
            <label>🏫 School Name</label>
            <input type="text" id="f-school" placeholder="Child's school">
          </div>

          <div class="form-group">
            <label>📍 City</label>
            <input type="text" id="f-city" placeholder="City / Location">
          </div>

          <div class="form-group full">
            <label>💻 Preferred Platform</label>
            <select id="f-platform">
              <option value="" disabled selected>Choose platform</option>
              <option value="Zoom">Zoom</option>
              <option value="Google Meet">Google Meet</option>
              <option value="Either">Either works</option>
            </select>
          </div>

          <div class="form-group full">
            <label>🧩 Topics of Interest <span style="font-weight:600;text-transform:none;letter-spacing:0;opacity:.7;">(select all that apply)</span></label>
            <div class="checkbox-group">
              <label class="checkbox-row"><input type="checkbox" name="topics" value="Vedic Maths"> 🧠 Vedic Maths</label>
              <label class="checkbox-row"><input type="checkbox" name="topics" value="Quick Square Tricks"> ⚡ Quick Square Tricks</label>
              <label class="checkbox-row"><input type="checkbox" name="topics" value="Concept Clarity"> 💡 Concept Clarity &amp; Basics</label>
              <label class="checkbox-row"><input type="checkbox" name="topics" value="Weekly Tests"> 📝 Weekly Tests &amp; Practice</label>
              <label class="checkbox-row"><input type="checkbox" name="topics" value="Fast Calculations"> 🔥 Fast Calculation Methods</label>
            </div>
          </div>

          <div class="form-group full">
            <label>💬 Questions or Special Requirements?</label>
            <textarea id="f-message" placeholder="Type anything you'd like us to know..."></textarea>
          </div>

          <div class="form-group full" style="background:rgba(245,158,11,.1);border:1px dashed rgba(245,158,11,.35);border-radius:14px;padding:16px;">
            <label style="color:var(--amber);text-transform:none;letter-spacing:0;font-size:13px;">📲 Payment Instructions</label>
            <p style="font-size:13px;font-weight:600;color:rgba(255,255,255,.75);margin-top:8px;line-height:1.6;">
              After submitting this form, pay ₹1500 via UPI / Google Pay / PhonePe to the number provided by us. Share your payment screenshot on WhatsApp to confirm your seat. <span style="color:var(--amber);font-weight:800;">Seat is confirmed only after payment.</span>
            </p>
          </div>

        </div><!-- /form-grid -->

        <button class="submit-btn" onclick="submitForm()">🚀 Submit Registration</button>
      </div><!-- /reg-form -->

      <!-- SUCCESS -->
      <div class="success-msg" id="success-panel">
        <div class="big-emoji">🎉</div>
        <h3>Registration Received!</h3>
        <p>
          Thank you! We'll contact you on the number you provided to confirm your seat in the<br>
          <strong style="color:#fff;">May 2026 Foundation Maths Batch</strong>.
          <br><br>
          Please complete the ₹1500 payment and share your screenshot via WhatsApp to secure your child's spot!
        </p>
        <div class="ref" id="ref-num"></div>
      </div>

    </div><!-- /form-card -->
  </section>

  <!-- CONTACT -->
  <div class="contact-strip">
    <div class="contact-card">
      <div class="contact-info">
        <div class="ci-name">🎓 Sai Tuition Centre</div>
        <div class="ci-phone">📞 +91 99522 79506</div>
        <div class="ci-note">Mon – Sat &nbsp;·&nbsp; 9 AM – 7 PM</div>
      </div>
      <a class="call-btn" href="tel:+919952279506">📞 Call Now</a>
    </div>
  </div>

</div><!-- /page-wrap -->

<script>
function showErr(id, show) {
  document.getElementById(id).style.display = show ? 'block' : 'none';
}

function submitForm() {
  const student = document.getElementById('f-student').value.trim();
  const grade   = document.getElementById('f-grade').value;
  const phone   = document.getElementById('f-phone').value.trim();

  let valid = true;

  if (!student) { showErr('err-student', true); valid = false; } else { showErr('err-student', false); }
  if (!grade)   { showErr('err-grade', true); valid = false; }   else { showErr('err-grade', false); }
  if (!phone || phone.length < 7) { showErr('err-phone', true); valid = false; } else { showErr('err-phone', false); }

  if (!valid) return;

  const topics    = [...document.querySelectorAll('input[name="topics"]:checked')].map(c => c.value);
  const refNum    = 'SAI-' + Date.now().toString().slice(-6);

  const data = {
    ref: refNum,
    student,
    grade: 'Grade ' + grade,
    phone,
    email:    document.getElementById('f-email').value,
    school:   document.getElementById('f-school').value,
    city:     document.getElementById('f-city').value,
    platform: document.getElementById('f-platform').value,
    topics,
    message:  document.getElementById('f-message').value,
    timestamp: new Date().toLocaleString('en-IN')
  };
  console.log('Registration Data:', data);

  document.getElementById('reg-form').style.display = 'none';
  document.getElementById('ref-num').textContent = 'Reference: ' + refNum;
  const panel = document.getElementById('success-panel');
  panel.style.display = 'block';
  panel.scrollIntoView({ behavior: 'smooth', block: 'center' });
}
</script>
</body>
</html>
