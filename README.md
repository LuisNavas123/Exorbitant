<title>Worth More?</title>
<meta name="claude:viewport-fit-sides" content="cover">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bodoni+Moda:wght@500;700;800&family=Jost:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
/* Layout: a private-club quiz. Onyx ground, gold-leaf cards against ivory type, one centred column that works at 400px. Gold fills mark the left choice and every reward; onyx with a gold edge marks the right choice. */
:root{
  --onyx:#0B0A08; --coal:#14120E; --panel:#1B1812; --panel2:#241F15; --line:#3B3223;
  --gold:#D4AF37; --gold-hi:#F5DF9A; --gold-deep:#8F6B14; --ivory:#F7F0DE; --mute:#A89B80;
  --oxblood:#7A1F2B; --oxblood-hi:#E8808D;
  --leaf:linear-gradient(135deg,#F8E7A8 0%,#D4AF37 48%,#A07A18 100%);
  --display:'Bodoni Moda','Didot','Bodoni 72',Georgia,serif;
  --body:'Jost','Avenir Next','Helvetica Neue',Arial,sans-serif;
  color-scheme:dark;
}
*{box-sizing:border-box}
html,body{height:auto}
body{background:var(--onyx);background-image:radial-gradient(120% 60% at 50% -10%,#3a2c0c 0%,#0B0A08 62%);background-repeat:no-repeat;background-color:var(--onyx);color:var(--ivory);font-family:var(--body);font-size:16px;line-height:1.4;
  padding-block:0 96px;padding-left:max(16px,env(safe-area-inset-left,0px));padding-right:max(16px,env(safe-area-inset-right,0px));
  -webkit-tap-highlight-color:transparent;-webkit-text-size-adjust:100%;overscroll-behavior-y:none}
button{font:inherit;color:inherit;cursor:pointer;border:0;background:none;touch-action:manipulation}
button:focus-visible,input:focus-visible{outline:3px solid var(--gold-hi);outline-offset:2px}
.wrap{max-width:560px;margin:0 auto;display:flex;flex-direction:column;gap:16px;padding-top:12px}
.num{font-variant-numeric:tabular-nums lining-nums}
h1,h2,h3{margin:0;text-wrap:balance}
.disp{font-family:var(--display);font-weight:700;letter-spacing:.01em}
.muted{color:var(--mute)}
.small{font-size:13px}
.label{font-size:11px;font-weight:600;letter-spacing:.22em;text-transform:uppercase;color:var(--gold)}

.top{display:flex;align-items:center;justify-content:space-between;gap:12px}
.brand{font-family:var(--display);font-weight:800;font-size:25px;line-height:1;display:flex;gap:6px;align-items:baseline;letter-spacing:.01em}
.brand .w{color:var(--gold-hi);background:var(--leaf);-webkit-background-clip:text;background-clip:text;-webkit-text-fill-color:transparent}
.brand .m{color:var(--ivory)} .brand .q{color:var(--gold)}
.pill{display:inline-flex;align-items:center;gap:8px;background:var(--coal);border:1px solid var(--gold-deep);border-radius:999px;padding:4px 12px 4px 4px;font-weight:600;font-size:13px}
.pill b{background:var(--leaf);color:var(--onyx);border-radius:50%;width:28px;height:28px;display:grid;place-items:center;font-family:var(--display);font-weight:800;font-size:13px}
.xpbar{height:4px;width:54px;background:var(--line);border-radius:9px;overflow:hidden}
.xpbar i{display:block;height:100%;background:var(--gold)}
.icon-btn{width:40px;height:40px;border-radius:50%;border:1px solid var(--gold-deep);background:var(--coal);display:grid;place-items:center;font-weight:600;font-size:12px;color:var(--gold-hi)}

.hero{position:relative;border:1px solid var(--gold);border-radius:24px;overflow:hidden;background:var(--coal);box-shadow:0 0 0 4px var(--onyx),0 0 0 5px var(--gold-deep),0 18px 40px #000a}
.hero .half{padding:22px 18px 30px;display:flex;flex-direction:column;gap:3px;min-height:100px;justify-content:center}
.hero .a{background:var(--leaf);color:var(--onyx)} .hero .b{background:var(--onyx);color:var(--gold-hi);align-items:flex-end;text-align:right}
.hero .half span{font-size:11px;font-weight:600;letter-spacing:.2em;text-transform:uppercase;opacity:.75}
.hero .half strong{font-family:var(--display);font-weight:700;font-size:24px;line-height:1.08}
.vs{position:absolute;left:50%;top:50%;transform:translate(-50%,-50%);background:var(--onyx);color:var(--gold-hi);border:2px solid var(--gold);border-radius:50%;width:56px;height:56px;display:grid;place-items:center;font-family:var(--display);font-weight:700;font-style:italic;font-size:19px;z-index:2}
.hero-cta{padding:12px 14px;display:flex;gap:10px;align-items:center;justify-content:space-between;background:var(--coal);border-top:1px solid var(--gold-deep)}
.hero-cta p{margin:0;font-weight:500;color:var(--ivory)}

.btn{display:inline-flex;align-items:center;justify-content:center;gap:8px;min-height:50px;padding:12px 22px;border-radius:14px;border:1px solid var(--gold-hi);font-weight:600;font-size:16px;letter-spacing:.04em;background:var(--leaf);color:var(--onyx);box-shadow:0 5px 0 var(--gold-deep),0 10px 20px #0008;transition:transform .08s,box-shadow .08s}
.btn:active{transform:translateY(4px);box-shadow:0 1px 0 var(--gold-deep)}
.btn.blue{background:var(--leaf);color:var(--onyx)}
.btn.red{background:var(--onyx);color:var(--gold-hi);border-color:var(--gold);box-shadow:0 5px 0 #4a3a12,0 10px 20px #0008}
.btn.white{background:var(--panel);color:var(--ivory);border-color:var(--line);box-shadow:0 5px 0 #000}
.btn.sm{min-height:42px;padding:8px 16px;font-size:14px;border-radius:12px;box-shadow:0 4px 0 var(--gold-deep)}
.btn.red.sm{box-shadow:0 4px 0 #4a3a12} .btn.white.sm{box-shadow:0 4px 0 #000}
.btn[disabled]{opacity:.4;pointer-events:none}
.row{display:flex;gap:10px;flex-wrap:wrap}
.row>*{flex:1 1 140px;min-width:0}

.panel{background:var(--panel);border:1px solid var(--line);border-radius:18px;padding:16px;display:flex;flex-direction:column;gap:12px}
.panel.flat{background:var(--coal)}
.daily{background:var(--leaf);color:var(--onyx);border-color:var(--gold-hi);box-shadow:0 10px 28px #0009}
.daily .label{color:#4a3608}
.daily h2{font-family:var(--display);font-weight:800;font-size:25px}
.daily .sub{color:#4a3608}
.pips{display:flex;gap:5px;flex-wrap:wrap}
.pip{width:20px;height:20px;border-radius:5px;border:1px solid var(--gold-deep);background:var(--coal)}
.pip.ok{background:var(--gold);border-color:var(--gold-hi)} .pip.no{background:#2a1115;border-color:var(--oxblood)} .pip.now{background:var(--ivory);border-color:var(--gold-hi)}
.daily .pip{border-color:#0b0a0866;background:#0b0a0822} .daily .pip.ok{background:var(--onyx);border-color:var(--onyx)} .daily .pip.no{background:#7A1F2B;border-color:#7A1F2B}
.chips{display:flex;gap:8px;flex-wrap:wrap}
.chip{padding:8px 14px;border-radius:999px;border:1px solid var(--line);background:var(--coal);font-weight:500;font-size:14px;color:var(--ivory)}
.chip[aria-pressed="true"]{background:var(--leaf);color:var(--onyx);border-color:var(--gold-hi);font-weight:600}
.modes{display:grid;grid-template-columns:1fr 1fr;gap:12px}
.mode{display:flex;flex-direction:column;gap:5px;text-align:left;padding:14px;border-radius:18px;border:1px solid var(--gold-deep);background:linear-gradient(160deg,var(--panel2),var(--coal));box-shadow:0 5px 0 #000,inset 0 1px 0 #ffffff12;transition:transform .08s,box-shadow .08s;min-width:0}
.mode:active{transform:translateY(4px);box-shadow:0 1px 0 #000}
.mode strong{font-family:var(--display);font-weight:700;font-size:19px;line-height:1.05;color:var(--gold-hi)}
.mode span{font-size:13px;color:var(--mute);font-weight:400}
.mode .tag{align-self:flex-start;font-size:10px;font-weight:600;letter-spacing:.16em;text-transform:uppercase;padding:2px 9px;border-radius:999px;background:var(--gold);color:var(--onyx);margin-bottom:4px}
.mode.r .tag{background:var(--ivory)} .mode.s .tag{background:transparent;color:var(--gold-hi);border:1px solid var(--gold)}
.banner{background:var(--leaf);color:var(--onyx);border:1px solid var(--gold-hi);border-radius:18px;padding:12px 14px;display:flex;gap:12px;align-items:center;justify-content:space-between;flex-wrap:wrap}
.banner p{margin:0;font-weight:600;flex:1 1 180px}
input.code{width:100%;min-height:46px;border:1px solid var(--gold-deep);border-radius:12px;padding:8px 12px;font:500 16px var(--body);background:var(--onyx);color:var(--ivory)}
input.code::placeholder{color:#7d725c}

.nav{position:fixed;left:0;right:0;bottom:0;z-index:20;background:var(--coal);border-top:1px solid var(--gold-deep);
  padding:8px max(16px,env(safe-area-inset-left,0px)) calc(8px + env(safe-area-inset-bottom,0px)) max(16px,env(safe-area-inset-right,0px))}
.nav div{max-width:560px;margin:0 auto;display:grid;grid-template-columns:repeat(4,1fr);gap:6px}
.nav button{padding:9px 4px;border-radius:12px;font-weight:600;font-size:12px;letter-spacing:.14em;text-transform:uppercase;color:var(--mute)}
.nav button[aria-current="page"]{background:var(--leaf);color:var(--onyx)}

.gbar{display:flex;align-items:center;gap:10px;justify-content:space-between}
.stat{display:flex;flex-direction:column;align-items:center;min-width:56px;background:var(--coal);border:1px solid var(--gold-deep);border-radius:14px;padding:4px 10px}
.stat b{font-family:var(--display);font-weight:700;font-size:20px;line-height:1.1;color:var(--gold-hi)}
.stat span{font-size:9px;font-weight:600;letter-spacing:.18em;text-transform:uppercase;color:var(--mute)}
.stat.hot{background:var(--leaf);border-color:var(--gold-hi)} .stat.hot b,.stat.hot span{color:var(--onyx)}
.track{height:8px;border-radius:9px;background:var(--coal);border:1px solid var(--gold-deep);overflow:hidden}
.track i{display:block;height:100%;background:var(--leaf);width:100%}
.ask{text-align:center;display:flex;flex-direction:column;gap:4px}
.ask h2{font-family:var(--display);font-weight:700;font-size:27px;color:var(--ivory)}
.stage{position:relative;display:flex;flex-direction:column;gap:16px}
.choice{position:relative;display:flex;align-items:center;gap:14px;text-align:left;width:100%;min-height:128px;padding:16px;border-radius:22px;transition:transform .08s,box-shadow .08s,opacity .2s}
.choice.a{background:var(--leaf);color:var(--onyx);border:1px solid var(--gold-hi);box-shadow:0 7px 0 var(--gold-deep),0 14px 26px #000a}
.choice.b{background:linear-gradient(160deg,#1d1a12,#0B0A08);color:var(--ivory);border:1px solid var(--gold);box-shadow:0 7px 0 #4a3a12,0 14px 26px #000a,inset 0 0 0 3px #0B0A08,inset 0 0 0 4px #5a4513}
.choice:active:not([disabled]){transform:translateY(5px)}
.choice[disabled]{cursor:default}
.mono{flex:0 0 auto;width:62px;height:62px;border-radius:50%;display:grid;place-items:center;font-family:var(--display);font-weight:800;font-size:22px}
.choice.a .mono{background:var(--onyx);color:var(--gold-hi);border:2px solid #0b0a08}
.choice.b .mono{background:var(--leaf);color:var(--onyx);border:2px solid var(--gold-hi)}
.cbody{display:flex;flex-direction:column;gap:2px;min-width:0;flex:1}
.cname{font-family:var(--display);font-weight:700;font-size:21px;line-height:1.08;overflow-wrap:anywhere}
.cmeta{font-size:12px;font-weight:600;letter-spacing:.12em;text-transform:uppercase;opacity:.7}
.cval{font-family:var(--display);font-weight:800;font-size:26px;line-height:1.1;margin-top:4px;min-height:29px}
.choice.b .cval{color:var(--gold-hi)}
.choice.win{outline:3px solid var(--ivory);outline-offset:3px}
.choice.lose{opacity:.5}
.crown{position:absolute;right:14px;top:-12px;background:var(--ivory);color:var(--onyx);border:1px solid var(--gold);border-radius:999px;padding:2px 12px;font-weight:700;font-size:11px;letter-spacing:.14em;text-transform:uppercase}
.mid{position:absolute;left:50%;top:50%;transform:translate(-50%,-50%);z-index:3;background:var(--onyx);color:var(--gold-hi);border:2px solid var(--gold);border-radius:50%;width:54px;height:54px;display:grid;place-items:center;font-family:var(--display);font-weight:700;font-style:italic;font-size:18px;pointer-events:none}
.fb{border:1px solid var(--gold-deep);border-radius:18px;padding:14px;display:flex;flex-direction:column;gap:10px;background:var(--panel)}
.fb.ok{background:#1f1b0f;border-color:var(--gold)} .fb.no{background:#1f1114;border-color:var(--oxblood)}
.fb h3{font-family:var(--display);font-weight:700;font-size:22px}
.fb.ok h3{color:var(--gold-hi)} .fb.no h3{color:var(--oxblood-hi)}
.hintline{font-weight:500;text-align:center;min-height:22px;color:var(--gold-hi)}
.float{position:absolute;left:50%;top:40%;transform:translateX(-50%);font-family:var(--display);font-weight:800;font-size:34px;color:var(--onyx);background:var(--leaf);border:1px solid var(--gold-hi);border-radius:14px;padding:2px 16px;z-index:5;animation:rise .9s ease-out forwards;pointer-events:none}
@keyframes rise{0%{opacity:0;transform:translate(-50%,10px) scale(.8)}20%{opacity:1;transform:translate(-50%,0) scale(1.05)}100%{opacity:0;transform:translate(-50%,-50px) scale(1)}}
.shake{animation:shake .35s}
@keyframes shake{0%,100%{transform:translateX(0)}20%{transform:translateX(-8px)}40%{transform:translateX(8px)}60%{transform:translateX(-5px)}80%{transform:translateX(5px)}}

.big{font-family:var(--display);font-weight:800;font-size:72px;line-height:1;color:var(--gold-hi);background:var(--leaf);-webkit-background-clip:text;background-clip:text;-webkit-text-fill-color:transparent}
.result{text-align:center;align-items:center}
.sq{display:flex;gap:6px;flex-wrap:wrap;justify-content:center}
.sq i{width:26px;height:26px;border-radius:6px;border:1px solid var(--gold-deep)}
.sq i.ok{background:var(--gold);border-color:var(--gold-hi)} .sq i.no{background:#2a1115;border-color:var(--oxblood)}
.kv{display:grid;grid-template-columns:repeat(3,1fr);gap:8px;width:100%}
.kv div{background:var(--panel2);border:1px solid var(--line);border-radius:14px;padding:10px 6px;display:flex;flex-direction:column;align-items:center}
.kv b{font-family:var(--display);font-weight:700;font-size:22px;color:var(--gold-hi)}
.kv span{font-size:10px;font-weight:600;letter-spacing:.14em;text-transform:uppercase;color:var(--mute)}
.newbest{background:var(--leaf);color:var(--onyx);border-radius:999px;padding:3px 14px;font-weight:700;font-size:11px;letter-spacing:.16em;text-transform:uppercase}
.cardimg{max-width:100%;border:1px solid var(--gold);border-radius:16px}

.bars{display:flex;flex-direction:column;gap:10px}
.bar{display:grid;grid-template-columns:110px 1fr 52px;gap:10px;align-items:center;font-weight:500;font-size:14px}
.bar .t{height:8px;border-radius:9px;background:var(--line);overflow:hidden}
.bar .t i{display:block;height:100%;background:var(--leaf)}
.list{display:flex;flex-direction:column}
.li{display:flex;gap:12px;align-items:center;justify-content:space-between;padding:10px 0;border-bottom:1px solid var(--line)}
.li:last-child{border-bottom:0}
.li .rk{font-family:var(--display);font-weight:800;width:26px;color:var(--gold)}
.li .nm{flex:1;min-width:0;font-weight:500}
.li b{font-family:var(--display);font-weight:700;font-size:18px;color:var(--gold-hi)}
.trophies{display:grid;grid-template-columns:1fr 1fr;gap:10px}
.tro{border:1px solid var(--line);border-radius:16px;padding:12px;display:flex;flex-direction:column;gap:4px;background:var(--coal);min-width:0}
.tro.on{border-color:var(--gold-hi);background:var(--leaf);color:var(--onyx)}
.tro.on .label{color:#4a3608}
.tro strong{font-family:var(--display);font-weight:700;font-size:16px;line-height:1.1}
.tro span{font-size:13px}
.tro:not(.on){color:var(--mute)} .tro:not(.on) strong{color:#cdbf9f}
.sheet{position:fixed;inset:0;z-index:40;background:#000c;display:flex;align-items:flex-end;justify-content:center;padding:0 max(0px,env(safe-area-inset-left,0px)) 0 max(0px,env(safe-area-inset-right,0px))}
.sheet .in{background:var(--panel);border:1px solid var(--gold);border-bottom:0;border-radius:24px 24px 0 0;max-width:560px;width:100%;max-height:86%;overflow:auto;padding:18px 18px calc(22px + env(safe-area-inset-bottom,0px));display:flex;flex-direction:column;gap:12px}
.sheet h2{font-family:var(--display);font-weight:700;font-size:26px;color:var(--gold-hi)}
.sheet ol,.sheet ul{margin:0;padding-left:20px;display:flex;flex-direction:column;gap:6px}
.toast{position:fixed;left:50%;transform:translateX(-50%);bottom:calc(88px + env(safe-area-inset-bottom,0px));background:var(--leaf);color:var(--onyx);border-radius:999px;padding:10px 18px;font-weight:600;z-index:60;max-width:90%;text-align:center;box-shadow:0 8px 24px #000a}
.foot{font-size:12px;color:var(--mute);text-align:center;padding:4px 8px 8px}
@media (prefers-reduced-motion:reduce){*{animation:none!important;transition:none!important}}
@media (max-width:380px){.bar{grid-template-columns:84px 1fr 44px}.big{font-size:58px}.cname{font-size:19px}}
</style>

<div id="app"></div>
<div id="layer"></div>

<script>
(function(){
'use strict';

/* ---------- DATA (rounded, recent approximations; market values move daily) ---------- */
var CATS=[
{k:'c',n:'Celebs & Money',groups:[
 {m:'Net worth',f:'usd',q:'Who is worth more?',items:[
  ['Elon Musk',4e11],['Jeff Bezos',2.2e11],['Warren Buffett',1.45e11],['Bill Gates',1.1e11],['Oprah Winfrey',3e9],['Michael Jordan',3.5e9],['George Lucas',5.5e9],['Steven Spielberg',5e9],['Jay-Z',2.5e9],['Taylor Swift',1.6e9],['Rihanna',1.4e9],['Cristiano Ronaldo',1.4e9],['LeBron James',1.2e9],['Tiger Woods',1.3e9],['Beyoncé',8e8],['Dwayne Johnson',8e8],['Tom Cruise',8e8],['Selena Gomez',7e8],['Lionel Messi',6e8],['Martha Stewart',4e8],['Will Smith',3.5e8],['Leonardo DiCaprio',3e8],['Jennifer Aniston',3e8],['Eminem',2.5e8],['Drake',2.5e8]]}]},
{k:'k',n:'Cars',groups:[
 {m:'New price (US starting)',f:'usd',q:'Which costs more?',items:[
  ['Toyota Corolla',23000],['Honda Civic',25000],['Toyota Camry',29000],['Mazda MX-5 Miata',30000],['Jeep Wrangler',35000],['Tesla Model 3',40000],['Ford F-150',40000],['Ford Mustang GT',45000],['Chevrolet Corvette Stingray',70000],['BMW M3',80000],['Cadillac Escalade',90000],['Range Rover',110000],['Porsche 911 Carrera',120000],['Mercedes G-Class',150000],['Aston Martin DB12',250000],['McLaren 750S',330000],['Ferrari 296 GTB',350000],['Rolls-Royce Cullinan',400000],['Rolls-Royce Phantom',480000],['Lamborghini Revuelto',600000],['Pagani Huayra',2600000],['Bugatti Chiron',3000000],['Koenigsegg Jesko',3000000]]}]},
{k:'s',n:'Sports',groups:[
 {m:'Team value',f:'usd',q:'Which team is worth more?',items:[
  ['Dallas Cowboys',1e10],['Golden State Warriors',9e9],['New York Yankees',8e9],['Real Madrid',6.6e9],['Manchester United',6e9],['Barcelona',5.5e9],['Liverpool',5e9],['Jacksonville Jaguars',5e9],['Chelsea',3.1e9],['Toronto Maple Leafs',3.1e9],['Arsenal',3e9],['Tampa Bay Rays',1.3e9],['Miami Marlins',1.2e9],['Inter Miami',1.2e9]]},
 {m:'Record transfer fee',f:'eur',q:'Which fee was bigger?',items:[
  ['Neymar to PSG',222e6],['Kylian Mbappé to PSG',180e6],['Ousmane Dembélé to Barcelona',135e6],['João Félix to Atlético',127e6],['Enzo Fernández to Chelsea',121e6],['Jack Grealish to Man City',117.5e6],['Declan Rice to Arsenal',116.6e6],['Jude Bellingham to Real Madrid',103e6],['Gareth Bale to Real Madrid',101e6],['Cristiano Ronaldo to Juventus',100e6],['Zinedine Zidane to Real Madrid',77.5e6],['Erling Haaland to Man City',60e6]]},
 {m:'Total contract',f:'usd',q:'Which contract is bigger?',items:[
  ['Juan Soto',765e6],['Shohei Ohtani',700e6],['Patrick Mahomes',450e6],['Mike Trout',426e6],['Mookie Betts',365e6],['Aaron Judge',360e6],['Jayson Tatum',314e6],['Nikola Jokić',276e6],['Stephen Curry',215e6]]}]},
{k:'b',n:'Companies',groups:[
 {m:'Market value',f:'usd',q:'Which company is worth more?',items:[
  ['Nvidia',4.5e12],['Apple',4e12],['Microsoft',3.8e12],['Alphabet',3e12],['Amazon',2.4e12],['Meta',1.7e12],['Tesla',1.3e12],['Walmart',8e11],['JPMorgan Chase',8e11],['Visa',6.5e11],['Netflix',4.5e11],['Costco',4e11],['Coca-Cola',3e11],['McDonald’s',2.2e11],['Disney',2e11],['Uber',1.9e11],['Boeing',1.5e11],['Spotify',1.3e11],['Nike',1e11],['Starbucks',1e11],['Airbnb',7.5e10],['General Motors',5.5e10],['Ford',4.5e10],['Target',4.5e10],['Lululemon',2.5e10],['Pinterest',2.5e10],['Snap',1.5e10],['Peloton',3e9]]},
 {m:'Purchase price',f:'usd',q:'Which deal was bigger?',items:[
  ['Activision Blizzard (Microsoft)',68.7e9],['Twitter (Musk)',44e9],['LinkedIn (Microsoft)',26.2e9],['Slack (Salesforce)',27.7e9],['WhatsApp (Facebook)',19e9],['Whole Foods (Amazon)',13.7e9],['GitHub (Microsoft)',7.5e9],['Pixar (Disney)',7.4e9],['Lucasfilm (Disney)',4.05e9],['Marvel (Disney)',4e9],['Beats (Apple)',3e9],['Minecraft maker Mojang (Microsoft)',2.5e9],['Fitbit (Google)',2.1e9],['YouTube (Google)',1.65e9],['Zappos (Amazon)',1.2e9],['Tumblr (Yahoo)',1.1e9],['Instagram (Facebook)',1e9]]}]},
{k:'l',n:'Luxury',groups:[
 {m:'Auction record',f:'usd',q:'Which sold for more?',items:[
  ['Pink Star diamond',71.2e6],['Blue Moon diamond',48.4e6],['Patek Philippe Grandmaster Chime',31e6],['Winston Blue diamond',23.8e6],['Paul Newman’s Rolex Daytona',17.8e6],['Jane Birkin’s original Hermès bag',10.1e6]]},
 {m:'Retail price',f:'usd',q:'Which costs more?',items:[
  ['Ray-Ban Wayfarer',180],['Gucci leather belt',500],['Apple Watch Ultra',799],['Montblanc Meisterstück 149',1000],['Louis Vuitton Speedy 30',1900],['Gucci GG Marmont bag',2600],['Cartier Tank',4000],['Cartier Love bracelet',7500],['Rolex Datejust 36',8000],['Rolex Submariner Date',11000],['Chanel Classic Flap (medium)',11000],['Hermès Birkin 25',12000],['Rolex Daytona (steel)',15500],['Audemars Piguet Royal Oak',35000]]},
 {m:'Price tag',f:'usd',q:'Which costs more?',items:[
  ['Cessna Citation CJ4 jet',10e6],['Gulfstream G700 jet',78e6],['Superyacht Octopus',200e6],['Superyacht Eclipse',400e6],['Superyacht Azzam',600e6]]}]},
{k:'e',n:'Entertainment',groups:[
 {m:'Worldwide box office',f:'usd',q:'Which earned more?',items:[
  ['Avatar',2.92e9],['Avengers: Endgame',2.8e9],['Avatar: The Way of Water',2.32e9],['Titanic',2.26e9],['Ne Zha 2',2.2e9],['Star Wars: The Force Awakens',2.07e9],['Avengers: Infinity War',2.05e9],['Spider-Man: No Way Home',1.92e9],['Inside Out 2',1.7e9],['Jurassic World',1.67e9],['The Lion King (2019)',1.66e9],['Top Gun: Maverick',1.5e9],['Barbie',1.44e9],['Black Panther',1.35e9],['Deadpool & Wolverine',1.34e9],['Frozen',1.28e9],['Minions',1.16e9],['Joker',1.08e9],['Toy Story 3',1.07e9],['Oppenheimer',9.75e8],['Shrek 2',9.28e8],['E.T.',7.97e8],['Home Alone',4.76e8]]},
 {m:'Copies sold',f:'units',q:'Which sold more?',items:[
  ['Minecraft',3e8],['Grand Theft Auto V',2e8],['Wii Sports',82.9e6],['Super Mario Bros.',40.2e6]]}]},
{k:'t',n:'Tech',groups:[
 {m:'Launch price',f:'usd',q:'Which cost more at launch?',items:[
  ['Apple I (1976)',666.66],['AirPods Pro',249],['Nintendo Switch 2',449],['PlayStation 5',499],['Meta Quest 3',499],['Steam Deck OLED',549],['Apple Watch Ultra',799],['iPhone 16 Pro Max',1199],['MacBook Pro 14″',1599],['Galaxy Z Fold6',1899],['Apple Vision Pro',3499],['Pro Display XDR',4999],['Mac Pro',6999]]}]},
{k:'x',n:'Collectibles',groups:[
 {m:'Auction price',f:'usd',q:'Which sold for more?',items:[
  ['Babe Ruth “Called Shot” jersey',24.12e6],['Stradivarius “Lady Blunt” violin',15.9e6],['Luka Dončić Logoman card',12.9e6],['1952 Topps Mickey Mantle',12.6e6],['Michael Jordan Last Dance jersey',10.1e6],['T206 Honus Wagner card',7.25e6],['Action Comics #1',6e6],['Wayne Gretzky rookie card',3.75e6],['Amazing Fantasy #15',3.6e6],['Tom Brady rookie auto card',3.1e6],['1st Edition Charizard (PSA 10)',4.2e5],['Michael Jordan 1986 Fleer rookie',7.38e5]]}]}
];
var EVERY=[
['banana','bananas',0.25],['pack of gum','packs of gum',2],['Hershey’s bar','Hershey’s bars',2],['can of Coke','cans of Coke',1.5],
['McDonald’s cheeseburger','McDonald’s cheeseburgers',3],['Costco hot dog combo','Costco hot dog combos',1.5],['slice of NYC pizza','slices of NYC pizza',1.5],
['avocado','avocados',1.5],['cup of coffee','cups of coffee',3.5],['gallon of gas','gallons of gas',3.2],['gallon of milk','gallons of milk',4],
['dozen eggs','dozen eggs',4],['pack of Pokémon cards','packs of Pokémon cards',4.5],['Costco rotisserie chicken','Costco rotisserie chickens',5],
['bag of Doritos','bags of Doritos',5],['Chick-fil-A sandwich','Chick-fil-A sandwiches',5.5],['Starbucks latte','Starbucks lattes',5.5],
['Big Mac','Big Macs',6],['month of Spotify','months of Spotify',12],['Subway footlong','Subway footlongs',9],['Chipotle burrito','Chipotle burritos',11],
['movie ticket','movie tickets',13],['Domino’s large pizza','Domino’s large pizzas',16],['month of Netflix','months of Netflix',18],
['Stanley tumbler','Stanley tumblers',45],['Xbox controller','Xbox controllers',65],['pair of Levi’s 501 jeans','pairs of Levi’s 501 jeans',80],
['pair of Nike Air Force 1s','pairs of Nike Air Force 1s',115],['pair of Air Jordan 1s','pairs of Air Jordan 1s',180],['pair of AirPods Pro','pairs of AirPods Pro',249],
['50-inch TV','50-inch TVs',350],['YETI cooler','YETI coolers',350],['Nintendo Switch 2','Nintendo Switch 2s',449],['PlayStation 5','PlayStation 5s',500],
['LEGO Millennium Falcon','LEGO Millennium Falcons',850],['MacBook Air','MacBook Airs',1099],['iPhone 16 Pro Max','iPhone 16 Pro Maxes',1199],
['Louis Vuitton Speedy 30','Louis Vuitton Speedy 30s',1900],['Apple Vision Pro','Apple Vision Pros',3499],['Rolex Submariner','Rolex Submariners',11000],
['Hermès Birkin 25','Hermès Birkin 25s',12000],['Toyota Corolla','Toyota Corollas',23000],['Honda Civic','Honda Civics',25000],['Toyota Camry','Toyota Camrys',29000],
['Tesla Model 3','Tesla Model 3s',40000],['Corvette Stingray','Corvette Stingrays',70000],['Cadillac Escalade','Cadillac Escalades',90000],['Porsche 911 Carrera','Porsche 911 Carreras',120000],
['Mercedes G-Class','Mercedes G-Classes',150000],['Ferrari 296 GTB','Ferrari 296 GTBs',350000],['median-priced US home','median-priced US homes',420000],['Rolls-Royce Phantom','Rolls-Royce Phantoms',480000],
['Lamborghini Revuelto','Lamborghini Revueltos',600000],['Bugatti Chiron','Bugatti Chirons',3000000],['Cessna Citation CJ4 jet','Cessna Citation CJ4 jets',10000000],
['Gulfstream G700 jet','Gulfstream G700 jets',78000000],['30-second Super Bowl ad','30-second Super Bowl ads',8000000],['Superyacht Eclipse','Eclipse-class superyachts',400000000]
];
function cap(t){return /^[a-z][A-Z]/.test(t)?t:t.charAt(0).toUpperCase()+t.slice(1)}
CATS.push({k:'y',n:'Everyday',groups:[{m:'Typical price',f:'usd',q:'Which costs more?',items:EVERY.map(function(e){return [cap(e[0]),e[2]]})}]});
CATS.forEach(function(c){c.groups.forEach(function(g){g.items.sort(function(a,b){return a[1]-b[1]})})});
var CATNAME={m:'Everything'};CATS.forEach(function(c){CATNAME[c.k]=c.n});

function trim(n,d){return (+n.toFixed(d)).toString()}
function fmt(v,f){
  var s=f==='eur'?'€':'$';
  if(f==='units'){return v>=1e6?trim(v/1e6,1)+'M copies':Math.round(v).toLocaleString('en-US')+' copies'}
  if(v>=1e12)return s+trim(v/1e12,2)+'T';
  if(v>=1e9)return s+trim(v/1e9,2)+'B';
  if(v>=1e6)return s+trim(v/1e6,1)+'M';
  if(v<100)return s+v.toFixed(2);
  return s+Math.round(v).toLocaleString('en-US');
}
function mulberry(a){return function(){a|=0;a=a+0x6D2B79F5|0;var t=Math.imul(a^a>>>15,1|a);t=t+Math.imul(t^t>>>7,61|t)^t;return((t^t>>>14)>>>0)/4294967296}}

function hash32(x){x=Math.imul(x^x>>>16,0x45d9f3b);x=Math.imul(x^x>>>16,0x45d9f3b);return (x^x>>>16)>>>0}
function shuffled(n,seed){var a=[],i,r=mulberry(seed);for(i=0;i<n;i++)a.push(i);for(i=n-1;i>0;i--){var j=Math.floor(r()*(i+1)),t=a[i];a[i]=a[j];a[j]=t}return a}
function dayNum(){var n=new Date();return Math.max(0,Math.round((Date.UTC(n.getFullYear(),n.getMonth(),n.getDate())-Date.UTC(2026,9,28))/864e5))}

/* Bundle questions: one big-ticket item against a pile of a cheaper one. Never a pile on both sides. */
var PG={m:'Total cost',f:'usd',q:'Which costs more?'};
function art(n){return /^[AEIOUaeiou]|^X/.test(n)?'an':'a'}
function gcd(a,b){return b?gcd(b,a%b):a}
var PX=null,PERM=null,LST=[[],[],[],[]],PC=0,PCMAX=0,PREP=5;
function procInit(){
  if(PX)return;PX=[];
  for(var i=0;i<EVERY.length;i++)for(var j=0;j<EVERY.length;j++){
    var a=EVERY[i],b=EVERY[j];
    if(!(b[2]>a[2]))continue;
    var q=b[2]/a[2],lo=Math.max(3,Math.ceil(q/PREP)),hi=Math.min(500,Math.floor(q*PREP));
    if(hi<lo)continue;
    var len=hi-lo+1,st=Math.max(1,Math.round(len*.618));
    while(gcd(st,len)!==1)st++;
    PX.push({a:a,b:b,lo:lo,len:len,st:st,off:hash32(i*131+j*7919)%len});
    if(len>PCMAX)PCMAX=len;
  }
  PERM=shuffled(PX.length,424242);
}
function bucketOf(r){return r>=2.4?0:r>=1.7?1:r>=1.3?2:3}
function rhoOf(p,n){var x=n*p.a[2],y=p.b[2];return Math.max(x,y)/Math.min(x,y)}
function scanNext(){
  var M=PX.length,r=Math.floor(PC/M),p=PX[PERM[PC%M]];
  PC++;
  if(r>=p.len)return;
  var n=p.lo+((r*p.st+p.off)%p.len),rho=rhoOf(p,n);
  if(rho<1.12)return;
  LST[bucketOf(rho)].push({a:p.a,b:p.b,n:n,rho:rho});
}
function listAt(D,k){
  procInit();
  var lim=PX.length*PCMAX;
  while(LST[D].length<=k&&PC<lim)scanNext();
  return LST[D][k]||null;
}
function procBuild(o,swap){
  var X=[cap(art(o.b[0])+' '+o.b[0]),o.b[2]],Y=[o.n.toLocaleString('en-US')+' '+o.a[1],o.n*o.a[2]];
  var L=swap?Y:X,R=swap?X:Y;
  return {cat:'y',g:PG,l:L,r:R,ratio:o.rho,win:L[1]>R[1]?0:1};
}
function procRand(rng,t){
  procInit();
  var best=null,k;
  for(k=0;k<300;k++){
    var p=PX[Math.floor(rng()*PX.length)],n=p.lo+Math.floor(rng()*p.len),rho=rhoOf(p,n);
    if(rho<1.12)continue;
    var o={a:p.a,b:p.b,n:n,rho:rho};
    if(rho>=t&&rho<=t*1.6)return procBuild(o,rng()<.5);
    if(!best||Math.abs(Math.log(rho/t))<Math.abs(Math.log(best.rho/t)))best=o;
  }
  if(!best){var q0=PX[0];best={a:q0.a,b:q0.b,n:q0.lo,rho:Math.max(1.2,rhoOf(q0,q0.lo))}}
  return procBuild(best,rng()<.5);
}

/* Static pairs, bucketed by difficulty and shuffled once with a fixed seed, so every device agrees. */
var SB=null,NEED=[4,6,10,10],FIRST=[0,4,10,20];
function staticInit(){
  if(SB)return;
  var all=[[],[],[],[]],seen={};
  CATS.forEach(function(c){c.groups.forEach(function(g){
    for(var i=0;i<g.items.length;i++)for(var j=i+1;j<g.items.length;j++){
      var lo=g.items[i],hi=g.items[j],r=hi[1]/lo[1];
      if(r<1.2||r>12)continue;
      var kk=[lo[0],hi[0]].sort().join('|').toLowerCase();if(seen[kk])continue;seen[kk]=1;
      all[r>=3.5?0:r>=2.2?1:r>=1.6?2:3].push([c.k,g,lo,hi,r]);
    }})});
  SB=all.map(function(a,bi){return shuffled(a.length,9001+bi).map(function(x){return a[x]})});
}
/* Daily Question: question i of day d. Every slot owns its own entry in a list that is only ever walked forward, so nothing repeats from one day to the next. */
var SD=[8,12,20,20],SS=[0,8,20,40];
function dailyQ(day,i){
  var s=day*60+i,swap=(hash32(s+12345)&1)===1;
  if(i%2===0){
    staticInit();
    var j=i/2,b=j<4?0:j<10?1:j<20?2:3,e=SB[b][day*NEED[b]+(j-FIRST[b])];
    if(e){var A=swap?e[3]:e[2],B=swap?e[2]:e[3];return {cat:e[0],g:e[1],l:A,r:B,ratio:e[4],win:A[1]>B[1]?0:1}}
  }
  var D=i<8?0:i<20?1:i<40?2:3,o=listAt(D,day*SD[D]+(i-SS[D]));
  if(!o)return procRand(mulberry(s*7+1),[3,2,1.5,1.25][D]);
  return procBuild(o,swap);
}

function pairFor(rng,cat,i,recent){
  var cats=cat==='m'?CATS:[CATS.filter(function(c){return c.k===cat})[0]||CATS[0]];
  var minR=i<2?3:i<5?2.2:i<9?1.7:i<15?1.45:1.25;
  if((cat==='y'&&rng()<.7)||(cat==='m'&&rng()<.22))return procRand(rng,minR*(1+rng()*.7));
  var maxR=minR*1.7;
  var found=null,fb=null,pass,t;
  for(pass=0;pass<2&&!found;pass++){
    for(t=0;t<150;t++){
      var c=cats[Math.floor(rng()*cats.length)];
      var g=c.groups[Math.floor(rng()*c.groups.length)];
      var a=g.items[Math.floor(rng()*g.items.length)];
      var b=g.items[Math.floor(rng()*g.items.length)];
      if(a===b)continue;
      if(pass===0&&(recent.indexOf(a[0])>-1||recent.indexOf(b[0])>-1))continue;
      var r=Math.max(a[1],b[1])/Math.min(a[1],b[1]);
      if(r<1.2)continue;
      var cand={c:c,g:g,a:a,b:b,r:r};
      if(r>=minR&&(r<=maxR||pass===1)){found=cand;break}
      if(!fb||Math.abs(Math.log(r/minR))<Math.abs(Math.log(fb.r/minR)))fb=cand;
    }
  }
  var p=found||fb;
  if(!p){var g0=CATS[0].groups[0];p={c:CATS[0],g:g0,a:g0.items[0],b:g0.items[g0.items.length-1],r:g0.items[g0.items.length-1][1]/g0.items[0][1]}}
  var left=rng()<.5?p.a:p.b,right=left===p.a?p.b:p.a;
  return {cat:p.c.k,g:p.g,l:left,r:right,ratio:p.r,win:left[1]>right[1]?0:1};
}

if(typeof module!=='undefined'&&module.exports){module.exports={CATS:CATS,pairFor:pairFor,mulberry:mulberry,fmt:fmt,dailyQ:dailyQ,listAt:listAt,lists:function(){return LST},EVERY:EVERY,staticInit:function(){staticInit();return SB}};return}

/* ---------- STATE ---------- */
var KEY='worthmore.v1';
function blank(){return {xp:0,ok:0,tot:0,bestStreak:0,best:{endless:0,lives:0,blitz:0,ten:0,daily:0},top:[],daily:{},cat:{},ach:{},sent:0,close:0,perfects:0,plays:0,sound:true}}
var S=blank();
try{var raw=localStorage.getItem(KEY);if(raw){S=Object.assign(blank(),JSON.parse(raw));S.best=Object.assign(blank().best,S.best||{})}}catch(e){}
function save(){try{localStorage.setItem(KEY,JSON.stringify(S))}catch(e){}}

function pad(n){return n<10?'0'+n:''+n}
function dkey(d){d=d||new Date();return d.getFullYear()+'-'+pad(d.getMonth()+1)+'-'+pad(d.getDate())}
function dnum(){return parseInt(dkey().replace(/-/g,''),10)}
function dailyStreak(){
  var d=new Date(),n=0;
  if(!S.daily[dkey(d)])d.setDate(d.getDate()-1);
  while(S.daily[dkey(d)]){n++;d.setDate(d.getDate()-1)}
  return n;
}
function bestDay(){var m=0;for(var k in S.daily)if(S.daily[k].s>m)m=S.daily[k].s;return m}
function lvl(xp){return Math.floor(Math.sqrt(xp/40))+1}
function lvlInfo(xp){var L=lvl(xp),lo=40*(L-1)*(L-1),hi=40*L*L;return {L:L,p:(xp-lo)/(hi-lo),need:hi-xp}}
var TITLES=['Apprentice','Collector','Appraiser','Broker','Dealmaker','Magnate','Tycoon','Legend'];
function title(L){return TITLES[Math.min(L-1,TITLES.length-1)]}

var ACH=[
 ['first','First Pick','Get one right.',function(){return S.ok>=1}],
 ['s5','Hot Hand','Reach a 5 streak.',function(){return S.bestStreak>=5}],
 ['s10','On Fire','Reach a 10 streak.',function(){return S.bestStreak>=10}],
 ['s20','Unstoppable','Reach a 20 streak.',function(){return S.bestStreak>=20}],
 ['perf','Perfect Ten','Go 10 for 10 in a set.',function(){return S.perfects>=1}],
 ['d3','Daily Habit','Play the daily 3 days in a row.',function(){return dailyStreak()>=3}],
 ['d7','Week Warrior','Play the daily 7 days in a row.',function(){return dailyStreak()>=7}],
 ['allc','Well Rounded','Play every category.',function(){return Object.keys(S.cat).length>=CATS.length}],
 ['b15','Speed Demon','Score 15 in a 60 second Blitz.',function(){return S.best.blitz>=15}],
 ['e25','Iron Streak','Score 25 in Endless.',function(){return S.best.endless>=25}],
 ['c100','Century','100 correct picks in total.',function(){return S.ok>=100}],
 ['c500','Big Brain','500 correct picks in total.',function(){return S.ok>=500}],
 ['send','Trash Talker','Send a friend challenge.',function(){return S.sent>=1}],
 ['close','Sharp Eye','Get a close call right (under 1.3× apart).',function(){return S.close>=1}],
 ['dd20','Deep Diver','Go 20 deep in the Daily Question.',function(){return bestDay()>=20}],
 ['dd40','Bottomless','Go 40 deep in the Daily Question.',function(){return bestDay()>=40}],
 ['l5','Dealmaker','Reach level 4.',function(){return lvl(S.xp)>=4}]
];
function checkAch(){
  var fresh=[];
  ACH.forEach(function(a){if(!S.ach[a[0]]&&a[3]()){S.ach[a[0]]=Date.now();fresh.push(a[1])}});
  if(fresh.length){save();toast('Trophy: '+fresh.join(', '))}
}

/* ---------- SOUND ---------- */
var AC=null;
function tone(f,d,type,vol,when){
  if(!S.sound)return;
  try{
    AC=AC||new (window.AudioContext||window.webkitAudioContext)();
    if(AC.state==='suspended')AC.resume();
    var o=AC.createOscillator(),g=AC.createGain(),t=AC.currentTime+(when||0);
    o.type=type||'sine';o.frequency.value=f;
    g.gain.setValueAtTime(vol||.12,t);g.gain.exponentialRampToValueAtTime(.0001,t+d);
    o.connect(g);g.connect(AC.destination);o.start(t);o.stop(t+d+.02);
  }catch(e){}
}
function sfx(k){
  if(k==='ok'){tone(660,.12,'triangle',.14);tone(880,.18,'triangle',.14,.09)}
  else if(k==='no'){tone(180,.3,'sawtooth',.1);tone(130,.35,'sawtooth',.1,.12)}
  else if(k==='hot'){[660,830,990,1320].forEach(function(f,i){tone(f,.15,'triangle',.12,i*.07)})}
  else if(k==='end'){[520,440,330].forEach(function(f,i){tone(f,.2,'square',.07,i*.14)})}
  else tone(500,.05,'sine',.07);
}

/* ---------- GAME ---------- */
var G=null,view='home',homeCat='m',pending=null,timer=null,sheet=null,cardURL=null;
var MODES={
 endless:{n:'Endless',d:'Keep going until you miss.'},
 lives:{n:'3 Lives',d:'Three misses and you are out.'},
 blitz:{n:'Blitz',d:'60 seconds. Misses cost 3 seconds.'},
 ten:{n:'Quick 10',d:'Ten picks. Challenge a friend.'},
 daily:{n:'Daily Question',d:'One try a day. One miss ends it.'}
};
function stopT(){if(timer){clearInterval(timer);timer=null}}
function seedFor(){return (Math.random()*2147483646|0)+1}

function startGame(mode,cat,o){
  o=o||{};stopT();cardURL=null;
  var seed=o.seed||(mode==='daily'?dnum():seedFor());
  var c=mode==='daily'?'m':cat;
  G={mode:mode,day:dayNum(),cat:c,seed:seed,rng:mulberry(seed),i:0,score:0,ok:0,streak:0,best:0,lives:3,
     hints:mode==='daily'?1:mode==='blitz'?0:2,grid:[],recent:[],locked:true,
     dk:dkey(),official:mode==='daily'&&!S.daily[dkey()],target:o.target,pen:0,t0:performance.now(),over:false,answered:0,newBest:false,xpGain:0};
  S.plays++;S.cat[c==='m'?'m':c]=S.cat[c]||{c:0,a:0};
  if(G.official){S.daily[G.dk]={s:0};save()}
  view='game';
  if(mode==='blitz'){timer=setInterval(tickBlitz,100)}
  nextQ();
}
function fixedLen(){return G.mode==='ten'}
function nextQ(){
  G.q=G.mode==='daily'?dailyQ(G.day,G.i):pairFor(G.rng,G.cat,G.i,G.recent);
  G.recent.push(G.q.l[0],G.q.r[0]);if(G.recent.length>10)G.recent.splice(0,2);
  G.locked=false;G.hintMsg='';G.hintUsed=false;G.picked=-1;
  render();
}
function timeLeft(){return Math.max(0,60000-(performance.now()-G.t0)-G.pen)}
function tickBlitz(){
  if(!G||G.mode!=='blitz'||G.over){stopT();return}
  var left=timeLeft(),el=document.getElementById('tbar'),tx=document.getElementById('ttxt');
  if(el)el.style.width=(left/600)+'%';
  if(tx)tx.textContent=Math.ceil(left/1000)+'s';
  if(left<=0){G.locked=true;finish()}
}
function hintText(r){
  var b=[100,25,10,5,3,2,1.5].filter(function(x){return x<=r*0.999})[0];
  return b?'One is worth over '+b+'× the other.':'These two are within 1.5× of each other.';
}
function useHint(){
  if(!G||G.locked||G.hints<1||G.hintUsed)return;
  G.hints--;G.hintUsed=true;G.hintMsg=hintText(G.q.ratio);sfx('tap');render();
}
function answer(side){
  if(!G||G.locked)return;
  G.locked=true;G.picked=side;
  var q=G.q,ok=side===q.win,c=S.cat[G.cat]||(S.cat[G.cat]={c:0,a:0});
  G.answered++;S.tot++;c.a++;
  var pts=0;
  if(ok){
    G.ok++;S.ok++;c.c++;G.streak++;
    if(G.streak>G.best)G.best=G.streak;
    if(G.streak>S.bestStreak)S.bestStreak=G.streak;
    pts=(G.hintUsed?50:100)+Math.min(G.streak,10)*10;
    G.score+=G.mode==='blitz'||fixedLen()?1:1; G.pts=(G.pts||0)+pts;
    var gain=10+(G.streak>=5?5:0);S.xp+=gain;G.xpGain+=gain;
    if(q.ratio<1.3)S.close++;
    sfx(G.streak>0&&G.streak%5===0?'hot':'ok');
  }else{
    G.streak=0;sfx('no');
    if(G.mode==='lives')G.lives--;
    if(G.mode==='blitz')G.pen+=3000;
  }
  G.grid.push(ok?1:0);G.lastOk=ok;
  if(G.mode==='daily'&&G.official)S.daily[G.dk]={s:G.ok};G.lastPts=pts;
  G.i++;
  var done=false;
  if(G.mode==='endless'&&!ok)done=true;
  if(G.mode==='lives'&&G.lives<=0)done=true;
  if(fixedLen()&&G.i>=10)done=true;
  if(G.mode==='daily'&&(!ok||G.i>=60))done=true;
  if(G.mode==='blitz'&&timeLeft()<=0)done=true;
  G.done=done;
  save();
  render();reveal(ok,pts);
  if(G.mode==='blitz'&&!done){setTimeout(function(){if(G&&!G.over&&view==='game'){nextQ()}},ok?450:900)}
  if(G.mode==='blitz'&&done){setTimeout(finish,700)}
}
function reveal(ok,pts){
  var q=G.q,els=[document.getElementById('v0'),document.getElementById('v1')],vals=[q.l[1],q.r[1]],f=q.g.f;
  var reduce=window.matchMedia&&matchMedia('(prefers-reduced-motion: reduce)').matches;
  var dur=reduce?0:650,t0=performance.now();
  function step(now){
    var p=dur?Math.min(1,(now-t0)/dur):1,e=1-Math.pow(1-p,3);
    for(var k=0;k<2;k++)if(els[k])els[k].textContent='≈ '+fmt(vals[k]*e,f);
    if(p<1)requestAnimationFrame(step);
  }
  requestAnimationFrame(step);
  var st=document.getElementById('stage');
  if(ok&&st){var fl=document.createElement('div');fl.className='float';fl.textContent='+'+pts;st.appendChild(fl)}
  if(!ok){var ch=document.getElementById('c'+G.picked);if(ch)ch.classList.add('shake')}
}
function finish(){
  if(!G||G.over)return;
  G.over=true;stopT();sfx('end');
  var m=G.mode,sc=m==='blitz'||m==='endless'||m==='lives'||fixedLen()?G.ok:G.ok;
  var bk=m;
  if((m!=='daily'||G.official)&&sc>(S.best[bk]||0)){S.best[bk]=sc;G.newBest=sc>0}
  if(m==='daily'&&G.official){
    S.daily[G.dk]={s:G.ok};
    S.xp+=20;G.xpGain+=20;
  }
  if(m==='ten'&&G.ok===10){S.perfects++}
  if(m!=='daily'||G.official){
    if(m==='endless'||m==='lives'||m==='blitz'){
      S.top.push({s:sc,m:m,c:G.cat,d:dkey()});
      S.top.sort(function(a,b){return b.s-a.s});S.top=S.top.slice(0,10);
    }
  }
  save();checkAch();view='result';render();
}

/* ---------- SHARE ---------- */
function codeFor(){return (G.cat==='m'?'m':G.cat)+G.seed.toString(36)}
function linkFor(score){return location.href.split('#')[0]+'#c-'+codeFor()+(typeof score==='number'?'-'+score:'')}
function shareText(){
  var sq=G.grid.map(function(x){return x?'🟦':'🟥'}).join('');
  var head;
  if(G.mode==='daily')head='Worth More? Daily Question No. '+(G.day+1)+' ('+G.dk+')  '+G.ok+' deep';
  else if(G.mode==='ten')head='Worth More? '+CATNAME[G.cat]+'  '+G.ok+'/10';
  else head='Worth More? '+MODES[G.mode].n+' ('+CATNAME[G.cat]+')  Score '+G.ok+'  Best streak '+G.best;
  var tail=G.mode==='ten'?'\nBeat me: '+linkFor(G.ok):G.mode==='daily'?'\n'+location.href.split('#')[0]:'\n'+location.href.split('#')[0];
  return head+(fixedLen()?'\n'+sq:'')+tail;
}
function copyText(t,msg){
  function fb(){
    var ta=document.createElement('textarea');ta.value=t;ta.setAttribute('readonly','');ta.style.cssText='position:fixed;left:0;top:0;opacity:.01';
    document.body.appendChild(ta);ta.focus();ta.select();ta.setSelectionRange(0,99999);
    var ok=false;try{ok=document.execCommand('copy')}catch(e){}
    document.body.removeChild(ta);toast(ok?msg:'Select and copy: '+t.slice(0,60));
  }
  try{navigator.clipboard.writeText(t).then(function(){toast(msg)},fb)}catch(e){fb()}
}
function makeCard(){
  var go=function(){
    var W=1080,H=1350,c=document.createElement('canvas');c.width=W;c.height=H;var x=c.getContext('2d');
    var D='"Bodoni Moda",Georgia,serif',B='Jost,Arial,sans-serif';
    x.fillStyle='#0B0A08';x.fillRect(0,0,W,H);
    var gr=x.createLinearGradient(0,0,W,H);gr.addColorStop(0,'#F8E7A8');gr.addColorStop(.5,'#D4AF37');gr.addColorStop(1,'#A07A18');
    x.fillStyle=gr;x.beginPath();x.moveTo(0,H*.66);x.lineTo(W,H*.5);x.lineTo(W,H);x.lineTo(0,H);x.closePath();x.fill();
    x.strokeStyle='#D4AF37';x.lineWidth=3;x.strokeRect(36,36,W-72,H-72);
    x.textAlign='center';
    x.fillStyle='#F5DF9A';x.font='800 92px '+D;x.fillText('Worth More?',W/2,175);
    x.fillStyle='#A89B80';x.font='600 30px '+B;
    var sub=(G.mode==='daily'?'Daily '+dkey():MODES[G.mode].n+'  \u2022  '+CATNAME[G.cat]).toUpperCase();
    x.fillText(sub.split('').join(String.fromCharCode(8202)),W/2,238);
    x.fillStyle='#0B0A08';x.strokeStyle=gr;x.lineWidth=8;
    x.beginPath();x.arc(W/2,620,250,0,Math.PI*2);x.fill();x.stroke();
    x.fillStyle=gr;x.font='800 290px '+D;x.fillText(G.ok+'',W/2,715);
    x.fillStyle='#F7F0DE';x.font='600 36px '+B;
    x.fillText(fixedLen()?'OUT OF 10':G.mode==='daily'?'DEEP IN TODAY\u2019S RUN':'CORRECT PICKS',W/2,800);
    if(fixedLen()){
      var n=G.grid.length,sz=64,gap=14,tot=n*sz+(n-1)*gap,sx=(W-tot)/2;
      for(var i=0;i<n;i++){x.fillStyle=G.grid[i]?'#0B0A08':'#7A1F2B';x.strokeStyle='#0B0A08';x.lineWidth=5;
        x.fillRect(sx+i*(sz+gap),1010,sz,sz);x.strokeRect(sx+i*(sz+gap),1010,sz,sz);
        if(G.grid[i]){x.fillStyle='#D4AF37';x.fillRect(sx+i*(sz+gap)+16,1026,32,32)}}
    }else{
      x.fillStyle='#0B0A08';x.font='700 52px '+B;x.fillText('BEST STREAK  '+G.best,W/2,1050);
    }
    x.fillStyle='#0B0A08';x.font='italic 700 44px '+D;x.fillText('Can you beat it?',W/2,1250);
    cardURL=c.toDataURL('image/png');render();
  };
  try{(document.fonts&&document.fonts.load?document.fonts.load('80px "Bodoni Moda"'):Promise.resolve()).then(go,go)}catch(e){go()}
}

/* ---------- RENDER ---------- */
function esc(s){return String(s).replace(/[&<>"]/g,function(c){return {'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;'}[c]})}
function mono(n){var w=n.replace(/[^A-Za-z0-9À-ɏ ]/g,'').split(/\s+/).filter(function(x){return /^[A-Za-zÀ-ɏ]/.test(x)});return esc(((w[0]||'?')[0]+(w[1]?w[1][0]:(w[0]&&w[0][1])||'')).toUpperCase())}
function pips(arr,total,cur){
  var h='';for(var i=0;i<total;i++){var c=i<arr.length?(arr[i]?'ok':'no'):(i===cur?'now':'');h+='<i class="pip '+c+'"></i>'}return '<div class="pips">'+h+'</div>';
}
function topbar(){
  var li=lvlInfo(S.xp);
  return '<div class="top"><div class="brand"><span class="w">Worth</span><span class="m">More</span><span class="q">?</span></div>'+
   '<div class="row" style="flex:0 0 auto;flex-wrap:nowrap;align-items:center"><div class="pill" aria-label="Level '+li.L+' '+title(li.L)+'"><b>'+li.L+'</b><span>'+title(li.L)+'</span><span class="xpbar"><i style="width:'+Math.round(li.p*100)+'%"></i></span></div>'+
   '<button class="icon-btn" data-a="sound" aria-label="Sound '+(S.sound?'on':'off')+'" style="flex:0 0 40px">'+(S.sound?'On':'Off')+'</button></div></div>';
}
function nav(){
  var t=[['home','Play'],['stats','Stats'],['trophies','Trophies'],['board','Boards']];
  return '<nav class="nav" aria-label="Main"><div>'+t.map(function(x){return '<button data-a="nav" data-v="'+x[0]+'"'+(view===x[0]?' aria-current="page"':'')+'>'+x[1]+'</button>'}).join('')+'</div></nav>';
}
function untilMidnight(){
  var n=new Date(),m=new Date(n.getFullYear(),n.getMonth(),n.getDate()+1),ms=m-n,h=Math.floor(ms/36e5),mi=Math.floor(ms%36e5/6e4);
  return h+'h '+mi+'m';
}
function homeView(){
  var sample=pairFor(mulberry(dnum()+(S.plays||0)),'m',4,[]);
  var d=S.daily[dkey()],ds=dailyStreak();
  var h=topbar();
  if(pending){
    h+='<div class="banner"><p>Friend challenge ready: '+esc(CATNAME[pending.cat]||'Everything')+(pending.target!=null?', beat '+pending.target+'/10':'')+'</p><button class="btn red sm" data-a="acceptChallenge">Accept</button></div>';
  }
  h+='<section class="hero" aria-label="Preview"><div class="half a"><span>'+esc(sample.g.m)+'</span><strong>'+esc(sample.l[0])+'</strong></div><div class="half b"><strong>'+esc(sample.r[0])+'</strong><span>'+esc(sample.g.m)+'</span></div><div class="vs">VS</div>'+
   '<div class="hero-cta"><p>'+esc(sample.g.q)+'</p><button class="btn red sm" data-a="play" data-m="endless">Play now</button></div></section>';
  h+='<section class="panel daily"><span class="label">Daily Question \u2022 No. '+(dayNum()+1)+' \u2022 '+dkey()+'</span>'+(d?'<h2>You went '+d.s+' deep today</h2>':'')+
   '<p class="small sub" style="margin:0">Up to 60 questions that get closer as you climb. One miss ends it and locks it for the day. A fresh set arrives every midnight and no question ever repeats.</p>'+
   '<div class="row" style="align-items:center"><p class="small sub" style="margin:0">'+(ds?ds+' day streak. ':'')+'Best day: '+bestDay()+'. '+(d?'Locked. New questions in '+untilMidnight()+'.':'One try per day.')+'</p>'+
   (d?'<button class="btn white" disabled>Locked until midnight</button>':'<button class="btn white" data-a="play" data-m="daily">Play today</button>')+'</div></section>';
  h+='<section class="panel flat"><span class="label">Category</span><div class="chips">'+
   [['m','Everything']].concat(CATS.map(function(c){return [c.k,c.n]})).map(function(c){return '<button class="chip" data-a="cat" data-k="'+c[0]+'" aria-pressed="'+(homeCat===c[0])+'">'+c[1]+'</button>'}).join('')+'</div></section>';
  h+='<div class="modes">'+
   ['endless','lives','blitz','ten'].map(function(m,i){
     var tag=m==='endless'?'Best '+S.best.endless:m==='lives'?'Best '+S.best.lives:m==='blitz'?'Best '+S.best.blitz:'Challenge';
     return '<button class="mode '+(i%2?'r':i===3?'s':'')+'" data-a="play" data-m="'+m+'"><span class="tag">'+tag+'</span><strong>'+MODES[m].n+'</strong><span>'+MODES[m].d+'</span></button>'}).join('')+'</div>';
  h+='<section class="panel flat"><span class="label">Got a code from a friend?</span><div class="row" style="align-items:center"><input class="code" id="joinCode" placeholder="Paste code or link" autocapitalize="off" autocomplete="off" spellcheck="false"><button class="btn blue sm" data-a="join" style="flex:0 0 auto">Join</button></div></section>';
  h+='<div class="row"><button class="btn white sm" data-a="howto">How to play</button><button class="btn white sm" data-a="resetAsk">Reset progress</button></div>';
  h+='<p class="foot">Values are rounded, recent estimates, and everyday prices are typical US prices. Net worth, team value and market value change daily, so close calls can shift.</p>';
  return h;
}
function qCard(side){
  var q=G.q,it=side?q.r:q.l,cls=side?'b':'a',locked=G.locked;
  var shown=locked&&G.picked!==undefined?'':'';
  var win=locked&&q.win===side,lose=locked&&q.win!==side;
  return '<button class="choice '+cls+(win?' win':'')+(lose?' lose':'')+'" id="c'+side+'" data-a="pick" data-s="'+side+'"'+(locked?' disabled':'')+' aria-label="'+esc(it[0])+'">'+
   (win?'<span class="crown">Worth more</span>':'')+
   '<span class="mono">'+mono(it[0])+'</span><span class="cbody"><span class="cname">'+esc(it[0])+'</span><span class="cmeta">'+esc(q.g.m)+'</span><span class="cval num" id="v'+side+'">'+(locked?'≈ '+fmt(it[1],q.g.f):'?')+'</span></span></button>';
}
function gameView(){
  var q=G.q,m=G.mode,h='';
  var hot=G.streak>=3;
  h+='<div class="gbar"><button class="btn white sm" data-a="quit" style="flex:0 0 auto">Quit</button>'+
    '<div class="row" style="flex:1;justify-content:flex-end;flex-wrap:nowrap;gap:8px">'+
    (m==='lives'?'<div class="stat" style="flex:0 0 auto"><b>'+G.lives+'</b><span>Lives</span></div>':'')+
    (m==='blitz'?'<div class="stat" style="flex:0 0 auto"><b id="ttxt" class="num">'+Math.ceil(timeLeft()/1000)+'s</b><span>Time</span></div>':'')+
    '<div class="stat'+(hot?' hot':'')+'" style="flex:0 0 auto"><b class="num">'+G.streak+'</b><span>Streak</span></div>'+
    '<div class="stat" style="flex:0 0 auto"><b class="num">'+G.ok+'</b><span>Score</span></div></div></div>';
  if(m==='blitz')h+='<div class="track" aria-hidden="true"><i id="tbar" style="width:'+(timeLeft()/600)+'%"></i></div>';
  if(fixedLen())h+=pips(G.grid,10,G.i);
  h+='<div class="ask"><span class="label">'+MODES[m].n+' • '+esc(CATNAME[G.cat])+(m==='daily'?' • Q'+(G.locked?G.i:G.i+1)+'/60':'')+(G.target!=null?' • beat '+G.target:'')+'</span><h2>'+esc(q.g.q)+'</h2></div>';
  h+='<div class="stage" id="stage">'+qCard(0)+'<div class="mid" aria-hidden="true">VS</div>'+qCard(1)+'</div>';
  if(!G.locked){
    h+='<div class="hintline" id="hint">'+esc(G.hintMsg)+'</div>';
    if(m!=='blitz')h+='<div class="row"><button class="btn white sm" data-a="hint"'+(G.hints<1||G.hintUsed?' disabled':'')+'>Hint ('+G.hints+' left, half points)</button></div>';
  }else if(m!=='blitz'||G.done){
    var r=q.ratio,more=trim(r,r<10?1:0)+'×';
    h+='<div class="fb '+(G.lastOk?'ok':'no')+'"><h3>'+(G.lastOk?(G.streak>=5?'On fire! '+G.streak+' in a row':'Correct'):'Not this time')+'</h3><div>'+esc((q.win?q.r:q.l)[0])+' is worth about '+more+' as much as '+esc((q.win?q.l:q.r)[0])+'.'+(G.lastOk?' <b>+'+G.lastPts+' pts</b>':'')+'</div>'+
     '<button class="btn '+(G.done?'red':'blue')+'" data-a="next">'+(G.done?'See results':'Next')+'</button></div>';
  }
  return h;
}
function resultView(){
  var m=G.mode,h=topbar();
  var isDaily=m==='daily';
  var li=lvlInfo(S.xp);
  var head=m==='endless'?'Run over':m==='lives'?'Out of lives':m==='blitz'?'Time’s up':isDaily?'Daily Question over':'Set complete';
  h+='<section class="panel result"><span class="label">'+MODES[m].n+' • '+esc(CATNAME[G.cat])+'</span><h2 class="disp" style="font-size:28px">'+head+'</h2>';
  if(G.newBest)h+='<span class="newbest">New personal best</span>';
  h+='<div class="big num">'+G.ok+(fixedLen()?'<span style="font-size:28px;color:var(--mute)">/10</span>':'')+'</div>';
  if(isDaily)h+='<p class="muted" style="margin:0">in a row, out of 60 possible</p>';
  if(fixedLen())h+='<div class="sq" aria-label="Answers">'+G.grid.map(function(x){return '<i class="'+(x?'ok':'no')+'"></i>'}).join('')+'</div>';
  if(G.target!=null){
    h+='<p style="margin:0;font-weight:700">'+(G.ok>G.target?'You beat the '+G.target+'/10 challenge.':G.ok===G.target?'You tied the '+G.target+'/10 challenge.':'The challenge was '+G.target+'/10. So close.')+'</p>';
  }
  if(isDaily)h+='<p class="muted small" style="margin:0">Locked for today. New questions in '+untilMidnight()+'.</p>';
  h+='<div class="kv"><div><b class="num">'+G.best+'</b><span>Best streak</span></div><div><b class="num">'+(G.answered?Math.round(G.ok/G.answered*100):0)+'%</b><span>Accuracy</span></div><div><b class="num">+'+G.xpGain+'</b><span>XP</span></div></div>';
  h+='<div class="small muted">Level '+li.L+' '+title(li.L)+', '+li.need+' XP to next</div>';
  h+='<div class="row" style="width:100%">'+(isDaily?'':'<button class="btn blue" data-a="again">Play again</button>')+'<button class="btn white" data-a="copyShare">Copy result</button></div>';
  if(m==='ten'){h+='<div class="row" style="width:100%"><button class="btn red" data-a="challengeBack">Challenge a friend</button></div>'}
  h+='<div class="row" style="width:100%"><button class="btn white sm" data-a="card">Make score card</button><button class="btn white sm" data-a="home">Home</button></div>';
  if(cardURL)h+='<img class="cardimg" src="'+cardURL+'" alt="Score card" width="540"><p class="small muted" style="margin:0">Press and hold the card to save it or share it.</p>';
  h+='</section>';
  return h;
}
function statsView(){
  var h=topbar()+'<h2 class="disp" style="font-size:28px">Your stats</h2>';
  var acc=S.tot?Math.round(S.ok/S.tot*100):0;
  h+='<div class="kv"><div><b class="num">'+S.ok+'</b><span>Correct</span></div><div><b class="num">'+acc+'%</b><span>Accuracy</span></div><div><b class="num">'+S.bestStreak+'</b><span>Best streak</span></div></div>';
  h+='<div class="kv"><div><b class="num">'+S.plays+'</b><span>Games</span></div><div><b class="num">'+dailyStreak()+'</b><span>Daily streak</span></div><div><b class="num">'+S.xp+'</b><span>XP</span></div></div>';
  h+='<section class="panel flat"><span class="label">Records</span><div class="list">'+
    [['Endless',S.best.endless],['3 Lives',S.best.lives],['Blitz (60s)',S.best.blitz],['Quick 10',S.best.ten],['Daily Question (best day)',bestDay()]].map(function(r){return '<div class="li"><span class="nm">'+r[0]+'</span><b class="num">'+r[1]+'</b></div>'}).join('')+'</div></section>';
  var keys=['m'].concat(CATS.map(function(c){return c.k}));
  h+='<section class="panel flat"><span class="label">Accuracy by category</span><div class="bars">'+keys.map(function(k){
    var c=S.cat[k]||{c:0,a:0},p=c.a?Math.round(c.c/c.a*100):0;
    return '<div class="bar"><span>'+esc(CATNAME[k])+'</span><div class="t"><i style="width:'+p+'%"></i></div><span class="num">'+(c.a?p+'%':'–')+'</span></div>'}).join('')+'</div></section>';
  return h;
}
function trophiesView(){
  var n=ACH.filter(function(a){return S.ach[a[0]]}).length;
  return topbar()+'<h2 class="disp" style="font-size:28px">Trophies <span class="muted num" style="font-size:18px">'+n+'/'+ACH.length+'</span></h2><div class="trophies">'+
   ACH.map(function(a){var on=!!S.ach[a[0]];return '<div class="tro'+(on?' on':'')+'"><strong>'+a[1]+'</strong><span>'+a[2]+'</span><span class="label" style="color:inherit">'+(on?'Unlocked':'Locked')+'</span></div>'}).join('')+'</div>';
}
function boardView(){
  var h=topbar()+'<h2 class="disp" style="font-size:28px">Leaderboards</h2><p class="muted small" style="margin:0">These boards live on this device. To compare with friends, send a Quick 10 challenge link and see who scores higher.</p>';
  h+='<section class="panel flat"><span class="label">Top runs</span><div class="list">'+
   (S.top.length?S.top.map(function(r,i){return '<div class="li"><span class="rk">'+(i+1)+'</span><span class="nm">'+MODES[r.m].n+' • '+esc(CATNAME[r.c]||'Everything')+'<br><span class="muted small">'+r.d+'</span></span><b class="num">'+r.s+'</b></div>'}).join(''):'<p class="muted" style="margin:0">Play Endless, 3 Lives or Blitz to set a score.</p>')+'</div></section>';
  var days=Object.keys(S.daily).sort().reverse().slice(0,14);
  h+='<section class="panel flat"><span class="label">Daily history</span><div class="list">'+
   (days.length?days.map(function(d){var r=S.daily[d];return '<div class="li"><span class="nm">'+d+'</span><b class="num">'+r.s+' deep</b></div>'}).join(''):'<p class="muted" style="margin:0">Play today’s Daily Question to start your history.</p>')+'</div></section>';
  return h;
}
function render(){
  var app=document.getElementById('app'),h='';
  if(view==='home')h=homeView();else if(view==='game')h=gameView();else if(view==='result')h=resultView();
  else if(view==='stats')h=statsView();else if(view==='trophies')h=trophiesView();else if(view==='board')h=boardView();
  app.innerHTML='<div class="wrap">'+h+'</div>'+(view==='game'||view==='result'?'':nav());
  var l=document.getElementById('layer');
  l.innerHTML=sheet==='howto'?'<div class="sheet" data-a="closeSheet"><div class="in" role="dialog" aria-label="How to play" data-a="stay"><h2>How to play</h2><ol><li>Two things appear. Tap the one that is worth more.</li><li>Each right pick builds your streak and your points. Streaks add bonus points.</li><li>Early rounds have a big gap. Later rounds get much closer.</li><li>Hints tell you how big the gap is, but cut that round’s points in half.</li><li>Daily Question is the same for everyone. You get one try a day, and your first miss locks it until midnight. Your score stays on the home screen.</li><li>Quick 10 gives you a code. Send it so a friend plays the exact same ten.</li></ol><button class="btn blue" data-a="closeSheet">Got it</button></div></div>'
   :sheet==='reset'?'<div class="sheet" data-a="closeSheet"><div class="in" role="dialog" aria-label="Reset progress" data-a="stay"><h2>Reset everything?</h2><p style="margin:0">This clears your records, trophies, XP and daily history on this device. It cannot be undone.</p><div class="row"><button class="btn red" data-a="resetYes">Reset</button><button class="btn white" data-a="closeSheet">Keep my progress</button></div></div></div>':'';
  window.scrollTo(0,0);
}
var toastT=null;
function toast(msg){
  var old=document.getElementById('toast');if(old)old.remove();
  var t=document.createElement('div');t.id='toast';t.className='toast';t.setAttribute('role','status');t.textContent=msg;document.body.appendChild(t);
  clearTimeout(toastT);toastT=setTimeout(function(){t.remove()},2600);
}

/* ---------- CHALLENGE LINKS ---------- */
function parseCode(s){
  var m=/(?:c-)?([a-z])([0-9a-z]{2,})(?:-(\d{1,2}))?\s*$/i.exec(String(s).trim());
  if(!m)return null;
  var k=m[1].toLowerCase();
  if(k!=='m'&&!CATS.some(function(c){return c.k===k}))return null;
  var seed=parseInt(m[2].toLowerCase(),36);
  if(!seed||seed<1||seed>2147483647)return null;
  return {cat:k,seed:seed,target:m[3]!==undefined?Math.min(10,+m[3]):null};
}
function readHash(){
  var m=/^#c-([a-z][0-9a-z]+(?:-\d{1,2})?)$/i.exec(location.hash);
  if(m){var p=parseCode(m[1]);if(p){pending=p;if(view==='home')render()}}
}
window.addEventListener('hashchange',readHash);

/* ---------- ACTIONS ---------- */
document.addEventListener('click',function(e){
  var t=e.target.closest('[data-a]');if(!t)return;
  var a=t.dataset.a;
  if(a==='stay'){if(e.target.closest('button[data-a]')===null)return}
  if(a==='closeSheet'){if(e.target!==t&&!(e.target.closest('button[data-a="closeSheet"]')))return;sheet=null;render();return}
  if(a==='stay')return;
  if(a==='pick'){answer(+t.dataset.s);return}
  if(a==='nav'){view=t.dataset.v;stopT();render();return}
  if(a==='home'){view='home';stopT();G=null;render();return}
  if(a==='cat'){homeCat=t.dataset.k;sfx('tap');render();return}
  if(a==='play'){var m=t.dataset.m;if(m==='daily'&&S.daily[dkey()]){toast('You already played today. New questions at midnight.');view='home';render();return}sfx('tap');startGame(m,homeCat);return}
  if(a==='next'){if(G.done){finish()}else{nextQ()}return}
  if(a==='hint'){useHint();return}
  if(a==='quit'){stopT();G=null;view='home';render();return}
  if(a==='again'){var gm=G.mode,gc=G.cat;if(gm==='daily'){view='home';render();return}startGame(gm,gc,{});return}
  if(a==='sound'){S.sound=!S.sound;save();if(S.sound)sfx('tap');render();return}
  if(a==='howto'){sheet='howto';render();return}
  if(a==='resetAsk'){sheet='reset';render();return}
  if(a==='resetYes'){S=blank();save();sheet=null;pending=null;toast('Progress reset');render();return}
  if(a==='copyShare'){copyText(shareText(),'Result copied');return}
  if(a==='card'){makeCard();return}
  if(a==='challengeBack'){
    S.sent++;save();checkAch();
    var code=codeFor(),link=linkFor(G.ok);
    copyText('Beat my '+G.ok+'/10 on Worth More? '+link+'  (code: '+code+'-'+G.ok+')','Challenge link copied');return;
  }
  if(a==='acceptChallenge'){var p=pending;pending=null;try{history.replaceState(null,'',location.href.split('#')[0])}catch(er){}startGame('ten',p.cat,{seed:p.seed,target:p.target});return}
  if(a==='join'){
    var inp=document.getElementById('joinCode'),p2=parseCode(inp?inp.value:'');
    if(!p2){toast('That code does not look right. Check it and try again.');return}
    startGame('ten',p2.cat,{seed:p2.seed,target:p2.target});return;
  }
});
document.addEventListener('keydown',function(e){
  if(view!=='game'||!G||sheet)return;
  if(!G.locked){if(e.key==='ArrowLeft'||e.key==='1')answer(0);else if(e.key==='ArrowRight'||e.key==='2')answer(1)}
  else if((e.key==='Enter'||e.key===' ')&&G.mode!=='blitz'&&document.activeElement===document.body){e.preventDefault();if(G.done)finish();else nextQ()}
});

var lastKey=dkey();
function dayCheck(){var k=dkey();if(k!==lastKey){lastKey=k;if(view!=='game'&&view!=='result'){render()}}}
setInterval(dayCheck,15000);
document.addEventListener('visibilitychange',function(){if(!document.hidden)dayCheck()});
readHash();
render();
checkAch();
})();
</script>