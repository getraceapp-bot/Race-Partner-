
<!DOCTYPE html>
<html lang="en" dir="ltr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>RACE — Become a Partner</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;500;600;700&family=DM+Mono:wght@300;400;500&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
:root {
  --gold: #C9A84C;
  --gold-light: #E8C96A;
  --gold-dim: #7A6030;
  --black: #080807;
  --surface: #0F0F0D;
  --surface2: #161613;
  --surface3: #1E1E1A;
  --text: #F0EBE0;
  --text-muted: #7A7568;
  --text-dim: #4A4840;
  --border: rgba(201,168,76,0.15);
  --border-bright: rgba(201,168,76,0.4);
  --green: #1D9E75;
  --green-bg: rgba(29,158,117,0.08);
  --green-border: rgba(29,158,117,0.25);
  --blue: #60a5fa;
  --blue-bg: rgba(96,165,250,0.08);
  --blue-border: rgba(96,165,250,0.2);
  --purple: #c084fc;
  --purple-bg: rgba(192,132,252,0.08);
  --purple-border: rgba(192,132,252,0.2);
}
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0;}
html,body{
  background:var(--black);
  color:var(--text);
  font-family:'DM Sans',sans-serif;
  min-height:100vh;
  overflow-x:hidden;
}
[dir="rtl"] body{font-family:'DM Sans',Tahoma,Arial,sans-serif;}
body::before{
  content:'';position:fixed;inset:0;z-index:0;pointer-events:none;
  background-image:url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.85' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.07'/%3E%3C/svg%3E");
  opacity:0.5;
}
.step{display:none;min-height:100vh;position:relative;z-index:1;animation:fadeIn 0.55s ease;}
.step.active{display:flex;flex-direction:column;}
@keyframes fadeIn{from{opacity:0;transform:translateY(18px)}to{opacity:1;transform:translateY(0)}}
@keyframes goldPulse{0%,100%{opacity:1}50%{opacity:0.55}}
@keyframes shimmer{0%{background-position:200% center}100%{background-position:-200% center}}
@keyframes ripple{0%{transform:scale(0.95);opacity:0.7}100%{transform:scale(1.6);opacity:0}}
@keyframes floatUp{0%{opacity:0;transform:translateY(24px)}100%{opacity:1;transform:translateY(0)}}

/* PROGRESS */
.progress-bar{position:fixed;top:0;left:0;right:0;z-index:200;height:2px;background:var(--surface3);}
.progress-fill{height:100%;background:var(--gold);transition:width 0.6s cubic-bezier(0.4,0,0.2,1);}
.step-dots{position:fixed;top:18px;right:24px;z-index:200;display:flex;gap:6px;align-items:center;}
[dir="rtl"] .step-dots{right:auto;left:24px;}
.dot{width:6px;height:6px;border-radius:50%;background:var(--text-dim);transition:all 0.3s ease;}
.dot.active{background:var(--gold);transform:scale(1.4);}
.dot.done{background:var(--gold-dim);}

/* LANG SWITCHER */
.lang-bar{
  position:fixed;top:10px;left:50%;transform:translateX(-50%);
  z-index:200;
  display:flex;align-items:center;gap:4px;
  background:rgba(14,14,12,0.9);
  border:0.5px solid var(--border);
  border-radius:100px;
  padding:4px 6px;
  backdrop-filter:blur(12px);
}
.lang-btn{
  font-size:11px;font-weight:500;letter-spacing:0.06em;
  padding:5px 12px;border-radius:100px;border:none;
  cursor:pointer;transition:all 0.2s;
  background:none;color:var(--text-muted);font-family:inherit;
}
.lang-btn.active{background:var(--gold);color:var(--black);}
.lang-btn:hover:not(.active){color:var(--text);}

/* LOGO */
.logo-mark{
  font-family:'DM Mono',monospace;font-size:12px;letter-spacing:0.3em;
  color:var(--gold);text-transform:uppercase;
  position:fixed;top:16px;left:24px;z-index:200;
}
[dir="rtl"] .logo-mark{left:auto;right:24px;}

/* WRAP */
.wrap{max-width:680px;margin:0 auto;padding:88px 28px 64px;flex:1;display:flex;flex-direction:column;justify-content:center;}

/* TYPOGRAPHY */
.display{
  font-family:'Cormorant Garamond',serif;
  font-size:clamp(40px,6.5vw,68px);font-weight:600;line-height:1.0;letter-spacing:-0.02em;
  color:var(--text);margin-bottom:22px;
}
[dir="rtl"] .display{letter-spacing:0;line-height:1.15;}
.display .gold{
  color:var(--gold);
  background:linear-gradient(120deg,var(--gold),var(--gold-light),var(--gold));
  background-size:200% auto;
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;
  animation:shimmer 3s linear infinite;
}
.subtitle{font-size:16px;color:var(--text-muted);font-weight:300;line-height:1.75;max-width:480px;margin-bottom:36px;}
.eyebrow{font-family:'DM Mono',monospace;font-size:10px;letter-spacing:0.25em;text-transform:uppercase;color:var(--gold-dim);margin-bottom:18px;}
[dir="rtl"] .eyebrow{letter-spacing:0.05em;}

/* BUTTONS */
.btn-primary{
  display:inline-flex;align-items:center;gap:12px;
  background:var(--gold);color:var(--black);
  font-family:'DM Sans',sans-serif;font-size:15px;font-weight:500;
  padding:16px 32px;border-radius:100px;border:none;cursor:pointer;
  transition:transform 0.2s,box-shadow 0.2s,background 0.2s;
  text-decoration:none;letter-spacing:0.01em;white-space:nowrap;
}
.btn-primary:hover{transform:scale(1.03);background:var(--gold-light);box-shadow:0 12px 40px rgba(201,168,76,0.3);}
.btn-primary:active{transform:scale(0.98);}
.btn-ghost{
  display:inline-flex;align-items:center;gap:8px;background:none;
  color:var(--text-muted);font-size:13px;padding:10px 0;border:none;
  cursor:pointer;transition:color 0.2s;font-family:'DM Sans',sans-serif;margin-top:16px;
}
.btn-ghost:hover{color:var(--text);}
.btn-row{display:flex;flex-direction:column;align-items:flex-start;}

/* STAT BLOCKS */
.stat-row{display:grid;grid-template-columns:repeat(auto-fit,minmax(140px,1fr));gap:12px;margin-bottom:36px;}
.stat{
  background:var(--surface2);border:0.5px solid var(--border);
  border-radius:16px;padding:20px 18px;transition:border-color 0.3s,transform 0.2s;
  position:relative;overflow:hidden;
}
.stat:hover{border-color:var(--border-bright);transform:translateY(-2px);}
.stat-val{font-family:'Cormorant Garamond',serif;font-size:34px;font-weight:600;color:var(--gold);line-height:1;margin-bottom:6px;}
.stat-label{font-size:12px;color:var(--text-muted);font-weight:300;line-height:1.5;}

/* NETWORK ROYALTY CARD — NEW KEY MECHANIC */
.network-royalty-card{
  background:linear-gradient(135deg,rgba(201,168,76,0.07) 0%,rgba(29,158,117,0.06) 100%);
  border:0.5px solid var(--border-bright);
  border-radius:20px;padding:28px;margin-bottom:28px;
  position:relative;overflow:hidden;
}
.network-royalty-card::before{
  content:'';position:absolute;top:0;left:0;right:0;height:1px;
  background:linear-gradient(90deg,transparent,var(--gold),var(--green),transparent);
  opacity:0.7;
}
.nr-title{
  font-family:'Cormorant Garamond',serif;
  font-size:22px;font-weight:600;color:var(--text);margin-bottom:8px;line-height:1.2;
}
.nr-sub{font-size:13px;color:var(--text-muted);font-weight:300;line-height:1.6;margin-bottom:20px;}
.nr-rows{display:flex;flex-direction:column;gap:0;}
.nr-row{
  display:flex;align-items:center;gap:14px;
  padding:12px 0;border-bottom:0.5px solid var(--border);
}
.nr-row:last-child{border-bottom:none;}
.nr-icon{
  width:34px;height:34px;border-radius:10px;flex-shrink:0;
  display:flex;align-items:center;justify-content:center;font-size:15px;
}
.nr-icon.gold-i{background:rgba(201,168,76,0.12);border:0.5px solid rgba(201,168,76,0.3);}
.nr-icon.green-i{background:var(--green-bg);border:0.5px solid var(--green-border);}
.nr-icon.blue-i{background:var(--blue-bg);border:0.5px solid var(--blue-border);}
.nr-text{flex:1;}
.nr-label{font-size:13px;color:var(--text);font-weight:400;margin-bottom:2px;}
.nr-desc{font-size:12px;color:var(--text-muted);font-weight:300;}
.nr-pct{
  font-family:'DM Mono',monospace;font-size:14px;font-weight:500;
  color:var(--gold);white-space:nowrap;
}
.nr-pct.green{color:var(--green);}

/* GHOST DRIVER BOX */
.ghost-box{
  background:rgba(201,168,76,0.04);
  border:0.5px solid rgba(201,168,76,0.25);
  border-radius:14px;padding:18px 20px;
  margin-top:16px;display:flex;align-items:flex-start;gap:14px;
}
.ghost-icon{font-size:22px;flex-shrink:0;margin-top:2px;}
.ghost-text{flex:1;}
.ghost-headline{font-size:14px;font-weight:500;color:var(--text);margin-bottom:4px;}
.ghost-desc{font-size:13px;color:var(--text-muted);font-weight:300;line-height:1.6;}
.ghost-highlight{
  display:inline-block;
  background:rgba(201,168,76,0.12);border:0.5px solid rgba(201,168,76,0.35);
  border-radius:6px;padding:2px 8px;
  font-family:'DM Mono',monospace;font-size:12px;color:var(--gold);margin-top:8px;
}

/* PROOF BAR */
.proof-bar{
  background:var(--surface2);border:0.5px solid var(--border);
  border-radius:14px;padding:16px 20px;
  display:flex;align-items:center;gap:14px;margin-bottom:28px;
}
.proof-dot{width:7px;height:7px;border-radius:50%;background:#4ade80;flex-shrink:0;animation:goldPulse 1.8s ease infinite;position:relative;}
.proof-dot::after{
  content:'';position:absolute;inset:-3px;border-radius:50%;
  border:1px solid rgba(74,222,128,0.3);animation:ripple 2s ease infinite;
}
.proof-text{font-size:13px;color:var(--text-muted);font-weight:300;line-height:1.5;}
.proof-text strong{color:var(--text);font-weight:500;}

/* CALCULATOR */
.calc-card{
  background:var(--surface2);border:0.5px solid var(--border);
  border-radius:20px;padding:28px;margin-bottom:24px;
  position:relative;overflow:hidden;
}
.calc-card::before{
  content:'';position:absolute;top:0;left:0;right:0;height:1px;
  background:linear-gradient(90deg,transparent,var(--gold),transparent);opacity:0.5;
}
.slider-group{margin-bottom:20px;}
.slider-label{display:flex;justify-content:space-between;align-items:baseline;margin-bottom:10px;}
.slider-name{font-size:13px;color:var(--text-muted);font-weight:300;}
.slider-value{font-family:'DM Mono',monospace;font-size:14px;color:var(--gold);}
input[type=range]{-webkit-appearance:none;width:100%;height:3px;background:var(--surface3);border-radius:2px;outline:none;}
input[type=range]::-webkit-slider-thumb{
  -webkit-appearance:none;width:18px;height:18px;border-radius:50%;
  background:var(--gold);cursor:pointer;border:3px solid var(--black);
  box-shadow:0 0 0 1px var(--gold);transition:transform 0.2s;
}
input[type=range]::-webkit-slider-thumb:hover{transform:scale(1.2);}
.result-grid{display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-top:24px;padding-top:24px;border-top:0.5px solid var(--border);}
.result-item{}
.result-label{font-size:11px;color:var(--text-dim);margin-bottom:4px;letter-spacing:0.04em;text-transform:uppercase;}
.result-val{font-family:'Cormorant Garamond',serif;font-size:26px;font-weight:600;color:var(--gold);transition:all 0.3s;}
.result-val.big{font-size:38px;grid-column:span 2;}

/* REFERRAL TOGGLE */
.ref-toggle{
  display:flex;align-items:center;gap:12px;
  padding:16px 20px;background:var(--surface2);
  border:0.5px solid var(--border);border-radius:14px;
  cursor:pointer;margin-bottom:10px;transition:border-color 0.2s,background 0.2s;
}
.ref-toggle:hover{border-color:var(--border-bright);}
.toggle-track{
  width:38px;height:22px;border-radius:11px;
  background:var(--surface3);border:1px solid var(--border-bright);
  position:relative;transition:background 0.3s;flex-shrink:0;
}
.toggle-track.on{background:var(--gold);border-color:var(--gold);}
.toggle-thumb{
  position:absolute;top:2px;left:2px;
  width:16px;height:16px;border-radius:50%;
  background:var(--text-muted);transition:transform 0.3s,background 0.3s;
}
.toggle-track.on .toggle-thumb{transform:translateX(16px);background:var(--black);}
.toggle-text{font-size:14px;color:var(--text-muted);flex:1;line-height:1.3;}
.toggle-badge{
  font-family:'DM Mono',monospace;font-size:10px;padding:3px 10px;border-radius:100px;
  background:rgba(201,168,76,0.1);border:0.5px solid var(--gold-dim);color:var(--gold);letter-spacing:0.08em;white-space:nowrap;
}
.ref-expanded{
  display:none;background:var(--surface2);border:0.5px solid var(--border);
  border-radius:14px;padding:20px;margin-bottom:10px;animation:fadeIn 0.3s ease;
}
.ref-expanded.show{display:block;}

/* FIXED STAT BADGE */
.fixed-stat{
  display:inline-flex;align-items:center;gap:8px;
  background:rgba(29,158,117,0.1);border:0.5px solid var(--green-border);
  border-radius:100px;padding:5px 14px;font-size:12px;color:var(--green);
  margin-bottom:10px;font-family:'DM Mono',monospace;letter-spacing:0.05em;
}
.fixed-stat svg{width:12px;height:12px;flex-shrink:0;}

/* FLOW STEPS */
.flow-steps{display:flex;flex-direction:column;gap:0;margin-bottom:32px;}
.flow-step{display:flex;align-items:flex-start;gap:16px;padding:20px 0;border-bottom:0.5px solid var(--border);}
.flow-step:last-child{border-bottom:none;}
.flow-icon{
  width:36px;height:36px;border-radius:10px;flex-shrink:0;
  display:flex;align-items:center;justify-content:center;
  font-family:'DM Mono',monospace;font-size:12px;color:var(--gold);
}
.fi-gold{background:rgba(201,168,76,0.12);border:0.5px solid rgba(201,168,76,0.3);}
.fi-blue{background:var(--blue-bg);border:0.5px solid var(--blue-border);color:var(--blue);}
.fi-green{background:var(--green-bg);border:0.5px solid var(--green-border);color:var(--green);}
.fi-purple{background:var(--purple-bg);border:0.5px solid var(--purple-border);color:var(--purple);}
.fi-orange{background:rgba(251,146,60,0.08);border:0.5px solid rgba(251,146,60,0.2);color:#fb923c;}
.flow-body{flex:1;}
.flow-title{font-size:15px;font-weight:500;color:var(--text);margin-bottom:4px;}
.flow-desc{font-size:13px;color:var(--text-muted);font-weight:300;line-height:1.6;}

/* TIMELINE */
.timeline{display:flex;flex-direction:column;gap:0;}
.tl-item{
  display:flex;gap:20px;padding-bottom:28px;position:relative;
  opacity:0;transform:translateY(20px);transition:opacity 0.5s ease,transform 0.5s ease;
}
.tl-item.visible{opacity:1;transform:translateY(0);}
.tl-left{display:flex;flex-direction:column;align-items:center;}
.tl-dot{
  width:32px;height:32px;border-radius:50%;flex-shrink:0;
  border:1px solid var(--border-bright);
  display:flex;align-items:center;justify-content:center;
  font-family:'DM Mono',monospace;font-size:10px;color:var(--gold);background:var(--surface2);
}
.tl-line{width:1px;flex:1;background:var(--border);margin-top:6px;}
.tl-content{flex:1;padding-top:4px;}
.tl-title{font-size:16px;font-weight:500;color:var(--text);margin-bottom:6px;}
.tl-desc{font-size:13px;color:var(--text-muted);font-weight:300;line-height:1.65;}
.tl-number{
  font-family:'Cormorant Garamond',serif;font-size:20px;font-weight:600;
  color:var(--gold);margin-top:8px;display:flex;align-items:center;gap:8px;
}
.tl-badge{
  font-family:'DM Mono',monospace;font-size:9px;padding:3px 9px;border-radius:100px;
  letter-spacing:0.1em;text-transform:uppercase;display:inline-block;
}
.badge-push{background:rgba(251,146,60,0.1);color:#fb923c;border:0.5px solid rgba(251,146,60,0.25);}
.badge-compound{background:var(--green-bg);color:var(--green);border:0.5px solid var(--green-border);}
.badge-self{background:var(--blue-bg);color:var(--blue);border:0.5px solid var(--blue-border);}
.badge-inf{background:rgba(201,168,76,0.1);color:var(--gold);border:0.5px solid var(--gold-dim);}

/* GHOST DRIVER HIGHLIGHT — STEP 4 */
.ghost-trigger-box{
  background:linear-gradient(135deg,rgba(201,168,76,0.06),rgba(29,158,117,0.05));
  border:1px solid rgba(201,168,76,0.3);
  border-radius:18px;padding:24px;margin:24px 0;
  position:relative;overflow:hidden;
}
.ghost-trigger-box::before{
  content:'';position:absolute;top:0;left:0;right:0;height:1px;
  background:linear-gradient(90deg,transparent,var(--gold),transparent);
}
.gtb-eyebrow{font-size:10px;font-family:'DM Mono',monospace;letter-spacing:0.2em;color:var(--gold-dim);text-transform:uppercase;margin-bottom:10px;}
.gtb-headline{
  font-family:'Cormorant Garamond',serif;font-size:clamp(20px,3.5vw,26px);
  font-weight:600;color:var(--text);line-height:1.2;margin-bottom:10px;
}
.gtb-headline .gold{color:var(--gold);}
.gtb-body{font-size:13px;color:var(--text-muted);font-weight:300;line-height:1.7;margin-bottom:16px;}
.gtb-row{
  display:flex;align-items:center;gap:10px;padding:10px 0;
  border-top:0.5px solid var(--border);
}
.gtb-num{
  font-family:'DM Mono',monospace;font-size:18px;color:var(--gold);
  min-width:56px;text-align:left;
}
.gtb-label{font-size:12px;color:var(--text-muted);flex:1;line-height:1.4;}

/* FORM */
.form-group{margin-bottom:18px;}
.form-label{font-size:11px;color:var(--text-muted);letter-spacing:0.1em;text-transform:uppercase;margin-bottom:8px;display:block;}
.form-input{
  width:100%;background:var(--surface2);border:0.5px solid var(--border);
  border-radius:12px;padding:14px 18px;font-size:15px;color:var(--text);
  font-family:'DM Sans',sans-serif;outline:none;transition:border-color 0.2s;
  -webkit-appearance:none;
}
.form-input:focus{border-color:var(--gold);}
.form-input::placeholder{color:var(--text-dim);}
select.form-input{cursor:pointer;}
select.form-input option{background:#161613;color:var(--text);}
.form-row{display:grid;grid-template-columns:1fr 1fr;gap:14px;}
.submit-btn{
  width:100%;background:var(--gold);color:var(--black);
  font-family:'Cormorant Garamond',serif;font-size:20px;font-weight:600;
  padding:20px;border-radius:100px;border:none;cursor:pointer;
  transition:transform 0.2s,box-shadow 0.2s,background 0.2s;margin-top:8px;
}
.submit-btn:hover{background:var(--gold-light);box-shadow:0 16px 48px rgba(201,168,76,0.35);transform:translateY(-2px);}
.submit-btn:active{transform:scale(0.99);}
.submit-btn:disabled{opacity:0.5;cursor:not-allowed;transform:none;}

/* SUCCESS */
.success-ring{
  width:80px;height:80px;border-radius:50%;border:1px solid var(--gold);
  display:flex;align-items:center;justify-content:center;margin:0 auto 28px;
  animation:goldPulse 2s ease infinite;
}

/* DIVIDER */
.gold-divider{width:40px;height:1px;background:var(--gold);opacity:0.4;margin:28px 0;}

/* HERO LIVE */
.hero-line{display:flex;align-items:center;gap:10px;margin-bottom:16px;}
.live-dot{width:8px;height:8px;border-radius:50%;background:#4ade80;animation:goldPulse 1.8s ease infinite;position:relative;}
.live-dot::after{content:'';position:absolute;inset:-3px;border-radius:50%;border:1px solid rgba(74,222,128,0.25);animation:ripple 2s ease infinite;}
.live-text{font-family:'DM Mono',monospace;font-size:11px;letter-spacing:0.15em;color:#4ade80;}

/* EXPANDING ICON */
.expand-badge{
  display:inline-flex;align-items:center;gap:6px;
  background:rgba(29,158,117,0.1);border:0.5px solid var(--green-border);
  border-radius:100px;padding:4px 12px;font-size:11px;color:var(--green);
  font-family:'DM Mono',monospace;letter-spacing:0.06em;
}
.expand-dot{width:5px;height:5px;border-radius:50%;background:var(--green);animation:goldPulse 1.5s ease infinite;}

/* RESPONSIVE */
@media(max-width:480px){
  .form-row{grid-template-columns:1fr;}
  .result-grid{grid-template-columns:1fr;}
  .result-val.big{grid-column:span 1;font-size:28px;}
  .stat-row{grid-template-columns:1fr 1fr;}
  .lang-bar{top:6px;}
}
</style>
</head>
<body>

<!-- FIXED CHROME -->
<div class="progress-bar"><div class="progress-fill" id="progress"></div></div>
<div class="logo-mark" id="logo-text">RACE</div>
<div class="step-dots" id="dots"></div>

<!-- LANGUAGE SWITCHER -->
<div class="lang-bar" id="lang-bar">
  <button class="lang-btn active" onclick="setLang('en')" id="btn-en">EN</button>
  <button class="lang-btn" onclick="setLang('ku')" id="btn-ku">کوردی</button>
  <button class="lang-btn" onclick="setLang('ar')" id="btn-ar">عربي</button>
</div>

<!-- ═══════════════════════════ STEP 1 ═══════════════════════════ -->
<div class="step active" id="step-1">
  <div class="wrap">
    <div class="hero-line">
      <div class="live-dot"></div>
      <span class="live-text" data-key="live_label">LIVE · ERBIL, KURDISTAN</span>
    </div>
    <div class="eyebrow" data-key="s1_eyebrow">For fuel station owners</div>
    <h1 class="display">
      <span data-key="s1_h1a">Every car that leaves,</span><br>
      <span data-key="s1_h1b">your station</span><br>
      <span data-key="s1_h1c">without joining</span><br>
      <span class="gold" data-key="s1_h1d">is money you lose forever.</span>
    </h1>
    <p class="subtitle" data-key="s1_sub">
      RACE turns every fill-up into a permanent income stream — for you, your employees, and your network. One system. No extra staff. No extra cost. The station starts working for you.
    </p>

    <!-- NEW: NETWORK ROYALTY MECHANIC TEASER -->
    <div class="network-royalty-card">
      <div class="nr-title" data-key="nr_title">The income that never sleeps — even when drivers leave.</div>
      <div class="nr-sub" data-key="nr_sub">RACE is not just about your station. When your members fuel anywhere in the RACE network, you still earn. Your income follows your drivers — everywhere.</div>
      <div class="nr-rows">
        <div class="nr-row">
          <div class="nr-icon gold-i">⛽</div>
          <div class="nr-text">
            <div class="nr-label" data-key="nr_r1_label">Members fuel at YOUR station</div>
            <div class="nr-desc" data-key="nr_r1_desc">0.98% on every transaction goes to the RACE ecosystem</div>
          </div>
          <div class="nr-pct">0.98%</div>
        </div>
        <div class="nr-row">
          <div class="nr-icon green-i">🌐</div>
          <div class="nr-text">
            <div class="nr-label" data-key="nr_r2_label">Members fuel at ANY RACE partner station</div>
            <div class="nr-desc" data-key="nr_r2_desc">You still earn — automatically. No action needed from you.</div>
          </div>
          <div class="nr-pct green">0.15%</div>
        </div>
        <div class="nr-row">
          <div class="nr-icon blue-i">♾️</div>
          <div class="nr-text">
            <div class="nr-label" data-key="nr_r3_label">Station you refer — every transaction</div>
            <div class="nr-desc" data-key="nr_r3_desc">Permanent referral royalty. No ceiling. No expiry.</div>
          </div>
          <div class="nr-pct">0.12%</div>
        </div>
      </div>
      <!-- GHOST DRIVER INSIGHT -->
      <div class="ghost-box">
        <div class="ghost-icon">👻</div>
        <div class="ghost-text">
          <div class="ghost-headline" data-key="ghost1_h">The "ghost driver" income.</div>
          <div class="ghost-desc" data-key="ghost1_d">A driver joins your network, moves away, starts fueling at another RACE station in Erbil, Duhok, or Sulaymaniyah. Most owners would call that a lost customer. You call it passive income. The 0.15% cross-network royalty means <em>distance doesn't end your earnings.</em></div>
          <div class="ghost-highlight" data-key="ghost1_badge">Your income travels with your network → forever</div>
        </div>
      </div>
    </div>

    <div class="stat-row">
      <div class="stat">
        <div class="stat-val">450+</div>
        <div class="stat-label" data-key="stat1">Members activated at one station in 30 days</div>
      </div>
      <div class="stat">
        <div class="stat-val">68%</div>
        <div class="stat-label" data-key="stat2">Of members return to the same station — consistently</div>
      </div>
      <div class="stat">
        <div class="stat-val">0.98%</div>
        <div class="stat-label" data-key="stat3">When RACE members spend at your station — earned by you</div>
      </div>
    </div>

    <div class="btn-row">
      <button class="btn-primary" onclick="goTo(2)">
        <span data-key="s1_cta">Show me how it works</span>
        <svg width="16" height="16" viewBox="0 0 16 16" fill="none"><path d="M3 8h10M9 4l4 4-4 4" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg>
      </button>
    </div>
  </div>
</div>

<!-- ═══════════════════════════ STEP 2 ═══════════════════════════ -->
<div class="step" id="step-2">
  <div class="wrap">
    <div class="eyebrow" data-key="s2_eyebrow">The idea · in one breath</div>
    <h1 class="display" style="font-size:clamp(30px,5vw,50px);margin-bottom:28px;">
      <span data-key="s2_h1a">Spend fuel →</span><br>
      <span data-key="s2_h1b">get </span><span class="gold" data-key="s2_gold1">protected</span> →<br>
      <span data-key="s2_h1c">invite friends →</span><br>
      <span class="gold" data-key="s2_gold2">earn. Everywhere.</span>
    </h1>

    <div class="flow-steps">
      <div class="flow-step">
        <div class="flow-icon fi-gold">01</div>
        <div class="flow-body">
          <div class="flow-title" data-key="f1_t">Driver fills up at your station</div>
          <div class="flow-desc" data-key="f1_d">They scan, join RACE in 30 seconds. Your pump employee registers them and earns 0.20% of every transaction they generate — forever. Zero cost to you.</div>
        </div>
      </div>
      <div class="flow-step">
        <div class="flow-icon fi-blue">02</div>
        <div class="flow-body">
          <div class="flow-title" data-key="f2_t">Instant emergency protection</div>
          <div class="flow-desc" data-key="f2_d">Fuel, breakdown, towing — covered from the moment they join. This is the reason they stay. Protection is the invisible chain that keeps drivers loyal.</div>
        </div>
      </div>
      <div class="flow-step">
        <div class="flow-icon fi-green">03</div>
        <div class="flow-body">
          <div class="flow-title" data-key="f3_t">Your network goes everywhere</div>
          <div class="flow-desc" data-key="f3_d">When your members fuel at ANY other RACE partner station in Kurdistan, you earn 0.15%. They leave your station — your income doesn't. This is the mechanic no other fuel loyalty system in the region has.</div>
        </div>
      </div>
      <div class="flow-step">
        <div class="flow-icon fi-purple">04</div>
        <div class="flow-body">
          <div class="flow-title" data-key="f4_t">Refer a station. Earn forever.</div>
          <div class="flow-desc" data-key="f4_d">Introduce another station owner to RACE. Earn 0.12% of every transaction at their station — permanently. One conversation. Lifetime income.</div>
        </div>
      </div>
      <div class="flow-step">
        <div class="flow-icon fi-orange">05</div>
        <div class="flow-body">
          <div class="flow-title" data-key="f5_t">Join 11 active stations. Access 1,455 drivers.</div>
          <div class="flow-desc" data-key="f5_d">When you join the RACE network, members from other stations can find and fuel at yours. New traffic arrives at your pump — from drivers you've never met — because your station is now part of something bigger.</div>
        </div>
      </div>
    </div>

    <div class="btn-row">
      <button class="btn-primary" onclick="goTo(3)">
        <span data-key="s2_cta">Calculate my numbers</span>
        <svg width="16" height="16" viewBox="0 0 16 16" fill="none"><path d="M3 8h10M9 4l4 4-4 4" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg>
      </button>
      <button class="btn-ghost" onclick="goTo(1)"><span data-key="back">← Back</span></button>
    </div>
  </div>
</div>

<!-- ═══════════════════════════ STEP 3 ═══════════════════════════ -->
<div class="step" id="step-3">
  <div class="wrap">
    <div class="eyebrow" data-key="s3_eyebrow">Your station · estimated numbers</div>
    <h2 class="display" style="font-size:clamp(26px,4vw,42px);margin-bottom:8px;">
      <span data-key="s3_h1a">Move the sliders.</span><br>
      <span data-key="s3_h1b">Watch your </span><span class="gold" data-key="s3_gold">income appear.</span>
    </h2>
    <p class="subtitle" style="margin-bottom:24px;font-size:15px;" data-key="s3_sub">Based on live data from active RACE stations. These are your numbers — not ours.</p>

    <div class="calc-card">
      <div class="slider-group">
        <div class="slider-label">
          <span class="slider-name" data-key="sl_cars">Cars per day at my station</span>
          <span class="slider-value" id="v-cars">190 cars</span>
        </div>
        <input type="range" min="50" max="600" step="10" value="190" id="r-cars" oninput="calcAll()">
      </div>
      <div class="slider-group">
        <div class="slider-label">
          <span class="slider-name" data-key="sl_fill">Average fill-up amount</span>
          <span class="slider-value" id="v-fill">25,000 IQD</span>
        </div>
        <input type="range" min="10000" max="60000" step="1000" value="25000" id="r-fill" oninput="calcAll()">
      </div>
      <div class="slider-group">
        <div class="slider-label">
          <span class="slider-name" data-key="sl_conv">Member conversion rate</span>
          <span class="slider-value" id="v-conv">15%</span>
        </div>
        <input type="range" min="5" max="35" step="1" value="15" id="r-conv" oninput="calcAll()">
      </div>
      <div class="result-grid">
        <div class="result-item">
          <div class="result-label" data-key="res_members_label">New members / month</div>
          <div class="result-val" id="res-members">—</div>
        </div>
        <div class="result-item">
          <div class="result-label" data-key="res_network_label">Network royalty / month*</div>
          <div class="result-val" id="res-network">—</div>
        </div>
        <div class="result-item" style="grid-column:span 2">
          <div class="result-label" data-key="res_year_label">Your estimated income · year one</div>
          <div class="result-val big" id="res-year">—</div>
        </div>
      </div>
      <div style="margin-top:12px;font-size:11px;color:var(--text-dim);" data-key="calc_note">*Cross-network royalty (0.15%) estimated based on 11 active partner stations and 1,455 network drivers.</div>
    </div>

    <!-- REFER TOGGLE -->
    <div style="font-size:11px;color:var(--text-dim);letter-spacing:0.05em;margin-bottom:8px;text-transform:uppercase;" data-key="optional">Optional</div>

    <div class="ref-toggle" onclick="toggleReferral()" id="ref-toggle">
      <div class="toggle-track" id="ref-track"><div class="toggle-thumb"></div></div>
      <span class="toggle-text" data-key="tog_refer">I want to refer another station owner</span>
      <span class="toggle-badge" data-key="tog_refer_badge">+0.12% ROYALTY</span>
    </div>
    <div class="ref-expanded" id="ref-expanded">
      <div class="fixed-stat">
        <svg viewBox="0 0 12 12" fill="none"><circle cx="6" cy="6" r="5" stroke="currentColor" stroke-width="1"/><path d="M6 4v4M4 6h4" stroke="currentColor" stroke-width="1" stroke-linecap="round"/></svg>
        <span data-key="ref_fixed_rate">Referral royalty locked at 0.12% — permanent</span>
      </div>
      <div class="slider-group" style="margin-top:14px;">
        <div class="slider-label">
          <span class="slider-name" data-key="sl_ref_cars">Their station · cars per day</span>
          <span class="slider-value" id="v-ref-cars">250 cars</span>
        </div>
        <input type="range" min="50" max="600" step="10" value="250" id="r-ref-cars" oninput="calcAll()">
      </div>
      <div style="display:grid;grid-template-columns:1fr 1fr;gap:10px;padding-top:14px;border-top:0.5px solid var(--border);margin-top:4px;">
        <div>
          <div class="result-label" data-key="ref_mo_label">Referral income / month</div>
          <div class="result-val" id="res-ref-mo" style="font-size:22px;">—</div>
        </div>
        <div>
          <div class="result-label" data-key="ref_yr_label">Referral income / year</div>
          <div class="result-val" id="res-ref-yr" style="font-size:22px;">—</div>
        </div>
      </div>
    </div>

    <!-- JOIN TOGGLE -->
    <div class="ref-toggle" onclick="toggleJoin()" id="join-toggle">
      <div class="toggle-track" id="join-track"><div class="toggle-thumb"></div></div>
      <span class="toggle-text" data-key="tog_join">I want to connect to active RACE stations</span>
      <span class="toggle-badge" data-key="tog_join_badge">+NETWORK</span>
    </div>
    <div class="ref-expanded" id="join-expanded">
      <div style="display:flex;align-items:center;justify-content:space-between;margin-bottom:14px;">
        <div class="fixed-stat">
          <svg viewBox="0 0 12 12" fill="none"><circle cx="6" cy="6" r="5" stroke="currentColor" stroke-width="1"/></svg>
          <span data-key="join_fixed">11 active stations · 1,455 drivers</span>
        </div>
        <div class="expand-badge">
          <div class="expand-dot"></div>
          <span data-key="expanding">expanding</span>
        </div>
      </div>
      <div style="padding-top:14px;border-top:0.5px solid var(--border);">
        <div class="result-label" data-key="join_access_label">Drivers your station accesses immediately</div>
        <div class="result-val" id="res-join-members" style="font-size:28px;margin-top:6px;">1,455</div>
        <div style="font-size:12px;color:var(--text-dim);margin-top:8px;" data-key="join_note">These 1,455 drivers are already RACE members in the network. The day you activate, they can see and fuel at your station.</div>
      </div>
    </div>

    <div style="margin-top:24px;" class="btn-row">
      <button class="btn-primary" onclick="goTo(4)">
        <span data-key="s3_cta">See my 6-month roadmap</span>
        <svg width="16" height="16" viewBox="0 0 16 16" fill="none"><path d="M3 8h10M9 4l4 4-4 4" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg>
      </button>
      <button class="btn-ghost" onclick="goTo(2)"><span data-key="back">← Back</span></button>
    </div>
  </div>
</div>

<!-- ═══════════════════════════ STEP 4 ═══════════════════════════ -->
<div class="step" id="step-4">
  <div class="wrap">
    <div class="eyebrow" data-key="s4_eyebrow">Your roadmap · from day one</div>
    <h2 class="display" style="font-size:clamp(26px,4vw,44px);margin-bottom:10px;">
      <span data-key="s4_h1a">The station that</span><br>
      <span class="gold" data-key="s4_gold">sells itself.</span>
    </h2>
    <p class="subtitle" style="font-size:14px;margin-bottom:28px;" data-key="s4_sub">This is exactly what happened inside the RACE ecosystem — at a station very similar to yours. The phases are predictable. The income is permanent.</p>

    <div class="timeline" id="timeline">
      <div class="tl-item">
        <div class="tl-left"><div class="tl-dot">W1</div><div class="tl-line"></div></div>
        <div class="tl-content">
          <div class="tl-title" data-key="tl1_t">Your employee becomes your best asset</div>
          <div class="tl-desc" data-key="tl1_d">One incentive conversation. Your pump employee registers every driver — 30 seconds per car. They earn 0.20% per transaction they generate. They stop being an employee and start being invested in your station's growth.</div>
          <div class="tl-number"><span id="roadmap-w1">+29 members day one</span> <span class="tl-badge badge-push" data-key="phase_push">Manual push</span></div>
        </div>
      </div>
      <div class="tl-item">
        <div class="tl-left"><div class="tl-dot">W6</div><div class="tl-line"></div></div>
        <div class="tl-content">
          <div class="tl-title" data-key="tl2_t">500 members. Social proof ignites.</div>
          <div class="tl-desc" data-key="tl2_d">WhatsApp groups start talking about your station. Drivers bring other drivers. The station has an identity — not just a price board. Other stations in Erbil cannot replicate this because it took time to build.</div>
          <div class="tl-number"><span id="roadmap-w6">~500 members</span> <span class="tl-badge badge-push" data-key="phase_push">Manual push</span></div>
        </div>
      </div>
      <div class="tl-item">
        <div class="tl-left"><div class="tl-dot">M3</div><div class="tl-line"></div></div>
        <div class="tl-content">
          <div class="tl-title" data-key="tl3_t">Network compounding begins</div>
          <div class="tl-desc" data-key="tl3_d">Each member brings 1.4 others. Growth is no longer linear. The flywheel turns without you — and the cross-network royalty means even members who fuel elsewhere are generating income for you.</div>
          <div class="tl-number"><span id="roadmap-m3">~2,100 members</span> <span class="tl-badge badge-compound" data-key="phase_compound">Compounding</span></div>
        </div>
      </div>
      <!-- GHOST DRIVER TRIGGER BOX -->
      <div class="tl-item">
        <div class="tl-left"><div class="tl-dot" style="border-color:var(--gold);color:var(--gold);">★</div><div class="tl-line"></div></div>
        <div class="tl-content">
          <div class="ghost-trigger-box">
            <div class="gtb-eyebrow" data-key="gtb_eyebrow">The mechanic your competitors don't have</div>
            <div class="gtb-headline">
              <span data-key="gtb_h1">A driver stops coming to your station.</span><br>
              <span class="gold" data-key="gtb_h2">You still earn from them. Forever.</span>
            </div>
            <div class="gtb-body" data-key="gtb_body">
              Most loyalty systems end the moment a customer leaves. RACE is different. When your network member fills up at <em>any</em> RACE partner station in Kurdistan — Erbil, Duhok, Sulaymaniyah — 0.15% of that transaction comes back to you. Automatically. Silently. Permanently.<br><br>
              This is not a discount scheme. This is not a points system. This is a <strong>royalty on human behavior</strong> — and humans always need fuel.
            </div>
            <div class="gtb-row">
              <div class="gtb-num">0.15%</div>
              <div class="gtb-label" data-key="gtb_r1">Cross-network royalty on every fill-up by your members at partner stations</div>
            </div>
            <div class="gtb-row">
              <div class="gtb-num">∞</div>
              <div class="gtb-label" data-key="gtb_r2">No expiry. No cap. No re-approval. The royalty is written into the network — permanently.</div>
            </div>
            <div class="gtb-row">
              <div class="gtb-num" id="ghost-monthly">—</div>
              <div class="gtb-label" data-key="gtb_r3">Estimated monthly ghost-driver royalty based on your network size at month 3</div>
            </div>
          </div>
        </div>
      </div>
      <div class="tl-item">
        <div class="tl-left"><div class="tl-dot">M6</div><div class="tl-line"></div></div>
        <div class="tl-content">
          <div class="tl-title" data-key="tl4_t">The station sells itself</div>
          <div class="tl-desc" data-key="tl4_d">Every competitor in Erbil is still just a price on a board. You have thousands of verified drivers locked to your network — filling up at your station, and at partner stations where you still earn. This asset took time. It cannot be copied overnight.</div>
          <div class="tl-number"><span id="roadmap-m6">6,000+ members</span> <span class="tl-badge badge-self" data-key="phase_self">Self-selling</span></div>
        </div>
      </div>
      <div class="tl-item">
        <div class="tl-left"><div class="tl-dot">∞</div></div>
        <div class="tl-content">
          <div class="tl-title" data-key="tl5_t">Referral royalties stack. Forever.</div>
          <div class="tl-desc" data-key="tl5_d">Every station you refer earns you 0.12% of their total volume — permanently. Refer 5 stations. Earn from 5 networks. You become a node in the only verified automotive network in Kurdistan.</div>
          <div class="tl-number"><span data-key="tl5_num">Passive income ·</span> <span data-key="tl5_num2"> no ceiling</span> <span class="tl-badge badge-inf">∞ royalty</span></div>
        </div>
      </div>
    </div>

    <div class="gold-divider"></div>
    <div class="btn-row">
      <button class="btn-primary" onclick="goTo(5)">
        <span data-key="s4_cta">I'm ready. Let's start.</span>
        <svg width="16" height="16" viewBox="0 0 16 16" fill="none"><path d="M3 8h10M9 4l4 4-4 4" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg>
      </button>
      <button class="btn-ghost" onclick="goTo(3)"><span data-key="back">← Back</span></button>
    </div>
  </div>
</div>

<!-- ═══════════════════════════ STEP 5 ═══════════════════════════ -->
<div class="step" id="step-5">
  <div class="wrap">
    <div class="eyebrow" data-key="s5_eyebrow">Become a RACE partner</div>
    <h2 class="display" style="font-size:clamp(26px,4vw,44px);margin-bottom:10px;">
      <span data-key="s5_h1a">One step between you</span><br>
      <span data-key="s5_h1b">and </span><span class="gold" data-key="s5_gold">permanent income.</span>
    </h2>
    <p class="subtitle" style="font-size:15px;margin-bottom:24px;" data-key="s5_sub">Fill this in. RACE will contact you within 24 hours to activate your station and connect you to the network.</p>

    <form id="partner-form" onsubmit="submitForm(event)">
      <div class="form-row">
        <div class="form-group">
          <label class="form-label" data-key="f_name_label">Your name</label>
          <input class="form-input" type="text" id="f-name" required>
          <input type="hidden" id="f-name-placeholder" data-placeholder="Ahmad Abdullah">
        </div>
        <div class="form-group">
          <label class="form-label" data-key="f_station_label">Station name</label>
          <input class="form-input" type="text" id="f-station" required>
          <input type="hidden" id="f-station-placeholder" data-placeholder="Al-Noor Fuel Station">
        </div>
      </div>
      <div class="form-row">
        <div class="form-group">
          <label class="form-label" data-key="f_loc_label">Location</label>
          <select class="form-input" id="f-location" required>
            <option value="" data-key="f_loc_opt0">Select area</option>
            <option>Masif Road</option><option>Ankawa</option><option>Gulan Street</option>
            <option>60 Metre Road</option><option>Dream City</option><option>Bakhtiyari</option>
            <option>Ainkawa</option><option>Italian Village</option><option>Baharka</option>
            <option>Duhok Road</option><option>Kirkuk Road</option>
            <option data-key="other_erbil">Other Erbil</option>
            <option>Duhok</option><option>Sulaymaniyah</option>
          </select>
        </div>
        <div class="form-group">
          <label class="form-label" data-key="f_cars_label">Cars per day</label>
          <select class="form-input" id="f-cars" required>
            <option value="" data-key="f_cars_opt0">Select range</option>
            <option>50–100</option><option>100–200</option><option>200–350</option>
            <option>350–500</option><option>500+</option>
          </select>
        </div>
      </div>
      <div class="form-group">
        <label class="form-label" data-key="f_phone_label">WhatsApp number</label>
        <input class="form-input" type="tel" id="f-phone" required>
        <input type="hidden" id="f-phone-placeholder" data-placeholder="+964 770 000 0000">
      </div>
      <div class="form-row">
        <div class="form-group">
          <label class="form-label" data-key="f_emp_label">Pump employees?</label>
          <select class="form-input" id="f-employees">
            <option data-key="f_emp_1">Yes, several</option>
            <option data-key="f_emp_2">Yes, one or two</option>
            <option data-key="f_emp_3">I run it myself</option>
          </select>
        </div>
        <div class="form-group">
          <label class="form-label" data-key="f_pri_label">My priority</label>
          <select class="form-input" id="f-priority">
            <option data-key="f_pri_1">More revenue from traffic</option>
            <option data-key="f_pri_2">Driver loyalty</option>
            <option data-key="f_pri_3">Standing out vs competitors</option>
            <option data-key="f_pri_4">Passive income from referrals</option>
          </select>
        </div>
      </div>
      <div class="form-group">
        <label class="form-label" data-key="f_notes_label">Anything else? (optional)</label>
        <input class="form-input" type="text" id="f-notes">
        <input type="hidden" id="f-notes-placeholder" data-placeholder="Questions, or who referred you">
      </div>

      <input type="hidden" id="f-calc-cars">
      <input type="hidden" id="f-calc-year">
      <input type="hidden" id="f-ref-data">
      <input type="hidden" id="f-join-data">
      <input type="hidden" id="f-lang">
      <input type="hidden" id="f-timestamp">

      <button type="submit" class="submit-btn" id="submit-btn" data-key="f_submit">
        Activate My Station with RACE →
      </button>
      <div style="text-align:center;margin-top:14px;font-size:12px;color:var(--text-dim);" data-key="f_note">
        No payment now. RACE contacts you within 24 hours.
      </div>
    </form>

    <button class="btn-ghost" onclick="goTo(4)" style="margin-top:20px;"><span data-key="back">← Back</span></button>
  </div>
</div>

<!-- ═══════════════════════════ STEP 6 ═══════════════════════════ -->
<div class="step" id="step-6">
  <div class="wrap" style="text-align:center;align-items:center;">
    <div class="success-ring">
      <svg width="32" height="32" viewBox="0 0 32 32" fill="none">
        <path d="M8 16l6 6 10-12" stroke="var(--gold)" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
      </svg>
    </div>
    <div class="eyebrow" style="text-align:center;" data-key="s6_eyebrow">Welcome to the network</div>
    <h2 class="display" style="font-size:clamp(26px,4.5vw,48px);text-align:center;margin-bottom:14px;">
      <span data-key="s6_h1a">You just made</span><br>
      <span data-key="s6_h1b">the best decision</span><br>
      <span data-key="s6_h1c">for your </span><span class="gold" data-key="s6_gold">station.</span>
    </h2>
    <p class="subtitle" style="text-align:center;margin-bottom:36px;" data-key="s6_sub">
      RACE will call you on WhatsApp within 24 hours to activate your station. Your income starts the day your first driver scans.
    </p>
    <div class="stat-row" style="max-width:420px;margin-bottom:32px;">
      <div class="stat" style="text-align:center;">
        <div class="stat-val" id="confirm-income">5M+ IQD</div>
        <div class="stat-label" data-key="s6_stat1">Your projected year-one income from RACE</div>
      </div>
      <div class="stat" style="text-align:center;">
        <div class="stat-val">24h</div>
        <div class="stat-label" data-key="s6_stat2">Until RACE contacts you on WhatsApp</div>
      </div>
    </div>
    <div class="proof-bar" style="max-width:440px;">
      <div class="proof-dot"></div>
      <div class="proof-text" data-key="s6_proof">BM Oil activated in <strong>one day</strong>. <strong>430 members and growing</strong> in 30 days.</div>
    </div>
    <div style="margin-top:24px;font-size:13px;color:var(--text-muted);max-width:360px;line-height:1.6;" data-key="s6_footer">
      Every day you wait is a day your competitors could join first. The network effect rewards the first movers — and right now, there is still space in Erbil.
    </div>
  </div>
</div>

<script>
/* ════════════════════════════════════════
   TRANSLATIONS
════════════════════════════════════════ */
const T = {
  en: {
    live_label:'LIVE · ERBIL, KURDISTAN',
    s1_eyebrow:'For fuel station owners',
    s1_h1a:'Every car that leaves',s1_h1b:'your station',s1_h1c:'without joining',s1_h1d:'is money you lose forever.',
    s1_sub:'RACE turns every fill-up into a permanent income stream — for you, your employees, and your network. One system. No extra staff. No extra cost. The station starts working for you.',
    nr_title:'The income that never sleeps — even when drivers leave.',
    nr_sub:'RACE is not just about your station. When your members fuel anywhere in the RACE network, you still earn. Your income follows your drivers — everywhere.',
    nr_r1_label:'Members fuel at YOUR station',nr_r1_desc:'0.98% on every transaction goes to the RACE ecosystem',
    nr_r2_label:'Members fuel at ANY RACE partner station',nr_r2_desc:'You still earn — automatically. No action needed from you.',
    nr_r3_label:'Station you refer — every transaction',nr_r3_desc:'Permanent referral royalty. No ceiling. No expiry.',
    ghost1_h:'The "ghost driver" income.',
    ghost1_d:'A driver joins your network, moves away, starts fueling at another RACE station in Erbil, Duhok, or Sulaymaniyah. Most owners would call that a lost customer. You call it passive income. The 0.15% cross-network royalty means distance doesn\'t end your earnings.',
    ghost1_badge:'Your income travels with your network → forever',
    stat1:'Members activated at one station in 30 days',stat2:'Of members return to the same station — consistently',stat3:'When RACE members spend at your station — earned by you',
    s1_cta:'Show me how it works',
    s2_eyebrow:'The idea · in one breath',
    s2_h1a:'Spend fuel →',s2_h1b:'get ',s2_gold1:'protected',s2_h1c:'invite friends →',s2_gold2:'earn. Everywhere.',
    f1_t:'Driver fills up at your station',f1_d:'They scan, join RACE in 30 seconds. Your pump employee registers them and earns 0.20% of every transaction they generate — forever. Zero cost to you.',
    f2_t:'Instant emergency protection',f2_d:'Fuel, breakdown, towing — covered from the moment they join. This is the reason they stay. Protection is the invisible chain that keeps drivers loyal.',
    f3_t:'Your network goes everywhere',f3_d:'When your members fuel at ANY other RACE partner station in Kurdistan, you earn 0.15%. They leave your station — your income doesn\'t. This is the mechanic no other fuel loyalty system in the region has.',
    f4_t:'Refer a station. Earn forever.',f4_d:'Introduce another station owner to RACE. Earn 0.12% of every transaction at their station — permanently. One conversation. Lifetime income.',
    f5_t:'Join 11 active stations. Access 1,455 drivers.',f5_d:'When you join the RACE network, members from other stations can find and fuel at yours. New traffic arrives at your pump from drivers you\'ve never met — because your station is now part of something bigger.',
    s2_cta:'Calculate my numbers',
    s3_eyebrow:'Your station · estimated numbers',
    s3_h1a:'Move the sliders.',s3_h1b:'Watch your ',s3_gold:'income appear.',
    s3_sub:'Based on live data from active RACE stations. These are your numbers — not ours.',
    sl_cars:'Cars per day at my station',sl_fill:'Average fill-up amount',sl_conv:'Member conversion rate',
    res_members_label:'New members / month',res_network_label:'Network royalty / month*',res_year_label:'Your estimated income · year one',
    calc_note:'*Cross-network royalty (0.15%) estimated based on 11 active partner stations and 1,455 network drivers.',
    optional:'Optional',
    tog_refer:'I want to refer another station owner',tog_refer_badge:'+0.12% ROYALTY',
    ref_fixed_rate:'Referral royalty locked at 0.12% — permanent',
    sl_ref_cars:'Their station · cars per day',
    ref_mo_label:'Referral income / month',ref_yr_label:'Referral income / year',
    tog_join:'I want to connect to active RACE stations',tog_join_badge:'+NETWORK',
    join_fixed:'11 active stations · 1,455 drivers',expanding:'expanding',
    join_access_label:'Drivers your station accesses immediately',
    join_note:'These 1,455 drivers are already RACE members in the network. The day you activate, they can see and fuel at your station.',
    s3_cta:'See my 6-month roadmap',
    s4_eyebrow:'Your roadmap · from day one',
    s4_h1a:'The station that',s4_gold:'sells itself.',
    s4_sub:'This is exactly what happened inside the RACE ecosystem — at a station very similar to yours. The phases are predictable. The income is permanent.',
    tl1_t:'Your employee becomes your best asset',tl1_d:'One incentive conversation. Your pump employee registers every driver — 30 seconds per car. They earn 0.20% per transaction they generate. They stop being an employee and start being invested in your station\'s growth.',
    tl2_t:'500 members. Social proof ignites.',tl2_d:'WhatsApp groups start talking about your station. Drivers bring other drivers. The station has an identity — not just a price board. Other stations in Erbil cannot replicate this because it took time to build.',
    tl3_t:'Network compounding begins',tl3_d:'Each member brings 1.4 others. Growth is no longer linear. The flywheel turns without you — and the cross-network royalty means even members who fuel elsewhere are generating income for you.',
    gtb_eyebrow:'The mechanic your competitors don\'t have',
    gtb_h1:'A driver stops coming to your station.',gtb_h2:'You still earn from them. Forever.',
    gtb_body:'Most loyalty systems end the moment a customer leaves. RACE is different. When your network member fills up at any RACE partner station in Kurdistan — Erbil, Duhok, Sulaymaniyah — 0.15% of that transaction comes back to you. Automatically. Silently. Permanently.<br><br>This is not a discount scheme. This is not a points system. This is a <strong>royalty on human behavior</strong> — and humans always need fuel.',
    gtb_r1:'Cross-network royalty on every fill-up by your members at partner stations',
    gtb_r2:'No expiry. No cap. No re-approval. The royalty is written into the network — permanently.',
    gtb_r3:'Estimated monthly ghost-driver royalty based on your network size at month 3',
    tl4_t:'The station sells itself',tl4_d:'Every competitor in Erbil is still just a price on a board. You have thousands of verified drivers locked to your network — filling up at your station, and at partner stations where you still earn. This asset took time. It cannot be copied overnight.',
    tl5_t:'Referral royalties stack. Forever.',tl5_d:'Every station you refer earns you 0.12% of their total volume — permanently. Refer 5 stations. Earn from 5 networks. You become a node in the only verified automotive network in Kurdistan.',
    tl5_num:'Passive income ·',tl5_num2:' no ceiling',
    phase_push:'Manual push',phase_compound:'Compounding',phase_self:'Self-selling',
    s4_cta:'I\'m ready. Let\'s start.',
    s5_eyebrow:'Become a RACE partner',
    s5_h1a:'One step between you',s5_h1b:'and ',s5_gold:'permanent income.',
    s5_sub:'Fill this in. RACE will contact you within 24 hours to activate your station and connect you to the network.',
    f_name_label:'Your name',f_station_label:'Station name',f_loc_label:'Location',f_cars_label:'Cars per day',
    f_phone_label:'WhatsApp number',f_emp_label:'Pump employees?',f_pri_label:'My priority',f_notes_label:'Anything else? (optional)',
    f_loc_opt0:'Select area',f_cars_opt0:'Select range',
    f_emp_1:'Yes, several',f_emp_2:'Yes, one or two',f_emp_3:'I run it myself',
    f_pri_1:'More revenue from traffic',f_pri_2:'Driver loyalty',f_pri_3:'Standing out vs competitors',f_pri_4:'Passive income from referrals',
    other_erbil:'Other Erbil',
    f_submit:'Activate My Station with RACE →',
    f_note:'No payment now. RACE contacts you within 24 hours.',
    s6_eyebrow:'Welcome to the network',
    s6_h1a:'You just made',s6_h1b:'the best decision',s6_h1c:'for your ',s6_gold:'station.',
    s6_sub:'RACE will call you on WhatsApp within 24 hours to activate your station. Your income starts the day your first driver scans.',
    s6_stat1:'Your projected year-one income from RACE',s6_stat2:'Until RACE contacts you on WhatsApp',
    s6_proof:'BM Oil activated in <strong>one day</strong>. <strong>430 members and growing</strong> in 30 days.',
    s6_footer:'Every day you wait is a day your competitors could join first. The network effect rewards the first movers — and right now, there is still space in Erbil.',
    back:'← Back',
    cars_unit:' cars',fill_unit:' IQD',conv_unit:'%',
    f_name_ph:'Ahmad Abdullah',f_station_ph:'Al-Noor Fuel Station',f_phone_ph:'+964 770 000 0000',f_notes_ph:'Questions, or who referred you',
    sending:'Sending...'
  },
  ku: {
    live_label:'راستەوخو · هەولێر، کوردستان',
    s1_eyebrow:'بۆ خاوەنانی بنکەی بەنزین',
    s1_h1a:'هەر ئۆتۆمبێلێک کە دەروات',s1_h1b:'لە بنکەکەت',s1_h1c:'بەبێ تۆمارکردن',s1_h1d:'پارەیەکی بەردەوامە کە لەدەستیدەدەیت.',
    s1_sub:'رە یس هەر پڕکردنەوەیەک دەکات بە گەشەی داهاتی بەردەوام — بۆ تۆ، کارمەندەکانت، و تۆڕەکەت. یەک سیستەم. بەبێ کارمەندی زیادە. بەبێ تێچووی  زیادە.',
    nr_title:'داھاتێک کە هیج کاتێک ناخەوێت، گەشە کردن ناوەستێت .',
    nr_sub:'رە یس تەنها دەربارەی بنکەکەت نییە. کاتێک تۆڕەکەت لە هەر بنکەیەکی دیکە بەنزین پربکات، داهاتەکەت زیاتر دەبیت، دەرامەتت بە دوای شۆفێرەکانت دەچێت — لە هەموو شوێنێک.',
    nr_r1_label:'شۆفێری زیاتر دێنە ناو بەنزینخانەکەت',nr_r1_desc:'0.98% لە هەر مامەڵەیەک دەچێتە ئیکۆسیستەمی RACE',
    nr_r2_label:'کاتێک شۆفێرەکانت لە هەر بنکەیەکی دیکە بەنزین تێبکەن',nr_r2_desc:'هێشتا داهاتت زیاد دەبێت — ئوتۆماتیکی. پێویستی بە هیچ ماندووبون نیە.',
    nr_r3_label:'هەر بنکەیەکی دیکە کە لەژێڕ ناوت بێت ،هەر مامەڵەیەک بکات',nr_r3_desc:'پشکی داهاتی بەردەوام، لە هەموو مامەلەیەک کە لەو بنکەیە دەکرێت .',
    ghost1_h:'داهات لە شۆفێڕی شاراوە".',
    ghost1_d:'شۆفێرێک هاتە ناو تۆڕەکەت، دوایی دەروات و ناییتەوە، بەنزین تێدەکات لە بنکەیەکی دیکەی RACE لە هەولێر، دهۆک، یان سلێمانی، یان تەنانەت لە بنکەی تەنیشتت، زۆر خاوەن بنکە وا بیر دەکەنەوە کە کڕیارێکیان لەدەست داوە. تۆ بە داهاتی بەردەوام دەیبینی. 0.15% پشکی توویە،  ئەمە مانای وایە  کە دووری و نەهاتنەوەی کریار دەرامەتەکەت کەم ناکات.',
    ghost1_badge:'دەرامەتت بە دوای تۆڕەکەت دەچێت ← بەردەوام',
    stat1:'ئەندام چالاک کراون لە یەک بنکە لە ٣٠ ڕۆژ',stat2:'لە ئەندامان دەگەڕێنەوە بۆ هەمان بنکە — بە بەردەوامی',stat3:'کاتێک ئەندامانی RACE لە بنکەکەت خەرج دەکەن تەنها ٠.٩٨٪ خەرجی رەیس دەبیت',
    s1_cta:'پیشانم بدە چۆن کاردەکات',
    s2_eyebrow:'بیرۆکەکە · لە یەک رستەدا',
    s2_h1a:'بەنزین پڕ بکەرەوە ←',s2_h1b:'',s2_gold1:'پاراستن وەربگرە',s2_h1c:'هاوڕێ بانگ بکە ←',s2_gold2:'داهاتت زیاتر بکە. لە هەر شوێنێک.',
    f1_t:'شۆفێر لە بنکەکەت بەنزین پردەکات',f1_d:'سکانی رایس ی بنکەکەت دەکات، لە ١٠ چرکه جوینی  RACE دەکات. کارمەندی پمپەکەت تۆماری دەکات و 0.20% لە هەر مامەڵەیەک دەستکەوتی دەبێت — بەردەوام. بەبێ تێچوون لەلایەن تۆ.',
    f2_t:'پاراستنی شۆفێر لە کاتی کێشەدا',f2_d:' کێشەی میکانیکی، کڕێن — لە هەمو بەنزین پڕکردنیک بری پاراستنی رەیس زیاد دەبێت. ئەوەیە هۆکاری مانەوەیان. لە بری ٠.٩٨٪ ی رەیس بویان دابیندەکریت، پاراستنی رەیس هوکاریکی گرنگی گەرانەوەی شۆفێرە، کە شۆفێرەکان وفادار دەخاتەوە.',
    f3_t:'تۆڕەکەت دەچێتە هەموو شوێنێک',f3_d:'کاتێک ئەندامەکانت لە هەر بنکەیەکی هاوبەشی RACE لە کوردستان بەنزین پربکەنەوە، تۆ 0.15% دەستکەوت دەکەیت. هەتا ئەگەر شارەکەش جێبهێلن - داهاتت بەجێناهێلن. ئەمە مەکانیزمێکە کە هیچ سیستەمێک لەم ناوچەیەدا نەیگەیاندوە.',
    f4_t:'بنکەیەک بانگهێشتی رەیس بکە. بەردەوام داهات زیاد بکە.',f4_d:'خاوەن بنکەیەکی تر بناسێنە RACE. 0.12% لە هەر مامەڵەیەک لە بنکەکەی بدەستبێنە — بەردەوام. یەک گفتوگۆ. دەرامەتی تەمەن.',
    f5_t:'پەیوەندێ بە ١١ بنکەی چالاک. دەستگەیشتن بە ١٤٥٥+ شۆفێر.',f5_d:'کاتێک دەچیتە تۆڕی RACE، ئەندامانی بنکەکانی تر دەتوانن بنکەکەت بدۆزنەوە و بەنزین تێبکەن. قەڕەباڵغی نوێ دەگاتە پمپەکەت لە شۆفێرانێک کە هەرگیز نەتناسیون— چونکە بنکەکەت ئێستا بەشێکی شتێکی گەورەترە.',
    s2_cta:'ژمارەکانم حیساب بکە',
    s3_eyebrow:'بنکەکەت · ژمارەی خەمڵێندراو',
    s3_h1a:'سلایدەرەکان بجووڵێنە.',s3_h1b:'تەماشا بکە ',s3_gold:'داهاتەکەت دەردەکەوێت.',
    s3_sub:'بە پشتبەستن بە داتای راستی لە بنکەکانی چالاکی ئێستای RACE. ئەمانە ژمارەکانی تۆن — نەک ئێمە.',
    sl_cars:'ژمارەی ڕوژانەی ئۆتۆمبێل لە بنکەکەم',sl_fill:'بڕی ڕێژەی پرکردنەوە',sl_conv:'ڕێژەی گواستنەوەی شۆفێڕ بو ئەندامی تۆڕەکەت',
    res_members_label:'ئەندامی نوێ / مانگ',res_network_label:'پشکی تۆڕ / مانگ*',res_year_label:'داهاتی خەمڵێندراوی تۆ · ساڵی یەکەم',
    calc_note:'*پشکی تۆڕی تەواوکراو (0.15%) لەسەر بنەمای ١١ بنکەی هاوبەشی چالاک و ١٤٥٥ شۆفێری تۆڕ خەمڵێندراوە.',
    optional:'ئارەزووی',
    tog_refer:'دەمەوێت خاوەن بنکەیەکی تر بانگهێشتبکەم',tog_refer_badge:'+0.12% پشک ',
    ref_fixed_rate:'پشکی بانگهێشتکردن بو تو لەو بنکەیەی بانگهێشتی دەکەی/0.12% — بەردەوام',
    sl_ref_cars:'بنکەکەیان · ئۆتۆمبێل لە ڕۆژ',
    ref_mo_label:'داهاتی ناساندن / مانگ',ref_yr_label:'داهاتی ناساندن / ساڵ',
    tog_join:'دەمەوێت ببم بە بەشێک لە بنکەکانی چالاکی RACE',tog_join_badge:'+تۆڕ',
    join_fixed:'١١ بنکەی چالاک · ١٤٥٥ شۆفێر',expanding:'فراوانبووە',
    join_access_label:'شۆفێرانێک کە بنکەکەت لەکاتیدا جالاکبووندا دەبینن، وە هەر لە زیادبون دان',
    join_note:'ئەم ١٤٥٥ شۆفێرە ئێستا ئەندامانی RACE لە تۆڕەکەن. ئەو ڕۆژەی چالاک دەبیت، دەتوانن بنکەکەت بدۆزنەوە و ببن بە کریاری داهاتووت.',
    s3_cta:'داهاتووی ٦ مانگەکەم ببینە',
    s4_eyebrow:'داهاتووی ڕێگات · لە ڕۆژی یەکەم',
    s4_h1a:'بنکەیەک کە',s4_gold:'شانازی پێوە بکرێت.',
    s4_sub:'ئەمە ئەو راستییانەن لە ناو ئیکۆسیستەمی RACE ڕووی دا — لە بنکەیەکی زۆر هاوشێوەی تۆ. قۆناغەکان پێشبینیکراون. داهاتەکە بەردەوامە.',
    tl1_t:'کارمەندەکەت دەبێتە باشترین سەرمایەکەت',tl1_d:'یەک گفتوگۆی هاندەر. کارمەندی پمپەکەت هەر شۆفێرێک تۆمار دەکات — ٣٠ چرکه لە هەر ئۆتۆمبێلێک. 0.20% لە هەر مامەڵەیەک دەستکەوتی دەبێت. کارمەندێکی دڵخوشت دەبێت و دەبێتە وەبەرهێنان لە گەشەی بنکەکەت.',
    tl2_t:'٥٠٠ ئەندام. فراوانبوونی تور.',tl2_d:'گروپەکانی واتسئاپ دەست دەکەن بە قسەکردن دەربارەی بنکەکەت. شۆفێرەکان شۆفێرانی دیکە دەهێننە بنکەکە کە دیارن  — نەک تەنها تابلۆیەکی بێنرخ. بنکەکانی دیکەی هەولێر ناتوانن ئەمەیان ھەبێت چونکە درەنگ گەیشتن.',
    tl3_t:'گەشەی تۆڕ دەستپێدەکات',tl3_d:'هەر ئەندامێک بە ڕێژەیی ٢ کەسی دیکە دەهێنێت. گەشە ئیتر وەستانی نییە. چەرخێکە بەبێ تۆ دەسووڕێتەوە — و تۆڕەکەت تەنانەت لە شوێنی دیکە بەنزین پربکەن، داهاتەکە بۆ تۆ دروست دەبیت.',
    gtb_eyebrow:'مەکانیزمێک کە ڕکابەرەکانت پێی ناگەن',
    gtb_h1:'شۆفێرێک کە تەنانەت نایێتەوە  بەنزینخانەکەت.',gtb_h2:'هەر لێیان قازانج دەکەیت. بەردەوام.',
    gtb_body:'زۆربەی سیستەمەکان کۆتایی دێن کاتێک کڕیار دەڕوات. RACE جیاوازە. کاتێک ئەندامی تۆڕەکەت لە هەر بنکەیەکی هاوبەشی RACE لە کوردستان بەنزین پردەکات هەولێر، دهۆک، سلێمانی — 0.15% لەو مامەڵەیە دەگەڕێتەوە بۆ تۆ. بە ئوتوماتیکی. بە بێدەنگی. بەردەوام.<br><br>ئەمە سیستەمی داشکاندن نییە. ئەمە سیستەمی پوینت نییە. ئەمە <strong>رۆیالتی لەسەر ڕەفتاری مرۆڤ</strong>ە — و مرۆڤ هەرگیز پێویستی بە بەنزین ناوەستیت.',
    gtb_r1:'پشکی تووە کاتێک تۆڕەکەت لە بنکەکانی هاوبەش بەنزین پردەکەن.',
    gtb_r2:'بێ کۆتایی. بێ راوەستان. بێ دووبارە-پەسەندکردن.  تۆڕەکەت چەند زیاتڕ بێت، قازانجەکەت زیاترە، بەردەوام.',
    gtb_r3:' پشکی مانگانەی ئەو شوفێرانەی کە لە بانزینخانەکانی دی بەنزین تێدەکەن خەملێنراوە لەسەر فراوانکردنی تۆڕەکەت بو نمونە لە ٢ مانگ',
    tl4_t:'بنکەکەت خۆی خوی گەورە دەکات',tl4_d:'هەر ڕکابەرێک لە هەولێر هێشتا تەنها بەس بەنزین دەفروشێت. تۆ هەزاران شۆفێری پشتیوانیکراوت هەیە کە بەستراون بە تورەکەت،لە بنکەکەت بەنزین پردەکەن، و لە بنکەکانی هاوبەشی رەیس پربکەن تو هەر داهاتت بو دیت. ئەم سەرمایەیە کاتی پێویست بوو. کە رکابەرەکانت ناتوانن دووبارەی بکەنەوە.',
    tl5_t:'پشکی بانگهێشتکردنی بنکەیەکی دی، هەتا هەتا.',tl5_d:'هەر بنکەیەک کە بانگھێشتی دەکەیت 0.12% لە کۆی قەبارەکەیان دەبیت بۆ تۆ — بەردەوام. ٥ بنکە بانگھێشتبکە. لە ٥ تۆڕ کەسب بکە. دەبیتە یەکەک لە گەورەترین تۆڕی ئۆتۆمبێلی پشتیوانیکردن لە کوردستان.',
    tl5_num:'دەرامەتی بەردەوام ·',tl5_num2:' بە رونی',
    phase_push:'دانانی دەستی',phase_compound:'دووبارەبوونەوە',phase_self:'خۆفرۆشتن',
    s4_cta:'ئامادەم. با دەستپێ بکەین.',
    s5_eyebrow:'ببە هاوبەشی RACE',
    s5_h1a:'یەک هەنگاو',s5_h1b:'لەنێوانت و ',s5_gold:'دەرامەتی بەردەوام.',
    s5_sub:'ئەمە پڕبکەرەوە. RACE لە ٢٤ کاتژمێر پەیوەندیت پێووە دەکات بۆ چالاککردنی بنکەکەت و فراوانکردنی تورەکەت.',
    f_name_label:'ناوت',f_station_label:'ناوی بنکە',f_loc_label:'شوێن',f_cars_label:'ئۆتۆمبێل لە ڕۆژ',
    f_phone_label:'ژمارەی واتسئاپ',f_emp_label:'کارمەندی پمپ؟',f_pri_label:'ئامانجی من',f_notes_label:'شتی تر؟ (ئارەزووی)',
    f_loc_opt0:'ناوچە هەڵبژێرە',f_cars_opt0:'ڕێنج هەڵبژێرە',
    f_emp_1:'بەڵێ، چەندان',f_emp_2:'بەڵێ، یەک یان دوو',f_emp_3:'خۆم بەڕێوەی دەبەم',
    f_pri_1:'دەرامەتی زیاتر لە ترافیک',f_pri_2:'وفاداری شۆفێر',f_pri_3:'جیاوازبوون لە ڕکابەر',f_pri_4:'دەرامەتی بەردەوام لە ناساندن',
    other_erbil:'شۆێنی دیکە',
    f_submit:'بنکەکەم بە RACE چالاک بکە ←',
    f_note:'هیج پارەدانەک نییە. RACE لە ٢٤ کاتژمێر پەیوەندیت دەکات.',
    s6_eyebrow:'بەخێربێیت بۆ تۆڕەکە',
    s6_h1a:'ئێستا باشترین',s6_h1b:'بڕیاری تەمەنت',s6_h1c:'دا بۆ',s6_gold:'بنکەکەت.',
    s6_sub:'RACE لە ٢٤ کاتژمێر لە سەر واتسئاپ پەیوەندیت پێوە دەکات بۆ چالاککردنی بنکەکەت. دەرامەتەکەت دەست پێدەکات ئەو ڕۆژەی یەکەم شۆفێر سکان دەکات.',
    s6_stat1:'دەرامەتی خەمڵێندراوی ساڵی یەکەمت لە RACE',s6_stat2:'تا RACE لە واتسئاپ پەیوەندیت دەکات',
    s6_proof:'BM Oil لە <strong>یەک ڕۆژ</strong> چالاک کرا. <strong>٤٣٠ ئەندام و بەردەوام زیاددەبن</strong> لە ٣٠ ڕۆژ.',
    s6_footer:'هەر ڕۆژێک چاوەڕوانی دەکەیت ڕۆژێکی دیکەیە کە ڕکابەرەکانت دەتوانن پێش تۆ بکەون. کاریگەری تۆڕ یەکەمەکان پاداشت دەکات— و ئێستا هێشتا شوێن هەیە لە هەولێر.',
    back:'← گەڕانەوە',
    cars_unit:' ئۆتۆمبێل',fill_unit:' دینار',conv_unit:'%',
    f_name_ph:'ئەحمەد عەبدوڵڵا',f_station_ph:'بنکەی  ئەلنوور',f_phone_ph:'+964 770 000 0000',f_notes_ph:'پرسیار، یان ناوی کەسێک کە بانگهێشتی دەکەیت',
    sending:'دەنێردرێت...'
  },
  ar: {
    live_label:'مباشر · أربيل، كوردستان',
    s1_eyebrow:'لأصحاب محطات الوقود',
    s1_h1a:'كل سيارة تغادر',s1_h1b:'محطتك',s1_h1c:'بدون انضمام',s1_h1d:'هي أموال تخسرها إلى الأبد.',
    s1_sub:'RACE يحوّل كل عملية تعبئة إلى تدفق دخل دائم — لك، ولموظفيك، ولشبكتك. نظام واحد. بدون موظفين إضافيين. بدون تكاليف إضافية.',
    nr_title:'الدخل الذي لا ينام — حتى عندما يغادر السائقون.',
    nr_sub:'RACE ليس فقط عن محطتك. عندما يتزود أعضاؤك بالوقود في أي مكان في شبكة RACE، تظل تكسب. دخلك يتبع سائقيك — في كل مكان.',
    nr_r1_label:'الأعضاء يتزودون في محطتك',nr_r1_desc:'0.98% من كل معاملة تذهب إلى منظومة RACE',
    nr_r2_label:'الأعضاء يتزودون في أي محطة شريكة',nr_r2_desc:'ما زلت تكسب — تلقائياً. لا حاجة لأي إجراء منك.',
    nr_r3_label:'المحطة التي تقدمها — كل معاملة',nr_r3_desc:'عائد إحالة دائم. بلا سقف. بلا انتهاء.',
    ghost1_h:'دخل "السائق الشبح".',
    ghost1_d:'سائق ينضم لشبكتك، يغادر، ويبدأ التزود في محطة RACE أخرى في أربيل أو دهوك أو السليمانية. معظم الأصحاب سيقولون إنهم خسروا زبوناً. أنت تسميه دخلاً سلبياً. عائد 0.15% عبر الشبكة يعني أن البُعد لا ينهي أرباحك.',
    ghost1_badge:'دخلك يتبع شبكتك ← إلى الأبد',
    stat1:'عضو تم تفعيله في محطة واحدة خلال 30 يوماً',stat2:'من الأعضاء يعودون لنفس المحطة — باستمرار',stat3:'عندما يصرف أعضاء RACE في محطتك — من نصيبك',
    s1_cta:'أرني كيف يعمل',
    s2_eyebrow:'الفكرة · في نفس واحد',
    s2_h1a:'اشحن الوقود ←',s2_h1b:'',s2_gold1:'احصل على حماية',s2_h1c:'ادعُ أصدقاء ←',s2_gold2:'اكسب. في كل مكان.',
    f1_t:'السائق يتزود في محطتك',f1_d:'يسجل، ينضم لـ RACE في 30 ثانية. موظف المضخة يسجله ويكسب 0.20% من كل معاملة يولدها — إلى الأبد. بدون تكلفة عليك.',
    f2_t:'حماية طارئة فورية',f2_d:'وقود، أعطال، سحب — مغطى من لحظة الانضمام. هذا هو سبب بقائهم. الحماية هي السلسلة غير المرئية التي تبقي السائقين أوفياء.',
    f3_t:'شبكتك تذهب في كل مكان',f3_d:'عندما يتزود أعضاؤك في أي محطة شريكة في كوردستان، تكسب 0.15%. يغادرون محطتك — دخلك لا يغادر. هذه هي الآلية التي لا يمتلكها أي نظام ولاء وقود آخر في المنطقة.',
    f4_t:'قدم محطة. اكسب إلى الأبد.',f4_d:'عرّف صاحب محطة آخر بـ RACE. اكسب 0.12% من كل معاملة في محطته — بشكل دائم. محادثة واحدة. دخل مدى الحياة.',
    f5_t:'انضم لـ 11 محطة نشطة. وصول لـ 1,455 سائق.',f5_d:'عندما تنضم لشبكة RACE، يمكن لأعضاء من المحطات الأخرى العثور على محطتك والتزود فيها. حركة مرور جديدة تصل لمضختك من سائقين لم تقابلهم قط — لأن محطتك أصبحت جزءاً من شيء أكبر.',
    s2_cta:'احسب أرقامي',
    s3_eyebrow:'محطتك · أرقام تقديرية',
    s3_h1a:'حرّك الأشرطة.',s3_h1b:'شاهد ',s3_gold:'دخلك يظهر.',
    s3_sub:'بناءً على بيانات حية من محطات RACE النشطة. هذه أرقامك — وليست أرقامنا.',
    sl_cars:'سيارات يومياً في محطتي',sl_fill:'متوسط مبلغ التعبئة',sl_conv:'معدل تحويل الأعضاء',
    res_members_label:'أعضاء جدد / شهر',res_network_label:'عائد الشبكة / شهر*',res_year_label:'دخلك التقديري · السنة الأولى',
    calc_note:'*عائد الشبكة الشامل (0.15%) تقديري بناءً على 11 محطة شريكة نشطة و1,455 سائقاً في الشبكة.',
    optional:'اختياري',
    tog_refer:'أريد تقديم صاحب محطة آخر',tog_refer_badge:'+0.12% عائد',
    ref_fixed_rate:'عائد الإحالة ثابت عند 0.12% — دائم',
    sl_ref_cars:'محطتهم · سيارات يومياً',
    ref_mo_label:'دخل الإحالة / شهر',ref_yr_label:'دخل الإحالة / سنة',
    tog_join:'أريد الاتصال بمحطات RACE النشطة',tog_join_badge:'+شبكة',
    join_fixed:'11 محطة نشطة · 1,455 سائق',expanding:'توسعة',
    join_access_label:'السائقون الذين تصل إليهم محطتك فوراً',
    join_note:'هؤلاء الـ 1,455 سائق أعضاء RACE بالفعل في الشبكة. يوم تفعيلك، يمكنهم العثور على محطتك والتزود فيها.',
    s3_cta:'أرِني خارطة الطريق لـ 6 أشهر',
    s4_eyebrow:'خارطة طريقك · من اليوم الأول',
    s4_h1a:'المحطة التي',s4_gold:'تبيع نفسها.',
    s4_sub:'هذا بالضبط ما حدث داخل منظومة RACE — في محطة شبيهة جداً بمحطتك. المراحل متوقعة. الدخل دائم.',
    tl1_t:'موظفك يصبح أفضل أصولك',tl1_d:'محادثة حوافز واحدة. موظف المضخة يسجل كل سائق — 30 ثانية لكل سيارة. يكسب 0.20% لكل معاملة يولدها. يتوقف عن كونه موظفاً ويصبح مستثمراً في نمو محطتك.',
    tl2_t:'500 عضو. الإثبات الاجتماعي يشتعل.',tl2_d:'مجموعات واتساب تبدأ بالحديث عن محطتك. السائقون يجلبون سائقين آخرين. المحطة لها هوية — وليس فقط لوحة أسعار. المحطات الأخرى في أربيل لا تستطيع تكرار هذا لأنه استغرق وقتاً.',
    tl3_t:'التراكب الشبكي يبدأ',tl3_d:'كل عضو يجلب 1.4 آخرين. النمو لم يعد خطياً. الدولاب يدور بدونك — وعائد الشبكة الشامل يعني حتى الأعضاء الذين يتزودون في مكان آخر يولدون لك دخلاً.',
    gtb_eyebrow:'الآلية التي لا يمتلكها منافسوك',
    gtb_h1:'سائق يتوقف عن القدوم لمحطتك.',gtb_h2:'ما زلت تكسب منه. إلى الأبد.',
    gtb_body:'معظم أنظمة الولاء تنتهي عندما يغادر العميل. RACE مختلف. عندما يتزود عضو شبكتك في أي محطة شريكة في كوردستان — أربيل، دهوك، السليمانية — 0.15% من تلك المعاملة تعود إليك. تلقائياً. بصمت. بشكل دائم.<br><br>هذا ليس نظام خصومات. هذا ليس نظام نقاط. هذا <strong>عائد على السلوك البشري</strong> — والبشر يحتاجون الوقود دائماً.',
    gtb_r1:'عائد الشبكة الشامل على كل تعبئة بواسطة أعضائك في المحطات الشريكة',
    gtb_r2:'بلا انتهاء. بلا سقف. بلا إعادة موافقة. العائد مكتوب في الشبكة — بشكل دائم.',
    gtb_r3:'العائد الشهري التقديري لسائق الشبح بناءً على حجم شبكتك في الشهر 3',
    tl4_t:'المحطة تبيع نفسها',tl4_d:'كل منافس في أربيل ما زال مجرد لوحة أسعار. أنت تملك آلاف السائقين الموثقين المرتبطين بشبكتك — يتزودون في محطتك، وفي محطات شريكة حيث ما زلت تكسب. هذا الأصل احتاج وقتاً. لا يمكن نسخه بين عشية وضحاها.',
    tl5_t:'عوائد الإحالة تتراكم. إلى الأبد.',tl5_d:'كل محطة تقدمها تدر لك 0.12% من إجمالي حجمها — بشكل دائم. قدم 5 محطات. اكسب من 5 شبكات. تصبح عقدة في الشبكة الأتوموبيلية الموثقة الوحيدة في كوردستان.',
    tl5_num:'دخل سلبي ·',tl5_num2:' بلا سقف',
    phase_push:'دفع يدوي',phase_compound:'تراكم',phase_self:'بيع ذاتي',
    s4_cta:'أنا مستعد. لنبدأ.',
    s5_eyebrow:'كن شريك RACE',
    s5_h1a:'خطوة واحدة بينك',s5_h1b:'وبين ',s5_gold:'دخل دائم.',
    s5_sub:'املأ هذا. RACE سيتصل بك خلال 24 ساعة لتفعيل محطتك وربطك بالشبكة.',
    f_name_label:'اسمك',f_station_label:'اسم المحطة',f_loc_label:'الموقع',f_cars_label:'سيارات يومياً',
    f_phone_label:'رقم واتساب',f_emp_label:'موظفو المضخة؟',f_pri_label:'أولويتي',f_notes_label:'أي شيء آخر؟ (اختياري)',
    f_loc_opt0:'اختر المنطقة',f_cars_opt0:'اختر النطاق',
    f_emp_1:'نعم، عدة',f_emp_2:'نعم، واحد أو اثنان',f_emp_3:'أدير بنفسي',
    f_pri_1:'المزيد من الدخل من الزيارات',f_pri_2:'ولاء السائق',f_pri_3:'التميز عن المنافسين',f_pri_4:'الدخل السلبي من الإحالات',
    other_erbil:'أربيل أخرى',
    f_submit:'فعّل محطتي مع RACE ←',
    f_note:'لا دفع الآن. RACE يتصل بك خلال 24 ساعة.',
    s6_eyebrow:'مرحباً بك في الشبكة',
    s6_h1a:'لقد اتخذت للتو',s6_h1b:'أفضل قرار',s6_h1c:'لـ',s6_gold:'محطتك.',
    s6_sub:'RACE سيتصل بك على واتساب خلال 24 ساعة لتفعيل محطتك. دخلك يبدأ اليوم الذي يسجل فيه أول سائق.',
    s6_stat1:'دخلك التقديري للسنة الأولى من RACE',s6_stat2:'حتى يتصل بك RACE على واتساب',
    s6_proof:'BM Oil تم تفعيله في <strong>يوم واحد</strong>. <strong>430 عضو وما زال يتزايد</strong> في 30 يوماً.',
    s6_footer:'كل يوم تنتظر هو يوم قد يسبقك فيه منافسوك. تأثير الشبكة يكافئ من يتحرك أولاً — والآن ما زال هناك مجال في أربيل.',
    back:'← رجوع',
    cars_unit:' سيارة',fill_unit:' دينار',conv_unit:'%',
    f_name_ph:'أحمد عبدالله',f_station_ph:'محطة النور للوقود',f_phone_ph:'+964 770 000 0000',f_notes_ph:'أسئلة، أو من أحالك',
    sending:'جاري الإرسال...'
  }
};

/* ════════════════════════════════════════
   LANG SYSTEM
════════════════════════════════════════ */
let lang = 'en';

function setLang(l) {
  lang = l;
  const isRTL = (l === 'ar' || l === 'ku');
  document.documentElement.setAttribute('lang', l);
  document.documentElement.setAttribute('dir', isRTL ? 'rtl' : 'ltr');

  ['btn-en','btn-ku','btn-ar'].forEach(id => document.getElementById(id).classList.remove('active'));
  document.getElementById('btn-' + l).classList.add('active');

  const t = T[l];
  // Update all data-key elements
  document.querySelectorAll('[data-key]').forEach(el => {
    const k = el.getAttribute('data-key');
    if (t[k] !== undefined) {
      el.innerHTML = t[k];
    }
  });

  // Placeholders
  const phMap = {
    'f-name': t.f_name_ph,
    'f-station': t.f_station_ph,
    'f-phone': t.f_phone_ph,
    'f-notes': t.f_notes_ph
  };
  Object.entries(phMap).forEach(([id, ph]) => {
    const el = document.getElementById(id);
    if (el) el.setAttribute('placeholder', ph);
  });

  // RTL adjustments for step dots and logo
  const dots = document.getElementById('dots');
  const logo = document.getElementById('logo-mark') || document.querySelector('.logo-mark');
  if (isRTL) {
    if (dots) { dots.style.right = 'auto'; dots.style.left = '24px'; }
    if (logo) { logo.style.right = 'auto'; logo.style.left = '24px'; }
  } else {
    if (dots) { dots.style.left = 'auto'; dots.style.right = '24px'; }
    if (logo) { logo.style.left = '24px'; logo.style.right = 'auto'; }
  }

  // Kurdish font note for display
  if (l === 'ku') {
    document.querySelectorAll('.display').forEach(el => {
      el.style.fontFamily = "'DM Sans', Tahoma, Arial, sans-serif";
      el.style.letterSpacing = '0';
      el.style.lineHeight = '1.2';
    });
  } else if (l === 'ar') {
    document.querySelectorAll('.display').forEach(el => {
      el.style.fontFamily = "'DM Sans', 'Segoe UI', Tahoma, Arial, sans-serif";
      el.style.letterSpacing = '0';
      el.style.lineHeight = '1.2';
    });
  } else {
    document.querySelectorAll('.display').forEach(el => {
      el.style.fontFamily = "'Cormorant Garamond', serif";
      el.style.letterSpacing = '-0.02em';
      el.style.lineHeight = '1.0';
    });
  }

  calcAll();
}

/* ════════════════════════════════════════
   NAVIGATION
════════════════════════════════════════ */
const TOTAL_STEPS = 6;
let currentStep = 1;
let refOpen = false;
let joinOpen = false;

function goTo(n) {
  document.getElementById('step-' + currentStep).classList.remove('active');
  currentStep = n;
  document.getElementById('step-' + n).classList.add('active');
  updateChrome();
  window.scrollTo(0, 0);
  if (n === 4) setTimeout(animateTimeline, 200);
  if (n === 3) calcAll();
}

function updateChrome() {
  const pct = ((currentStep - 1) / (TOTAL_STEPS - 1)) * 100;
  document.getElementById('progress').style.width = pct + '%';
  const dotsEl = document.getElementById('dots');
  dotsEl.innerHTML = '';
  for (let i = 1; i <= TOTAL_STEPS; i++) {
    const d = document.createElement('div');
    d.className = 'dot' + (i === currentStep ? ' active' : i < currentStep ? ' done' : '');
    dotsEl.appendChild(d);
  }
}

/* ════════════════════════════════════════
   CALCULATOR
════════════════════════════════════════ */
function fmt(n) { return Math.round(n).toLocaleString(); }
function fmtK(n) {
  if (n >= 1000000) return (n / 1000000).toFixed(1) + 'M';
  if (n >= 1000) return Math.round(n / 1000) + 'K';
  return Math.round(n).toString();
}

function calcAll() {
  const t = T[lang];
  const cars = parseInt(document.getElementById('r-cars').value);
  const fill = parseInt(document.getElementById('r-fill').value);
  const conv = parseInt(document.getElementById('r-conv').value) / 100;

  document.getElementById('v-cars').textContent = cars + (t.cars_unit || ' cars');
  document.getElementById('v-fill').textContent = fmt(fill) + (t.fill_unit || ' IQD');
  document.getElementById('v-conv').textContent = Math.round(conv * 100) + (t.conv_unit || '%');

  // Core calc
  const newPerDay = Math.round(cars * conv);
  const retRate = 0.68;
  const activeMembers = Math.round(newPerDay * 30 * retRate);
  const txPerMonth = activeMembers * 4;
  const monthlyVol = txPerMonth * fill;

  // Network royalty: 1455 drivers * avg 4 tx/mo * avg fill * 0.15%
  const networkRoyaltyMo = 1455 * 4 * fill * 0.0015;

  // Year income = station income + network royalty * 12
  const stationIncomeMo = monthlyVol * 0.0098;
  const totalYearIncome = (stationIncomeMo + networkRoyaltyMo) * 12;

  document.getElementById('res-members').textContent = fmt(activeMembers);
  document.getElementById('res-network').textContent = fmtK(networkRoyaltyMo) + (t.fill_unit || ' IQD');
  document.getElementById('res-year').textContent = fmtK(totalYearIncome) + (t.fill_unit || ' IQD');

  // Roadmap numbers
  if (document.getElementById('roadmap-w1')) {
    document.getElementById('roadmap-w1').textContent = '+' + newPerDay + (t.cars_unit || ' cars');
    document.getElementById('roadmap-w6').textContent = '~' + fmt(Math.round(newPerDay * 42 * retRate));
    document.getElementById('roadmap-m3').textContent = '~' + fmt(Math.round(activeMembers * 2.4));
    document.getElementById('roadmap-m6').textContent = fmt(Math.round(activeMembers * 6.5)) + '+';
  }

  // Ghost driver monthly at month 3
  const m3Members = Math.round(activeMembers * 2.4);
  const ghostMo = m3Members * 4 * fill * 0.0015;
  if (document.getElementById('ghost-monthly')) {
    document.getElementById('ghost-monthly').textContent = fmtK(ghostMo) + (t.fill_unit || ' IQD') + '/mo';
  }

  // Referral calc
  if (refOpen) {
    const refCars = parseInt(document.getElementById('r-ref-cars').value);
    document.getElementById('v-ref-cars').textContent = refCars + (t.cars_unit || ' cars');
    const refMembers = Math.round(refCars * conv * 30 * retRate);
    const refVol = refMembers * 4 * fill;
    const refMo = refVol * 0.0012; // locked at 0.12%
    document.getElementById('res-ref-mo').textContent = fmtK(refMo) + (t.fill_unit || ' IQD');
    document.getElementById('res-ref-yr').textContent = fmtK(refMo * 12) + (t.fill_unit || ' IQD');
    document.getElementById('f-ref-data').value = 'Referral royalty: ' + fmtK(refMo) + '/mo';
  }

  // Confirm income on step 6
  const confirmEl = document.getElementById('confirm-income');
  if (confirmEl) confirmEl.textContent = fmtK(totalYearIncome) + (t.fill_unit || ' IQD');

  // Store hidden form fields
  document.getElementById('f-calc-cars').value = cars;
  document.getElementById('f-calc-year').value = fmtK(totalYearIncome) + (t.fill_unit || ' IQD') + '/year';
  document.getElementById('f-lang').value = lang;
}

/* ════════════════════════════════════════
   TOGGLES
════════════════════════════════════════ */
function toggleReferral() {
  refOpen = !refOpen;
  document.getElementById('ref-track').classList.toggle('on', refOpen);
  document.getElementById('ref-expanded').classList.toggle('show', refOpen);
  calcAll();
}

function toggleJoin() {
  joinOpen = !joinOpen;
  document.getElementById('join-track').classList.toggle('on', joinOpen);
  document.getElementById('join-expanded').classList.toggle('show', joinOpen);
  document.getElementById('f-join-data').value = joinOpen ? '11 stations · 1455 drivers' : '';
}

/* ════════════════════════════════════════
   TIMELINE
════════════════════════════════════════ */
function animateTimeline() {
  document.querySelectorAll('.tl-item').forEach((item, i) => {
    setTimeout(() => item.classList.add('visible'), i * 160);
  });
}

/* ════════════════════════════════════════
   FORM SUBMIT
════════════════════════════════════════ */
function submitForm(e) {
  e.preventDefault();
  const btn = document.getElementById('submit-btn');
  const t = T[lang];
  btn.disabled = true;
  btn.textContent = t.sending || 'Sending...';
  document.getElementById('f-timestamp').value = new Date().toISOString();

  const data = {
    name: document.getElementById('f-name').value,
    station: document.getElementById('f-station').value,
    location: document.getElementById('f-location').value,
    cars_range: document.getElementById('f-cars').value,
    phone: document.getElementById('f-phone').value,
    employees: document.getElementById('f-employees').value,
    priority: document.getElementById('f-priority').value,
    notes: document.getElementById('f-notes').value,
    calc_cars_per_day: document.getElementById('f-calc-cars').value,
    calc_year_income: document.getElementById('f-calc-year').value,
    referral_data: document.getElementById('f-ref-data').value,
    join_network: document.getElementById('f-join-data').value,
    language: document.getElementById('f-lang').value,
    timestamp: document.getElementById('f-timestamp').value,
    source: 'RACE Partner Flow v2'
  };

  console.log('RACE Lead:', data);

  // ── REPLACE WITH YOUR GOOGLE SHEET WEBHOOK URL ──
  const WEBHOOK_URL = 'YOUR_GOOGLE_SHEET_WEBHOOK_URL_HERE';

  const finish = () => {
    calcAll(); // ensure confirm-income is populated
    goTo(6);
    btn.disabled = false;
    btn.textContent = t.f_submit || 'Activate →';
  };

  if (WEBHOOK_URL === 'YOUR_GOOGLE_SHEET_WEBHOOK_URL_HERE') {
    setTimeout(finish, 1000);
    return;
  }

  fetch(WEBHOOK_URL, {
    method: 'POST',
    mode: 'no-cors',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify(data)
  }).then(finish).catch(finish);
}

/* ════════════════════════════════════════
   INIT
════════════════════════════════════════ */
updateChrome();
calcAll();
</script>
</body>
</html>
