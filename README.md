<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>Akash Kourav — BI Analyst & Power BI Developer</title>
<link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&family=Syne:wght@400;500;600;700;800&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<style>
*,*::before,*::after{margin:0;padding:0;box-sizing:border-box;}
:root{
  /* Light theme base */
  --bg:#f0f4ff;
  --bg2:#ffffff;
  --bg3:#e8eeff;
  --bg4:#dde5ff;
  /* Primary palette — purple/blue gradient from image */
  --primary:#5b4df5;
  --primary2:#7c6ff7;
  --primary3:#a599ff;
  --secondary:#3b82f6;
  --accent:#06b6d4;
  --green:#10b981;
  --amber:#f59e0b;
  --rose:#f43f5e;
  /* Gradient hero colors */
  --grad-start:#4f46e5;
  --grad-mid:#7c3aed;
  --grad-end:#2563eb;
  /* Text */
  --text:#0f172a;
  --text2:#1e293b;
  --muted:#64748b;
  --muted2:#94a3b8;
  --card:#ffffff;
  --border:#e2e8f0;
  --border2:#cbd5e1;
  --glass:rgba(255,255,255,0.7);
  --shadow:0 4px 24px rgba(79,70,229,0.08);
  --shadow-lg:0 16px 48px rgba(79,70,229,0.14);
  --radius:16px;
  --radius-sm:10px;
}
html{scroll-behavior:smooth;}
body{background:var(--bg);color:var(--text);font-family:'Plus Jakarta Sans',sans-serif;overflow-x:hidden;min-width:1280px;}

/* ── NAV ── */
nav{display:flex;align-items:center;gap:1rem;padding:0 2.5rem;height:62px;position:fixed;top:0;left:0;right:0;z-index:300;background:rgba(255,255,255,0.9);backdrop-filter:blur(20px);border-bottom:1px solid var(--border);box-shadow:0 1px 12px rgba(79,70,229,0.07);}
.nav-brand{display:flex;align-items:center;gap:.65rem;flex-shrink:0;margin-right:.5rem;}
.nav-logo{width:36px;height:36px;border-radius:10px;background:linear-gradient(135deg,var(--primary),var(--secondary));display:flex;align-items:center;justify-content:center;font-weight:800;font-size:.72rem;color:#fff;font-family:'Syne',sans-serif;letter-spacing:.02em;box-shadow:0 4px 12px rgba(91,77,245,0.35);}
.nav-name{font-weight:700;font-size:.88rem;font-family:'Syne',sans-serif;letter-spacing:.01em;color:var(--text);}
.nav-subtitle{font-size:.62rem;color:var(--muted);font-weight:500;}
.nav-brand-text{display:flex;flex-direction:column;}
.nav-tabs{display:flex;align-items:center;gap:.06rem;background:var(--bg3);border:1px solid var(--border);border-radius:12px;padding:.22rem;flex:1;overflow-x:auto;scrollbar-width:none;}
.nav-tabs::-webkit-scrollbar{display:none;}
.nav-tab{padding:.3rem .85rem;border-radius:9px;color:var(--muted);font-size:.73rem;font-weight:600;cursor:pointer;border:none;background:transparent;transition:all .18s;white-space:nowrap;font-family:'Plus Jakarta Sans',sans-serif;letter-spacing:.01em;}
.nav-tab:hover{color:var(--primary);background:rgba(91,77,245,0.07);}
.nav-tab.active{background:linear-gradient(135deg,var(--primary),var(--secondary));color:#fff;box-shadow:0 3px 10px rgba(91,77,245,0.3);}
.nav-actions{display:flex;align-items:center;gap:.5rem;flex-shrink:0;}
.socials-nav{display:flex;gap:.35rem;align-items:center;margin-right:.2rem;}
.soc-n{width:32px;height:32px;border-radius:9px;display:flex;align-items:center;justify-content:center;text-decoration:none;font-weight:700;font-size:.65rem;transition:all .18s;color:#fff;flex-shrink:0;box-shadow:0 2px 8px rgba(0,0,0,0.12);}
.soc-n:hover{transform:translateY(-2px) scale(1.08);box-shadow:0 6px 16px rgba(0,0,0,0.18);}
.soc-li{background:#0077b5;}.soc-gh{background:#24292e;}.soc-em{background:var(--primary);}.soc-wa{background:#25d366;}
.btn-edit{display:inline-flex;align-items:center;gap:.28rem;padding:.35rem .85rem;border-radius:9px;border:1.5px solid var(--border2);cursor:pointer;font-family:'Plus Jakarta Sans',sans-serif;font-weight:600;font-size:.69rem;background:var(--bg2);color:var(--muted);transition:all .18s;}
.btn-edit:hover{color:var(--primary);border-color:var(--primary);background:rgba(91,77,245,0.05);}
.btn-edit.unlocked{background:rgba(16,185,129,.08);color:#059669;border-color:rgba(16,185,129,.3);}
.btn-resume{background:linear-gradient(135deg,var(--primary),var(--secondary));color:#fff;padding:.35rem 1rem;border-radius:9px;font-weight:700;font-size:.72rem;display:inline-flex;align-items:center;gap:.28rem;transition:all .18s;border:none;cursor:pointer;font-family:'Plus Jakarta Sans',sans-serif;box-shadow:0 4px 14px rgba(91,77,245,0.35);}
.btn-resume:hover{transform:translateY(-1px);box-shadow:0 8px 22px rgba(91,77,245,0.42);}

/* ── PAGES ── */
.page{display:none;animation:fade .22s ease;padding-top:62px;}
.page.active{display:block;}
@keyframes fade{from{opacity:0;transform:translateY(6px);}to{opacity:1;transform:none;}}

/* ── HERO ── */
.hero{
  min-height:calc(100vh - 62px);
  display:grid;
  grid-template-columns:320px 1fr 380px;
  gap:2rem;
  padding:1.8rem 2.5rem 2rem;
  align-items:start;
  position:relative;
  overflow:hidden;
  max-width:100%;
}
.hero::before{content:'';position:absolute;width:700px;height:700px;border-radius:50%;background:radial-gradient(circle,rgba(91,77,245,.06) 0%,transparent 70%);top:-200px;right:-100px;pointer-events:none;}
.hero::after{content:'';position:absolute;width:400px;height:400px;border-radius:50%;background:radial-gradient(circle,rgba(59,130,246,.05) 0%,transparent 70%);bottom:-100px;left:-60px;pointer-events:none;}

/* LEFT */
.hero-left{z-index:2;display:flex;flex-direction:column;gap:1rem;position:sticky;top:80px;}
.info-panel{background:var(--bg2);border:1px solid var(--border);border-radius:var(--radius);padding:1.3rem;box-shadow:var(--shadow);}
.info-panel-title{font-size:.58rem;letter-spacing:.13em;text-transform:uppercase;color:var(--primary);font-weight:700;margin-bottom:.9rem;display:flex;align-items:center;gap:.4rem;}
.info-panel-title::before{content:'';width:14px;height:2px;background:linear-gradient(90deg,var(--primary),var(--secondary));border-radius:2px;}
.info-item{display:flex;align-items:center;gap:.7rem;padding:.5rem .65rem;border-radius:10px;background:var(--bg);border:1px solid var(--border);transition:all .18s;cursor:pointer;text-decoration:none;margin-bottom:.35rem;}
.info-item:last-child{margin-bottom:0;}
.info-item:hover{border-color:rgba(91,77,245,0.3);background:rgba(91,77,245,0.04);transform:translateX(2px);}
.info-icon{width:30px;height:30px;border-radius:8px;background:linear-gradient(135deg,rgba(91,77,245,.1),rgba(59,130,246,.1));display:flex;align-items:center;justify-content:center;font-size:.82rem;flex-shrink:0;}
.info-text{flex:1;min-width:0;}
.info-label{font-size:.52rem;color:var(--muted2);line-height:1;margin-bottom:2px;text-transform:uppercase;letter-spacing:.07em;font-weight:600;}
.info-value{font-size:.73rem;font-weight:600;color:var(--text);overflow:hidden;text-overflow:ellipsis;white-space:nowrap;}
.avail-badge{display:inline-flex;align-items:center;gap:.45rem;background:linear-gradient(135deg,rgba(16,185,129,.08),rgba(6,182,212,.06));border:1.5px solid rgba(16,185,129,.22);color:#059669;padding:.38rem .9rem;border-radius:10px;font-size:.65rem;font-weight:700;width:100%;justify-content:center;margin-top:.3rem;}
.avail-dot{width:6px;height:6px;border-radius:50%;background:#10b981;animation:pulse 1.6s infinite;flex-shrink:0;}
@keyframes pulse{0%,100%{opacity:1;transform:scale(1);}50%{opacity:.4;transform:scale(.75);}}

/* CENTER */
.hero-center{display:flex;justify-content:center;align-items:flex-start;z-index:2;flex-direction:column;gap:1rem;padding-top:.2rem;}
.profile-outer{position:relative;width:260px;height:260px;align-self:center;}
.ring-outer{position:absolute;inset:-10px;border-radius:50%;border:1.5px dashed rgba(91,77,245,.3);animation:spinRing 28s linear infinite;}
.ring-inner{position:absolute;inset:0;border-radius:50%;border:2px solid rgba(91,77,245,.12);}
.profile-circle{position:absolute;inset:0;border-radius:50%;overflow:hidden;cursor:default;transition:all .3s;box-shadow:0 0 0 4px rgba(91,77,245,.1),0 16px 48px rgba(91,77,245,.2);}
.profile-img{width:100%;height:100%;object-fit:cover;display:block;}
.metric{position:absolute;background:rgba(255,255,255,0.95);backdrop-filter:blur(16px);border:1px solid var(--border);border-radius:12px;padding:.52rem .8rem;text-align:center;white-space:nowrap;box-shadow:0 6px 24px rgba(91,77,245,.12);}
.metric-val{font-size:1.1rem;font-weight:800;line-height:1;font-family:'Syne',sans-serif;color:var(--primary);}
.metric-lbl{font-size:.52rem;color:var(--muted);margin-top:2px;font-weight:500;}
.m1{top:-4px;right:-44px;animation:mf1 3.5s ease-in-out infinite;}
.m2{top:50%;left:-56px;transform:translateY(-50%);animation:mf2 3.8s ease-in-out .6s infinite;}
.m3{bottom:2px;right:-42px;animation:mf3 3.2s ease-in-out 1.1s infinite;}
@keyframes spinRing{to{transform:rotate(360deg);}}
@keyframes mf1{0%,100%{transform:translateY(0);}50%{transform:translateY(-6px);}}
@keyframes mf2{0%,100%{transform:translateY(-50%);}50%{transform:translateY(calc(-50% - 6px));}}
@keyframes mf3{0%,100%{transform:translateY(0);}50%{transform:translateY(-6px);}}

/* Thought of the Day */
.thought-card{background:var(--bg2);border:1px solid var(--border);border-radius:var(--radius);padding:1.1rem 1.2rem;width:260px;align-self:center;position:relative;overflow:hidden;box-shadow:var(--shadow);}
.thought-card::before{content:'';position:absolute;top:0;left:0;right:0;height:3px;background:linear-gradient(90deg,var(--primary),var(--secondary),var(--accent));}
.thought-hdr{display:flex;align-items:center;justify-content:space-between;margin-bottom:.65rem;}
.thought-label{font-size:.56rem;color:var(--primary);text-transform:uppercase;letter-spacing:.12em;font-weight:700;display:flex;align-items:center;gap:.35rem;}
.thought-label::before{content:'💡';font-size:.8rem;}
.thought-refresh{background:rgba(91,77,245,.08);border:1px solid rgba(91,77,245,.2);color:var(--primary);padding:.22rem .62rem;border-radius:7px;font-size:.6rem;font-weight:700;cursor:pointer;font-family:'Plus Jakarta Sans',sans-serif;transition:all .18s;display:inline-flex;align-items:center;gap:.25rem;}
.thought-refresh:hover{background:rgba(91,77,245,.16);transform:rotate(15deg) scale(1.05);}
.thought-text{font-size:.76rem;color:var(--text2);line-height:1.65;font-style:italic;opacity:.9;}
.thought-author{font-size:.62rem;color:var(--primary);margin-top:.45rem;font-weight:600;}

/* RIGHT */
.hero-right{z-index:2;display:flex;flex-direction:column;gap:1.1rem;padding-top:.5rem;}
.hero-eyebrow{color:var(--muted);font-size:.78rem;font-weight:500;display:flex;align-items:center;gap:.45rem;}
.hero-eyebrow::before{content:'';width:18px;height:1.5px;background:linear-gradient(90deg,var(--primary),var(--secondary));}
.hero-name{font-size:clamp(2rem,3vw,3rem);font-weight:800;line-height:1;font-family:'Syne',sans-serif;background:linear-gradient(135deg,var(--primary) 0%,var(--secondary) 50%,var(--accent) 100%);-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;letter-spacing:-.02em;}
.hero-role{font-size:clamp(.85rem,1.2vw,1rem);font-weight:600;color:var(--text2);letter-spacing:.01em;}
.hero-desc{color:var(--muted);font-size:.8rem;line-height:1.85;max-width:420px;}

/* Tech Stack Section */
.tech-section{display:flex;flex-direction:column;gap:.6rem;}
.tech-section-label{font-size:.58rem;text-transform:uppercase;letter-spacing:.12em;color:var(--muted);font-weight:700;}
.tech-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:.5rem;}
.tech-chip{background:var(--bg2);border:1px solid var(--border);border-radius:10px;padding:.55rem .65rem;display:flex;align-items:center;gap:.5rem;transition:all .2s;cursor:default;box-shadow:0 1px 4px rgba(0,0,0,0.04);}
.tech-chip:hover{border-color:rgba(91,77,245,.35);background:rgba(91,77,245,.04);transform:translateY(-2px);box-shadow:0 6px 16px rgba(91,77,245,.1);}
.tech-chip-icon{font-size:.95rem;flex-shrink:0;}
.tech-chip-name{font-size:.65rem;font-weight:700;color:var(--text);white-space:nowrap;}
.tech-chip-level{font-size:.52rem;color:var(--muted2);margin-top:1px;}

.hero-ctas{display:flex;gap:.65rem;flex-wrap:wrap;align-items:center;padding-top:.2rem;}
.btn-primary{background:linear-gradient(135deg,var(--primary),var(--secondary));color:#fff;padding:.65rem 1.4rem;border-radius:10px;font-weight:700;font-size:.8rem;border:none;cursor:pointer;font-family:'Plus Jakarta Sans',sans-serif;transition:all .2s;letter-spacing:.01em;box-shadow:0 6px 20px rgba(91,77,245,.32);}
.btn-primary:hover{transform:translateY(-2px);box-shadow:0 10px 28px rgba(91,77,245,.42);}
.btn-secondary{background:var(--bg2);color:var(--primary);padding:.65rem 1.4rem;border-radius:10px;font-weight:600;font-size:.8rem;border:1.5px solid rgba(91,77,245,.25);cursor:pointer;font-family:'Plus Jakarta Sans',sans-serif;transition:all .2s;}
.btn-secondary:hover{background:rgba(91,77,245,.06);border-color:var(--primary);}

/* ── STATS ── */
.stats-sec{padding:2rem 2.5rem 2.5rem;background:linear-gradient(180deg,rgba(240,244,255,.5),transparent);}
.stats-title{text-align:center;margin-bottom:1.8rem;}
.stats-title h3{font-size:1.15rem;font-weight:700;font-family:'Syne',sans-serif;margin-bottom:.28rem;letter-spacing:-.01em;color:var(--text);}
.stats-title p{color:var(--muted);font-size:.79rem;}
.stats-grid{display:grid;grid-template-columns:repeat(5,1fr);gap:.9rem;max-width:100%;}
.scard{background:var(--bg2);border:1px solid var(--border);border-radius:var(--radius);padding:1.4rem .9rem;text-align:center;position:relative;overflow:hidden;transition:all .3s;cursor:default;box-shadow:var(--shadow);}
.scard::before{content:'';position:absolute;top:0;left:0;right:0;height:3px;background:linear-gradient(90deg,var(--primary),var(--secondary),var(--accent));opacity:.7;}
.scard:hover{transform:translateY(-6px);border-color:rgba(91,77,245,.3);box-shadow:0 20px 48px rgba(91,77,245,.13);}
.scard-icon{font-size:1.7rem;margin-bottom:.5rem;display:block;}
.scard-val{font-size:1.9rem;font-weight:800;background:linear-gradient(135deg,var(--primary),var(--secondary));-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;line-height:1;font-family:'Syne',sans-serif;}
.scard-label{font-size:.74rem;color:var(--text);font-weight:700;margin:.4rem 0 .22rem;}
.scard-desc{font-size:.63rem;color:var(--muted);line-height:1.45;}

/* SKILL VISUAL */
.hero-visual-wrap{max-width:100%;margin:1.5rem 0 0;background:var(--bg2);border:1px solid var(--border);border-radius:var(--radius);padding:1.6rem;display:grid;grid-template-columns:1fr 1fr;gap:2rem;align-items:center;box-shadow:var(--shadow);}
.visual-section-title{font-size:.6rem;color:var(--muted);text-transform:uppercase;letter-spacing:.1em;font-weight:700;margin-bottom:.9rem;text-align:center;grid-column:1/-1;}
.radar-wrap{display:flex;flex-direction:column;align-items:center;}
.skill-bars{display:flex;flex-direction:column;gap:.7rem;}
.skill-bar-label{display:flex;justify-content:space-between;font-size:.67rem;font-weight:700;margin-bottom:.28rem;color:var(--text2);}
.skill-bar-label span:last-child{color:var(--primary);}
.skill-bar-track{height:6px;background:var(--bg3);border-radius:6px;overflow:hidden;}
.skill-bar-fill{height:100%;border-radius:6px;background:linear-gradient(90deg,var(--primary),var(--secondary));transition:width 1.4s cubic-bezier(.25,1,.5,1);}

/* ── MARKET ── */
.home-market-sec{padding:2rem 2.5rem 2.5rem;background:rgba(240,244,255,0.5);}
.home-market-inner{max-width:100%;}
.home-market-hdr{display:flex;align-items:flex-start;justify-content:space-between;margin-bottom:1.3rem;flex-wrap:wrap;gap:.8rem;}
.home-market-hdr h3{font-size:1rem;font-weight:700;font-family:'Syne',sans-serif;letter-spacing:-.01em;color:var(--text);}
.home-market-hdr p{color:var(--muted);font-size:.75rem;margin-top:.18rem;}
.refresh-small{background:rgba(91,77,245,.07);border:1.5px solid rgba(91,77,245,.2);color:var(--primary);padding:.32rem .88rem;border-radius:8px;font-family:'Plus Jakarta Sans',sans-serif;font-size:.67rem;font-weight:700;cursor:pointer;transition:all .18s;display:inline-flex;align-items:center;gap:.3rem;flex-shrink:0;}
.refresh-small:hover{background:rgba(91,77,245,.14);}
.market-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(240px,1fr));gap:1rem;}
.market-card{background:var(--bg2);border:1px solid var(--border);border-radius:var(--radius);padding:1.2rem;transition:all .25s;cursor:pointer;text-decoration:none;display:block;position:relative;overflow:hidden;box-shadow:var(--shadow);}
.market-card:hover{border-color:rgba(91,77,245,.35);transform:translateY(-3px);box-shadow:0 12px 32px rgba(91,77,245,.12);}
.market-card::after{content:'↗';position:absolute;top:.8rem;right:.8rem;color:var(--primary);font-size:.8rem;opacity:0;transition:opacity .2s;}
.market-card:hover::after{opacity:1;}
.market-tag{font-size:.6rem;letter-spacing:.1em;text-transform:uppercase;font-weight:700;margin-bottom:.38rem;}
.market-title{font-weight:700;font-size:.82rem;margin-bottom:.3rem;color:var(--text);padding-right:1.1rem;line-height:1.4;}
.market-desc{color:var(--muted);font-size:.74rem;line-height:1.55;}
.market-date{font-size:.6rem;color:var(--muted2);margin-top:.5rem;}
.market-loading{text-align:center;padding:2.5rem;color:var(--muted);}
.market-spinner{width:28px;height:28px;border:2px solid rgba(91,77,245,.15);border-top-color:var(--primary);border-radius:50%;animation:spin .7s linear infinite;margin:0 auto .6rem;}
@keyframes spin{to{transform:rotate(360deg);}}

/* ── CONTACT ── */
.contact-section{padding:2.5rem 2.5rem 3rem;background:linear-gradient(180deg,var(--bg),var(--bg3));}
.contact-wrap{max-width:760px;margin:0 auto;}
.contact-header{text-align:center;margin-bottom:1.8rem;}
.contact-header .sec-label-sm{color:var(--primary);font-size:.62rem;letter-spacing:.13em;text-transform:uppercase;font-weight:700;display:block;margin-bottom:.38rem;}
.contact-header h2{font-size:clamp(1.3rem,2.5vw,1.85rem);font-weight:700;font-family:'Syne',sans-serif;margin-bottom:.45rem;letter-spacing:-.01em;color:var(--text);}
.contact-header p{color:var(--muted);font-size:.8rem;}
.contact-form{background:var(--bg2);border:1px solid rgba(91,77,245,.18);border-radius:20px;padding:2rem;position:relative;overflow:hidden;box-shadow:var(--shadow-lg);}
.contact-form::before{content:'';position:absolute;top:0;left:0;right:0;height:3px;background:linear-gradient(90deg,var(--primary),var(--secondary),var(--accent));border-radius:20px 20px 0 0;}
.form-grid{display:grid;grid-template-columns:1fr 1fr;gap:1rem;position:relative;z-index:1;}
.form-grid .full{grid-column:1/-1;}
.fg-contact{position:relative;}
.fg-contact label{display:block;font-size:.62rem;color:var(--muted);margin-bottom:.38rem;font-weight:700;text-transform:uppercase;letter-spacing:.07em;}
.fg-contact .fi{position:absolute;left:.85rem;top:50%;transform:translateY(-50%);font-size:.8rem;pointer-events:none;z-index:2;}
.fg-contact input,.fg-contact select,.fg-contact textarea{width:100%;background:var(--bg);border:1.5px solid var(--border);border-radius:10px;padding:.65rem .85rem .65rem 2.4rem;color:var(--text);font-family:'Plus Jakarta Sans',sans-serif;font-size:.79rem;outline:none;transition:all .2s;appearance:none;}
.fg-contact textarea{padding:.65rem .85rem;height:90px;resize:none;}
.fg-contact.no-icon input,.fg-contact.no-icon select,.fg-contact.no-icon textarea{padding-left:.85rem;}
.fg-contact input:focus,.fg-contact textarea:focus,.fg-contact select:focus{border-color:var(--primary);background:rgba(91,77,245,.03);box-shadow:0 0 0 3px rgba(91,77,245,.1);}
.fg-contact select option{background:#fff;color:#0f172a;}
.form-submit{width:100%;padding:.82rem;background:linear-gradient(135deg,var(--primary),var(--secondary));color:#fff;border:none;border-radius:10px;font-family:'Plus Jakarta Sans',sans-serif;font-weight:700;font-size:.88rem;cursor:pointer;transition:all .2s;box-shadow:0 6px 20px rgba(91,77,245,.3);margin-top:.35rem;letter-spacing:.01em;}
.form-submit:hover{transform:translateY(-2px);box-shadow:0 10px 28px rgba(91,77,245,.42);}
.form-submit:disabled{opacity:.55;cursor:not-allowed;transform:none;}

/* ── GROWTH KPIs ── */
.growth-kpi-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:.9rem;margin-bottom:1.8rem;}
.gkpi{background:var(--bg2);border:1px solid var(--border);border-radius:var(--radius);padding:1.3rem 1rem;position:relative;overflow:hidden;transition:all .28s;box-shadow:var(--shadow);}
.gkpi:hover{transform:translateY(-4px);border-color:rgba(91,77,245,.28);box-shadow:0 14px 36px rgba(91,77,245,.1);}
.gkpi::before{content:'';position:absolute;top:0;left:0;right:0;height:3px;background:linear-gradient(90deg,var(--primary),var(--secondary));opacity:.7;}
.gkpi-icon{font-size:1.4rem;margin-bottom:.5rem;}
.gkpi-val{font-size:1.8rem;font-weight:800;background:linear-gradient(135deg,var(--primary),var(--secondary));-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;line-height:1;font-family:'Syne',sans-serif;}
.gkpi-label{font-size:.7rem;color:var(--text2);font-weight:700;margin:.25rem 0 .4rem;}
.gkpi-badge{display:inline-flex;align-items:center;gap:.2rem;padding:.12rem .5rem;border-radius:100px;font-size:.58rem;font-weight:700;}
.gkpi-badge.up{background:rgba(16,185,129,.09);border:1px solid rgba(16,185,129,.22);color:#059669;}
.gkpi-sub{font-size:.62rem;color:var(--muted);margin-top:.25rem;}
.growth-container{background:var(--bg2);border:1px solid var(--border);border-radius:var(--radius);padding:1.5rem;position:relative;box-shadow:var(--shadow);}
.growth-canvas{width:100%;height:340px;}

/* ── CERTS ── */
.cert-hero-stats{display:grid;grid-template-columns:repeat(3,1fr);gap:1.1rem;margin-bottom:1.8rem;}
.cert-hero-stat{background:var(--bg2);border:1px solid var(--border);border-radius:var(--radius);padding:1.6rem 1.1rem;text-align:center;position:relative;overflow:hidden;transition:all .3s;box-shadow:var(--shadow);}
.cert-hero-stat::before{content:'';position:absolute;top:0;left:0;right:0;height:3px;border-radius:var(--radius) var(--radius) 0 0;}
.cert-hero-stat:nth-child(1)::before{background:linear-gradient(90deg,var(--primary),var(--primary2));}
.cert-hero-stat:nth-child(2)::before{background:linear-gradient(90deg,var(--secondary),#60a5fa);}
.cert-hero-stat:nth-child(3)::before{background:linear-gradient(90deg,var(--accent),#34d3eb);}
.cert-hero-stat:hover{transform:translateY(-5px);box-shadow:0 16px 40px rgba(91,77,245,.1);}
.cert-stat-icon{font-size:1.9rem;margin-bottom:.5rem;}
.cert-stat-val{font-size:2.6rem;font-weight:800;line-height:1;font-family:'Syne',sans-serif;}
.cert-hero-stat:nth-child(1) .cert-stat-val{background:linear-gradient(135deg,var(--primary),var(--primary2));-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;}
.cert-hero-stat:nth-child(2) .cert-stat-val{background:linear-gradient(135deg,var(--secondary),#60a5fa);-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;}
.cert-hero-stat:nth-child(3) .cert-stat-val{background:linear-gradient(135deg,var(--accent),#34d3eb);-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;}
.cert-stat-label{font-size:.74rem;color:var(--text2);font-weight:700;margin:.35rem 0 .25rem;}
.cert-stat-sub{font-size:.64rem;color:var(--muted);line-height:1.45;}
.skills-learned-wrap{background:var(--bg);border:1px solid var(--border);border-radius:var(--radius);padding:1.1rem 1.3rem;margin-bottom:1.8rem;}
.skills-learned-hdr{display:flex;align-items:center;justify-content:space-between;margin-bottom:.7rem;}
.skills-learned-title{font-size:.62rem;color:var(--muted);text-transform:uppercase;letter-spacing:.1em;font-weight:700;}
.skills-learned-count{font-size:.62rem;color:var(--primary);font-weight:700;}
.skills-learned-chips{display:flex;flex-wrap:wrap;gap:.35rem;}
.sl-chip{background:var(--bg2);border:1px solid var(--border);color:var(--text2);padding:.23rem .7rem;border-radius:8px;font-size:.65rem;font-weight:600;transition:all .18s;cursor:default;}
.sl-chip.hot{background:rgba(91,77,245,.08);border-color:rgba(91,77,245,.28);color:var(--primary);}
.sl-chip:hover{border-color:rgba(91,77,245,.35);color:var(--primary);background:rgba(91,77,245,.06);}
.certs-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(240px,1fr));gap:1.2rem;}
.cert-card{background:var(--bg2);border:1px solid var(--border);border-radius:var(--radius);overflow:hidden;transition:all .28s;position:relative;box-shadow:var(--shadow);}
.cert-card:hover{border-color:rgba(91,77,245,.35);transform:translateY(-3px);box-shadow:0 12px 32px rgba(91,77,245,.12);}
.cert-card-badge{position:absolute;top:.7rem;right:.7rem;background:rgba(91,77,245,.1);border:1px solid rgba(91,77,245,.25);color:var(--primary);padding:.12rem .5rem;border-radius:6px;font-size:.56rem;font-weight:800;text-transform:uppercase;letter-spacing:.06em;}
.cert-wrap{width:100%;height:138px;background:linear-gradient(145deg,var(--bg3),var(--bg4));display:flex;align-items:center;justify-content:center;overflow:hidden;}
.cert-placeholder{display:flex;flex-direction:column;align-items:center;justify-content:center;gap:.45rem;color:var(--muted);font-size:.7rem;text-align:center;padding:.9rem;width:100%;height:100%;}
.cert-placeholder .cert-emoji{font-size:2.3rem;filter:drop-shadow(0 3px 10px rgba(91,77,245,.2));}
.cert-body{padding:.9rem 1rem 1.1rem;}
.cert-org{font-size:.62rem;color:var(--muted);margin-bottom:.08rem;}
.cert-name{font-weight:700;font-size:.82rem;margin-bottom:.38rem;color:var(--text);}
.cert-meta{display:flex;align-items:center;justify-content:space-between;}
.cert-year{font-size:.62rem;color:var(--primary);font-weight:700;}
.cert-level{font-size:.58rem;background:var(--bg);border:1px solid var(--border);padding:.1rem .5rem;border-radius:6px;color:var(--muted);}
.add-cert{background:var(--bg);border:1.5px dashed var(--border2);border-radius:var(--radius);display:flex;flex-direction:column;align-items:center;justify-content:center;gap:.45rem;cursor:pointer;min-height:230px;transition:all .25s;color:var(--muted);font-size:.77rem;}
.add-cert:hover{border-color:var(--primary);background:rgba(91,77,245,.04);color:var(--primary);}

/* ── GENERAL SECTIONS ── */
.sec{padding:2rem 2.5rem 2.5rem;}
.sec-label{color:var(--primary);font-size:.62rem;letter-spacing:.13em;text-transform:uppercase;margin-bottom:.38rem;font-weight:700;display:flex;align-items:center;gap:.38rem;}
.sec-label::before{content:'';width:12px;height:2px;background:linear-gradient(90deg,var(--primary),var(--secondary));border-radius:2px;}
.sec h2{font-size:clamp(1.3rem,2.2vw,1.85rem);font-weight:800;font-family:'Syne',sans-serif;margin-bottom:.35rem;letter-spacing:-.01em;color:var(--text);}
.sec-bar{height:3px;width:36px;background:linear-gradient(90deg,var(--primary),var(--secondary));border-radius:3px;margin-bottom:1.5rem;}
.sec-sub{color:var(--muted);font-size:.8rem;line-height:1.8;max-width:480px;margin-bottom:1.8rem;}

/* ── SKILLS ── */
.skills-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(180px,1fr));gap:1rem;}
.sk{background:var(--bg2);border:1px solid var(--border);border-radius:var(--radius);padding:1.2rem;transition:all .25s;position:relative;overflow:hidden;box-shadow:var(--shadow);}
.sk:hover{border-color:rgba(91,77,245,.35);transform:translateY(-3px);box-shadow:0 10px 28px rgba(91,77,245,.1);}
.sk-icon{font-size:1.5rem;margin-bottom:.55rem;display:block;}
.sk-title{font-weight:700;font-size:.82rem;margin-bottom:.65rem;color:var(--text);}
.tags{display:flex;flex-wrap:wrap;gap:.25rem;}
.tag{background:var(--bg3);border:1px solid var(--border);border-radius:7px;padding:.12rem .52rem;font-size:.61rem;color:var(--muted);transition:all .18s;}
.tag:hover,.tag.h{background:rgba(91,77,245,.08);border-color:rgba(91,77,245,.3);color:var(--primary);}

/* ── PROJECTS ── */
.projects-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:1.1rem;}
.proj{background:var(--bg2);border:1px solid var(--border);border-radius:var(--radius);padding:1.4rem;transition:all .25s;position:relative;overflow:hidden;box-shadow:var(--shadow);}
.proj::before{content:'';position:absolute;top:0;left:0;right:0;height:3px;background:linear-gradient(90deg,var(--primary),var(--secondary));opacity:0;transition:opacity .25s;}
.proj:hover{border-color:rgba(91,77,245,.3);transform:translateY(-3px);box-shadow:0 12px 32px rgba(91,77,245,.1);}
.proj:hover::before{opacity:1;}
.proj-type{font-size:.6rem;letter-spacing:.09em;text-transform:uppercase;color:var(--primary);margin-bottom:.38rem;font-weight:700;}
.proj-title{font-weight:800;font-size:.87rem;margin-bottom:.38rem;font-family:'Syne',sans-serif;color:var(--text);}
.proj-desc{color:var(--muted);font-size:.76rem;line-height:1.62;}

/* ── EXPERIENCE ── */
.exp-timeline{max-width:840px;position:relative;}
.exp-timeline::before{content:'';position:absolute;left:21px;top:22px;bottom:22px;width:2px;background:linear-gradient(180deg,var(--primary),rgba(91,77,245,.04));border-radius:2px;}
.exp-item{display:flex;gap:1.3rem;margin-bottom:1.8rem;}
.exp-dot{width:42px;height:42px;border-radius:12px;flex-shrink:0;background:linear-gradient(135deg,var(--primary),var(--secondary));display:flex;align-items:center;justify-content:center;font-size:.92rem;position:relative;z-index:2;box-shadow:0 4px 16px rgba(91,77,245,.28);}
.exp-card{flex:1;background:var(--bg2);border:1px solid var(--border);border-radius:var(--radius);padding:1.2rem 1.4rem;transition:all .25s;position:relative;overflow:hidden;box-shadow:var(--shadow);}
.exp-card::before{content:'';position:absolute;top:0;left:0;bottom:0;width:3px;background:linear-gradient(180deg,var(--primary),var(--secondary));opacity:0;transition:opacity .25s;}
.exp-card:hover{border-color:rgba(91,77,245,.28);transform:translateX(3px);}
.exp-card:hover::before{opacity:1;}
.exp-header{display:flex;align-items:flex-start;justify-content:space-between;gap:.9rem;margin-bottom:.4rem;flex-wrap:wrap;}
.exp-title{font-weight:700;font-size:.88rem;font-family:'Syne',sans-serif;color:var(--text);}
.exp-period{background:rgba(91,77,245,.08);border:1px solid rgba(91,77,245,.2);color:var(--primary);padding:.18rem .65rem;border-radius:8px;font-size:.6rem;font-weight:700;white-space:nowrap;flex-shrink:0;}
.exp-company{font-size:.74rem;color:var(--primary);font-weight:600;margin-bottom:.55rem;}
.exp-bullets{list-style:none;display:flex;flex-direction:column;gap:.35rem;}
.exp-bullets li{display:flex;align-items:flex-start;gap:.38rem;color:var(--muted);font-size:.74rem;line-height:1.62;}
.exp-bullets li::before{content:'▹';color:var(--primary);flex-shrink:0;margin-top:2px;}

/* ── AWARDS ── */
.awards-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:1.2rem;}
.award-card{background:var(--bg2);border:1px solid var(--border);border-radius:var(--radius);overflow:hidden;transition:all .28s;box-shadow:var(--shadow);}
.award-card:hover{border-color:rgba(91,77,245,.35);transform:translateY(-3px);box-shadow:0 12px 32px rgba(91,77,245,.12);}
.award-wrap{width:100%;height:130px;background:linear-gradient(145deg,var(--bg3),var(--bg4));display:flex;align-items:center;justify-content:center;}
.award-placeholder{display:flex;flex-direction:column;align-items:center;justify-content:center;gap:.38rem;color:var(--muted);font-size:.7rem;}
.award-body{padding:.85rem 1rem 1.05rem;}
.award-badge{display:inline-flex;align-items:center;gap:.22rem;background:rgba(91,77,245,.08);border:1px solid rgba(91,77,245,.22);color:var(--primary);padding:.15rem .65rem;border-radius:8px;font-size:.56rem;font-weight:700;margin-bottom:.32rem;}
.award-title{font-weight:700;font-size:.83rem;margin-bottom:.2rem;color:var(--text);}
.award-desc{color:var(--muted);font-size:.73rem;line-height:1.58;}
.add-award{background:var(--bg);border:1.5px dashed var(--border2);border-radius:var(--radius);display:flex;flex-direction:column;align-items:center;justify-content:center;gap:.45rem;cursor:pointer;min-height:230px;transition:all .25s;color:var(--muted);font-size:.77rem;}
.add-award:hover{border-color:var(--primary);background:rgba(91,77,245,.04);color:var(--primary);}

/* ── ABOUT ── */
.about-grid{display:grid;grid-template-columns:220px 1fr;gap:2.2rem;align-items:start;max-width:960px;}
.about-img{aspect-ratio:3/4;background:linear-gradient(145deg,var(--bg3),var(--bg4));border-radius:var(--radius);border:1px solid var(--border);display:flex;align-items:center;justify-content:center;font-size:4.5rem;box-shadow:var(--shadow);}
.about-body p{color:var(--muted);font-size:.81rem;line-height:1.85;margin-bottom:.8rem;}
.chips{display:flex;flex-wrap:wrap;gap:.38rem;margin-top:1rem;}
.chip{background:rgba(91,77,245,.07);border:1px solid rgba(91,77,245,.2);color:var(--primary);padding:.26rem .78rem;border-radius:8px;font-size:.67rem;font-weight:600;}

/* ── LIGHTBOX ── */
.lb{display:none;position:fixed;inset:0;z-index:999;background:rgba(0,0,0,.88);backdrop-filter:blur(8px);align-items:center;justify-content:center;}
.lb.open{display:flex;}
.lb-inner{position:relative;}
.lb-inner img{max-width:92vw;max-height:90vh;border-radius:10px;object-fit:contain;}
.lb-close{position:absolute;top:-12px;right:-12px;width:28px;height:28px;border-radius:50%;background:var(--primary);color:#fff;border:none;font-size:.9rem;cursor:pointer;display:flex;align-items:center;justify-content:center;}

/* ── LOGIN ── */
.login-overlay{display:none;position:fixed;inset:0;z-index:800;background:rgba(15,23,42,.7);backdrop-filter:blur(10px);align-items:center;justify-content:center;}
.login-overlay.open{display:flex;}
.login-box{background:var(--bg2);border:1px solid rgba(91,77,245,.22);border-radius:20px;padding:2rem;width:100%;max-width:340px;position:relative;box-shadow:0 32px 80px rgba(91,77,245,.2);}
.login-box::before{content:'';position:absolute;top:0;left:0;right:0;height:3px;background:linear-gradient(90deg,var(--primary),var(--secondary),var(--accent));border-radius:20px 20px 0 0;}
.login-logo{width:46px;height:46px;border-radius:12px;background:linear-gradient(135deg,var(--primary),var(--secondary));display:flex;align-items:center;justify-content:center;font-weight:800;font-size:.85rem;font-family:'Syne',sans-serif;margin:0 auto .9rem;color:#fff;box-shadow:0 6px 18px rgba(91,77,245,.35);}
.login-title{text-align:center;font-size:1rem;font-weight:700;font-family:'Syne',sans-serif;margin-bottom:.18rem;color:var(--text);}
.login-sub{text-align:center;color:var(--muted);font-size:.72rem;margin-bottom:1.2rem;}
.login-err{background:rgba(244,63,94,.07);border:1px solid rgba(244,63,94,.25);color:#e11d48;border-radius:9px;padding:.5rem .8rem;font-size:.71rem;margin-bottom:.8rem;display:none;text-align:center;}
.login-err.show{display:block;}
.lf{margin-bottom:.8rem;position:relative;}
.lf label{display:block;font-size:.62rem;color:var(--muted);margin-bottom:.3rem;font-weight:700;text-transform:uppercase;letter-spacing:.06em;}
.lf input{width:100%;background:var(--bg);border:1.5px solid var(--border);border-radius:10px;padding:.65rem .9rem .65rem 2.4rem;color:var(--text);font-family:'Plus Jakarta Sans',sans-serif;font-size:.8rem;outline:none;transition:all .18s;}
.lf input:focus{border-color:var(--primary);background:rgba(91,77,245,.03);}
.lf-icon{position:absolute;left:.85rem;bottom:.7rem;font-size:.8rem;pointer-events:none;}
.login-btn{width:100%;padding:.75rem;background:linear-gradient(135deg,var(--primary),var(--secondary));color:#fff;border:none;border-radius:10px;font-family:'Plus Jakarta Sans',sans-serif;font-weight:700;font-size:.86rem;cursor:pointer;transition:all .18s;margin-top:.25rem;box-shadow:0 6px 18px rgba(91,77,245,.3);}
.login-btn:hover{transform:translateY(-1px);box-shadow:0 10px 24px rgba(91,77,245,.4);}
.login-xbtn{position:absolute;top:.9rem;right:.9rem;background:var(--bg);border:1px solid var(--border);color:var(--muted);width:26px;height:26px;border-radius:50%;cursor:pointer;display:flex;align-items:center;justify-content:center;font-size:.7rem;transition:all .18s;}
.login-xbtn:hover{background:var(--bg3);color:var(--text);}

/* ── EDIT ── */
.edit-banner{display:none;position:fixed;top:62px;left:0;right:0;z-index:250;background:linear-gradient(90deg,rgba(16,185,129,.08),rgba(6,182,212,.06));border-bottom:1px solid rgba(16,185,129,.22);padding:.38rem 2rem;text-align:center;font-size:.68rem;color:#059669;font-weight:500;align-items:center;justify-content:center;gap:.45rem;}
.edit-banner.show{display:flex;}
.edit-dot{width:5px;height:5px;border-radius:50%;background:#10b981;animation:pulse 1.5s infinite;}
.editable{outline:none;border-radius:3px;transition:all .18s;cursor:default;}
body.edit-mode .editable{cursor:text;background:rgba(91,77,245,.08);box-shadow:0 0 0 2px rgba(91,77,245,.25);padding:1px 4px;}

/* ── TOAST ── */
.toast{position:fixed;bottom:1.8rem;left:50%;transform:translateX(-50%) translateY(110px);background:rgba(255,255,255,.97);border:1px solid rgba(91,77,245,.25);color:var(--text);padding:.65rem 1.4rem;border-radius:10px;font-size:.73rem;font-weight:600;z-index:9999;transition:transform .28s;pointer-events:none;backdrop-filter:blur(12px);box-shadow:0 10px 32px rgba(91,77,245,.16);}
.toast.show{transform:translateX(-50%) translateY(0);}

/* ── CHATBOT ── */
.chat-fab{position:fixed;bottom:1.8rem;right:1.8rem;z-index:400;width:54px;height:54px;border-radius:50%;background:linear-gradient(135deg,var(--primary),var(--secondary));border:none;cursor:pointer;display:flex;align-items:center;justify-content:center;box-shadow:0 8px 28px rgba(91,77,245,.42);transition:all .18s;animation:chatPulse 2.8s ease-in-out infinite;}
.chat-fab:hover{transform:scale(1.08);animation:none;}
.chat-fab-icon{font-size:1.2rem;}
.chat-badge{position:absolute;top:-3px;right:-3px;width:16px;height:16px;border-radius:50%;background:#10b981;border:2px solid #fff;display:flex;align-items:center;justify-content:center;font-size:.42rem;font-weight:900;color:#fff;}
@keyframes chatPulse{0%,100%{box-shadow:0 8px 28px rgba(91,77,245,.42);}50%{box-shadow:0 8px 36px rgba(91,77,245,.62),0 0 0 6px rgba(91,77,245,.08);}}
.cwin{position:fixed;bottom:5.8rem;right:1.8rem;z-index:400;width:352px;height:514px;background:var(--bg2);border:1px solid rgba(91,77,245,.16);border-radius:20px;display:none;flex-direction:column;box-shadow:0 24px 60px rgba(91,77,245,.18);overflow:hidden;}
.cwin.open{display:flex;animation:chatSlide .25s ease;}
@keyframes chatSlide{from{opacity:0;transform:translateY(12px) scale(.96);}to{opacity:1;transform:none;}}
.chat-hdr{padding:.85rem 1rem;display:flex;align-items:center;gap:.65rem;background:linear-gradient(135deg,rgba(91,77,245,.06),rgba(59,130,246,.04));border-bottom:1px solid var(--border);flex-shrink:0;}
.chat-av{width:34px;height:34px;border-radius:10px;background:linear-gradient(135deg,var(--primary),var(--secondary));display:flex;align-items:center;justify-content:center;font-weight:800;font-size:.72rem;flex-shrink:0;color:#fff;font-family:'Syne',sans-serif;}
.chat-av-name{font-weight:700;font-size:.8rem;color:var(--text);}
.chat-av-status{font-size:.6rem;color:#059669;display:flex;align-items:center;gap:.24rem;}
.chat-av-status::before{content:'';width:5px;height:5px;border-radius:50%;background:#10b981;}
.cclose{background:none;border:none;color:var(--muted);cursor:pointer;font-size:.95rem;padding:.08rem;transition:color .18s;margin-left:auto;}
.cclose:hover{color:var(--text);}
.cmsgs{flex:1;overflow-y:auto;padding:.85rem;display:flex;flex-direction:column;gap:.6rem;}
.cmsgs::-webkit-scrollbar{width:2px;}
.cmsgs::-webkit-scrollbar-thumb{background:var(--border2);border-radius:2px;}
.cmsg{display:flex;gap:.4rem;align-items:flex-end;}
.cmsg.user{flex-direction:row-reverse;}
.cbubble{padding:.56rem .82rem;border-radius:14px;font-size:.74rem;line-height:1.58;max-width:82%;word-break:break-word;}
.cmsg.bot .cbubble{background:var(--bg);border:1px solid var(--border);color:var(--text2);border-radius:14px 14px 14px 4px;}
.cmsg.user .cbubble{background:linear-gradient(135deg,var(--primary),var(--secondary));color:#fff;border-radius:14px 14px 4px 14px;}
.cdot{width:26px;height:26px;border-radius:8px;background:linear-gradient(135deg,var(--primary),var(--secondary));display:flex;align-items:center;justify-content:center;font-size:.55rem;font-weight:800;flex-shrink:0;font-family:'Syne',sans-serif;color:#fff;}
.cmsg.user .cdot{background:var(--bg3);}
.cquick{padding:.4rem .85rem;display:flex;gap:.25rem;flex-wrap:wrap;border-top:1px solid var(--border);}
.cqbtn{background:rgba(91,77,245,.07);border:1px solid rgba(91,77,245,.18);color:var(--primary);padding:.26rem .65rem;border-radius:8px;font-size:.6rem;cursor:pointer;font-family:'Plus Jakarta Sans',sans-serif;font-weight:700;transition:all .18s;white-space:nowrap;}
.cqbtn:hover{background:rgba(91,77,245,.14);}
.cinput-row{padding:.72rem .85rem;display:flex;gap:.4rem;border-top:1px solid var(--border);flex-shrink:0;background:var(--bg);}
.cinput{flex:1;background:var(--bg2);border:1.5px solid var(--border);border-radius:10px;padding:.52rem .9rem;color:var(--text);font-family:'Plus Jakarta Sans',sans-serif;font-size:.74rem;outline:none;transition:border-color .18s;}
.cinput:focus{border-color:rgba(91,77,245,.4);}
.csend{width:34px;height:34px;border-radius:9px;background:linear-gradient(135deg,var(--primary),var(--secondary));border:none;color:#fff;cursor:pointer;display:flex;align-items:center;justify-content:center;font-size:.8rem;flex-shrink:0;transition:opacity .18s;box-shadow:0 3px 10px rgba(91,77,245,.3);}
.csend:hover{opacity:.88;}
.typing-dots span{display:inline-block;width:4px;height:4px;border-radius:50%;background:var(--muted2);margin:0 1px;animation:dot 1.2s infinite;}
.typing-dots span:nth-child(2){animation-delay:.2s;}
.typing-dots span:nth-child(3){animation-delay:.4s;}
@keyframes dot{0%,80%,100%{opacity:.2;}40%{opacity:1;}}

/* ── FOOTER ── */
footer{padding:1.2rem 2.5rem;border-top:1px solid var(--border);display:flex;justify-content:space-between;align-items:center;color:var(--muted2);font-size:.68rem;background:var(--bg2);}

.section-divider{height:1px;background:var(--border);margin:0 2.5rem;}
</style>
</head>
<body>

<!-- LOGIN MODAL -->
<div class="login-overlay" id="loginModal">
  <div class="login-box">
    <button class="login-xbtn" onclick="closeLogin()">✕</button>
    <div class="login-logo">AK</div>
    <div class="login-title">Admin Login</div>
    <div class="login-sub">Enter credentials to unlock edit mode</div>
    <div class="login-err" id="loginErr">❌ Incorrect ID or Password</div>
    <div class="lf"><label>User ID</label><span class="lf-icon">👤</span><input type="text" id="lid" placeholder="Akash7566" autocomplete="off" onkeydown="if(event.key==='Enter')doLogin()"></div>
    <div class="lf"><label>Password</label><span class="lf-icon">🔒</span><input type="password" id="lpwd" placeholder="••••••••" onkeydown="if(event.key==='Enter')doLogin()"></div>
    <button class="login-btn" onclick="doLogin()">🔓 Unlock Edit Mode</button>
  </div>
</div>

<div class="edit-banner" id="editBanner"><div class="edit-dot"></div><span>✏️ Edit Mode Active — Click highlighted text to edit</span></div>
<div class="lb" id="lightbox" onclick="if(event.target===this)closeLB()"><div class="lb-inner"><button class="lb-close" onclick="closeLB()">✕</button><img id="lb-img" src="" alt=""></div></div>
<div class="toast" id="toast"></div>

<!-- NAV -->
<nav>
  <div class="nav-brand">
    <div class="nav-logo">AK</div>
    <div class="nav-brand-text">
      <span class="nav-name">Akash Kourav</span>
      <span class="nav-subtitle">Power BI Developer & BI Analyst</span>
    </div>
  </div>
  <div class="nav-tabs">
    <button class="nav-tab active" onclick="showPage('home',this)">Home</button>
    <button class="nav-tab" onclick="showPage('about',this)">About</button>
    <button class="nav-tab" onclick="showPage('skills',this)">Skills</button>
    <button class="nav-tab" onclick="showPage('projects',this)">Projects</button>
    <button class="nav-tab" onclick="showPage('experience',this)">Experience</button>
    <button class="nav-tab" onclick="showPage('growth',this)">Growth</button>
    <button class="nav-tab" onclick="showPage('market',this)">Market</button>
    <button class="nav-tab" onclick="showPage('certs',this)">Certs</button>
    <button class="nav-tab" onclick="showPage('awards',this)">Awards</button>
  </div>
  <div class="nav-actions">
    <div class="socials-nav">
      <a href="https://linkedin.com/in/akashkourav" target="_blank" class="soc-n soc-li" title="LinkedIn">in</a>
      <a href="https://github.com/akashkourav" target="_blank" class="soc-n soc-gh" title="GitHub">
        <svg width="12" height="12" viewBox="0 0 24 24" fill="white"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0 1.5 3.78c.1.85.34 2.75-.5 6.23"/></svg>
      </a>
      <a href="mailto:akashkoyrav7566@gmail.com" class="soc-n soc-em" title="Email">✉</a>
      <a href="https://wa.me/917509762086" target="_blank" class="soc-n soc-wa" title="WhatsApp">
        <svg width="12" height="12" viewBox="0 0 24 24" fill="white"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 0 1-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 0 1-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 0 1 2.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0 0 12.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 0 0 5.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 0 0-3.48-8.413z"/></svg>
      </a>
    </div>
    <button class="btn-edit" id="editBtn" onclick="handleEditBtn()">🔒 Edit</button>
    <button class="btn-resume" onclick="showToast('📄 Resume download coming soon!')">⬇ Resume</button>
  </div>
</nav>

<!-- ════ HOME ════ -->
<div class="page active" id="page-home">
  <div class="hero">
    <!-- LEFT -->
    <div class="hero-left">
      <div class="info-panel">
        <div class="info-panel-title">Quick Info</div>
        <a class="info-item" href="mailto:akashkoyrav7566@gmail.com">
          <div class="info-icon">📧</div>
          <div class="info-text"><div class="info-label">Email</div><div class="info-value"><span class="editable" id="info-email" contenteditable="false">akashkoyrav7566@gmail.com</span></div></div>
        </a>
        <a class="info-item" href="tel:+917509762086">
          <div class="info-icon">📱</div>
          <div class="info-text"><div class="info-label">Mobile</div><div class="info-value"><span class="editable" id="info-mobile" contenteditable="false">+91 75097 62086</span></div></div>
        </a>
        <a class="info-item" href="https://wa.me/917509762086" target="_blank">
          <div class="info-icon">💬</div>
          <div class="info-text"><div class="info-label">WhatsApp</div><div class="info-value">+91 75097 62086</div></div>
        </a>
        <a class="info-item" href="https://linkedin.com/in/akashkourav" target="_blank">
          <div class="info-icon">🔗</div>
          <div class="info-text"><div class="info-label">LinkedIn</div><div class="info-value"><span class="editable" id="info-li" contenteditable="false">linkedin.com/in/akashkourav</span></div></div>
        </a>
        <div class="info-item">
          <div class="info-icon">🎓</div>
          <div class="info-text"><div class="info-label">Education</div><div class="info-value"><span class="editable" id="info-edu" contenteditable="false">B.Tech — Computer Science</span></div></div>
        </div>
        <div class="info-item">
          <div class="info-icon">📍</div>
          <div class="info-text"><div class="info-label">Location</div><div class="info-value"><span class="editable" id="info-loc" contenteditable="false">Mumbai, India</span></div></div>
        </div>
        <div class="info-item">
          <div class="info-icon">💼</div>
          <div class="info-text"><div class="info-label">Experience</div><div class="info-value"><span class="editable" id="info-exp" contenteditable="false">2+ Years BI Analytics</span></div></div>
        </div>
        <div class="avail-badge"><div class="avail-dot"></div>Available for Hire</div>
      </div>
    </div>

    <!-- CENTER -->
    <div class="hero-center">
      <div class="profile-outer">
        <div class="ring-outer"></div>
        <div class="ring-inner"></div>
        <div class="profile-circle">
          <img id="profileImg" src="https://i.ibb.co/6R65B232" alt="Akash Kourav" onerror="this.src='data:image/svg+xml,%3Csvg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22%3E%3Crect fill=%22%235b4df5%22 width=%22100%22 height=%22100%22/%3E%3Ctext x=%2250%22 y=%2250%22 font-size=%2238%22 font-weight=%22bold%22 fill=%22white%22 text-anchor=%22middle%22 dy=%220.35em%22 font-family=%22sans-serif%22%3EAK%3C/text%3E%3C/svg%3E'">
        </div>
        <div class="metric m1"><div class="metric-val">50+</div><div class="metric-lbl">Dashboards</div></div>
        <div class="metric m2"><div class="metric-val">2+</div><div class="metric-lbl">Years Exp</div></div>
        <div class="metric m3"><div class="metric-val">⭐5.0</div><div class="metric-lbl">Rating</div></div>
      </div>

      <!-- Thought of the Day -->
      <div class="thought-card">
        <div class="thought-hdr">
          <div class="thought-label">Thought of the Day</div>
          <button class="thought-refresh" onclick="refreshThought()" title="New thought">↻ New</button>
        </div>
        <div class="thought-text" id="thoughtText">"Data is the new oil, but insight is the refinery."</div>
        <div class="thought-author" id="thoughtAuthor">— Anonymous</div>
      </div>
    </div>

    <!-- RIGHT -->
    <div class="hero-right">
      <p class="hero-eyebrow">Hello, I'm</p>
      <h1 class="hero-name"><span class="editable" id="info-name" contenteditable="false">Akash Kourav</span></h1>
      <p class="hero-role"><span class="editable" id="info-role" contenteditable="false">Power BI Developer & BI Analyst</span></p>
      <p class="hero-desc"><span class="editable" id="info-desc" contenteditable="false">Transforming raw data into powerful insights that drive smarter business decisions. Specializing in interactive dashboards, ETL pipelines, and data storytelling across industries.</span></p>

      <div class="tech-section">
        <div class="tech-section-label">Core Technologies</div>
        <div class="tech-grid">
          <div class="tech-chip"><span class="tech-chip-icon">📊</span><div><div class="tech-chip-name">Power BI</div><div class="tech-chip-level">Expert · 95%</div></div></div>
          <div class="tech-chip"><span class="tech-chip-icon">🗄️</span><div><div class="tech-chip-name">SQL</div><div class="tech-chip-level">Advanced · 90%</div></div></div>
          <div class="tech-chip"><span class="tech-chip-icon">🐍</span><div><div class="tech-chip-name">Python</div><div class="tech-chip-level">Intermediate · 80%</div></div></div>
          <div class="tech-chip"><span class="tech-chip-icon">📈</span><div><div class="tech-chip-name">Tableau</div><div class="tech-chip-level">Advanced · 85%</div></div></div>
          <div class="tech-chip"><span class="tech-chip-icon">☁️</span><div><div class="tech-chip-name">Azure</div><div class="tech-chip-level">Intermediate · 70%</div></div></div>
          <div class="tech-chip"><span class="tech-chip-icon">⚙️</span><div><div class="tech-chip-name">ETL / DAX</div><div class="tech-chip-level">Advanced · 88%</div></div></div>
        </div>
      </div>

      <div class="hero-ctas">
        <button onclick="showPage('projects',document.querySelectorAll('.nav-tab')[3])" class="btn-primary">Discover My Work →</button>
        <button onclick="scrollToContact()" class="btn-secondary">📩 Hire Me</button>
      </div>
    </div>
  </div>

  <!-- STATS -->
  <div class="stats-sec">
    <div class="stats-title">
      <h3>What I Bring To The Table</h3>
      <p>Proven expertise delivering measurable business impact through data intelligence</p>
    </div>
    <div class="stats-grid">
      <div class="scard"><span class="scard-icon">📊</span><div class="scard-val">50+</div><div class="scard-label">Dashboards</div><div class="scard-desc">Power BI & Tableau interactive reports</div></div>
      <div class="scard"><span class="scard-icon">⚡</span><div class="scard-val">40%</div><div class="scard-label">Time Saved</div><div class="scard-desc">Automated data pipelines & ETL</div></div>
      <div class="scard"><span class="scard-icon">💰</span><div class="scard-val">30%</div><div class="scard-label">Cost Savings</div><div class="scard-desc">Operational efficiency gains</div></div>
      <div class="scard"><span class="scard-icon">🎯</span><div class="scard-val">100%</div><div class="scard-label">Accuracy</div><div class="scard-desc">SQL-optimized data integrity</div></div>
      <div class="scard"><span class="scard-icon">🏆</span><div class="scard-val">5+</div><div class="scard-label">Certifications</div><div class="scard-desc">Microsoft, Google, Tableau</div></div>
    </div>

    <div class="hero-visual-wrap">
      <p class="visual-section-title">Skills Proficiency Overview</p>
      <div class="radar-wrap"><canvas id="radarChart" style="max-width:240px;max-height:240px;"></canvas></div>
      <div class="skill-bars">
        <div class="skill-bar-item">
          <div class="skill-bar-label"><span>Power BI / DAX</span><span>95%</span></div>
          <div class="skill-bar-track"><div class="skill-bar-fill" style="width:0" data-width="95%"></div></div>
        </div>
        <div class="skill-bar-item">
          <div class="skill-bar-label"><span>SQL / MySQL</span><span>90%</span></div>
          <div class="skill-bar-track"><div class="skill-bar-fill" style="width:0" data-width="90%"></div></div>
        </div>
        <div class="skill-bar-item">
          <div class="skill-bar-label"><span>Python / ETL</span><span>80%</span></div>
          <div class="skill-bar-track"><div class="skill-bar-fill" style="width:0" data-width="80%"></div></div>
        </div>
        <div class="skill-bar-item">
          <div class="skill-bar-label"><span>Tableau</span><span>85%</span></div>
          <div class="skill-bar-track"><div class="skill-bar-fill" style="width:0" data-width="85%"></div></div>
        </div>
        <div class="skill-bar-item">
          <div class="skill-bar-label"><span>Azure / Cloud</span><span>70%</span></div>
          <div class="skill-bar-track"><div class="skill-bar-fill" style="width:0" data-width="70%"></div></div>
        </div>
        <div class="skill-bar-item">
          <div class="skill-bar-label"><span>Data Modeling</span><span>88%</span></div>
          <div class="skill-bar-track"><div class="skill-bar-fill" style="width:0" data-width="88%"></div></div>
        </div>
      </div>
    </div>
  </div>

  <!-- MARKET UPDATES -->
  <div class="home-market-sec">
    <div class="home-market-inner">
      <div class="home-market-hdr">
        <div>
          <h3>📡 Latest Tech Updates</h3>
          <p>Power BI · Microsoft Fabric · Cloud · AI/ML — refreshed daily</p>
        </div>
        <button class="refresh-small" onclick="loadHomeMarket(true)">🔄 Refresh</button>
      </div>
      <div id="homeMarketFeed">
        <div class="market-loading"><div class="market-spinner"></div>Fetching latest updates...</div>
      </div>
    </div>
  </div>

  <!-- CONTACT -->
  <div class="contact-section" id="contactSection">
    <div class="contact-wrap">
      <div class="contact-header">
        <span class="sec-label-sm">Let's Connect</span>
        <h2>Get In Touch</h2>
        <p>Have a project in mind? Want to collaborate or hire? Drop a message — I'll get back within 24 hours.</p>
      </div>
      <div class="contact-form">
        <div class="form-grid">
          <div class="fg-contact"><label>Your Name</label><span class="fi">👤</span><input type="text" id="f-name" placeholder="John Doe"></div>
          <div class="fg-contact"><label>Mobile Number</label><span class="fi">📱</span><input type="tel" id="f-mobile" placeholder="+91 98765 43210"></div>
          <div class="fg-contact"><label>Email Address</label><span class="fi">📧</span><input type="email" id="f-email" placeholder="you@company.com"></div>
          <div class="fg-contact no-icon"><label>Purpose of Connect</label>
            <select id="f-purpose"><option value="" disabled selected>Select purpose...</option><option>Full-time Hire</option><option>Freelance / Project</option><option>Collaboration</option><option>Mentorship</option><option>Networking</option><option>Other</option></select>
          </div>
          <div class="fg-contact full no-icon"><label>Message / Description</label><textarea id="f-desc" placeholder="Tell me about your project or requirement..."></textarea></div>
          <div class="full"><button class="form-submit" id="formSubmitBtn" onclick="handleFormSubmit()">🚀 Send Message</button></div>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- ABOUT -->
<div class="page" id="page-about">
  <section class="sec">
    <p class="sec-label">About</p><h2>Data-driven Analyst</h2><div class="sec-bar"></div>
    <div class="about-grid">
      <div class="about-img">🧑‍💻</div>
      <div class="about-body">
        <h3 style="font-size:1rem;margin-bottom:.7rem;font-family:'Syne',sans-serif;color:var(--text);">Hi, I'm Akash 👋</h3>
        <p>Power BI Developer & BI Analyst based in Mumbai, India. I specialize in designing interactive dashboards, building data pipelines, and translating complex datasets into clear, actionable insights that decision-makers can actually use.</p>
        <p>My work sits at the intersection of analytics, visualization, and business strategy — helping organizations make smarter, faster decisions backed by real data. I've delivered 50+ dashboards across sales, operations, and customer analytics domains.</p>
        <p>Currently open to full-time roles, freelance projects, and exciting collaborations in the BI & Analytics space.</p>
        <div class="chips">
          <span class="chip">📍 Mumbai, India</span><span class="chip">💼 BI Analyst</span>
          <span class="chip">🎓 B.Tech CS</span><span class="chip">⚡ Available Now</span>
          <span class="chip">📊 Power BI Expert</span><span class="chip">🐍 Python</span>
        </div>
      </div>
    </div>
  </section>
</div>

<!-- SKILLS -->
<div class="page" id="page-skills">
  <section class="sec">
    <p class="sec-label">Skills</p><h2>Technical Expertise</h2><div class="sec-bar"></div>
    <div class="skills-grid">
      <div class="sk"><div class="sk-icon">📊</div><div class="sk-title">BI & Visualization</div><div class="tags"><span class="tag h">Power BI</span><span class="tag h">Tableau</span><span class="tag">Looker Studio</span><span class="tag">DAX</span></div></div>
      <div class="sk"><div class="sk-icon">🗄️</div><div class="sk-title">Database & SQL</div><div class="tags"><span class="tag h">SQL</span><span class="tag h">MySQL</span><span class="tag">BigQuery</span><span class="tag">PostgreSQL</span></div></div>
      <div class="sk"><div class="sk-icon">🐍</div><div class="sk-title">Programming</div><div class="tags"><span class="tag h">Python</span><span class="tag">Pandas</span><span class="tag">NumPy</span><span class="tag">Matplotlib</span></div></div>
      <div class="sk"><div class="sk-icon">⚙️</div><div class="sk-title">Data Engineering</div><div class="tags"><span class="tag h">ETL Pipelines</span><span class="tag">Data Modeling</span><span class="tag">KPI Design</span></div></div>
      <div class="sk"><div class="sk-icon">☁️</div><div class="sk-title">Cloud & Platforms</div><div class="tags"><span class="tag">Azure</span><span class="tag">Google Cloud</span><span class="tag">MS Fabric</span></div></div>
      <div class="sk"><div class="sk-icon">🤝</div><div class="sk-title">Soft Skills</div><div class="tags"><span class="tag h">Data Storytelling</span><span class="tag">Stakeholder Mgmt</span><span class="tag">Agile</span></div></div>
    </div>
  </section>
</div>

<!-- PROJECTS -->
<div class="page" id="page-projects">
  <section class="sec">
    <p class="sec-label">Work</p><h2>Featured Projects</h2><div class="sec-bar"></div>
    <div class="projects-grid">
      <div class="proj"><div class="proj-type">Power BI · DAX · SQL</div><div class="proj-title">Executive Sales Dashboard</div><p class="proj-desc">Multi-page Power BI dashboard for 3 regions. Drill-through from KPIs to rep-level performance. Reduced reporting time by 6 hrs/week.</p></div>
      <div class="proj"><div class="proj-type">Python · ETL · Automation</div><div class="proj-title">Automated Reporting Pipeline</div><p class="proj-desc">Python ETL replacing 8 hours/week of manual reporting with a fully automated scheduled pipeline. Zero manual intervention needed.</p></div>
      <div class="proj"><div class="proj-type">Tableau · Data Modeling</div><div class="proj-title">Customer Churn Analysis</div><p class="proj-desc">Tableau story with predictive churn indicators helping identify at-risk customers. Reduced churn rate by 15% in 2 quarters.</p></div>
      <div class="proj"><div class="proj-type">BigQuery · Looker Studio</div><div class="proj-title">Operations Performance Tracker</div><p class="proj-desc">Real-time ops tracker monitoring SLA compliance, team productivity metrics, and escalation trends across 5 departments.</p></div>
    </div>
  </section>
</div>

<!-- EXPERIENCE -->
<div class="page" id="page-experience">
  <section class="sec">
    <p class="sec-label">Career</p><h2>Work Experience</h2><div class="sec-bar"></div>
    <div class="exp-timeline">
      <div class="exp-item">
        <div class="exp-dot">💼</div>
        <div class="exp-card">
          <div class="exp-header"><div class="exp-title">Associate Analyst – BI</div><div class="exp-period">2023 – Present</div></div>
          <div class="exp-company">🏢 XYZ Analytics, Mumbai</div>
          <ul class="exp-bullets">
            <li>Designed 15+ Power BI dashboards for C-suite stakeholders, replacing legacy Excel reports</li>
            <li>Built Python ETL pipelines reducing manual reporting effort by 40% across 3 departments</li>
            <li>Optimized SQL queries improving dashboard load times by 60% via indexing & query restructuring</li>
            <li>Delivered automated weekly MIS reports saving 8+ hours of analyst time per week</li>
          </ul>
        </div>
      </div>
      <div class="exp-item">
        <div class="exp-dot">📊</div>
        <div class="exp-card">
          <div class="exp-header"><div class="exp-title">Data Analyst Intern</div><div class="exp-period">2022 – 2023</div></div>
          <div class="exp-company">🏢 ABC Solutions, Mumbai</div>
          <ul class="exp-bullets">
            <li>Developed Tableau dashboards for real-time sales tracking across 4 product lines</li>
            <li>Performed EDA on large customer datasets (500K+ rows) using Python & SQL</li>
            <li>Created automated Excel MIS reports streamlining monthly reporting for management</li>
          </ul>
        </div>
      </div>
      <div class="exp-item">
        <div class="exp-dot">🎓</div>
        <div class="exp-card">
          <div class="exp-header"><div class="exp-title">B.Tech — Computer Science</div><div class="exp-period">2018 – 2022</div></div>
          <div class="exp-company">🏛️ University of Mumbai</div>
          <ul class="exp-bullets">
            <li>Focused on databases, data structures, algorithms & software engineering principles</li>
            <li>Final year project: Power BI analytics platform for academic performance tracking</li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</div>

<!-- GROWTH -->
<div class="page" id="page-growth">
  <section class="sec">
    <p class="sec-label">Growth</p>
    <h2>Skills & Certifications Growth</h2>
    <div class="sec-bar"></div>
    <p class="sec-sub">My learning journey 2021–2025: technologies mastered, certifications earned, impact delivered, and costs saved.</p>
    <div class="growth-kpi-grid">
      <div class="gkpi"><div class="gkpi-icon">🛠️</div><div class="gkpi-val">12</div><div class="gkpi-label">Skills Mastered</div><div class="gkpi-badge up">▲ +20% vs last year</div><div class="gkpi-sub">10 skills (2024) → 12 (2025)</div></div>
      <div class="gkpi"><div class="gkpi-icon">🎓</div><div class="gkpi-val">5</div><div class="gkpi-label">Certifications Earned</div><div class="gkpi-badge up">▲ +25% vs last year</div><div class="gkpi-sub">4 certs (2024) → 5 (2025)</div></div>
      <div class="gkpi"><div class="gkpi-icon">⚡</div><div class="gkpi-val">60%</div><div class="gkpi-label">Time Saved</div><div class="gkpi-badge up">▲ +50% vs last year</div><div class="gkpi-sub">40% (2024) → 60% (2025)</div></div>
      <div class="gkpi"><div class="gkpi-icon">💰</div><div class="gkpi-val">30%</div><div class="gkpi-label">Cost Savings</div><div class="gkpi-badge up">▲ +20% vs last year</div><div class="gkpi-sub">25% (2024) → 30% (2025)</div></div>
    </div>
    <div class="growth-container">
      <canvas id="growthChart" class="growth-canvas"></canvas>
    </div>
  </section>
</div>

<!-- MARKET -->
<div class="page" id="page-market">
  <section class="sec">
    <p class="sec-label">Market</p><h2>Latest Tech Updates</h2><div class="sec-bar"></div>
    <p class="sec-sub">Daily-refreshed updates on Power BI, Microsoft Fabric, Cloud, and AI/ML. Click any card to read more.</p>
    <div id="marketFeed">
      <div class="market-loading"><div class="market-spinner"></div>Fetching latest updates...</div>
    </div>
  </section>
</div>

<!-- CERTS -->
<div class="page" id="page-certs">
  <section class="sec">
    <p class="sec-label">Credentials</p>
    <h2>Certifications</h2>
    <div class="sec-bar"></div>
    <div class="cert-hero-stats">
      <div class="cert-hero-stat"><div class="cert-stat-icon">🏆</div><div class="cert-stat-val">5</div><div class="cert-stat-label">Total Certifications</div><div class="cert-stat-sub">Verified from Microsoft, Google & Tableau</div></div>
      <div class="cert-hero-stat"><div class="cert-stat-icon">🛠️</div><div class="cert-stat-val">12</div><div class="cert-stat-label">Skills Acquired</div><div class="cert-stat-sub">From Power BI to Cloud to Python</div></div>
      <div class="cert-hero-stat"><div class="cert-stat-icon">🌐</div><div class="cert-stat-val">3</div><div class="cert-stat-label">Platforms Certified</div><div class="cert-stat-sub">Microsoft · Google · Tableau / Cisco</div></div>
    </div>
    <div class="skills-learned-wrap">
      <div class="skills-learned-hdr">
        <div class="skills-learned-title">Skills Learned via Certifications</div>
        <div class="skills-learned-count">12 skills</div>
      </div>
      <div class="skills-learned-chips">
        <span class="sl-chip hot">Power BI</span><span class="sl-chip hot">DAX</span><span class="sl-chip hot">Data Modeling</span>
        <span class="sl-chip">SQL</span><span class="sl-chip">Python</span><span class="sl-chip hot">Tableau</span>
        <span class="sl-chip">BigQuery</span><span class="sl-chip">Google Analytics</span><span class="sl-chip">ETL Pipelines</span>
        <span class="sl-chip">Azure Fundamentals</span><span class="sl-chip">Data Storytelling</span><span class="sl-chip">KPI Design</span>
      </div>
    </div>
    <div class="certs-grid">
      <div class="cert-card"><div class="cert-card-badge">2024</div><div class="cert-wrap"><div class="cert-placeholder"><div class="cert-emoji">🪟</div><div>Microsoft Certified</div></div></div><div class="cert-body"><div class="cert-org">🏢 Microsoft</div><div class="cert-name">PL-300: Power BI Data Analyst</div><div class="cert-meta"><span class="cert-year">✦ Jan 2024</span><span class="cert-level">Expert</span></div></div></div>
      <div class="cert-card"><div class="cert-card-badge">2023</div><div class="cert-wrap"><div class="cert-placeholder"><div class="cert-emoji">🔍</div><div>Google Certified</div></div></div><div class="cert-body"><div class="cert-org">🏢 Google</div><div class="cert-name">Data Analytics Professional Certificate</div><div class="cert-meta"><span class="cert-year">✦ Jun 2023</span><span class="cert-level">Professional</span></div></div></div>
      <div class="cert-card"><div class="cert-card-badge">2023</div><div class="cert-wrap"><div class="cert-placeholder"><div class="cert-emoji">📊</div><div>Tableau Certified</div></div></div><div class="cert-body"><div class="cert-org">🏢 Tableau / Salesforce</div><div class="cert-name">Tableau Desktop Specialist</div><div class="cert-meta"><span class="cert-year">✦ Mar 2023</span><span class="cert-level">Specialist</span></div></div></div>
      <div class="cert-card"><div class="cert-card-badge">2022</div><div class="cert-wrap"><div class="cert-placeholder"><div class="cert-emoji">☁️</div><div>Azure Certified</div></div></div><div class="cert-body"><div class="cert-org">🏢 Microsoft</div><div class="cert-name">AZ-900: Azure Fundamentals</div><div class="cert-meta"><span class="cert-year">✦ Sep 2022</span><span class="cert-level">Foundational</span></div></div></div>
      <div class="cert-card"><div class="cert-card-badge">2022</div><div class="cert-wrap"><div class="cert-placeholder"><div class="cert-emoji">🐍</div><div>Cisco NetAcad</div></div></div><div class="cert-body"><div class="cert-org">🏢 Cisco / NetAcad</div><div class="cert-name">Python Essentials 1 & 2</div><div class="cert-meta"><span class="cert-year">✦ Apr 2022</span><span class="cert-level">Intermediate</span></div></div></div>
      <div class="add-cert" onclick="guardedAction(()=>showToast('Enter edit mode to add certifications'))"><span style="font-size:1.4rem;">＋</span><div>Add Certification</div></div>
    </div>
  </section>
</div>

<!-- AWARDS -->
<div class="page" id="page-awards">
  <section class="sec">
    <p class="sec-label">Recognition</p><h2>Awards & Appreciation</h2><div class="sec-bar"></div>
    <div class="awards-grid">
      <div class="award-card"><div class="award-wrap"><div class="award-placeholder"><span style="font-size:1.9rem">🏆</span><div>Star Performer</div></div></div><div class="award-body"><div class="award-badge">🏆 Recognition</div><div class="award-title">Star Performer Award</div><div class="award-desc">Outstanding contribution to the BI team in Q3 2024. Delivered 5 dashboards ahead of schedule.</div></div></div>
      <div class="award-card"><div class="award-wrap"><div class="award-placeholder"><span style="font-size:1.9rem">🌟</span><div>Client Appreciation</div></div></div><div class="award-body"><div class="award-badge">🌟 Appreciation</div><div class="award-title">Client Appreciation Letter</div><div class="award-desc">Excellent delivery of executive dashboard project with zero revisions requested by the client.</div></div></div>
      <div class="add-award" onclick="guardedAction(()=>showToast('Enter edit mode to add awards'))"><span style="font-size:1.4rem;">＋</span><div>Add Award</div></div>
    </div>
  </section>
</div>

<footer>
  <span>© 2025 Akash Kourav — BI Analyst & Power BI Developer · Mumbai, India</span>
  <span>Built with precision & purpose</span>
</footer>

<!-- CHATBOT -->
<button class="chat-fab" id="chatFab" onclick="toggleChat()">
  <span class="chat-fab-icon">💬</span>
  <div class="chat-badge">AI</div>
</button>
<div class="cwin" id="chatWin">
  <div class="chat-hdr">
    <div class="chat-av">AK</div>
    <div><div class="chat-av-name">Akash's AI Assistant</div><div class="chat-av-status">Online now</div></div>
    <button class="cclose" onclick="toggleChat()">✕</button>
  </div>
  <div class="cmsgs" id="cmsgs">
    <div class="cmsg bot"><div class="cdot">AK</div><div class="cbubble">Hi there! 👋 I'm Akash's AI assistant. Ask me anything about his skills, projects, experience, certifications, or how to hire him!</div></div>
  </div>
  <div class="cquick">
    <button class="cqbtn" onclick="quickAsk('What are Akash\'s main skills?')">🛠 Skills</button>
    <button class="cqbtn" onclick="quickAsk('Tell me about Akash\'s projects')">💼 Work</button>
    <button class="cqbtn" onclick="quickAsk('What certifications does Akash have?')">🎓 Certs</button>
    <button class="cqbtn" onclick="quickAsk('How can I connect with Akash?')">🔗 Connect</button>
    <button class="cqbtn" onclick="quickAsk('I want to hire Akash')">📩 Hire</button>
  </div>
  <div class="cinput-row">
    <input class="cinput" id="chatIn" type="text" placeholder="Ask anything about Akash..." onkeydown="if(event.key==='Enter')sendChat()">
    <button class="csend" onclick="sendChat()">➤</button>
  </div>
</div>

<script>
const ADMIN_ID='Akash7566',ADMIN_PWD='Aman7566';
const OWNER_EMAIL='akashkoyrav7566@gmail.com';
const OWNER_WHATSAPP='+917509762086';
let isEdit=false,chatOpen=false,marketLoaded=false,homeMarketLoaded=false;

const THOUGHTS=[
  {text:'"Data is the new oil, but insight is the refinery."',author:'— Anonymous'},
  {text:'"Without data, you\'re just another person with an opinion."',author:'— W. Edwards Deming'},
  {text:'"The goal is to turn data into information and information into insight."',author:'— Carly Fiorina'},
  {text:'"In God we trust; all others must bring data."',author:'— W. Edwards Deming'},
  {text:'"Data will talk to you if you\'re willing to listen."',author:'— Jim Bergeson'},
  {text:'"Torture the data long enough and it will confess to anything."',author:'— Ronald Coase'},
  {text:'"The world is one big data problem."',author:'— Andrew McAfee'},
  {text:'"Data beats emotions."',author:'— Sean Rad'},
  {text:'"It is a capital mistake to theorize before one has data."',author:'— Arthur Conan Doyle'},
  {text:'"Numbers have an important story to tell. They rely on you to give them a clear and convincing voice."',author:'— Stephen Few'},
  {text:'"Information is the oil of the 21st century, and analytics is the combustion engine."',author:'— Peter Sondergaard'},
  {text:'"The most valuable commodity I know of is information."',author:'— Gordon Gekko'},
  {text:'"Data is not information; information is not knowledge; knowledge is not wisdom."',author:'— Clifford Stoll'},
  {text:'"Make it simple, but significant."',author:'— Don Draper'},
  {text:'"Every company has big data in its future, and every company will eventually be in the data business."',author:'— Thomas H. Davenport'},
];
let lastThoughtIdx=-1;
function refreshThought(){
  let idx;do{idx=Math.floor(Math.random()*THOUGHTS.length);}while(idx===lastThoughtIdx&&THOUGHTS.length>1);
  lastThoughtIdx=idx;
  const t=THOUGHTS[idx];
  const textEl=document.getElementById('thoughtText');
  const authEl=document.getElementById('thoughtAuthor');
  textEl.style.opacity='0';authEl.style.opacity='0';
  setTimeout(()=>{textEl.textContent=t.text;authEl.textContent=t.author;textEl.style.transition='opacity .4s';authEl.style.transition='opacity .4s';textEl.style.opacity='1';authEl.style.opacity='1';},220);
}

const KB={
  name:`Akash Kourav`,role:`Power BI Developer & BI Analyst based in Mumbai, India`,
  email:`akashkoyrav7566@gmail.com`,phone:`+91 75097 62086`,
  about:`Akash Kourav is a Power BI Developer & BI Analyst based in Mumbai, India with 2+ years of experience. He specializes in designing interactive dashboards, building data pipelines, and translating complex datasets into actionable insights. Currently available for full-time roles, freelance projects, and collaborations.`,
  skills:`Akash's core skills:\n• Power BI & DAX — Expert (95%)\n• SQL / MySQL — Advanced (90%)\n• Tableau — Advanced (85%)\n• Data Modeling — Advanced (88%)\n• Python (Pandas, NumPy) — Intermediate (80%)\n• ETL Pipelines — Advanced\n• Azure / Cloud — Intermediate (70%)\n• Data Storytelling & Stakeholder Management`,
  projects:`Key projects:\n1. 📊 Executive Sales Dashboard — Power BI, 3 regions, reduced reporting by 6hrs/week\n2. ⚡ Automated Reporting Pipeline — Python ETL, eliminated 8hrs/week manual work\n3. 📉 Customer Churn Analysis — Tableau, reduced churn 15%\n4. 🏭 Operations Performance Tracker — BigQuery/Looker, SLA dashboard across 5 depts`,
  certs:`5 certifications:\n• 🪟 PL-300: Power BI Data Analyst (Microsoft, 2024)\n• 🔍 Google Data Analytics Professional (2023)\n• 📊 Tableau Desktop Specialist (2023)\n• ☁️ AZ-900: Azure Fundamentals (2022)\n• 🐍 Python Essentials 1 & 2 (Cisco, 2022)`,
  experience:`Experience:\n• Associate Analyst – BI at XYZ Analytics (2023–Present): 15+ dashboards, 40% effort reduction\n• Data Analyst Intern at ABC Solutions (2022–2023): Tableau, 500K+ row EDA\n• B.Tech CS, University of Mumbai (2018–2022)`,
  impact:`Impact:\n• 50+ dashboards built\n• 40% time saved\n• 30% cost savings\n• 60% faster dashboards via SQL optimization\n• 8+ hrs/week saved via automation`,
  awards:`Awards:\n• 🏆 Star Performer Award — Q3 2024\n• 🌟 Client Appreciation Letter — zero-revision delivery`,
  hire:`To hire or connect with Akash:\n📧 akashkoyrav7566@gmail.com\n📱 +91 75097 62086\n🔗 linkedin.com/in/akashkourav\n\nOpen to: Full-time roles, Freelance, Collaborations, Mentorship\n\nSay "open contact form" to reach out directly!`,
  contact_form:`Opening the contact form now! Fill in your details and Akash will respond within 24 hours. 📩`,
};
function getBotReply(msg){
  const m=msg.toLowerCase();
  if(m==='yes'||m.includes('open contact')||m.includes('get in touch')||m.includes('contact form')){setTimeout(()=>{toggleChat();scrollToContact();},400);return KB.contact_form;}
  if(m.includes('skill')||m.includes('tool')||m.includes('technolog'))return KB.skills;
  if(m.includes('project')||m.includes('work')||m.includes('dashboard')||m.includes('portfolio'))return KB.projects;
  if(m.includes('cert')||m.includes('pl-300')||m.includes('credential'))return KB.certs;
  if(m.includes('award')||m.includes('recognition')||m.includes('achiev'))return KB.awards;
  if(m.includes('hire')||m.includes('recruit')||m.includes('available')||m.includes('open to'))return KB.hire;
  if(m.includes('connect')||m.includes('contact')||m.includes('email')||m.includes('reach')||m.includes('whatsapp'))return KB.hire;
  if(m.includes('experience')||m.includes('job')||m.includes('career')||m.includes('company'))return KB.experience;
  if(m.includes('impact')||m.includes('result')||m.includes('saving')||m.includes('stat'))return KB.impact;
  if(m.includes('hello')||m.includes('hi ')||m==='hi'||m==='hello'||m.includes('hey'))return `Hi! 👋 I'm Akash's AI assistant. Ask me about his skills, projects, certifications, experience, or how to hire him.`;
  if(m.includes('location')||m.includes('where')||m.includes('mumbai'))return `Akash is based in Mumbai, India. Available for remote work globally as well as on-site opportunities in Mumbai.`;
  if(m.includes('education')||m.includes('degree')||m.includes('btech'))return `B.Tech in Computer Science from University of Mumbai (2018–2022). Final year project was a Power BI analytics platform.`;
  if(m.includes('about')||m.includes('who is'))return KB.about;
  return `I can help with:\n• 🛠 Skills & technologies\n• 💼 Projects & portfolio\n• 🎓 Certifications\n• 📋 Work experience\n• 🏆 Awards\n• 📩 How to hire Akash\n\nWhat would you like to know?`;
}

function handleEditBtn(){isEdit?logoutEdit():openLogin();}
function openLogin(){document.getElementById('loginModal').classList.add('open');document.getElementById('lid').focus();}
function closeLogin(){document.getElementById('loginModal').classList.remove('open');}
function doLogin(){
  const id=document.getElementById('lid').value.trim(),pw=document.getElementById('lpwd').value;
  if(id===ADMIN_ID&&pw===ADMIN_PWD){closeLogin();enableEdit();}
  else{document.getElementById('loginErr').classList.add('show');document.getElementById('lpwd').value='';document.getElementById('lpwd').focus();}
}
function enableEdit(){
  isEdit=true;document.body.classList.add('edit-mode');
  document.getElementById('editBanner').classList.add('show');
  const btn=document.getElementById('editBtn');btn.className='btn-edit unlocked';btn.innerHTML='✏️ Exit Edit';
  document.querySelectorAll('.editable').forEach(e=>e.setAttribute('contenteditable','true'));
  showToast('✅ Edit Mode Active — click text to edit');
}
function logoutEdit(){
  isEdit=false;document.body.classList.remove('edit-mode');
  document.getElementById('editBanner').classList.remove('show');
  const btn=document.getElementById('editBtn');btn.className='btn-edit';btn.innerHTML='🔒 Edit';
  document.querySelectorAll('.editable').forEach(e=>e.setAttribute('contenteditable','false'));
  showToast('🔒 Edits Saved');
}
function guardedAction(fn){isEdit?fn():openLogin();}

function showPage(id,tab){
  document.querySelectorAll('.page').forEach(p=>p.classList.remove('active'));
  document.querySelectorAll('.nav-tab').forEach(t=>t.classList.remove('active'));
  document.getElementById('page-'+id).classList.add('active');
  if(tab&&tab.classList)tab.classList.add('active');
  window.scrollTo({top:0,behavior:'smooth'});
  if(id==='growth')setTimeout(initGrowthChart,120);
  if(id==='market'&&!marketLoaded)loadMarket();
}

function showToast(msg,dur=3000){
  const t=document.getElementById('toast');t.textContent=msg;t.classList.add('show');
  setTimeout(()=>t.classList.remove('show'),dur);
}
function openLB(src){document.getElementById('lb-img').src=src;document.getElementById('lightbox').classList.add('open');}
function closeLB(){document.getElementById('lightbox').classList.remove('open');}

function scrollToContact(){
  showPage('home',document.querySelector('.nav-tab'));
  setTimeout(()=>document.getElementById('contactSection').scrollIntoView({behavior:'smooth',block:'start'}),300);
}

async function handleFormSubmit(){
  const name=document.getElementById('f-name').value.trim();
  const mobile=document.getElementById('f-mobile').value.trim();
  const email=document.getElementById('f-email').value.trim();
  const purpose=document.getElementById('f-purpose').value;
  const desc=document.getElementById('f-desc').value.trim();
  if(!name||!email||!purpose){showToast('⚠️ Please fill Name, Email & Purpose');return;}
  const btn=document.getElementById('formSubmitBtn');btn.disabled=true;btn.textContent='⏳ Sending...';
  const msgBody=`New Contact Request from Portfolio:\n\nName: ${name}\nMobile: ${mobile||'Not provided'}\nEmail: ${email}\nPurpose: ${purpose}\nMessage: ${desc||'No message'}`;
  try{
    const mailtoLink=`mailto:${OWNER_EMAIL}?subject=Portfolio Contact: ${encodeURIComponent(purpose)} from ${encodeURIComponent(name)}&body=${encodeURIComponent(msgBody)}`;
    const waMsg=`🔔 *New Portfolio Contact*\n\n*Name:* ${name}\n*Mobile:* ${mobile||'N/A'}\n*Email:* ${email}\n*Purpose:* ${purpose}\n*Message:* ${desc||'N/A'}`;
    const waLink=`https://wa.me/${OWNER_WHATSAPP.replace(/\D/g,'')}?text=${encodeURIComponent(waMsg)}`;
    window.open(mailtoLink,'_blank');
    showToast('✅ Message sent! Akash will respond within 24 hours 🚀',4500);
    setTimeout(()=>{if(confirm('Message sent via Email! 📧\n\nWould you also like to send via WhatsApp for faster response?'))window.open(waLink,'_blank');},1000);
  }catch{showToast('⚠️ Please email akashkoyrav7566@gmail.com directly',5000);}
  ['f-name','f-mobile','f-email','f-desc'].forEach(id=>{document.getElementById(id).value='';});
  document.getElementById('f-purpose').selectedIndex=0;
  btn.disabled=false;btn.textContent='🚀 Send Message';
}

function toggleChat(){
  chatOpen=!chatOpen;
  const w=document.getElementById('chatWin');
  chatOpen?w.classList.add('open'):w.classList.remove('open');
}
function quickAsk(q){
  if(!chatOpen){chatOpen=true;document.getElementById('chatWin').classList.add('open');}
  document.getElementById('chatIn').value=q;sendChat();
}
function sendChat(){
  const inp=document.getElementById('chatIn'),msg=inp.value.trim();
  if(!msg)return;inp.value='';
  appendMsg('user',msg);
  const typingId='t'+Date.now();appendTyping(typingId);
  setTimeout(()=>{removeTyping(typingId);appendMsg('bot',getBotReply(msg));},480+Math.random()*300);
}
function appendMsg(role,text){
  const c=document.getElementById('cmsgs');
  const d=document.createElement('div');d.className='cmsg '+role;
  const dot=document.createElement('div');dot.className='cdot';dot.textContent=role==='bot'?'AK':'👤';
  const b=document.createElement('div');b.className='cbubble';b.textContent=text;
  d.appendChild(dot);d.appendChild(b);c.appendChild(d);c.scrollTop=c.scrollHeight;
}
function appendTyping(id){
  const c=document.getElementById('cmsgs');
  const d=document.createElement('div');d.className='cmsg bot';d.id=id;
  const dot=document.createElement('div');dot.className='cdot';dot.textContent='AK';
  const b=document.createElement('div');b.className='cbubble';
  b.innerHTML='<span class="typing-dots"><span></span><span></span><span></span></span>';
  d.appendChild(dot);d.appendChild(b);c.appendChild(d);c.scrollTop=c.scrollHeight;
}
function removeTyping(id){const el=document.getElementById(id);if(el)el.remove();}

function initRadarChart(){
  const ctx=document.getElementById('radarChart');if(!ctx)return;
  if(ctx._chartInstance){ctx._chartInstance.destroy();}
  ctx._chartInstance=new Chart(ctx,{
    type:'radar',
    data:{
      labels:['Power BI','SQL','Python','Tableau','Azure','Data Modeling'],
      datasets:[{label:'Proficiency',data:[95,90,80,85,70,88],backgroundColor:'rgba(91,77,245,.1)',borderColor:'#5b4df5',borderWidth:2.5,pointBackgroundColor:'#5b4df5',pointBorderColor:'#fff',pointBorderWidth:2,pointRadius:4,pointHoverRadius:6}]
    },
    options:{responsive:true,maintainAspectRatio:true,plugins:{legend:{display:false},tooltip:{callbacks:{label:c=>' '+c.raw+'%'}}},scales:{r:{min:0,max:100,ticks:{display:false,stepSize:20},grid:{color:'rgba(91,77,245,.08)'},angleLines:{color:'rgba(91,77,245,.08)'},pointLabels:{color:'#64748b',font:{size:10,family:'Plus Jakarta Sans',weight:'600'}}}}}
  });
  setTimeout(()=>document.querySelectorAll('.skill-bar-fill').forEach(bar=>{bar.style.width=bar.dataset.width;}),350);
}

let growthChartInst=null;
function initGrowthChart(){
  const ctx=document.getElementById('growthChart');if(!ctx)return;
  if(growthChartInst){growthChartInst.destroy();}
  growthChartInst=new Chart(ctx,{
    type:'line',
    data:{
      labels:['2021','2022','2023','2024','2025'],
      datasets:[
        {label:'Skills Mastered',data:[2,5,8,10,12],borderColor:'#5b4df5',backgroundColor:'rgba(91,77,245,.08)',borderWidth:2.5,fill:true,tension:.4,pointBackgroundColor:'#5b4df5',pointRadius:4,pointHoverRadius:7},
        {label:'Certifications',data:[0,1,2,4,5],borderColor:'#10b981',backgroundColor:'rgba(16,185,129,.07)',borderWidth:2.5,fill:true,tension:.4,pointBackgroundColor:'#10b981',pointRadius:4,pointHoverRadius:7},
        {label:'% Time Saved',data:[0,5,15,40,60],borderColor:'#3b82f6',backgroundColor:'rgba(59,130,246,.07)',borderWidth:2.5,fill:true,tension:.4,pointBackgroundColor:'#3b82f6',pointRadius:4,pointHoverRadius:7},
        {label:'% Cost Savings',data:[0,3,10,25,30],borderColor:'#f59e0b',backgroundColor:'rgba(245,158,11,.06)',borderWidth:2.5,fill:true,tension:.4,pointBackgroundColor:'#f59e0b',pointRadius:4,pointHoverRadius:7}
      ]
    },
    options:{responsive:true,maintainAspectRatio:false,interaction:{mode:'index',intersect:false},plugins:{legend:{labels:{color:'#64748b',usePointStyle:true,pointStyle:'circle',padding:14,font:{family:'Plus Jakarta Sans',size:11}}},tooltip:{backgroundColor:'rgba(255,255,255,.97)',borderColor:'rgba(91,77,245,.2)',borderWidth:1,titleColor:'#0f172a',bodyColor:'#64748b',padding:10,titleFont:{weight:'bold',family:'Plus Jakarta Sans'}}},scales:{y:{ticks:{color:'#94a3b8',font:{size:10}},grid:{color:'rgba(148,163,184,.12)'},beginAtZero:true},x:{ticks:{color:'#94a3b8',font:{size:11}},grid:{color:'rgba(148,163,184,.12)'}}}}
  });
}

const FALLBACK_ARTICLES=[
  {category:'POWER BI',title:'Copilot in Power BI: AI-Powered Report Generation',summary:'Microsoft\'s Copilot reduces dashboard creation time by up to 50% with AI-generated insights and narratives.',url:'https://powerbi.microsoft.com/blog',date:'May 2025'},
  {category:'FABRIC',title:'Microsoft Fabric OneLake: Unified Data Lake Updates',summary:'New Fabric features simplify data engineering with a unified lakehouse architecture for all analytics workloads.',url:'https://learn.microsoft.com/en-us/fabric',date:'May 2025'},
  {category:'CLOUD',title:'Azure Synapse: Serverless SQL Pools Expansion',summary:'Enterprise adoption surges as serverless SQL pools become the new analytics standard in the cloud.',url:'https://azure.microsoft.com/blog',date:'May 2025'},
  {category:'AI & ML',title:'Azure AI Foundry: New Model APIs for Predictive Analytics',summary:'AI-skilled BI analysts increasingly in demand as Azure expands its ML and predictive modeling capabilities.',url:'https://azure.microsoft.com/en-us/products/ai-foundry',date:'May 2025'},
  {category:'POWER BI',title:'Power BI May 2025 Feature Update',summary:'New DAX improvements, incremental refresh enhancements and composite model updates shipped this month.',url:'https://powerbi.microsoft.com/blog',date:'May 2025'},
  {category:'AI & ML',title:'AI-Driven Data Storytelling Trends 2025',summary:'BI professionals integrating LLMs with dashboards for automated narrative generation — the next frontier.',url:'https://www.gartner.com/en/analytics',date:'May 2025'},
];
const catColors={'POWER BI':'#5b4df5','FABRIC':'#7c3aed','CLOUD':'#3b82f6','AI & ML':'#10b981'};

function renderMarketInto(containerId,articles){
  const feed=document.getElementById(containerId);
  if(!articles||!articles.length){feed.innerHTML='<p style="color:var(--muted);text-align:center;padding:2rem;">No updates found. Try refreshing.</p>';return;}
  const grid=document.createElement('div');grid.className='market-grid';
  articles.forEach(a=>{
    const color=catColors[a.category]||'var(--primary)';
    const card=document.createElement('a');card.className='market-card';card.href=a.url||'#';card.target='_blank';card.rel='noopener noreferrer';
    card.innerHTML=`<div class="market-tag" style="color:${color}">● ${a.category}</div><div class="market-title">${a.title}</div><div class="market-desc">${a.summary}</div><div class="market-date">📅 ${a.date||'Latest'}</div>`;
    grid.appendChild(card);
  });
  feed.innerHTML='';feed.appendChild(grid);
}

async function loadMarketData(force){
  const today=new Date().toDateString(),cacheKey='mkt_'+today;
  if(!force){const c=sessionStorage.getItem(cacheKey);if(c)return JSON.parse(c);}
  try{
    const res=await fetch('https://api.anthropic.com/v1/messages',{method:'POST',headers:{'Content-Type':'application/json','anthropic-version':'2023-06-01','anthropic-dangerous-direct-browser-access':'true'},body:JSON.stringify({model:'claude-sonnet-4-20250514',max_tokens:1200,tools:[{type:'web_search_20250305',name:'web_search'}],system:'Return ONLY a valid JSON array, no markdown, no preamble.',messages:[{role:'user',content:'Search for 6 latest news articles this week about Power BI updates, Microsoft Fabric, Azure cloud, AI/ML for data analytics. Return ONLY JSON array: [{"category":"POWER BI","title":"...","summary":"...","url":"https://...","date":"..."},...] Categories must be one of: POWER BI, FABRIC, CLOUD, AI & ML'}]})});
    if(!res.ok)throw new Error('api');
    const data=await res.json();
    const text=data.content.map(b=>b.type==='text'?b.text:'').join('');
    const match=text.match(/\[[\s\S]*\]/);
    const articles=JSON.parse(match?match[0]:text);
    sessionStorage.setItem(cacheKey,JSON.stringify(articles));
    return articles;
  }catch{return FALLBACK_ARTICLES;}
}

async function loadHomeMarket(force=false){
  if(!force&&homeMarketLoaded)return;homeMarketLoaded=true;
  document.getElementById('homeMarketFeed').innerHTML='<div class="market-loading"><div class="market-spinner"></div>Fetching latest updates...</div>';
  const articles=await loadMarketData(force);renderMarketInto('homeMarketFeed',articles);
}

async function loadMarket(force=false){
  marketLoaded=true;
  document.getElementById('marketFeed').innerHTML='<div class="market-loading"><div class="market-spinner"></div>Fetching latest updates...</div>';
  const articles=await loadMarketData(force);renderMarketInto('marketFeed',articles);
  const feed=document.getElementById('marketFeed');
  const rb=document.createElement('button');
  rb.style.cssText='display:block;margin:1.5rem auto 0;background:rgba(91,77,245,.07);border:1.5px solid rgba(91,77,245,.2);color:var(--primary);padding:.45rem 1.2rem;border-radius:8px;font-family:Plus Jakarta Sans,sans-serif;font-size:.71rem;font-weight:700;cursor:pointer;';
  rb.textContent='🔄 Refresh Updates';rb.onclick=()=>{marketLoaded=false;loadMarket(true);};
  feed.appendChild(rb);
}

window.addEventListener('load',()=>{
  initRadarChart();
  loadHomeMarket();
  refreshThought();
});
</script>
</body>
</html>
