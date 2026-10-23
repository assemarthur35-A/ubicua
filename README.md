# ubicua
trabalho da semana ubiqua da Universidade da amazônia (UNAMA)


<!doctype html><html><head><meta charset=utf8><meta name=viewport content="width=device-width,initial-scale=1,viewport-fit=cover"><style>:root{color-scheme:light;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}html{scroll-padding-top:env(safe-area-inset-top,0px)}body{margin:0;padding:0;font:14px -apple-system,BlinkMacSystemFont,sans-serif;background:#fff;color:#000}img{max-width:100%}[hidden]:not([hidden=until-found i]){display:none!important}</style></head><body>
<title>Saúde Agora</title>
<meta name="claude:viewport-fit-sides" content="cover">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,500..800&family=IBM+Plex+Mono:wght@400;500;600&family=Source+Sans+3:wght@400;600;700&display=swap">
<style>
/* Layout: cabeçalho fixo; lista de unidades ordenada por demanda; detalhe da unidade escolhida; médicos e agendamento dessa unidade; consultas do paciente; painel da equipe; assistente flutuante. */
:root{
  --bg:#F2F6F6; --surface:#FFFFFF; --surface-2:#E7EFF0; --ink:#0F2A2E; --muted:#4D6468; --line:#D3E0E1;
  --accent:#0A6C74; --accent-ink:#FFFFFF; --accent-soft:#D6EBEC;
  --ok:#1B7F46; --ok-bg:#DDF1E4; --warn:#8F5A00; --warn-bg:#FBEBC8; --hi:#B3440E; --hi-bg:#FBDDCB;
  --crit:#B3261E; --crit-bg:#F9D8D5; --off:#566A6D; --off-bg:#E4EAEB; --info:#1F5FA8; --info-bg:#D9E7F7;
  --f-display:'Bricolage Grotesque','Trebuchet MS',sans-serif;
  --f-body:'Source Sans 3','Segoe UI',system-ui,sans-serif;
  --f-mono:'IBM Plex Mono',ui-monospace,Menlo,monospace;
}
@media (prefers-color-scheme: dark){:root:not([data-theme="light"]){
  --bg:#0B1A1D; --surface:#112428; --surface-2:#173035; --ink:#E4F0F1; --muted:#98B1B5; --line:#26434A;
  --accent:#4CC2C9; --accent-ink:#06282B; --accent-soft:#16373B;
  --ok:#5BD08A; --ok-bg:#12321F; --warn:#F0B84A; --warn-bg:#3A2D0E; --hi:#F29A68; --hi-bg:#3E2412;
  --crit:#FF8D84; --crit-bg:#431B18; --off:#9DB0B3; --off-bg:#1E3236; --info:#7FB5F0; --info-bg:#142C47;
  color-scheme:dark}}
:root[data-theme="dark"]{
  --bg:#0B1A1D; --surface:#112428; --surface-2:#173035; --ink:#E4F0F1; --muted:#98B1B5; --line:#26434A;
  --accent:#4CC2C9; --accent-ink:#06282B; --accent-soft:#16373B;
  --ok:#5BD08A; --ok-bg:#12321F; --warn:#F0B84A; --warn-bg:#3A2D0E; --hi:#F29A68; --hi-bg:#3E2412;
  --crit:#FF8D84; --crit-bg:#431B18; --off:#9DB0B3; --off-bg:#1E3236; --info:#7FB5F0; --info-bg:#142C47;
  color-scheme:dark}

*{box-sizing:border-box}
html{scroll-behavior:smooth}
@media (prefers-reduced-motion:reduce){html{scroll-behavior:auto}*{transition:none!important;animation:none!important}}
body{margin:0;background:var(--bg);color:var(--ink);font:400 1rem/1.55 var(--f-body);-webkit-text-size-adjust:100%}
body::before{content:"";position:fixed;inset:0 0 auto;height:env(safe-area-inset-top,0px);background:var(--surface);z-index:30}
.wrap{max-width:1120px;margin-inline:auto;padding-left:max(16px,env(safe-area-inset-left,0px));padding-right:max(16px,env(safe-area-inset-right,0px))}
a{color:var(--accent)}
:focus-visible{outline:2px solid var(--accent);outline-offset:2px}
h1,h2,h3{text-wrap:balance}
.mono{font-family:var(--f-mono);font-variant-numeric:tabular-nums}

/* cabeçalho */
.top{position:sticky;top:env(safe-area-inset-top,0px);z-index:20;background:var(--surface);border-bottom:1px solid var(--line)}
.bar{display:flex;flex-wrap:wrap;align-items:center;justify-content:space-between;gap:6px 24px;padding-block:10px}
.brand{display:flex;align-items:center;gap:10px;text-decoration:none;color:var(--ink)}
.brand strong{font:700 1.2rem/1.1 var(--f-display);display:block;letter-spacing:-.01em}
.brand small{font:500 .7rem var(--f-mono);color:var(--muted);letter-spacing:.02em}
nav{display:flex;gap:2px;overflow-x:auto;max-width:100%;min-width:0}
nav a{padding:8px 12px;border-radius:6px;color:var(--muted);text-decoration:none;font-weight:600;font-size:.94rem;white-space:nowrap;display:inline-flex;gap:6px;align-items:center}
nav a:hover{background:var(--surface-2);color:var(--ink)}
.count{background:var(--accent);color:var(--accent-ink);border-radius:99px;font:600 .72rem var(--f-mono);padding:1px 7px}

section{padding-block:56px 0;scroll-margin-top:104px}
#hospitais{padding-top:34px}
.eyebrow{font:500 .75rem var(--f-mono);letter-spacing:.08em;text-transform:uppercase;color:var(--muted);margin:0}
h1{font:700 clamp(2rem,5vw,3.2rem)/1.05 var(--f-display);letter-spacing:-.025em;margin:10px 0 14px;max-width:20ch}
h2{font:700 clamp(1.5rem,3vw,1.9rem)/1.15 var(--f-display);letter-spacing:-.015em;margin:6px 0 6px}
h3{font:700 1.05rem/1.25 var(--f-display);margin:0}
.big{font:700 clamp(1.8rem,4.2vw,2.7rem)/1.06 var(--f-display);letter-spacing:-.02em;margin:10px 0 12px}
.lead{color:var(--muted);max-width:62ch;margin:0}
.lvl.ok{color:var(--ok)}.lvl.warn{color:var(--warn)}.lvl.hi{color:var(--hi)}.lvl.crit{color:var(--crit)}
.where{font-size:.95rem;color:var(--muted);margin:10px 0 0}
.where strong{color:var(--ink)}

/* lista de unidades */
.sumrow{display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:12px;margin:22px 0 14px}
.sum{background:var(--surface);border:1px solid var(--line);border-radius:10px;padding:14px 16px;min-width:0}
.sum small{display:block;font:500 .72rem var(--f-mono);letter-spacing:.06em;text-transform:uppercase;color:var(--muted)}
.sum strong{display:block;font:700 1.1rem/1.25 var(--f-display);margin-top:4px;overflow-wrap:anywhere}
.sum span{font-size:.9rem;color:var(--muted)}
.hlist{display:grid;gap:10px}
.hosp{display:grid;grid-template-columns:minmax(0,2.2fr) minmax(0,1.4fr) minmax(0,.8fr) auto;gap:10px 20px;align-items:center;background:var(--surface);border:1px solid var(--line);border-radius:10px;padding:14px 18px}
.hosp.sel{box-shadow:0 0 0 2px var(--accent)}
.hosp h3{margin:0 0 4px}
.h-meta{margin:0;font-size:.9rem;color:var(--muted);display:flex;flex-wrap:wrap;gap:6px 8px;align-items:center}
.tag{font:600 .72rem var(--f-body);padding:3px 8px;border-radius:4px;background:var(--accent-soft);color:var(--accent)}
.tag.priv{background:var(--surface-2);color:var(--muted)}
.h-lvl{display:grid;gap:8px;justify-items:start;min-width:0}
.h-lvl .row{display:flex;align-items:center;gap:8px;width:100%}
.h-wait b{font:700 1.5rem/1 var(--f-display);font-variant-numeric:tabular-nums}
.h-wait small{display:block;color:var(--muted);font-size:.8rem}
.best{font:600 .75rem var(--f-body);color:var(--ok)}

/* painel de demanda */
.dhead{display:flex;flex-wrap:wrap;gap:16px 32px;justify-content:space-between;align-items:end;margin-bottom:22px}
.dsel{flex:0 1 340px;min-width:min(100%,240px)}
.hero{display:grid;grid-template-columns:minmax(0,1.55fr) minmax(0,1fr);gap:28px;align-items:start}
.panel{background:var(--surface);border:1px solid var(--line);border-radius:10px;padding:20px;min-width:0}
.meter{position:relative;padding-top:30px;margin-top:24px}
.segs{display:flex;height:14px;border-radius:4px;overflow:hidden}
.segs i{display:block;opacity:.3;border-right:2px solid var(--surface)}
.segs i:last-child{border-right:0}
.segs i.on{opacity:1}
.segs .s-ok{background:var(--ok);flex:0 0 50%}.segs .s-warn{background:var(--warn);flex:0 0 25%}
.segs .s-hi{background:var(--hi);flex:0 0 15%}.segs .s-crit{background:var(--crit);flex:0 0 10%}
.mk{position:absolute;top:0;transform:translateX(-50%);display:flex;flex-direction:column;align-items:center;transition:left .4s ease}
.mk b{font:600 .8rem/1 var(--f-mono);background:var(--ink);color:var(--bg);padding:5px 8px;border-radius:4px}
.mk::after{content:"";width:2px;height:22px;background:var(--ink)}
.axis{position:relative;height:20px;margin-top:6px;font:400 .72rem var(--f-mono);color:var(--muted)}
.axis span{position:absolute;transform:translateX(-50%)}
.axis span:first-child{transform:none}.axis span:last-child{transform:translateX(-100%)}
.legend{display:flex;flex-wrap:wrap;gap:4px 16px;margin:14px 0 0;padding:0;list-style:none;font-size:.85rem;color:var(--muted)}
.legend li{display:flex;align-items:center;gap:6px}
.legend i{width:10px;height:10px;border-radius:2px;display:block}
.stats{display:grid;grid-template-columns:1fr 1fr;gap:18px 16px;margin:0}
.stats div{min-width:0}
.stats dt{font-size:.82rem;color:var(--muted)}
.stats dd{margin:2px 0 0;font:700 2rem/1.1 var(--f-display);font-variant-numeric:tabular-nums}
.stats dd small{font:500 .85rem var(--f-body);color:var(--muted)}
.panel .note{font-size:.85rem;color:var(--muted);margin:16px 0 0;border-top:1px solid var(--line);padding-top:12px}

.sub{margin-top:36px}
.sub h2{font-size:1.25rem}
.tbl{overflow-x:auto;margin-top:10px}
table{width:100%;border-collapse:collapse;min-width:520px}
th{font:500 .72rem var(--f-mono);letter-spacing:.06em;text-transform:uppercase;color:var(--muted);text-align:left;padding:8px 12px 8px 0;border-bottom:1px solid var(--ink)}
td{padding:12px 12px 12px 0;border-bottom:1px solid var(--line);font-variant-numeric:tabular-nums;vertical-align:middle}
td:first-child{font-weight:600}
.occ{display:flex;align-items:center;gap:10px}
.occ .num{width:3ch;text-align:right;font-family:var(--f-mono);font-size:.9rem}
.track{display:block;height:8px;background:var(--surface-2);border-radius:4px;overflow:hidden;width:120px;max-width:100%}
.track i{display:block;height:100%;border-radius:4px}
.track i.ok{background:var(--ok)}.track i.warn{background:var(--warn)}.track i.hi{background:var(--hi)}.track i.crit{background:var(--crit)}

.pill{display:inline-flex;align-items:center;gap:6px;font:600 .78rem/1 var(--f-body);padding:5px 10px;border-radius:99px;white-space:nowrap}
.pill::before{content:"";width:7px;height:7px;border-radius:50%;background:currentColor;flex:none}
.pill.ok{background:var(--ok-bg);color:var(--ok)}.pill.warn{background:var(--warn-bg);color:var(--warn)}
.pill.hi{background:var(--hi-bg);color:var(--hi)}.pill.crit{background:var(--crit-bg);color:var(--crit)}
.pill.info{background:var(--info-bg);color:var(--info)}.pill.off{background:var(--off-bg);color:var(--off)}

.tri{display:grid;grid-template-columns:repeat(auto-fit,minmax(180px,1fr));gap:10px 18px;margin:10px 0 0;padding:0;list-style:none}
.tri li{display:flex;gap:10px;align-items:flex-start;font-size:.9rem;min-width:0}
.tri i{width:12px;height:12px;border-radius:50%;margin-top:5px;flex:none}
.tri strong{display:block}.tri span{color:var(--muted)}
.tri-note{font-size:.88rem;color:var(--muted);margin:12px 0 0;max-width:70ch}

/* controles */
.btn{font:600 .95rem var(--f-body);min-height:44px;padding:10px 16px;border-radius:6px;border:1px solid var(--accent);background:var(--accent);color:var(--accent-ink);cursor:pointer}
.btn:hover{filter:brightness(1.07)}
.btn:disabled{opacity:.5;cursor:not-allowed;filter:none}
.btn.ghost{background:transparent;color:var(--accent)}
.btn.ghost:hover{background:var(--accent-soft);filter:none}
.btn.danger{background:var(--crit);border-color:var(--crit);color:var(--bg)}
.btn.small{min-height:36px;padding:6px 12px;font-size:.88rem}
input[type=text],input[type=tel],input[type=date],select{font:inherit;width:100%;min-height:44px;padding:9px 12px;border:1px solid var(--line);border-radius:6px;background:var(--surface);color:var(--ink)}
input:disabled,select:disabled{opacity:.55;cursor:not-allowed}
input[type=text]::placeholder,input[type=tel]::placeholder{color:var(--muted);opacity:.8}
label.f{display:block;font-weight:600;font-size:.9rem;margin-bottom:6px}
fieldset{border:0;padding:0;margin:0;min-width:0}
legend{font-weight:600;font-size:.9rem;padding:0;margin-bottom:6px}

.filters{display:flex;flex-wrap:wrap;gap:12px;align-items:end;margin:22px 0 18px}
.filters .fld{flex:1 1 200px;min-width:0}
.seg{display:inline-flex;border:1px solid var(--line);border-radius:6px;overflow:hidden;background:var(--surface);flex-wrap:wrap}
.seg button{font:600 .9rem var(--f-body);min-height:44px;padding:8px 14px;border:0;background:transparent;color:var(--muted);cursor:pointer}
.seg button+button{border-left:1px solid var(--line)}
.seg button[aria-pressed=true]{background:var(--accent);color:var(--accent-ink)}
.meta{font:500 .8rem var(--f-mono);color:var(--muted);margin:0 0 10px}

/* médicos */
.docs{display:grid;grid-template-columns:repeat(auto-fill,minmax(min(100%,290px),1fr));gap:16px}
.doc{background:var(--surface);border:1px solid var(--line);border-radius:10px;padding:18px;display:flex;flex-direction:column;gap:12px;min-width:0}
.doc header{display:flex;gap:12px;align-items:center}
.av{width:44px;height:44px;border-radius:50%;background:var(--accent-soft);color:var(--accent);display:grid;place-items:center;font:700 .95rem var(--f-display);flex:none}
.doc .esp{margin:2px 0 0;color:var(--muted);font-size:.9rem}
.abs{background:var(--crit-bg);border-radius:6px;padding:10px 12px;font-size:.9rem}
.abs strong{color:var(--crit)}
.abs p{margin:0}.abs p+p{margin-top:6px}
.soon{font-size:.85rem;color:var(--warn);margin:0}
dl.kv{margin:0;display:grid;grid-template-columns:auto minmax(0,1fr);gap:4px 12px;font-size:.9rem}
dl.kv dt{color:var(--muted)}dl.kv dd{margin:0;font-variant-numeric:tabular-nums}
.doc .btn{margin-top:auto}
.empty{color:var(--muted);padding:24px 0}

/* agendamento */
.book{display:grid;grid-template-columns:minmax(0,1.5fr) minmax(0,1fr);gap:24px;margin-top:22px;align-items:start}
.form{display:grid;gap:18px}
.row2{display:grid;grid-template-columns:1fr 1fr;gap:14px}
.slots{display:flex;flex-wrap:wrap;gap:8px}
.slot{position:relative}
.slot input{position:absolute;opacity:0;inset:0;width:100%;height:100%;margin:0;cursor:pointer}
.slot label{display:block;min-width:68px;text-align:center;padding:9px 12px;border:1px solid var(--line);border-radius:6px;background:var(--surface);font:500 .92rem var(--f-mono);font-variant-numeric:tabular-nums}
.slot input:checked+label{background:var(--accent);border-color:var(--accent);color:var(--accent-ink)}
.slot input:focus-visible+label{outline:2px solid var(--accent);outline-offset:2px}
.slot input:disabled{cursor:not-allowed}
.slot input:disabled+label{color:var(--muted);text-decoration:line-through;background:var(--surface-2);opacity:.7}
.hint{color:var(--muted);margin:0;font-size:.92rem}
.notice{border-radius:6px;padding:12px 14px;font-size:.92rem;background:var(--warn-bg);display:grid;gap:10px;width:100%}
.notice.crit{background:var(--crit-bg)}
.notice p{margin:0}
.notice .acts{display:flex;flex-wrap:wrap;gap:8px}
.err{background:var(--crit-bg);border-radius:6px;padding:10px 14px;font-size:.92rem}
.err ul{margin:0;padding-left:18px}
.summary h3{margin-bottom:12px}
.summary dl.kv{grid-template-columns:auto minmax(0,1fr);gap:8px 14px}
.summary dd{font-weight:600}
.summary dd.dim{color:var(--muted);font-weight:400}
.done{background:var(--ok-bg);border-radius:10px;padding:16px 18px;margin-top:16px}
.done h3{color:var(--ok);margin-bottom:6px}
.done p{margin:4px 0}

/* consultas */
.appts{display:grid;gap:12px;margin-top:20px}
.appt{display:grid;grid-template-columns:auto minmax(0,1fr) auto;gap:18px;align-items:center;background:var(--surface);border:1px solid var(--line);border-radius:10px;padding:16px 18px}
.appt .when{font:700 1.5rem/1 var(--f-display);text-align:center;min-width:72px}
.appt .when small{display:block;font:500 .72rem var(--f-mono);color:var(--muted);text-transform:uppercase;letter-spacing:.06em;margin-top:6px}
.appt p{margin:0;font-size:.92rem;color:var(--muted)}
.appt h3{margin-bottom:2px}

/* equipe */
.team{display:grid;grid-template-columns:minmax(0,1fr) minmax(0,1fr);gap:24px;margin-top:22px;align-items:start}
.ctl{display:grid;gap:18px}
.ctl .head{display:flex;justify-content:space-between;gap:12px;font-weight:600;font-size:.92rem}
.ctl output{font-family:var(--f-mono);font-variant-numeric:tabular-nums}
.ctl input[type=range]{width:100%;accent-color:var(--accent);margin:6px 0 0}
.chips{display:flex;flex-wrap:wrap;gap:8px;margin-top:10px}
.chip{display:inline-flex;align-items:center;gap:6px;background:var(--crit-bg);border-radius:99px;padding:4px 6px 4px 12px;font-size:.85rem}
.chip button{border:0;background:transparent;color:var(--ink);font-size:1.1rem;line-height:1;cursor:pointer;width:28px;height:28px;border-radius:50%}
.chip button:hover{background:var(--surface)}
.calc{font-size:.92rem}
.calc p{margin:0 0 10px}
.calc code{font:500 .85rem var(--f-mono);background:var(--surface-2);padding:2px 6px;border-radius:4px}
.calc table{min-width:0;margin-top:8px}
.calc td,.calc th{padding-right:8px}
.live{font:500 .85rem var(--f-mono);background:var(--surface-2);border-radius:6px;padding:10px 12px;margin-top:12px;font-variant-numeric:tabular-nums}

footer{margin-top:72px;border-top:1px solid var(--line);background:var(--surface)}
footer .wrap{padding-block:24px;display:flex;flex-wrap:wrap;gap:8px 32px;justify-content:space-between;font-size:.88rem;color:var(--muted)}
footer p{margin:0;max-width:60ch}
footer strong{color:var(--ink)}

/* tamanho da letra */
html[data-size="grande"]{font-size:118%}
html[data-size="enorme"]{font-size:138%}
.sizer{display:flex;align-items:center;gap:4px;font-size:.85rem;color:var(--muted)}
.sizer span{margin-right:4px}
.sizer button{min-width:40px;min-height:40px;border:1px solid var(--line);border-radius:6px;background:var(--surface);color:var(--ink);font:700 1rem var(--f-body);cursor:pointer;line-height:1}
.sizer button[aria-pressed=true]{background:var(--accent);border-color:var(--accent);color:var(--accent-ink)}

/* assistente de ajuda */
.sr{position:absolute;width:1px;height:1px;overflow:hidden;clip:rect(0 0 0 0);white-space:nowrap}
.help-fab{position:fixed;z-index:40;right:calc(16px + env(safe-area-inset-right,0px));bottom:calc(16px + env(safe-area-inset-bottom,0px));display:inline-flex;align-items:center;gap:10px;min-height:58px;padding:12px 22px;border-radius:99px;border:0;background:var(--accent);color:var(--accent-ink);font:700 1.05rem var(--f-body);cursor:pointer;box-shadow:0 6px 22px rgba(0,0,0,.28)}
.help-fab:hover{filter:brightness(1.08)}
.help{position:fixed;z-index:50;right:calc(16px + env(safe-area-inset-right,0px));bottom:calc(16px + env(safe-area-inset-bottom,0px));width:min(460px,calc(100vw - 32px));height:min(700px,calc(100% - 32px - env(safe-area-inset-bottom,0px) - env(safe-area-inset-top,0px)));display:flex;flex-direction:column;background:var(--surface);color:var(--ink);border:1px solid var(--line);border-radius:14px;box-shadow:0 14px 44px rgba(0,0,0,.32);overflow:hidden}
.help-h{display:flex;flex-wrap:wrap;justify-content:space-between;align-items:flex-start;gap:10px;padding:14px 16px;background:var(--accent);color:var(--accent-ink)}
.help-h h2{font:700 1.2rem/1.2 var(--f-display);margin:0;color:inherit}
.help-h h2:focus{outline:none}
.help-h p{margin:2px 0 0;font-size:.92rem;opacity:.92}
.help-hb{display:flex;gap:8px;flex-wrap:wrap}
.help-hb button{min-height:40px;border:1px solid currentColor;background:transparent;color:inherit;border-radius:6px;padding:6px 12px;font:600 .9rem var(--f-body);cursor:pointer}
.help-hb button:hover{background:rgba(255,255,255,.14)}
.help-log{flex:1;min-height:0;overflow-y:auto;padding:16px;display:flex;flex-direction:column;gap:12px}
.msg{max-width:94%;padding:12px 14px;border-radius:12px;font-size:1.08rem;line-height:1.5}
.msg p{margin:0;white-space:pre-wrap}
.msg.bot{background:var(--surface-2);align-self:flex-start;border-bottom-left-radius:4px}
.msg.me{background:var(--accent-soft);align-self:flex-end;border-bottom-right-radius:4px}
.msg .who{display:block;font:600 .72rem var(--f-mono);letter-spacing:.05em;text-transform:uppercase;color:var(--muted);margin-bottom:4px}
.msg.think p{color:var(--muted)}
.macts{display:flex;flex-wrap:wrap;gap:8px;margin-top:10px}
.macts:empty{display:none}
.help-chips{display:flex;flex-wrap:wrap;gap:8px;padding:0 16px 12px;max-height:34%;overflow-y:auto}
.qchip{min-height:44px;padding:8px 14px;border-radius:99px;border:1px solid var(--accent);background:transparent;color:var(--accent);font:600 .95rem var(--f-body);cursor:pointer;text-align:left}
.qchip:hover:not(:disabled){background:var(--accent-soft)}
.qchip:disabled{opacity:.5;cursor:not-allowed}
.help-opt{display:flex;align-items:center;gap:10px;padding:0 16px 10px;font-size:.92rem;color:var(--muted)}
.help-opt input{width:22px;height:22px;accent-color:var(--accent);margin:0}
.help-f{display:flex;gap:8px;padding:12px 16px;border-top:1px solid var(--line)}
.help-f input{flex:1;min-width:0;width:auto;font-size:1.05rem}
.help-note{font-size:.8rem;color:var(--muted);margin:0;padding:0 16px 12px}

@media (max-width:860px){
  .hero,.book,.team{grid-template-columns:minmax(0,1fr)}
  .hosp{grid-template-columns:minmax(0,1fr) minmax(0,1fr)}
  .hosp .h-main,.hosp .h-act{grid-column:1 / -1}
  .sumrow{grid-template-columns:minmax(0,1fr)}
}
@media (max-width:560px){
  .row2{grid-template-columns:minmax(0,1fr)}
  .appt{grid-template-columns:auto minmax(0,1fr)}
  .appt .acts{grid-column:1 / -1}
  .stats dd{font-size:1.7rem}
  section{padding-top:44px}
  .help{width:calc(100vw - 16px);right:calc(8px + env(safe-area-inset-right,0px));bottom:calc(8px + env(safe-area-inset-bottom,0px))}
}
</style>

<header class="top">
  <div class="wrap bar">
    <a class="brand" href="#hospitais" aria-label="Saúde Agora, início">
      <svg width="30" height="30" viewBox="0 0 30 30" aria-hidden="true"><rect width="30" height="30" rx="7" fill="var(--accent)"/><path d="M12.5 6h5v6.5H24v5h-6.5V24h-5v-6.5H6v-5h6.5z" fill="var(--accent-ink)"/></svg>
      <span><strong>Saúde Agora</strong><small>Rede de hospitais · dados fictícios</small></span>
    </a>
    <nav aria-label="Seções do site">
      <a href="#hospitais">Unidades</a>
      <a href="#medicos">Médicos</a>
      <a href="#agendar">Agendar</a>
      <a href="#consultas">Minhas consultas <span class="count" id="navCount" hidden>0</span></a>
      <a href="#equipe">Equipe</a>
    </nav>
    <div class="sizer" role="group" aria-label="Tamanho da letra">
      <span>Letra</span>
      <button type="button" data-size="normal" aria-pressed="true" aria-label="Letra normal" style="font-size:.9rem">A</button>
      <button type="button" data-size="grande" aria-pressed="false" aria-label="Letra grande" style="font-size:1.15rem">A</button>
      <button type="button" data-size="enorme" aria-pressed="false" aria-label="Letra muito grande" style="font-size:1.4rem">A</button>
    </div>
  </div>
</header>

<main>
<section id="hospitais">
  <div class="wrap">
    <p class="eyebrow">Hospitais e UPAs · atualizado às <span id="upd">--:--</span></p>
    <h1>Veja qual unidade está menos cheia</h1>
    <p class="lead">A situação dos hospitais públicos e particulares, a ausência de médicos e o agendamento de consultas em um só lugar. Em emergência, ligue 192 (SAMU).</p>

    <div class="filters">
      <div class="seg" role="group" aria-label="Filtrar por tipo" id="hType">
        <button type="button" data-t="todos" aria-pressed="true">Todas</button>
        <button type="button" data-t="publico" aria-pressed="false">Públicas</button>
        <button type="button" data-t="particular" aria-pressed="false">Particulares</button>
      </div>
      <div class="fld"><label class="f" for="hCat">Tipo de unidade</label><select id="hCat"></select></div>
    </div>

    <div class="sumrow" id="sumrow" aria-live="polite"></div>
    <div class="hlist" id="hlist"></div>
  </div>
</section>

<section id="demanda">
  <div class="wrap">
    <div class="dhead">
      <div>
        <p class="eyebrow">Unidade selecionada</p>
        <h2 id="dName">—</h2>
        <p class="lead" id="dMeta"></p>
      </div>
      <div class="dsel"><label class="f" for="hospSel">Trocar de unidade</label><select id="hospSel"></select></div>
    </div>
    <div class="hero">
      <div>
        <h3 class="big" id="h1">Demanda <span class="lvl" id="lvlWord">alta</span> agora</h3>
        <p class="lead" id="lvlAdvice" aria-live="polite"></p>
        <div class="panel" style="margin-top:24px">
          <p class="eyebrow">Nível de demanda · pontuação de 0 a 100</p>
          <div class="meter" role="img" id="meterImg" aria-label="">
            <div class="segs"><i class="s-ok"></i><i class="s-warn"></i><i class="s-hi"></i><i class="s-crit"></i></div>
            <div class="mk" id="mk" style="left:0%"><b id="mkVal">0</b></div>
            <div class="axis" aria-hidden="true"><span style="left:0%">0</span><span style="left:50%">50</span><span style="left:75%">75</span><span style="left:90%">90</span><span style="left:100%">100</span></div>
          </div>
          <ul class="legend">
            <li><i style="background:var(--ok)"></i>Baixa</li>
            <li><i style="background:var(--warn)"></i>Moderada</li>
            <li><i style="background:var(--hi)"></i>Alta</li>
            <li><i style="background:var(--crit)"></i>Crítica</li>
          </ul>
        </div>
      </div>
      <aside class="panel" aria-label="Números do pronto-atendimento">
        <dl class="stats">
          <div><dt>Espera estimada</dt><dd><span id="stWait">0</span> <small>min</small></dd></div>
          <div><dt>Pacientes aguardando</dt><dd id="stFila">0</dd></div>
          <div><dt>Médicos de plantão</dt><dd id="stPlant">0</dd></div>
          <div><dt>Leitos ocupados</dt><dd><span id="stLeitos">0</span><small> de <span id="stTotal">80</span></small></dd></div>
        </dl>
        <p class="note">A espera estimada vale para pacientes classificados como pouco urgentes. Casos graves passam na frente.</p>
      </aside>
    </div>

    <div class="sub">
      <h2>Situação por setor</h2>
      <div class="tbl">
        <table>
          <thead><tr><th scope="col">Setor</th><th scope="col">Ocupação</th><th scope="col">Espera</th><th scope="col">Situação</th></tr></thead>
          <tbody id="sectors"></tbody>
        </table>
      </div>
    </div>

    <div class="sub">
      <h2>Quem é atendido primeiro</h2>
      <ul class="tri">
        <li><i style="background:#D32F2F"></i><div><strong>Vermelho · emergência</strong><span>atendimento imediato</span></div></li>
        <li><i style="background:#F57C00"></i><div><strong>Laranja · muito urgente</strong><span>até 10 min</span></div></li>
        <li><i style="background:#FBC02D"></i><div><strong>Amarelo · urgente</strong><span>até 60 min</span></div></li>
        <li><i style="background:#388E3C"></i><div><strong>Verde · pouco urgente</strong><span>até 120 min</span></div></li>
        <li><i style="background:#1976D2"></i><div><strong>Azul · não urgente</strong><span>até 240 min</span></div></li>
      </ul>
      <p class="tri-note">A triagem segue o Protocolo de Manchester. O atendimento não é por ordem de chegada. Com a demanda alta, os casos verdes e azuis esperam mais. Em risco de vida, ligue 192 (SAMU).</p>
    </div>
  </div>
</section>

<section id="medicos">
  <div class="wrap">
    <p class="eyebrow">Corpo clínico</p>
    <h2>Médicos e disponibilidade</h2>
    <p class="lead">Veja quem está atendendo hoje, quem está ausente e quando é o próximo horário livre de cada médico.</p>
    <p class="where">Unidade: <strong class="whereName">—</strong> · <a href="#hospitais">trocar de unidade</a></p>
    <div class="filters">
      <div class="fld"><label class="f" for="fQ">Buscar</label><input type="text" id="fQ" placeholder="Nome ou especialidade" autocomplete="off"></div>
      <div class="fld"><label class="f" for="fEsp">Especialidade</label><select id="fEsp"></select></div>
      <div class="seg" role="group" aria-label="Filtrar por situação" id="fStatus">
        <button type="button" data-f="todos" aria-pressed="true">Todos</button>
        <button type="button" data-f="hoje" aria-pressed="false">Atendem hoje</button>
        <button type="button" data-f="ausentes" aria-pressed="false">Ausentes</button>
      </div>
    </div>
    <p class="meta" id="docCount" aria-live="polite"></p>
    <div class="docs" id="docs"></div>
  </div>
</section>

<section id="agendar">
  <div class="wrap">
    <p class="eyebrow">Consultas ambulatoriais</p>
    <h2>Agendar consulta</h2>
    <p class="lead">Escolha o médico e a data. O site só mostra horários livres e avisa quando o médico estará ausente.</p>
    <p class="where">Unidade: <strong class="whereName">—</strong> · <a href="#hospitais">trocar de unidade</a></p>
    <div class="book">
      <form class="form panel" id="form" novalidate>
        <div class="row2">
          <div><label class="f" for="esp">Especialidade</label><select id="esp"></select></div>
          <div><label class="f" for="doc">Médico</label><select id="doc" disabled></select></div>
        </div>
        <div><label class="f" for="date">Data</label><input type="date" id="date"></div>
        <fieldset>
          <legend>Horário</legend>
          <div class="slots" id="slots" role="radiogroup" aria-label="Horários disponíveis"></div>
        </fieldset>
        <div class="row2">
          <div><label class="f" for="nome">Nome completo do paciente</label><input type="text" id="nome" autocomplete="name" placeholder="Ex.: Maria da Silva"></div>
          <div><label class="f" for="tel">Telefone com DDD</label><input type="tel" id="tel" inputmode="tel" autocomplete="tel" placeholder="(00) 90000-0000"></div>
        </div>
        <div>
          <label class="f" for="motivo">Tipo de consulta</label>
          <select id="motivo"><option>Primeira consulta</option><option>Retorno</option><option>Resultado de exames</option></select>
        </div>
        <div id="err" class="err" role="alert" hidden></div>
        <div><button class="btn" type="submit" id="submit">Confirmar consulta</button></div>
      </form>

      <div>
        <aside class="panel summary" aria-label="Resumo da consulta">
          <h3>Resumo</h3>
          <dl class="kv">
            <dt>Unidade</dt><dd id="sUni" class="dim">—</dd>
            <dt>Médico</dt><dd id="sMed" class="dim">—</dd>
            <dt>Especialidade</dt><dd id="sEsp" class="dim">—</dd>
            <dt>Data</dt><dd id="sData" class="dim">—</dd>
            <dt>Horário</dt><dd id="sHora" class="dim">—</dd>
            <dt>Duração</dt><dd id="sDur" class="dim">—</dd>
            <dt>Local</dt><dd id="sLocal" class="dim">—</dd>
          </dl>
        </aside>
        <div class="done" id="done" role="status" hidden></div>
      </div>
    </div>
  </div>
</section>

<section id="consultas">
  <div class="wrap">
    <p class="eyebrow">Neste aparelho</p>
    <h2>Minhas consultas</h2>
    <p class="lead">As consultas agendadas aparecem aqui. Para cancelar, libere o horário para outro paciente.</p>
    <div class="appts" id="appts"></div>
  </div>
</section>

<section id="equipe">
  <div class="wrap">
    <p class="eyebrow">Modo demonstração</p>
    <h2>Painel da equipe</h2>
    <p class="lead">Ajuste os números do plantão da unidade e veja o nível de demanda mudar na lista e no detalhe. Em um site real, cada hospital teria seu login, e esta área ficaria separada da página pública.</p>
    <p class="where">Unidade: <strong class="whereName">—</strong> · <a href="#hospitais">trocar de unidade</a></p>
    <div class="team">
      <div class="panel ctl">
        <div>
          <div class="head"><label for="fila">Pacientes aguardando atendimento</label><output id="filaV" for="fila"></output></div>
          <input type="range" id="fila" min="0" max="60" step="1">
        </div>
        <div>
          <div class="head"><label for="plant">Médicos de plantão no pronto-atendimento</label><output id="plantV" for="plant"></output></div>
          <input type="range" id="plant" min="1" max="10" step="1">
        </div>
        <div>
          <div class="head"><label for="leitos" id="leitosL">Leitos ocupados</label><output id="leitosV" for="leitos"></output></div>
          <input type="range" id="leitos" min="0" max="80" step="1">
        </div>
        <div>
          <label class="f" for="absDoc">Registrar médico ausente hoje</label>
          <div style="display:flex;gap:8px;flex-wrap:wrap">
            <select id="absDoc" style="flex:1 1 200px;width:auto"></select>
            <button class="btn ghost" type="button" id="absBtn">Marcar ausente</button>
          </div>
          <div class="chips" id="absList" aria-live="polite"></div>
        </div>
        <div><button class="btn ghost small" type="button" id="reset">Restaurar valores de exemplo</button></div>
      </div>

      <div class="panel calc">
        <h3>Como o nível de demanda é calculado</h3>
        <p style="margin-top:10px">Duas medidas contam metade da pontuação cada uma.</p>
        <p><code>ocupação = leitos ocupados ÷ leitos totais</code></p>
        <p><code>pressão da fila = aguardando ÷ (médicos × 5 por hora)</code>, limitada a 100%</p>
        <p><code>pontuação = 50% ocupação + 50% pressão da fila</code></p>
        <p><code>espera estimada = aguardando ÷ médicos × 12 min</code></p>
        <div class="tbl">
          <table>
            <thead><tr><th scope="col">Pontuação</th><th scope="col">Nível</th><th scope="col">Orientação ao paciente</th></tr></thead>
            <tbody>
              <tr><td class="mono">0–49</td><td><span class="pill ok">Baixa</span></td><td>Pode vir sem espera relevante.</td></tr>
              <tr><td class="mono">50–74</td><td><span class="pill warn">Moderada</span></td><td>Fluxo normal, com alguma espera.</td></tr>
              <tr><td class="mono">75–89</td><td><span class="pill hi">Alta</span></td><td>Casos leves: prefira agendar.</td></tr>
              <tr><td class="mono">90–100</td><td><span class="pill crit">Crítica</span></td><td>Venha só em caso de urgência.</td></tr>
            </tbody>
          </table>
        </div>
        <div class="live" id="live"></div>
        <p style="margin-top:14px">Em um sistema real, esses números chegam de cada hospital (triagem, ocupação de leitos e escala médica) por uma API, e o Saúde Agora reúne tudo em uma tela. Aqui a equipe digita os valores à mão para demonstrar a lógica.</p>
      </div>
    </div>
  </div>
</section>
</main>

<footer>
  <div class="wrap">
    <p><strong>Saúde Agora</strong> é um projeto de demonstração. Os hospitais, médicos, horários e números deste site são fictícios.</p>
    <p><strong>Emergência:</strong> ligue 192 (SAMU) ou vá à unidade mais próxima. Não use o agendamento para casos urgentes.</p>
  </div>
</footer>

<button type="button" class="help-fab" id="helpOpen" aria-haspopup="dialog" aria-controls="helpPanel" aria-expanded="false">
  <svg width="24" height="24" viewBox="0 0 24 24" aria-hidden="true"><path d="M4 4h16a2 2 0 0 1 2 2v9a2 2 0 0 1-2 2h-8l-5 4v-4H4a2 2 0 0 1-2-2V6a2 2 0 0 1 2-2z" fill="currentColor"/><circle cx="8" cy="10.5" r="1.4" fill="var(--accent)"/><circle cx="12" cy="10.5" r="1.4" fill="var(--accent)"/><circle cx="16" cy="10.5" r="1.4" fill="var(--accent)"/></svg>
  <span>Preciso de ajuda</span>
</button>

<div class="help" id="helpPanel" role="dialog" aria-labelledby="helpTitle" hidden>
  <div class="help-h">
    <div>
      <h2 id="helpTitle" tabindex="-1">Assistente Saúde Agora</h2>
      <p>Eu ajudo você a usar o site.</p>
    </div>
    <div class="help-hb">
      <button type="button" id="helpSize">Letra maior</button>
      <button type="button" id="helpClose">Fechar</button>
    </div>
  </div>
  <div class="help-log" id="helpLog" role="log" aria-live="polite" aria-label="Conversa com o assistente"></div>
  <div class="help-chips" id="helpChips" aria-label="Perguntas prontas"></div>
  <label class="help-opt" id="helpAutoRow" for="helpAuto"><input type="checkbox" id="helpAuto"> Ler as respostas em voz alta</label>
  <form class="help-f" id="helpForm" novalidate>
    <label class="sr" for="helpIn">Escreva sua pergunta</label>
    <input type="text" id="helpIn" placeholder="Escreva sua pergunta aqui" autocomplete="off">
    <button class="btn" type="submit" id="helpSend">Enviar</button>
  </form>
  <p class="help-note">Eu sou uma inteligência artificial e posso errar. Não substituo o médico. Em emergência, ligue 192.</p>
</div>

<script>
(function(){
'use strict';

var DOW=['dom','seg','ter','qua','qui','sex','sáb'];
var DOW_LONG=['domingo','segunda-feira','terça-feira','quarta-feira','quinta-feira','sexta-feira','sábado'];
function $(s,r){return (r||document).querySelector(s);}
function esc(s){return String(s).replace(/[&<>"']/g,function(c){return {'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c];});}

var mem={};
function load(k,d){try{var v=localStorage.getItem(k);if(v!==null)return JSON.parse(v);}catch(e){} return (k in mem)?mem[k]:d;}
function save(k,v){mem[k]=v;try{localStorage.setItem(k,JSON.stringify(v));}catch(e){}}

/* datas */
function pad(n){return String(n).padStart(2,'0');}
function key(d){return d.getFullYear()+'-'+pad(d.getMonth()+1)+'-'+pad(d.getDate());}
function fromKey(k){var p=k.split('-').map(Number);return new Date(p[0],p[1]-1,p[2]);}
function addDays(d,n){var x=new Date(d.getFullYear(),d.getMonth(),d.getDate());x.setDate(x.getDate()+n);return x;}
function today(){var n=new Date();return new Date(n.getFullYear(),n.getMonth(),n.getDate());}
function fmtShort(d){return DOW[d.getDay()]+', '+pad(d.getDate())+'/'+pad(d.getMonth()+1);}
function fmtDM(d){return pad(d.getDate())+'/'+pad(d.getMonth()+1);}
function toMin(t){var p=t.split(':').map(Number);return p[0]*60+p[1];}
function fromMin(n){return pad(Math.floor(n/60))+':'+pad(n%60);}
function hash(s){var h=5381;for(var i=0;i<s.length;i++)h=((h<<5)+h+s.charCodeAt(i))>>>0;return h;}
function fmtDias(dias){
  var a=dias.slice().sort(function(x,y){return x-y;});
  var consec=a.every(function(v,i){return i===0||v===a[i-1]+1;});
  if(a.length>=3&&consec)return DOW[a[0]]+' a '+DOW[a[a.length-1]];
  var n=a.map(function(v){return DOW[v];});
  if(n.length>1){var last=n.pop();return n.join(', ')+' e '+last;}
  return n[0];
}

/* dados de exemplo (todos fictícios) */
var HOSPITALS=[
 {id:'hmv',nome:'Hospital Municipal Vale Verde',tipo:'Público',cat:'Hospital geral',bairro:'Centro',staff:{fila:41,plant:6,leitos:118,total:130}},
 {id:'upa',nome:'UPA 24h Alvorada',tipo:'Público',cat:'UPA 24h',bairro:'Zona Leste',staff:{fila:28,plant:4,leitos:14,total:16}},
 {id:'hri',nome:'Hospital Regional Ipê',tipo:'Público',cat:'Hospital geral',bairro:'Zona Norte',staff:{fila:24,plant:6,leitos:96,total:120}},
 {id:'msa',nome:'Maternidade Santa Aurora',tipo:'Público',cat:'Maternidade',bairro:'Zona Sul',staff:{fila:6,plant:3,leitos:38,total:60}},
 {id:'psr',nome:'Pronto-Socorro Infantil Ribeirinho',tipo:'Público',cat:'Pronto-socorro infantil',bairro:'Ribeirinho',staff:{fila:14,plant:3,leitos:20,total:30}},
 {id:'hph',nome:'Hospital Particular Horizonte',tipo:'Particular',cat:'Hospital geral',bairro:'Bairro Nobre',staff:{fila:5,plant:5,leitos:44,total:90}}
];
var DOCS=[
 {id:'hm',h:'hmv',nome:'Dra. Helena Marques',esp:'Clínica geral',crm:'10482',dias:[1,2,3,4,5],turnos:[['08:00','12:00'],['14:00','17:00']],dur:30,sala:'Bloco B, sala 101',aus:null},
 {id:'ps',h:'hmv',nome:'Dr. Paulo Sampaio',esp:'Clínica geral',crm:'11937',dias:[1,3,5],turnos:[['13:00','18:00']],dur:30,sala:'Bloco B, sala 102',aus:{de:-2,ate:4,motivo:'Licença médica'}},
 {id:'rt',h:'hmv',nome:'Dr. Rafael Teixeira',esp:'Cardiologia',crm:'09874',dias:[2,4],turnos:[['08:00','12:00'],['14:00','16:00']],dur:30,sala:'Bloco C, sala 301',aus:{de:0,ate:6,motivo:'Congresso de cardiologia'}},
 {id:'eb',h:'hmv',nome:'Dr. Eduardo Brandão',esp:'Cardiologia',crm:'14021',dias:[1,3,5],turnos:[['09:00','12:00']],dur:30,sala:'Bloco C, sala 302',aus:null},
 {id:'ol',h:'hmv',nome:'Dr. Otávio Lima',esp:'Ortopedia',crm:'10033',dias:[1,3,4],turnos:[['08:00','12:00']],dur:30,sala:'Bloco B, sala 110',aus:null,cirurgia:true},
 {id:'sa',h:'hri',nome:'Dra. Sofia Almeida',esp:'Clínica geral',crm:'12011',dias:[1,2,3,4,5],turnos:[['08:00','12:00']],dur:30,sala:'Ambulatório, sala 4',aus:null},
 {id:'tr',h:'hri',nome:'Dr. Tiago Ramos',esp:'Cardiologia',crm:'13390',dias:[2,3,4],turnos:[['13:30','17:30']],dur:30,sala:'Ambulatório, sala 7',aus:null},
 {id:'lb',h:'hri',nome:'Dr. Lucas Batista',esp:'Ortopedia',crm:'11720',dias:[1,2,4],turnos:[['08:00','12:00']],dur:30,sala:'Ambulatório, sala 9',aus:{de:1,ate:5,motivo:'Férias'}},
 {id:'ac',h:'hri',nome:'Dr. André Cavalcante',esp:'Dermatologia',crm:'13577',dias:[2,3,5],turnos:[['14:00','18:00']],dur:20,sala:'Ambulatório, sala 12',aus:null},
 {id:'lp',h:'hri',nome:'Dra. Luciana Prado',esp:'Neurologia',crm:'11145',dias:[2,4],turnos:[['08:00','12:00']],dur:40,sala:'Ambulatório, sala 15',aus:{de:3,ate:10,motivo:'Férias'}},
 {id:'mv',h:'hri',nome:'Dr. Marcos Vieira',esp:'Oftalmologia',crm:'12804',dias:[1,3,5],turnos:[['08:00','11:30']],dur:30,sala:'Ambulatório, sala 18',aus:null},
 {id:'bn',h:'msa',nome:'Dra. Beatriz Nogueira',esp:'Ginecologia e obstetrícia',crm:'12290',dias:[1,2,3,4,5],turnos:[['08:00','12:00']],dur:30,sala:'Ambulatório, sala 2',aus:null},
 {id:'vc',h:'msa',nome:'Dra. Verônica Castro',esp:'Ginecologia e obstetrícia',crm:'12941',dias:[2,4],turnos:[['13:00','17:00']],dur:30,sala:'Ambulatório, sala 3',aus:{de:-1,ate:3,motivo:'Licença médica'}},
 {id:'cf',h:'psr',nome:'Dra. Camila Ferraz',esp:'Pediatria',crm:'12655',dias:[1,2,3,4,5],turnos:[['08:00','12:00']],dur:30,sala:'Consultório 1',aus:null},
 {id:'rd',h:'psr',nome:'Dra. Renata Duarte',esp:'Pediatria',crm:'13208',dias:[2,4],turnos:[['13:30','17:30']],dur:30,sala:'Consultório 2',aus:null},
 {id:'fc',h:'hph',nome:'Dr. Fernando Coelho',esp:'Clínica geral',crm:'14402',dias:[1,2,3,4,5],turnos:[['08:00','12:00'],['14:00','18:00']],dur:30,sala:'Torre A, sala 210',aus:null},
 {id:'pl',h:'hph',nome:'Dra. Patrícia Luz',esp:'Cardiologia',crm:'14118',dias:[1,3,5],turnos:[['09:00','13:00']],dur:30,sala:'Torre A, sala 305',aus:null},
 {id:'im',h:'hph',nome:'Dra. Isabela Moura',esp:'Dermatologia',crm:'14560',dias:[2,4],turnos:[['08:00','12:00']],dur:20,sala:'Torre B, sala 112',aus:{de:0,ate:2,motivo:'Congresso'}}
];
var SECTORS_BY={
 'Hospital geral':[
  {n:'Pronto-socorro adulto',base:82,k:0.9,w:30},{n:'Pronto-socorro infantil',base:62,k:0.8,w:20},
  {n:'Ortopedia e trauma',base:70,k:0.6,w:35},{n:'Exames de imagem',base:66,k:0.7,w:25},
  {n:'Maternidade',base:55,k:0.3,w:15},{n:'UTI',base:78,k:0.35,w:0}],
 'UPA 24h':[
  {n:'Sala de emergência',base:70,k:0.8,w:0},{n:'Observação adulto',base:84,k:0.9,w:40},
  {n:'Observação infantil',base:60,k:0.8,w:30},{n:'Raio-X e exames',base:66,k:0.7,w:25}],
 'Maternidade':[
  {n:'Pré-parto',base:55,k:0.5,w:15},{n:'Centro obstétrico',base:60,k:0.4,w:20},
  {n:'Alojamento conjunto',base:72,k:0.5,w:0},{n:'UTI neonatal',base:78,k:0.3,w:0},{n:'Ultrassom',base:60,k:0.6,w:25}],
 'Pronto-socorro infantil':[
  {n:'Classificação de risco',base:70,k:0.9,w:25},{n:'Consultório pediátrico',base:68,k:0.8,w:30},
  {n:'Observação',base:62,k:0.7,w:0},{n:'Raio-X e exames',base:60,k:0.6,w:30},{n:'UTI pediátrica',base:75,k:0.3,w:0}]
};
var LEVELS=[
 {id:'baixa',nome:'baixa',max:50,cls:'ok',advice:'Esta unidade está tranquila. Não há fila relevante neste momento.'},
 {id:'moderada',nome:'moderada',max:75,cls:'warn',advice:'O fluxo é normal, com alguma espera para casos pouco urgentes.'},
 {id:'alta',nome:'alta',max:90,cls:'hi',advice:'Casos leves podem esperar bastante. Se não for urgente, agende uma consulta, procure uma unidade menos cheia ou uma unidade básica de saúde.'},
 {id:'critica',nome:'crítica',max:101,cls:'crit',advice:'A capacidade está no limite. Venha apenas em caso de urgência. Casos graves continuam sendo atendidos primeiro. Em risco de vida, ligue 192.'}
];

function hosp(id){return HOSPITALS.filter(function(h){return h.id===id;})[0];}
function docsOf(hid){return DOCS.filter(function(d){return d.h===hid;});}

/* estado */
var staffStore=load('an_staff2',{});
var absStore=load('an_abs',{d:'',ids:{}});
if(absStore.d!==key(today()))absStore={d:key(today()),ids:{}};
var state={
  hs:{},
  sel:load('an_sel','hmv'),
  absentToday:absStore.ids,
  appts:load('an_appts',[]).filter(function(a){return a.date>=key(today());})
};
HOSPITALS.forEach(function(h){
  state.hs[h.id]=Object.assign({},h.staff,staffStore[h.id]||{});
  state.hs[h.id].total=h.staff.total;
});
if(!hosp(state.sel))state.sel='hmv';
function saveAbs(){save('an_abs',{d:key(today()),ids:state.absentToday});}

/* regras de agenda */
function absenceOn(doc,d){
  var k=key(d),t=today();
  if(doc.aus){
    var a=key(addDays(t,doc.aus.de)),b=key(addDays(t,doc.aus.ate));
    if(k>=a&&k<=b)return {motivo:doc.aus.motivo,ate:addDays(t,doc.aus.ate)};
  }
  if(k===key(t)&&state.absentToday[doc.id])return {motivo:'Ausência registrada pela recepção',ate:t};
  return null;
}
function returnDate(doc,ab){
  var d=addDays(ab.ate,1);
  for(var i=0;i<14;i++){if(doc.dias.indexOf(d.getDay())>=0)return d;d=addDays(d,1);}
  return d;
}
function slotsFor(doc,d){
  if(doc.dias.indexOf(d.getDay())<0||absenceOn(doc,d))return [];
  var k=key(d);
  var booked={};
  state.appts.forEach(function(a){if(a.doc===doc.id&&a.date===k)booked[a.time]=true;});
  var now=new Date(),isToday=k===key(today()),limit=now.getHours()*60+now.getMinutes()+30,out=[];
  doc.turnos.forEach(function(tn){
    for(var m=toMin(tn[0]);m+doc.dur<=toMin(tn[1]);m+=doc.dur){
      if(isToday&&m<limit)continue;
      var t=fromMin(m);
      var taken=hash(doc.id+k+t)%100<38||booked[t];
      out.push({t:t,free:!taken});
    }
  });
  return out;
}
function nextFree(doc,from){
  var start=from||today();
  for(var i=0;i<=60;i++){
    var d=addDays(start,i);
    var f=slotsFor(doc,d).filter(function(s){return s.free;})[0];
    if(f)return {d:d,t:f.t};
  }
  return null;
}
function altFor(doc){
  return DOCS.filter(function(x){return x.id!==doc.id&&x.esp===doc.esp;})
    .map(function(x){return {x:x,n:nextFree(x)};})
    .filter(function(o){return o.n;})
    .sort(function(a,b){return ((a.x.h===doc.h?0:1)-(b.x.h===doc.h?0:1))||(a.n.d-b.n.d);})[0];
}
function altText(doc,alt){
  return alt.x.nome+(alt.x.h!==doc.h?' ('+hosp(alt.x.h).nome+')':'');
}
function statusNow(doc){
  var t=today(),n=new Date(),m=n.getHours()*60+n.getMinutes();
  var ab=absenceOn(doc,t);
  if(ab)return {cls:'crit',label:'Ausente',ab:ab};
  if(doc.dias.indexOf(t.getDay())<0)return {cls:'off',label:'Sem atendimento hoje'};
  var inTurn=doc.turnos.some(function(tn){return m>=toMin(tn[0])&&m<toMin(tn[1]);});
  if(inTurn)return doc.cirurgia?{cls:'info',label:'Em cirurgia'}:{cls:'ok',label:'Atendendo agora'};
  var nx=doc.turnos.filter(function(tn){return toMin(tn[0])>m;})[0];
  if(nx)return {cls:'warn',label:'Atende hoje às '+nx[0]};
  return {cls:'off',label:'Expediente encerrado'};
}

/* demanda */
function demand(hid){
  var s=state.hs[hid||state.sel];
  var occ=s.leitos/s.total*100;
  var press=Math.min(100,s.fila/(s.plant*5)*100);
  var score=Math.round(0.5*occ+0.5*press);
  var wait=Math.round(s.fila/s.plant*12);
  var lvl=LEVELS.filter(function(l){return score<l.max;})[0]||LEVELS[3];
  return {occ:occ,press:press,score:score,wait:wait,lvl:lvl,s:s};
}
function renderDemand(){
  var h=hosp(state.sel),D=demand(),s=D.s;
  $('#dName').textContent=h.nome;
  $('#dMeta').textContent=h.tipo+' · '+h.cat+' · '+h.bairro;
  var w=$('#lvlWord');
  w.textContent=D.lvl.nome;
  w.className='lvl '+D.lvl.cls;
  $('#lvlAdvice').textContent=D.lvl.advice;
  $('#mk').style.left=D.score+'%';
  $('#mkVal').textContent=D.score;
  var idx=LEVELS.indexOf(D.lvl);
  [].forEach.call(document.querySelectorAll('.segs i'),function(el,i){el.classList.toggle('on',i===idx);});
  $('#meterImg').setAttribute('aria-label','Pontuação de demanda '+D.score+' de 100, nível '+D.lvl.nome);
  $('#stWait').textContent=D.wait;
  $('#stFila').textContent=s.fila;
  $('#stPlant').textContent=s.plant;
  $('#stLeitos').textContent=s.leitos;
  $('#stTotal').textContent=s.total;
  $('#live').textContent='Agora: ocupação '+Math.round(D.occ)+'% · pressão da fila '+Math.round(D.press)+'% · pontuação '+D.score+' · nível '+D.lvl.nome;

  var rows=(SECTORS_BY[h.cat]||SECTORS_BY['Hospital geral']).map(function(sec){
    var occ=Math.max(20,Math.min(100,Math.round(sec.base+(D.score-70)*sec.k)));
    var cls=occ<60?'ok':occ<80?'warn':occ<92?'hi':'crit';
    var lab=occ<60?'Livre':occ<80?'Movimentado':occ<92?'Cheio':'Lotado';
    var wt=sec.w?Math.round(sec.w*(0.4+D.score/100*1.2))+' min':'—';
    return '<tr><td>'+esc(sec.n)+'</td><td><div class="occ"><span class="num">'+occ+'%</span><span class="track"><i class="'+cls+'" style="width:'+occ+'%"></i></span></div></td><td>'+wt+'</td><td><span class="pill '+cls+'">'+lab+'</span></td></tr>';
  });
  $('#sectors').innerHTML=rows.join('');
  [].forEach.call(document.querySelectorAll('.whereName'),function(n){n.textContent=h.nome;});
}

/* lista de unidades */
var hFilter={t:'todos',cat:''};
function renderHospitals(){
  var all=HOSPITALS.map(function(h){return {h:h,D:demand(h.id)};});
  var rows=all.filter(function(o){
    var okT=hFilter.t==='todos'||(hFilter.t==='publico'?o.h.tipo==='Público':o.h.tipo==='Particular');
    return okT&&(!hFilter.cat||o.h.cat===hFilter.cat);
  }).sort(function(a,b){return a.D.score-b.D.score;});
  var sum=$('#sumrow');
  if(!rows.length){sum.innerHTML='';$('#hlist').innerHTML='<p class="empty">Nenhuma unidade encontrada com esses filtros.</p>';return;}
  var lo=rows[0],hi=rows[rows.length-1];
  var busy=rows.filter(function(o){return o.D.lvl.cls==='hi'||o.D.lvl.cls==='crit';}).length;
  sum.innerHTML=
    '<div class="sum"><small>Menos cheia agora</small><strong>'+esc(lo.h.nome)+'</strong><span>demanda '+lo.D.lvl.nome+' · espera de cerca de '+lo.D.wait+' min</span></div>'+
    '<div class="sum"><small>Mais cheia agora</small><strong>'+esc(hi.h.nome)+'</strong><span>demanda '+hi.D.lvl.nome+' · espera de cerca de '+hi.D.wait+' min</span></div>'+
    '<div class="sum"><small>Com demanda a... (34 KB restante(s))
