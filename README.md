# MEAL-PLAN
Meal plan and shopping list
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="theme-color" content="#0f1117">
<meta name="description" content="Kiska & Paul — 6 week meal plan">
<title>Kiska &amp; Paul — 6 Week Plan</title>
<style>
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:-apple-system,'Inter',system-ui,sans-serif;background:#0f1117;color:#e8e8e4}
.hdr{background:linear-gradient(135deg,#1a4a2e,#0f2d1a 50%,#0f1117);padding:22px 20px 16px;border-bottom:1px solid #1e3a28}
.in{max-width:780px;margin:0 auto}
.hdr h1{font-size:19px;font-weight:700;color:#a8d5b8;letter-spacing:-.3px}
.hdr p{font-size:11.5px;color:#5a8a6a;margin-top:3px}
.today{margin-top:12px;background:#0f1a14;border:1px solid #2a5a3a;border-radius:10px;padding:10px 12px;display:flex;justify-content:space-between;align-items:center;gap:10px;flex-wrap:wrap}
.today-l{font-size:11px;color:#6bc489;font-weight:600}
.today-d{font-size:13px;color:#a8d5b8;font-weight:700}
.today input{background:#0a1510;border:1px solid #2a4a3a;color:#a8d5b8;border-radius:6px;padding:4px 8px;font-size:11px;font-family:inherit}
.btn-s{background:#1a4a2e;border:1px solid #4a9a6e;color:#a8d5b8;border-radius:6px;padding:4px 10px;font-size:11px;cursor:pointer;font-family:inherit}
.nav{background:#12181a;border-bottom:1px solid #1e2a22;padding:0 20px;overflow-x:auto}
.nav-in{max-width:780px;margin:0 auto;display:flex;min-width:max-content}
.nav button{background:none;border:none;cursor:pointer;padding:11px 13px;font-size:12px;font-family:inherit;color:#5a7a6a;border-bottom:2px solid transparent;white-space:nowrap}
.nav button.on{color:#6bc489;border-bottom-color:#6bc489;font-weight:600}
.main{max-width:780px;margin:0 auto;padding:18px 20px 60px}
.lbl{font-size:10.5px;color:#5a8a6a;text-transform:uppercase;letter-spacing:.8px;font-weight:600;margin-bottom:7px}
.wbtns{display:flex;gap:5px;flex-wrap:wrap;margin-bottom:5px}
.wb{background:#12181a;border:1px solid #1e2a22;border-radius:7px;padding:6px 11px;cursor:pointer;color:#5a7a6a;font-size:12px;font-family:inherit}
.wb.on{background:#1a4a2e;border-color:#4a9a6e;color:#a8d5b8;font-weight:600}
.wtheme{font-size:11.5px;color:#6bc489;font-style:italic;margin-bottom:14px}
.dbtns{display:flex;gap:5px;margin-bottom:18px}
.db{flex:1;background:#12181a;border:1px solid #1e2a22;border-radius:7px;padding:7px 3px;cursor:pointer;color:#5a7a6a;font-size:11px;font-family:inherit;text-align:center;position:relative}
.db.on{background:#1a4a2e;border-color:#4a9a6e;color:#a8d5b8;font-weight:700}
.db .dot{position:absolute;top:-3px;right:-2px;font-size:8px}
.grid{display:grid;grid-template-columns:1fr 1fr;gap:9px;margin:9px 0}
.c{border-radius:11px;padding:13px}
.c.shared{grid-column:1/-1;background:#0a1510;border:1px solid #1e2a22}
.c.k{background:#0a1510;border:1px solid #1a3a2a}
.c.p{background:#0a1018;border:1px solid #1a2a3a}
.c.taco{background:#1a1408;border:1px solid #4a3a10}
.c.deliv{background:#0a1020;border:1px solid #1a3a5a}
.c.toss{background:#0a1018;border:1px solid #1a3060}
.ch{display:flex;justify-content:space-between;align-items:flex-start;margin-bottom:5px;gap:6px}
.cl{font-size:9.5px;font-weight:600;color:#3a5a4a;text-transform:uppercase;letter-spacing:.5px}
.badges{display:flex;gap:4px;flex-shrink:0}
.bk{font-size:9.5px;background:#1a3a2a;color:#a8d5b8;border-radius:9px;padding:2px 6px;white-space:nowrap}
.bp{font-size:9.5px;background:#1a2a3a;color:#93c5fd;border-radius:9px;padding:2px 6px;white-space:nowrap}
.bpro{font-size:9.5px;background:#2a1a3a;color:#c4a8f5;border-radius:9px;padding:2px 6px;white-space:nowrap;font-weight:600}
.cn{font-size:12.5px;font-weight:600;line-height:1.3;margin-bottom:4px}
.cd{font-size:10.5px;color:#4a6a5a;line-height:1.5;margin-bottom:5px}
.rr{display:flex;align-items:center;gap:5px;flex-wrap:wrap;margin-top:4px}
.rt{font-size:9.5px;color:#3a5a4a}
.rl{border-radius:5px;padding:2px 7px;font-size:9.5px;font-weight:600;text-decoration:none;display:inline-block}
.s-bbc{background:#2a1a0a;border:1px solid #5a3a1a;color:#e07030}
.s-min{background:#1a2a1a;border:1px solid #3a5a3a;color:#6bc489}
.s-ll{background:#1a1a2a;border:1px solid #3a3a5a;color:#93c5fd}
.s-none{background:#0a1a1a;border:1px solid #1a3a3a;color:#34d399}
.s-della{background:#2a1a2a;border:1px solid #5a3a5a;color:#d08ad0}
.s-gso{background:#10242a;border:1px solid #205a66;color:#5ac8d9}
.s-tin{background:#241a10;border:1px solid #5a4020;color:#d9a05a}
.s-own{background:#1a2a20;border:1px solid #2a5a3a;color:#6bc489}
.nt{font-size:9.5px;font-style:italic;margin-top:4px;display:block}
.box{background:#0a1510;border:1px solid #1e2a22;border-radius:11px;padding:14px;margin-top:9px}
.box h3{font-size:13.5px;color:#a8d5b8;margin-bottom:10px}
.tags{display:flex;gap:5px;flex-wrap:wrap}
.tag{background:#12201a;border:1px solid #1e3228;border-radius:14px;padding:3px 9px;font-size:10.5px;color:#6bc489}
.tot{display:grid;grid-template-columns:1fr 1fr;gap:9px;margin-top:9px}
.tb{background:#12181a;border-radius:8px;padding:11px}
.tbn{font-size:11.5px;font-weight:600;margin-bottom:8px}
.mrow{margin-bottom:9px}
.mtop{display:flex;justify-content:space-between;align-items:baseline;font-size:10px;color:#5a8a6a;margin-bottom:3px}
.mval{font-size:17px;font-weight:700}
.bar{height:4px;background:#1e2a22;border-radius:2px;margin-top:3px;overflow:hidden}
.bfill{height:100%;border-radius:2px;transition:width .3s}
.ovr{background:#0a1510;border:1px solid #1e2a22;border-radius:9px;padding:11px 13px;margin-bottom:7px;cursor:pointer;display:flex;justify-content:space-between;gap:9px}
.ovr:hover{border-color:#2a4a3a}
.tip{display:flex;gap:9px;margin-bottom:11px;padding-bottom:11px;border-bottom:1px solid #1e2a22}
.tip:last-child{border:none;margin:0;padding:0}
.ti{font-size:17px;flex-shrink:0}
.tt{font-size:12.5px;font-weight:600;color:#a8d5b8;margin-bottom:2px}
.tbd{font-size:11.5px;color:#5a8a6a;line-height:1.5}
.shop{display:flex;flex-direction:column;gap:7px}
.shop label{display:flex;align-items:flex-start;gap:9px;font-size:12.5px;color:#a8d5b8;cursor:pointer;line-height:1.4}
.shop input{margin-top:2px;flex-shrink:0;width:15px;height:15px;accent-color:#6bc489;cursor:pointer}
.shop label:has(input:checked){color:#3a5a4a;text-decoration:line-through}
.prog{font-size:10.5px;color:#5a8a6a;margin-top:8px;font-style:italic}
.swaps{display:grid;grid-template-columns:1fr 1fr;gap:8px;margin-top:10px}
.swap{border-radius:9px;padding:10px}
.swap.k{background:#0d1a12;border:1px solid #1e4030}
.swap.p{background:#0b1220;border:1px solid #1c3050}
.swap-who{font-size:9.5px;font-weight:700;text-transform:uppercase;letter-spacing:.5px;margin-bottom:4px}
.swap.k .swap-who{color:#a8d5b8}
.swap.p .swap-who{color:#93c5fd}
.swap-p{font-size:12.5px;font-weight:600;color:#e8e8e4;line-height:1.3;margin-bottom:6px}
.swap-n{display:flex;gap:4px;flex-wrap:wrap}
.hide{display:none}
@media(max-width:560px){
 .grid{grid-template-columns:1fr}
 .swaps{grid-template-columns:1fr}
 .tot{grid-template-columns:1fr}
 .dbtns{flex-wrap:wrap}
 .db{flex:1 1 13%;min-width:40px}
 .today{flex-direction:column;align-items:flex-start}
 .hdr h1{font-size:17px}
}
.stamp{font-size:10px;color:#3a5a4a;text-align:center;padding:14px 0 0}
.tog{display:flex;align-items:center;gap:7px;font-size:11px;color:#5a8a6a;cursor:pointer;margin-top:8px}
.tog input{width:15px;height:15px;accent-color:#93c5fd;cursor:pointer}
.warn{background:#1a1408;border:1px solid #4a3a10;border-radius:9px;padding:11px 13px;margin-bottom:12px;font-size:11.5px;color:#c8a860;line-height:1.5}
</style>
</head>
<body>
<div class="hdr"><div class="in">
<h1>🥗 Kiska &amp; Paul — 6 Week Plan</h1>
<p>Mediterranean · High Protein · Low Carb · Tofu &amp; Tempeh Forward · Free Recipes Only</p>
<div class="today">
<div><div class="today-l">PLAN STARTS</div><input type="date" id="startDate" onchange="setStart()"></div>
<div><div class="today-l">TODAY</div><div class="today-d" id="todayLbl">—</div></div>
<div><div class="today-l">KISKA PROTEIN TARGET</div><select id="proSel" onchange="setProTarget()" style="background:#0a1510;border:1px solid #2a4a3a;color:#a8d5b8;border-radius:6px;padding:4px 8px;font-size:11px;font-family:inherit"><option value="140">140g — realistic</option><option value="160">160g — coach's target</option></select></div><button class="btn-s" onclick="jumpToday()">Jump to today</button>
</div>
</div></div>
<div class="nav"><div class="nav-in" id="navBar"></div></div>
<div class="main">
<div id="selectors">
<div class="lbl">Week</div><div class="wbtns" id="wbtns"></div><div class="wtheme" id="wtheme"></div>
<div class="lbl">Day</div><div class="dbtns" id="dbtns"></div>
</div>
<div id="content"></div>
</div>
<div class="stamp" id="stamp"></div>
<script>
const PLAN_VERSION="2026-08-17";
// ─── CONFIG ───────────────────────────────────────────────────────
const TARGETS={k:{cal:1400,pro:160,calT:1700,proT:180},p:{cal:1900,pro:170,calT:2200,proT:190}};
const DAYS=["Mon","Tue","Wed","Thu","Fri","Sat","Sun"];
const THEMES=["Greek & E. Mediterranean","Middle Eastern & Levantine","Italian & Spanish Coast","Turkish & North African","French Riviera & Provençal","Light Summer Favourites"];

// ─── STATE ────────────────────────────────────────────────────────
const SKEY="kp_mealplan_v2";
let S={start:null,ticks:{},training:{},view:"plan",week:0,day:0,proK:140};
function load(){try{const r=localStorage.getItem(SKEY);if(r)S=Object.assign(S,JSON.parse(r));}catch(e){}}
function save(){try{localStorage.setItem(SKEY,JSON.stringify(S));}catch(e){}}

// ─── RECIPE LINKS ─────────────────────────────────────────────────
function rurl(src,q){
  if(!q)return null;
  if(q.startsWith("http"))return q;
  const e=encodeURIComponent(q);
  if(src==="bbc")return"https://www.bbcgoodfood.com/search?q="+e;
  if(src==="min")return"https://minimalistbaker.com/?s="+e;
  if(src==="ll")return"https://www.loveandlemons.com/?s="+e;
  if(src==="della")return"https://deliciouslyella.com/?s="+e;
  if(src==="gso")return"https://www.gimmesomeoven.com/all-recipes/";
  if(src==="tin")return null;
  if(src==="own")return null;
  return"https://www.bbcgoodfood.com/search?q="+e;
}
const SRCN={bbc:"BBC Good Food",min:"Minimalist Baker",ll:"Love & Lemons",della:"Deliciously Ella",gso:"Gimme Some Oven",tin:"Quick Roasting Tin 📖",none:"No-Cook",own:"Your recipe"};

// ─── BREAKFASTS (shared base, same food) ─────────────────────────
const BF=[
 {n:"Greek Yoghurt Protein Bowl",d:"Greek yoghurt, berries, protein powder, walnuts",kc:340,kp:36,pc:470,pp:44},
 {n:"Scrambled Eggs & Avocado",d:"Eggs scrambled with spinach, avocado, cherry tomatoes",kc:330,kp:26,pc:480,pp:38},
 {n:"Green Protein Smoothie",d:"Spinach, protein powder, almond milk, banana, almond butter",kc:320,kp:34,pc:460,pp:42},
 {n:"Poached Eggs & Avocado",d:"Poached eggs, avocado, rocket, cucumber, lemon",kc:330,kp:24,pc:475,pp:36},
 {n:"Omelette with Feta & Veg",d:"Omelette with feta, roasted peppers, spinach",kc:335,kp:28,pc:480,pp:40},
 {n:"Protein Pancakes",d:"Banana, egg & protein powder pancakes, yoghurt, berries",kc:345,kp:34,pc:485,pp:42},
 {n:"Cottage Cheese Bowl",d:"Cottage cheese, cucumber, cherry tomatoes, seeds, olive oil",kc:310,kp:32,pc:450,pp:40},
];

// ─── FIXED SLOTS ──────────────────────────────────────────────────
const TOSS={n:"Tossed — Grilled Chicken Salad",d:"Double chicken, loads of veg, NO dressing — ask for lemon wedges. Add egg or avocado.",c:520,pr:48,toss:1};
const KALE={n:"Your Kale Salad 🥬 + edamame",d:"500g kale, red + green pepper, carrot, 100g houmous, 1 tbsp almond butter — one batch makes 2 lunches. Add 100g edamame per serving.",c:450,pr:29,kale:1,r:[15,"own","Your own recipe"]};

// ─── DINNERS: one base dish, protein swapped ─────────────────────
// dn:{n:base name, d:base description, r:[mins,src,query],
//     k:{sw:Kiska's protein, c, pr}, p:{sw:Paul's protein, c, pr}, eggs:true if both eggs}
const TACO={n:"🌮 Taco Tuesday",d:"Homemade flour tortillas, black beans, grilled peppers, onions & tomatoes, cheese, soured cream, hot sauce",
 taco:1,k:{sw:"Extra black beans + cheese",c:520,pr:36},p:{sw:"Grilled chicken or beef mince",c:760,pr:56}};
const DELIV={n:"🥡 SE Asian Delivery",d:"Your easy night — nothing to cook or shop for",
 deliv:1,k:{sw:"Tofu or edamame dish",c:480,pr:36},p:{sw:"Grilled chicken or fish",c:700,pr:52}};

const W=[
// ── WEEK 1 — Greek & E. Mediterranean ────────────────────────────
[
{b:0,lk:{n:"Houmous & Halloumi Plate",d:"Grilled halloumi, houmous, cucumber, cherry tomatoes, olives, rocket, seeds",c:400,pr:30},lp:TOSS,
 dn:{n:"Greek Salad Bowl with Roasted Veg",d:"Roasted courgette, peppers & cherry tomatoes on cucumber, olives, red onion, oregano, olive oil",r:[25,"tin","Roasted veg traybake"],
  k:{sw:"Crispy sesame tofu",c:440,pr:38},p:{sw:"Baked sea bass",c:700,pr:54}}},
{b:3,lk:KALE,lp:TOSS,dn:TACO},
{b:1,lk:{n:"Spinach & Feta Mezze Bowl",d:"Spinach, feta, cucumber, cherry tomatoes, olives, lemon oil, pumpkin seeds",c:380,pr:28},lp:TOSS,dn:DELIV},
{b:4,lk:{n:"Lentil & Cucumber Salad",d:"Puy lentils, cucumber, mint, parsley, lemon dressing, crumbled feta",c:390,pr:30},lp:TOSS,
 dn:{n:"Shakshuka with Feta",d:"Eggs poached in spiced tomato & pepper sauce, wilted spinach, crumbled feta — one pan",r:[20,"gso","https://www.gimmesomeoven.com/proteins/egg-recipes/"],eggs:1,
  k:{sw:"3 eggs + feta",c:430,pr:34},p:{sw:"5 eggs + extra feta",c:690,pr:52}}},
{b:2,lk:KALE,lp:TOSS,
 dn:{n:"Souvlaki Skewers with Tzatziki",d:"Oregano, lemon & garlic marinated skewers, tzatziki, rocket & tomato salad",r:[25,"bbc","souvlaki skewers"],
  k:{sw:"Marinated tempeh",c:450,pr:40},p:{sw:"Chicken thigh",c:700,pr:56}}},
{b:5,lk:{n:"Watermelon & Feta Salad",d:"Watermelon, feta, mint, cucumber, pumpkin seeds, lime",c:360,pr:26},lp:TOSS,
 dn:{n:"Courgette Fritters with Green Salad",d:"Grated courgette fritters, big rocket & tomato salad, lemon yoghurt",r:[20,"bbc","courgette fritters"],
  k:{sw:"Halloumi in the fritters",c:450,pr:36},p:{sw:"Fritters + grilled chicken",c:710,pr:56}}},
{b:6,lk:{n:"Roasted Pepper & Houmous Bowl",d:"Roasted red peppers, houmous, olives, rocket, seeds, lemon oil",c:380,pr:28},lp:TOSS,
 dn:{n:"Miso Bowl with Edamame",d:"Edamame, shredded carrot, cucumber, spring onion, sesame, miso dressing",r:[15,"gso","https://www.gimmesomeoven.com/proteins/tofu-recipes/"],
  k:{sw:"Silken tofu",c:430,pr:38},p:{sw:"Grilled cod",c:680,pr:54}}},
],
// ── WEEK 2 — Middle Eastern & Levantine ──────────────────────────
[
{b:1,lk:{n:"Fattoush with Halloumi",d:"Grilled halloumi, cucumber, tomato, radish, parsley, sumac, lemon",c:410,pr:30,r:[15,"gso","https://www.gimmesomeoven.com/fattoush-salad/"]},lp:TOSS,
 dn:{n:"Shawarma-Spiced Bowl",d:"Warm spices, cucumber, tomato, parsley, tahini drizzle, pickled onion — no pitta",r:[25,"gso","https://www.gimmesomeoven.com/proteins/chicken-recipes/"],
  k:{sw:"Crispy tempeh",c:450,pr:40},p:{sw:"Chicken breast",c:700,pr:56}}},
{b:3,lk:KALE,lp:TOSS,dn:TACO},
{b:4,lk:{n:"Tabbouleh with Feta",d:"Parsley, mint, tomato, cucumber, lemon, olive oil, crumbled feta",c:380,pr:28},lp:TOSS,dn:DELIV},
{b:0,lk:{n:"Spinach & Chickpea Salad",d:"Baby spinach, chickpeas, roasted peppers, tahini dressing, pomegranate",c:400,pr:30},lp:TOSS,
 dn:{n:"Za'atar Roasted Aubergine",d:"Aubergine roasted with za'atar, thick yoghurt, mint, pomegranate, pine nuts",r:[25,"tin","Aubergine traybake"],
  k:{sw:"Chickpeas + extra yoghurt",c:440,pr:36},p:{sw:"Chicken thighs",c:700,pr:55}}},
{b:2,lk:KALE,lp:TOSS,
 dn:{n:"Ginger Garlic Stir-Fry",d:"Pak choi, broccoli, spring onion, soy, ginger, garlic, sesame — over shredded cabbage",r:[20,"min","https://minimalistbaker.com/quick-easy-crispy-tofu/"],
  k:{sw:"Firm tofu",c:440,pr:38},p:{sw:"Cod fillet",c:680,pr:54}}},
{b:5,lk:{n:"Cucumber & Feta Mezze Bowl",d:"Feta, cucumber, cherry tomatoes, olives, dolmades, lemon oil",c:390,pr:28},lp:TOSS,
 dn:{n:"Stuffed Peppers",d:"Peppers stuffed with quinoa, spinach, pine nuts, herbs, lemon",r:[30,"ll","stuffed peppers"],
  k:{sw:"Feta + extra quinoa",c:450,pr:34},p:{sw:"Turkey mince",c:700,pr:56}}},
{b:6,lk:{n:"Houmous & Roasted Veg Plate",d:"Houmous, roasted courgette, peppers, cherry tomatoes, rocket, seeds",c:380,pr:28},lp:TOSS,
 dn:{n:"Burrata, Tomato & Basil",d:"Burrata, heirloom tomatoes, basil, olive oil, sea salt — no cooking at all",r:[8,"none","caprese"],
  k:{sw:"Warm edamame",c:450,pr:36},p:{sw:"King prawns",c:690,pr:54}}},
],
// ── WEEK 3 — Italian & Spanish Coast ─────────────────────────────
[
{b:3,lk:{n:"Rocket, Parmesan & Egg Salad",d:"Rocket, parmesan, boiled eggs, toasted pine nuts, lemon, avocado",c:400,pr:30},lp:TOSS,
 dn:{n:"Italian Herb Panzanella (no bread)",d:"Heirloom tomatoes, cucumber, basil, capers, red onion, red wine vinegar, olive oil",r:[30,"min","https://minimalistbaker.com/italian-herb-crispy-baked-tofu/"],
  k:{sw:"Herb-baked crispy tofu",c:445,pr:38},p:{sw:"Chicken breast",c:700,pr:56}}},
{b:1,lk:KALE,lp:TOSS,dn:TACO},
{b:4,lk:{n:"Italian Lentil Salad",d:"Puy lentils, sun-dried tomatoes, basil, parmesan, pine nuts, rocket",c:400,pr:30},lp:TOSS,dn:DELIV},
{b:0,lk:{n:"Burrata & Peach Salad",d:"Burrata, white peach, rocket, walnuts, basil oil",c:395,pr:28},lp:TOSS,
 dn:{n:"Spinach & Ricotta Frittata",d:"Frittata with spinach, ricotta, lemon zest — big tomato salad alongside",r:[20,"bbc","spinach ricotta frittata"],eggs:1,
  k:{sw:"3 eggs + ricotta",c:430,pr:34},p:{sw:"5 eggs + parmesan",c:690,pr:52}}},
{b:2,lk:KALE,lp:TOSS,
 dn:{n:"Tomato & Herb Ragu on Courgette Noodles",d:"Slow-blistered tomato, garlic and herb ragu over spiralised courgette — no pasta",r:[25,"della","ragu"],
  k:{sw:"Tempeh crumbles",c:450,pr:40},p:{sw:"King prawns",c:690,pr:54}}},
{b:5,lk:{n:"Niçoise-Style Egg Salad",d:"Boiled eggs, green beans, olives, tomatoes, capers, lemon oil",c:390,pr:30},lp:TOSS,
 dn:{n:"Baked Feta & Cherry Tomatoes",d:"Feta baked in cherry tomatoes with oregano and olives, rocket alongside",r:[20,"gso","https://www.gimmesomeoven.com/dietary/vegetarian/"],
  k:{sw:"Edamame stirred through",c:450,pr:36},p:{sw:"Grilled chicken",c:700,pr:56}}},
{b:6,lk:{n:"Gazpacho with Feta & Avocado",d:"Chilled gazpacho, crumbled feta, cucumber, avocado on the side",c:380,pr:26},lp:TOSS,
 dn:{n:"All'Acqua Pazza",d:"Poached in cherry tomatoes, garlic, white wine, parsley and chilli",r:[20,"bbc","acqua pazza"],
  k:{sw:"Butter beans",c:430,pr:34},p:{sw:"Sea bass",c:680,pr:54}}},
],
// ── WEEK 4 — Turkish & North African ─────────────────────────────
[
{b:0,lk:{n:"Turkish Shepherd's Salad",d:"Fine-diced cucumber, tomato, red onion, parsley, pomegranate molasses, feta",c:375,pr:28},lp:TOSS,
 dn:{n:"Menemen",d:"Eggs folded through spiced tomatoes, green peppers and cumin — one pan, rocket alongside",r:[20,"bbc","menemen"],eggs:1,
  k:{sw:"3 eggs + feta",c:425,pr:34},p:{sw:"5 eggs + extra feta",c:685,pr:52}}},
{b:3,lk:KALE,lp:TOSS,dn:TACO},
{b:4,lk:{n:"Moroccan Carrot & Chickpea Salad",d:"Roasted carrots, chickpeas, cumin, harissa yoghurt, coriander, lemon",c:395,pr:28},lp:TOSS,dn:DELIV},
{b:1,lk:{n:"Lentil & Roasted Pepper Salad",d:"Green lentils, roasted peppers, cumin, coriander, lemon, feta",c:400,pr:30},lp:TOSS,
 dn:{n:"Aubergine with Tahini & Pomegranate",d:"Roasted aubergine, tahini sauce, pomegranate, pine nuts, fresh herbs",r:[25,"tin","Aubergine traybake"],
  k:{sw:"Chickpeas",c:440,pr:36},p:{sw:"Chicken thighs",c:700,pr:55}}},
{b:2,lk:KALE,lp:TOSS,
 dn:{n:"Chermoula with Roasted Cauliflower",d:"Moroccan herb, lemon and cumin sauce over roasted cauliflower, rocket",r:[30,"tin","Cauliflower traybake"],
  k:{sw:"Crispy tofu",c:450,pr:38},p:{sw:"Sea bass",c:690,pr:54}}},
{b:5,lk:{n:"Fattoush with Halloumi & Sumac",d:"Halloumi, lettuce, tomato, cucumber, radish, mint, sumac dressing",c:415,pr:30,r:[15,"gso","https://www.gimmesomeoven.com/fattoush-salad/"]},lp:TOSS,
 dn:{n:"Spiced Chickpea & Spinach Stew",d:"Chickpeas, spinach, tomato, cumin, coriander, lemon — one pot",r:[25,"della","chickpea stew"],
  k:{sw:"Extra chickpeas + yoghurt",c:440,pr:34},p:{sw:"Cod chunks stirred in",c:690,pr:54}}},
{b:6,lk:{n:"Whipped Feta & Roast Veg Bowl",d:"Whipped feta, roasted aubergine, peppers, cherry tomatoes, herbs",c:400,pr:28},lp:TOSS,
 dn:{n:"Mezze Plate",d:"Houmous, cucumber, olives, cherry tomatoes, feta, flatbread-free — no cooking",r:[8,"none","mezze platter"],
  k:{sw:"Warm edamame",c:450,pr:36},p:{sw:"Grilled prawns",c:690,pr:54}}},
],
// ── WEEK 5 — French Riviera & Provençal ──────────────────────────
[
{b:1,lk:{n:"Salade Niçoise (no fish)",d:"Boiled eggs, green beans, olives, tomatoes, cucumber, capers, lemon oil",c:390,pr:30},lp:TOSS,
 dn:{n:"Ratatouille with Goat's Cheese",d:"Provençal ratatouille — courgette, aubergine, peppers, tomato, thyme — goat's cheese, basil",r:[30,"della","ratatouille"],
  k:{sw:"Tempeh stirred through",c:455,pr:40},p:{sw:"Chicken thighs",c:700,pr:55}}},
{b:3,lk:KALE,lp:TOSS,dn:TACO},
{b:4,lk:{n:"Fennel & Orange Salad",d:"Shaved fennel, orange segments, olives, rocket, lemon oil, feta",c:375,pr:26},lp:TOSS,dn:DELIV},
{b:0,lk:{n:"Egg & Asparagus Salad",d:"Soft boiled eggs, asparagus, shaved parmesan, lemon oil, rocket",c:385,pr:30},lp:TOSS,
 dn:{n:"Omelette aux Fines Herbes",d:"Classic French herb omelette, green salad, shallot vinaigrette",r:[10,"bbc","french omelette"],eggs:1,
  k:{sw:"3 eggs + herbs",c:420,pr:32},p:{sw:"5 eggs + gruyère",c:685,pr:52}}},
{b:2,lk:KALE,lp:TOSS,
 dn:{n:"Niçoise Bowl",d:"Green beans, olives, cherry tomatoes, capers, boiled egg, shallot vinaigrette",r:[30,"min","https://minimalistbaker.com/quick-easy-crispy-tofu/"],
  k:{sw:"Crispy tofu",c:455,pr:38},p:{sw:"Seared tuna",c:690,pr:56}}},
{b:5,lk:{n:"Warm Goat's Cheese Salad",d:"Warm goat's cheese, walnuts, rocket, beetroot, honey-mustard dressing",c:400,pr:28},lp:TOSS,
 dn:{n:"Provençal Stuffed Tomatoes",d:"Beef tomatoes stuffed with basil, garlic, parmesan and herbs — green salad",r:[20,"ll","stuffed tomatoes"],
  k:{sw:"White beans",c:435,pr:34},p:{sw:"Turkey mince",c:700,pr:56}}},
{b:6,lk:{n:"Roasted Pepper & Feta Bowl",d:"Roasted peppers, feta, capers, olive oil, rocket, seeds",c:385,pr:28},lp:TOSS,
 dn:{n:"Courgette Ribbons with Pesto",d:"Raw ribbon courgette, light pesto, lemon, pine nuts — no cooking",r:[8,"none","courgette ribbon salad"],
  k:{sw:"Burrata + edamame",c:455,pr:36},p:{sw:"Sea bass",c:690,pr:54}}},
],
// ── WEEK 6 — Light Summer Favourites ─────────────────────────────
[
{b:3,lk:{n:"Mango, Avocado & Halloumi Salad",d:"Grilled halloumi, mango, avocado, rocket, lime, chilli, coriander",c:420,pr:30},lp:TOSS,
 dn:{n:"Mango & Pak Choi Stir-Fry",d:"Mango, pak choi, spring onion, soy, ginger, sesame — over shredded cabbage",r:[25,"min","https://minimalistbaker.com/easy-baked-tempeh/"],
  k:{sw:"Marinated tempeh",c:455,pr:40},p:{sw:"Chicken breast",c:700,pr:56}}},
{b:1,lk:KALE,lp:TOSS,dn:TACO},
{b:4,lk:{n:"Rainbow Salad with Tahini",d:"Shredded red cabbage, carrot, cucumber, edamame, avocado, tahini",c:410,pr:30},lp:TOSS,dn:DELIV},
{b:0,lk:{n:"Peach, Feta & Rocket Salad",d:"White peach, feta, rocket, toasted pecans, basil, lemon oil",c:385,pr:26},lp:TOSS,
 dn:{n:"Courgette, Pea & Mint Frittata",d:"Frittata with courgette, peas, mint and ricotta — tomato & rocket salad",r:[20,"bbc","courgette frittata"],eggs:1,
  k:{sw:"3 eggs + ricotta",c:425,pr:34},p:{sw:"5 eggs + parmesan",c:690,pr:52}}},
{b:2,lk:KALE,lp:TOSS,
 dn:{n:"Summer Sesame Bowl",d:"Edamame, shredded carrot, cucumber, avocado, spring onion, sesame dressing",r:[25,"min","https://minimalistbaker.com/quick-easy-crispy-tofu/"],
  k:{sw:"Crispy tofu",c:460,pr:40},p:{sw:"Sea bass",c:690,pr:54}}},
{b:5,lk:{n:"Tomato & Burrata Salad",d:"Heirloom tomatoes, burrata, basil, toasted pine nuts, olive oil",c:400,pr:28},lp:TOSS,
 dn:{n:"Caesar-Style Salad (no croutons)",d:"Romaine, parmesan, anchovy-lemon dressing, black pepper — no croutons",r:[15,"gso","https://www.gimmesomeoven.com/courses/salad/"],
  k:{sw:"Grilled halloumi",c:450,pr:36},p:{sw:"Grilled chicken",c:700,pr:56}}},
{b:6,lk:{n:"Avocado & Egg Salad",d:"Avocado, hard boiled eggs, cucumber, cherry tomatoes, seeds, lemon",c:390,pr:30},lp:TOSS,
 dn:{n:"Greek Mezze Finale",d:"Houmous, dolmades, tzatziki, olives, cucumber, big salad — you made it!",r:[15,"none","mezze platter"],
  k:{sw:"Grilled halloumi + edamame",c:460,pr:38},p:{sw:"Chicken souvlaki",c:700,pr:56}}},
],
];
// ─── PANTRY STAPLES (buy once, check occasionally) ───────────────
const PANTRY=[
 {t:"Oils, Vinegars & Sauces",i:["Extra virgin olive oil (large)","Sesame oil","Soy sauce or tamari","Red wine vinegar","Hot sauce (Cholula / Valentina)","Dijon mustard","Pomegranate molasses"]},
 {t:"Jars & Tins",i:["Tahini (large jar)","Capers","Olives (large jar)","Harissa paste","Tinned chopped tomatoes × 6","Chickpeas × 4 tins","Black beans × 6 tins (Taco Tuesdays)","White beans × 2 tins","Miso paste"]},
 {t:"Dry Goods",i:["Plain flour (tortillas — 2kg)","Baking powder","Puy / green lentils","Quinoa","Pine nuts","Walnuts","Pecans","Almonds & cashews (snacking)","Pumpkin seeds","Mixed seeds","Sesame seeds"]},
 {t:"Spices",i:["Ground cumin","Ground coriander","Smoked paprika","Sweet paprika","Dried oregano","Za'atar","Sumac","Ras el hanout","Herbes de Provence","Cinnamon","Chilli flakes","Sea salt & black pepper"]},
 {t:"Freezer",i:["Edamame (several bags — your protein secret weapon)","Peas","Mixed berries (breakfasts)"]},
 {t:"Supplements & Snacks",i:["Protein powder (bulk tub)","Protein bars (bulk box)","Almond milk (long-life × 4)"]},
];

// ─── TACO TUESDAY (same every week) ──────────────────────────────
const TACO_SHOP=["Red peppers × 2 (grilling)","White onions × 2 (grilling)","Large tomatoes × 2 (grilling)","Grated cheddar or Mexican blend × 1 bag","Soured cream × 1 tub","Fresh coriander × 1 bunch","Lime × 2"];

// ─── WEEKLY FRESH SHOPPING ───────────────────────────────────────
const SHOP=[
// W1
{fresh:[
 {t:"🥬 Produce",i:["Rocket × 3 bags","Baby spinach × 2 bags","Cucumber × 6","Cherry tomatoes × 3 punnets","Courgettes × 3","Red peppers × 3 (+2 in taco list)","Red onion × 2","Watermelon × 1 small","Avocado × 4","Carrots × 2","Pak choi × 1","Spring onions × 1 bunch","Lemons × 6","Garlic × 1 bulb","Fresh ginger × 1 piece","Mint × 1 bunch","Parsley × 1 bunch","Dill × 1 bunch"]},
 {t:"🧀 Dairy & Eggs",i:["Eggs × 12","Halloumi × 2 packs","Feta × 2 blocks","Greek yoghurt (large) × 2","Cottage cheese × 1 tub","Tzatziki × 1 tub"]},
 {t:"🌱 Kiska — Protein Swaps Only",i:["Firm tofu × 2 packs","Silken tofu × 1 pack","Tempeh × 1 pack","Pre-cooked puy lentils × 1 pack"]},
 {t:"🍗 Paul — Protein Swaps Only",i:["Sea bass fillets × 2","Cod fillets × 2","Chicken thighs × 4","Sirloin steak × 2"]},
 {t:"🧆 Deli",i:["Houmous (large) × 1"]},
]},
// W2
{fresh:[
 {t:"🥬 Produce",i:["Rocket × 2 bags","Baby spinach × 2 bags","Cucumber × 6","Cherry tomatoes × 3 punnets","Radishes × 1 bunch","Aubergines × 2","Courgettes × 2","Red peppers × 3 (+2 taco)","Pak choi × 2","Broccoli × 1 head","Mango × 1","Avocado × 2","Pomegranate seeds × 1 pot","Red onion × 2","Lemons × 6","Garlic × 1 bulb","Mint × 1 bunch","Parsley × 2 bunches","Coriander × 1 bunch","Basil × 1 bunch"]},
 {t:"🧀 Dairy & Eggs",i:["Eggs × 14","Halloumi × 1 pack","Feta × 2 blocks","Burrata × 1 ball","Greek yoghurt (large) × 2"]},
 {t:"🌱 Kiska — Protein Swaps Only",i:["Tempeh × 2 packs","Firm tofu × 1 pack"]},
 {t:"🍗 Paul — Protein Swaps Only",i:["Chicken breast × 2","Cod fillets × 2","Turkey mince × 1 pack","King prawns (cooked) × 1 pack"]},
 {t:"🧆 Deli",i:["Houmous (large) × 1","Dolmades × 1 tin"]},
]},
// W3
{fresh:[
 {t:"🥬 Produce",i:["Rocket × 3 bags","Baby spinach × 1 bag","Cucumber × 4","Cherry tomatoes × 2 punnets","Heirloom tomatoes × 2 punnets","Courgettes × 5 (incl. spiralising)","Aubergine × 1","Green beans × 2 packs","White peaches × 2","Red peppers × 2 (taco)","Red onion × 2","Avocado × 2","Peas (fresh or frozen)","Lemons × 6","Garlic × 1 bulb","Basil × 2 bunches","Parsley × 1 bunch","Mint × 1 bunch"]},
 {t:"🧀 Dairy & Eggs",i:["Eggs × 16","Burrata × 1 ball","Feta × 1 block","Ricotta × 2 tubs","Parmesan × 1 piece","Greek yoghurt (large) × 2"]},
 {t:"🌱 Kiska — Protein Swaps Only",i:["Firm tofu × 2 packs","Tempeh × 1 pack"]},
 {t:"🍗 Paul — Protein Swaps Only",i:["Chicken breast × 4","Swordfish steaks × 2","King prawns (raw) × 1 pack","Sea bass fillets × 2"]},
 {t:"🧆 Deli",i:["Sun-dried tomatoes × 1 jar","Gazpacho × 1 carton (or make)"]},
]},
// W4
{fresh:[
 {t:"🥬 Produce",i:["Rocket × 2 bags","Baby spinach × 2 bags","Cucumber × 6","Cherry tomatoes × 2 punnets","Aubergines × 3","Cauliflower × 1","Carrots × 4","Radishes × 1 bunch","Little gem lettuce × 2","Red peppers × 3 (+2 taco)","Red onion × 2","Pomegranate seeds × 1 pot","Lemons × 6","Garlic × 1 bulb","Mint × 1 bunch","Parsley × 2 bunches","Coriander × 2 bunches"]},
 {t:"🧀 Dairy & Eggs",i:["Eggs × 12","Halloumi × 2 packs","Feta × 2 blocks","Greek yoghurt (large) × 2"]},
 {t:"🌱 Kiska — Protein Swaps Only",i:["Tempeh × 2 packs","Firm tofu × 1 pack"]},
 {t:"🍗 Paul — Protein Swaps Only",i:["Chicken breast × 2","Sea bass fillets × 2","King prawns (raw) × 1 pack"]},
 {t:"🧆 Deli",i:["Houmous (large) × 1"]},
]},
// W5
{fresh:[
 {t:"🥬 Produce",i:["Rocket × 3 bags","Cucumber × 4","Cherry tomatoes × 3 punnets","Beef tomatoes × 4 (stuffing)","Courgettes × 4","Aubergines × 3","Red peppers × 3 (+2 taco)","Green beans × 2 packs","Asparagus × 1 bunch","Fennel × 1 bulb","Oranges × 2","Cooked beetroot × 1 pack","Shallots × 4","Red onion × 1","Lemons × 6","Garlic × 1 bulb","Basil × 2 bunches","Tarragon × 1 bunch","Parsley × 1 bunch","Thyme × 1 bunch"]},
 {t:"🧀 Dairy & Eggs",i:["Eggs × 16","Burrata × 1 ball","Goat's cheese × 2 logs","Feta × 1 block","Parmesan × 1 piece","Greek yoghurt (large) × 2"]},
 {t:"🌱 Kiska — Protein Swaps Only",i:["Tempeh × 2 packs","Firm tofu × 1 pack"]},
 {t:"🍗 Paul — Protein Swaps Only",i:["Chicken breast × 4","Sirloin steak × 2","Cod fillets × 2","Sea bass fillets × 2"]},
 {t:"🧆 Deli",i:["Pesto × 1 small jar","Anchovies × 1 tin (optional)"]},
]},
// W6
{fresh:[
 {t:"🥬 Produce",i:["Rocket × 2 bags","Romaine lettuce × 2","Cucumber × 5","Cherry tomatoes × 2 punnets","Heirloom tomatoes × 2 punnets","Courgettes × 3","Carrots × 4","Red cabbage × 1 small","Pak choi × 2","Mangoes × 3","White peaches × 2","Avocado × 4","Red peppers × 2 (taco)","Red onion × 1","Spring onions × 1 bunch","Lemons × 5","Limes × 3","Garlic × 1 bulb","Fresh ginger × 1 piece","Coriander × 2 bunches","Basil × 1 bunch","Mint × 1 bunch"]},
 {t:"🧀 Dairy & Eggs",i:["Eggs × 14","Halloumi × 2 packs","Feta × 1 block","Burrata × 1 ball","Ricotta × 1 tub","Parmesan × 1 piece","Greek yoghurt (large) × 2","Tzatziki × 1 tub"]},
 {t:"🌱 Kiska — Protein Swaps Only",i:["Tempeh × 2 packs","Firm tofu × 1 pack"]},
 {t:"🍗 Paul — Protein Swaps Only",i:["Chicken thighs × 4","Chicken breast × 2","Turkey mince × 1 pack","Sea bass fillets × 2"]},
 {t:"🧆 Deli",i:["Houmous (large) × 1","Dolmades × 1 tin"]},
]},
];

// ─── SNACK OPTIONS ────────────────────────────────────────────────
const SNACKS=[
 {n:"Protein shake",c:150,pr:30},{n:"Edamame, 100g",c:120,pr:11},
 {n:"Protein bar",c:200,pr:20},{n:"Skyr / Fage pot",c:130,pr:15},
 {n:"2 boiled eggs",c:140,pr:12},{n:"Almonds, 25g",c:150,pr:6},
 {n:"Cottage cheese, 100g",c:100,pr:12},
];
// ─── DATE LOGIC ───────────────────────────────────────────────────
function todayISO(){const d=new Date();return d.getFullYear()+"-"+String(d.getMonth()+1).padStart(2,"0")+"-"+String(d.getDate()).padStart(2,"0");}
function getStart(){if(!S.start){ // default: Monday of current week
  const d=new Date();const dow=(d.getDay()+6)%7;d.setDate(d.getDate()-dow);
  S.start=d.getFullYear()+"-"+String(d.getMonth()+1).padStart(2,"0")+"-"+String(d.getDate()).padStart(2,"0");save();}
 return S.start;}
function dayIndexFromStart(){
  const s=new Date(getStart()+"T00:00:00");const t=new Date(todayISO()+"T00:00:00");
  return Math.floor((t-s)/86400000);}
function currentSlot(){
  const n=dayIndexFromStart();
  if(n<0)return{w:0,d:0,pre:true,n};
  if(n>41)return{w:5,d:6,post:true,n};
  return{w:Math.floor(n/7),d:n%7,n};}
function setStart(){S.start=document.getElementById("startDate").value;save();jumpToday();}
function setProTarget(){S.proK=+document.getElementById("proSel").value;save();renderAll();}
function jumpToday(){const c=currentSlot();S.week=c.w;S.day=c.d;S.view="plan";save();renderAll();}

// ─── RENDER HELPERS ───────────────────────────────────────────────
function isTraining(w,d,who){return !!S.training[who+"_"+w+"_"+d];}
function toggleTraining(w,d,who){const k=who+"_"+w+"_"+d;S.training[k]=!S.training[k];save();renderMain();}
function tgt(who,w,d){const T=TARGETS[who];const tr=isTraining(w,d,who);
  let pro=tr?T.proT:T.pro;
  if(who==="k"){pro=S.proK; if(tr)pro+=20;}
  return{cal:tr?T.calT:T.cal,pro,tr};}

function recipeRow(m){
  if(!m.r||m.deliv||m.taco)return"";
  const[mins,src,q]=m.r;
  const u=rurl(src,q);
  const tag=u?`<a class="rl s-${src}" href="${u}" target="_blank" rel="noopener">${SRCN[src]} ↗</a>`
             :`<span class="rl s-${src}" title="${q}">${SRCN[src]}</span>`;
  const hint=(!u&&src==="tin")?`<span class="rt" style="color:#8a6a3a">— ${q}</span>`:"";
  return `<div class="rr"><span class="rt">⏱ ${mins} min</span>${tag}${hint}</div>`;
}
function card(m,who,emoji,label,isBf){
  const cls=m.taco?"taco":m.deliv?"deliv":m.toss?"toss":isBf?"shared":who;
  let col=isBf?"#e8e8e4":who==="k"?"#a8d5b8":"#93c5fd";
  if(m.taco)col="#f5c842";if(m.deliv)col="#60c8f5";if(m.kale)col="#6bc489";
  const badges=isBf
    ?`<span class="bk">${m.kc} · ${m.kp}g</span><span class="bp">${m.pc} · ${m.pp}g</span>`
    :`<span class="${who==="k"?"bk":"bp"}">${m.c} kcal</span><span class="bpro">${m.pr}g</span>`;
  const sub=isBf?"":`<span style="font-size:9.5px;font-weight:600;color:${col};margin-left:5px">${who==="k"?"Kiska 🌿":"Paul 🍖"}</span>`;
  return `<div class="c ${cls}" style="grid-column:${isBf?"1/-1":"auto"}">
   <div class="ch"><div><span class="cl">${emoji} ${label}</span>${sub}</div><div class="badges">${badges}</div></div>
   <div class="cn" style="color:${col}">${m.n}</div><div class="cd">${m.d}</div>${recipeRow(m)}
   ${m.taco?'<span class="nt" style="color:#a07820">⚠️ Higher-carb night — go easy on tortillas</span>':""}
   ${m.deliv?'<span class="nt" style="color:#3a7aaa">🥡 No cooking tonight</span>':""}
   ${m.toss?'<span class="nt" style="color:#3a6aaa">🥗 Bought out — nothing to shop for</span>':""}
   ${m.kale?'<span class="nt" style="color:#4a9a5a">🥬 Your own recipe</span>':""}</div>`;
}
function dinnerCard(dn){
  const cls=dn.taco?"taco":dn.deliv?"deliv":"shared";
  let col=dn.taco?"#f5c842":dn.deliv?"#60c8f5":"#e8e8e4";
  const eggNote=dn.eggs?'<span class="nt" style="color:#c8a860">🥚 Egg night — you\'re both eating the same thing</span>':"";
  return `<div class="c ${cls}" style="grid-column:1/-1">
   <div class="ch"><div><span class="cl">🌙 Dinner · one base dish</span></div></div>
   <div class="cn" style="color:${col}">${dn.n}</div>
   <div class="cd">${dn.d}</div>
   ${recipeRow(dn)}
   <div class="swaps">
     <div class="swap k">
       <div class="swap-who">Kiska 🌿</div>
       <div class="swap-p">${dn.k.sw}</div>
       <div class="swap-n"><span class="bk">${dn.k.c} kcal</span><span class="bpro">${dn.k.pr}g</span></div>
     </div>
     <div class="swap p">
       <div class="swap-who">Paul 🍖</div>
       <div class="swap-p">${dn.p.sw}</div>
       <div class="swap-n"><span class="bp">${dn.p.c} kcal</span><span class="bpro">${dn.p.pr}g</span></div>
     </div>
   </div>
   ${eggNote}
   ${dn.taco?'<span class="nt" style="color:#a07820">⚠️ Higher-carb night — go easy on tortillas</span>':""}
   ${dn.deliv?'<span class="nt" style="color:#3a7aaa">🥡 No cooking tonight</span>':""}</div>`;
}
function meter(lbl,val,target,col,unit){
  const pct=Math.min(100,Math.round(val/target*100));
  const short=target-val;
  const good=val>=target*0.92;
  return `<div class="mrow"><div class="mtop"><span>${lbl}</span><span style="color:${good?"#6bc489":"#c8a860"}">${pct}%</span></div>
   <div class="mval" style="color:${col}">${val}<span style="font-size:10px;color:#5a8a6a;font-weight:400"> / ${target}${unit}</span></div>
   <div class="bar"><div class="bfill" style="width:${pct}%;background:${good?col:"#c8a860"}"></div></div>
   ${!good&&short>0?`<div style="font-size:9.5px;color:#c8a860;margin-top:3px">${short}${unit} short — add a snack</div>`:""}</div>`;
}

// ─── VIEWS ────────────────────────────────────────────────────────
function viewPlan(){
  const day=W[S.week][S.day],bf=BF[day.b],dn=day.dn;
  const kT=tgt("k",S.week,S.day),pT=tgt("p",S.week,S.day);
  const kc=bf.kc+day.lk.c+dn.k.c, kp=bf.kp+day.lk.pr+dn.k.pr;
  const pc=bf.pc+day.lp.c+dn.p.c, pp=bf.pp+day.lp.pr+dn.p.pr;
  return `
  ${card(bf,null,"🌅","Breakfast · shared",true)}
  <div class="grid">${card(day.lk,"k","☀️","Lunch")}${card(day.lp,"p","☀️","Lunch")}</div>
  ${dinnerCard(dn)}
  <div class="box"><h3>📊 Running Totals — meals only</h3>
   <div class="tot">
    <div class="tb"><div class="tbn" style="color:#a8d5b8">Kiska ${kT.tr?"⚡":""}</div>
      ${meter("Protein",kp,kT.pro,"#c4a8f5","g")}${meter("Calories",kc,kT.cal,"#a8d5b8","")}
      <label class="tog"><input type="checkbox" ${kT.tr?"checked":""} onchange="toggleTraining(${S.week},${S.day},'k')"> Training day</label></div>
    <div class="tb"><div class="tbn" style="color:#93c5fd">Paul ${pT.tr?"⚡":""}</div>
      ${meter("Protein",pp,pT.pro,"#c4a8f5","g")}${meter("Calories",pc,pT.cal,"#93c5fd","")}
      <label class="tog"><input type="checkbox" ${pT.tr?"checked":""} onchange="toggleTraining(${S.week},${S.day},'p')"> Training day</label></div>
   </div>
   <div class="prog">Protein is the number that matters most. Meals alone won't hit target — close the gap with snacks below.</div>
  </div>
  <div class="box"><h3>🍎 Snacks — close the protein gap</h3>
   <div class="tags">${SNACKS.map(s=>`<span class="tag">${s.n} · ${s.pr}g · ${s.c}kcal</span>`).join("")}</div>
   <div class="prog">A daily protein shake plus one other snack covers roughly 40–50g.</div>
  </div>`;
}
function viewOverview(){
  let h=`<div class="box" style="margin-top:0"><h3>Week ${S.week+1}: ${THEMES[S.week]}</h3><div class="tbd">One base dish each night — only the protein changes. Tap a day to open it.</div></div>`;
  W[S.week].forEach((day,i)=>{
    const bf=BF[day.b],dn=day.dn;
    const kp=bf.kp+day.lk.pr+dn.k.pr, pp=bf.pp+day.lp.pr+dn.p.pr;
    h+=`<div class="ovr" onclick="goDay(${i})"><div style="flex:1">
     <div style="font-size:11.5px;font-weight:700;color:#6bc489;margin-bottom:3px">${DAYS[i]}
      <span style="font-weight:400;color:#7a5aa8;margin-left:6px">🌿 ${kp}g · 🍖 ${pp}g</span></div>
     <div style="font-size:10.5px;color:#a8d5b8;margin:1px 0">🌅 ${bf.n}</div>
     <div style="font-size:10.5px;color:#5a8a6a;margin:1px 0">☀️ ${day.lk.n} / Tossed</div>
     <div style="font-size:11px;color:#e8e8e4;margin:2px 0 1px"><b>🌙 ${dn.n}</b></div>
     <div style="font-size:10px;color:#6a8a7a">${dn.k.sw} <span style="color:#3a5a4a">|</span> ${dn.p.sw}</div>
    </div><span style="font-size:17px;color:#2a4a3a">›</span></div>`;});
  return h;
}
function tickKey(scope,i,j){return scope+"_"+i+"_"+j;}
function toggleTick(k){S.ticks[k]=!S.ticks[k];save();renderMain();}
function shopSection(sec,scope,si){
  let done=0;
  const rows=sec.i.map((item,ii)=>{
    const k=tickKey(scope+si,ii,0);const on=!!S.ticks[k];if(on)done++;
    return `<label><input type="checkbox" ${on?"checked":""} onchange="toggleTick('${k}')"> ${item}</label>`;}).join("");
  return `<div class="box"><h3>${sec.t} <span style="font-weight:400;color:#5a8a6a;font-size:11px">${done}/${sec.i.length}</span></h3><div class="shop">${rows}</div></div>`;
}
function viewShop(wi){
  const s=SHOP[wi];
  let h=`<div class="box" style="margin-top:0"><h3>🛒 Week ${wi+1} — Fresh Shop</h3>
   <div class="tbd">You now cook <b>one base dish</b> each night, so the vegetables below feed you both — no doubling up.
   The only split is the protein: tofu and tempeh for Kiska, chicken and fish for Paul.<br><br>
   Pantry staples are on their own tab. No lunch items for Paul (Tossed). No Wednesday dinner items (delivery). No lamb.</div></div>`;
  s.fresh.forEach((sec,i)=>h+=shopSection(sec,"w"+wi,i));
  h+=shopSection({t:"🌮 Taco Tuesday",i:TACO_SHOP},"w"+wi,99);
  return h;
}
function viewPantry(){
  let h=`<div class="box" style="margin-top:0"><h3>🫙 Pantry Staples</h3>
   <div class="tbd">Buy once at the start, then top up as needed. Keeping these separate stops you re-buying cumin every week.</div></div>`;
  PANTRY.forEach((sec,i)=>h+=shopSection(sec,"pantry",i));
  return h;
}
function viewTips(){
  return `
  <div class="box" style="margin-top:0"><h3>🎯 The One Number That Matters</h3>
   <div class="tip"><span class="ti">💪</span><div><div class="tt">Protein: 160g Kiska · 170g Paul</div><div class="tbd">This protects muscle while you're in deficit. Calories can drift a little; protein shouldn't. Every meal card shows its protein in purple, and the daily meter tells you how far off you are.</div></div></div>
   <div class="tip"><span class="ti">🫘</span><div><div class="tt">Tempeh, tofu & edamame — the how</div><div class="tbd"><b>Tempeh</b> (~19g protein/100g): slice, marinate in soy, garlic and ginger, bake 25 min at 200°C. <b>Tofu</b> (~17g/100g): use extra-firm, press 15 min, crumble rather than cube for maximum crispy edges, bake 25–30 min at 220°C. <b>Edamame</b> (~11g/100g): straight from frozen, 3 min in the microwave. Keep bags in the freezer as your emergency protein.</div></div></div>
   <div class="tip"><span class="ti">🥬</span><div><div class="tt">100–150g green veg with every dinner</div><div class="tbd">Rocket, spinach, pak choi, broccoli, cucumber. Fibre and volume for very few calories.</div></div></div>
   <div class="tip"><span class="ti">🍞</span><div><div class="tt">Taco Tuesday is the planned exception</div><div class="tbd">Every other day sits under about 50g carbs. Tuesday doesn't, deliberately. One planned higher-carb night a week is far more sustainable than pretending you'll never eat a tortilla.</div></div></div>
   <div class="tip"><span class="ti">💧</span><div><div class="tt">3 litres of water a day</div><div class="tbd">Big bottle on the desk at both offices.</div></div></div>
  </div>
  <div class="warn"><b>⚠️ Why the protein target defaults to 140g</b><br><br>Protein costs calories. Across realistic vegetarian sources — powder at 4.4 kcal per gram of protein, tofu 8.5, tempeh 10.1, edamame 11.0, eggs 11.7, halloumi 14.6 — a real diet with vegetables and healthy fats runs about 9–10 kcal per gram of protein.<br><br>Running the full six weeks with the snacks needed to reach each target:<br>• <b>140g</b> → averages <b>1,420 kcal</b>, just 1.4% over your 1,400 target ✓<br>• <b>160g</b> → averages <b>1,530 kcal</b>, 9.3% over ✗<br><br>Your coach's own rule is a weekly average within 5%. At 160g you would breach that every single week — not through poor discipline, but arithmetic. 140g is still well above what's needed to protect muscle in a deficit.<br><br>The toggle above switches to 160g if your coach prefers it. Expect the meter to run short most days.<br><br><b>Paul:</b> his meals plus one shake average 1,828 kcal against a 1,900 target — 3.8% under, so he has room for a generous evening snack. That 1,900 figure is still my estimate; two weeks of MyFitnessPal will confirm it.</div>
  <div class="box"><h3>🍽 How Dinners Work Now</h3>
   <div class="tip"><span class="ti">1️⃣</span><div><div class="tt">One base dish, cooked once</div><div class="tbd">The vegetables, sauce and seasoning are identical for both of you. You're cooking a single meal, not two.</div></div></div>
   <div class="tip"><span class="ti">2️⃣</span><div><div class="tt">Protein cooked separately, added at the end</div><div class="tbd">Kiska's tofu or tempeh goes in one pan or tray, Paul's chicken or fish in another. Both get folded into the same base at the table.</div></div></div>
   <div class="tip"><span class="ti">🥚</span><div><div class="tt">Egg nights — you eat the same thing</div><div class="tbd">Shakshuka, menemen, the frittatas and the French omelette. Five nights across the six weeks where there's no swap at all, just a bigger portion for Paul.</div></div></div>
   <div class="tip" style="border:none;padding:0;margin:0"><span class="ti">🚫</span><div><div class="tt">No lamb</div><div class="tbd">Removed throughout. Paul's proteins are chicken, sea bass, cod, tuna, prawns, turkey, beef mince on Taco Tuesday, and eggs.</div></div></div>
  </div>
  <div class="box"><h3>⏱ Sunday Prep — 40 minutes</h3>
   <div class="tip"><span class="ti">1️⃣</span><div><div class="tt">Bake a tray of tempeh and a tray of tofu</div><div class="tbd">Both keep 4 days in the fridge and cover most of Kiska's dinners. This is the single highest-value 30 minutes of the week.</div></div></div>
   <div class="tip"><span class="ti">2️⃣</span><div><div class="tt">Hard boil 6 eggs</div><div class="tbd">Breakfasts, lunches, snacks. 12g protein per two.</div></div></div>
   <div class="tip"><span class="ti">3️⃣</span><div><div class="tt">Make a jar of tahini-lemon dressing</div><div class="tbd">Tahini, lemon, garlic, water. Goes on almost every lunch this plan contains.</div></div></div>
   <div class="tip"><span class="ti">4️⃣</span><div><div class="tt">Make the kale salad — it covers Tuesday and Friday</div><div class="tbd">One batch (500g kale, both peppers, carrot, 100g houmous, 2 tbsp almond butter) = 851 kcal and 40g protein, so it splits neatly into two 425 kcal lunches at 20g protein each. Kale holds up dressed for days, unlike softer leaves.</div></div></div>
  </div>
  <div class="box"><h3>🥬 Your Kale Salad — the numbers</h3>
   <div class="tbd" style="margin-bottom:10px">Calculated from your ingredients. Whole batch: <b>851 kcal · 40g protein · 48g fat · 53g net carbs</b>. Split in two:</div>
   <div class="tip"><span class="ti">📊</span><div><div class="tt">Per lunch: 425 kcal · 20g protein · 26g net carbs</div><div class="tbd">Calories and carbs both sit comfortably. Protein is the weak spot — 20g is well below the ~30g your other lunches deliver.</div></div></div>
   <div class="tip"><span class="ti">➕</span><div><div class="tt">Closing the gap</div><div class="tbd">100g cottage cheese adds 11g protein for 98 kcal — the leanest option. 100g edamame is near-identical at 11g for 121 kcal and suits the salad better. Either takes you to about 31g and 525 kcal, in line with your other lunches.</div></div></div>
   <div class="tip"><span class="ti">🥜</span><div><div class="tt">Worth noting</div><div class="tbd">Almond butter and houmous together account for 490 of the 851 calories and 42 of the 48g of fat. That's fine — they're the flavour and the healthy fats — but if you ever need to trim the salad down, halving the almond butter saves 95 kcal per serving and costs only 3g of protein.</div></div></div>
  </div>
  <div class="box"><h3>🍖 Paul at Tossed</h3>
   <div class="tip"><span class="ti">✅</span><div><div class="tt">Order this</div><div class="tbd">Double grilled chicken on a leaf base, as many veg toppings as they'll give you, no dressing — ask for lemon wedges instead. Add egg or avocado if they have it.</div></div></div>
   <div class="tip"><span class="ti">⚠️</span><div><div class="tt">Skip this</div><div class="tbd">Dressings (easily 200+ calories), croutons, anything "crispy", and grain bases. Protein and veg only.</div></div></div>
  </div>
  <div class="box"><h3>📖 Recipe Sources</h3>
   <div class="tbd" style="margin-bottom:10px">Your own two books lead. Everything else links to a free recipe — no paywalls, no sign-ups. Roasting Tin entries have no link because it's a physical book; the dish name tells you what to look for.</div>
   <div style="display:flex;flex-direction:column;gap:10px">
    <div><span class="rl s-tin">Quick Roasting Tin 📖</span> <span class="tbd">Your book — traybake nights. No link; the dish name tells you what to look for.</span></div>
    <div><span class="rl s-della">Deliciously Ella</span> <span class="tbd">Your app &amp; book — links go to the free website search.</span></div>
    <div><span class="rl s-gso">Gimme Some Oven</span> <span class="tbd">Bowls, salads and 30-minute dinners. Their site search is unreliable, so these links open the relevant category — browse from there. US measures: cups and °F.</span></div>
    <div><span class="rl s-bbc">BBC Good Food</span> <span class="tbd">Reliable weeknight cooking</span></div>
    <div><span class="rl s-min">Minimalist Baker</span> <span class="tbd">The tofu and tempeh specialists</span></div>
    <div><span class="rl s-ll">Love &amp; Lemons</span> <span class="tbd">Vegetable-forward Mediterranean</span></div>
    <div><span class="rl s-none">No-Cook</span> <span class="tbd">Assembly only — no recipe needed</span></div>
   </div>
  </div>`;
}

// ─── SHELL ────────────────────────────────────────────────────────
const TABS=[["plan","Daily Plan"],["overview","Week"],["tips","How To"],["pantry","🫙 Pantry"],["shop","🛒 Fresh Shop"]];
function renderNav(){
  document.getElementById("navBar").innerHTML=TABS.map(([id,lbl])=>
   `<button class="${S.view===id?"on":""}" onclick="setView('${id}')">${lbl}</button>`).join("");
}
function setView(v){S.view=v;save();renderAll();}
function setWeek(i){S.week=i;S.day=0;save();renderAll();}
function setDay(i){S.day=i;save();renderAll();}
function goDay(i){S.day=i;S.view="plan";save();renderAll();}
function renderSelectors(){
  const showW=["plan","overview","shop"].includes(S.view);
  const showD=S.view==="plan";
  document.getElementById("selectors").style.display=showW?"block":"none";
  document.querySelectorAll("#selectors .lbl")[1].style.display=showD?"block":"none";
  document.getElementById("dbtns").style.display=showD?"flex":"none";
  document.getElementById("wbtns").innerHTML=THEMES.map((t,i)=>
   `<button class="wb ${i===S.week?"on":""}" onclick="setWeek(${i})">W${i+1}</button>`).join("");
  document.getElementById("wtheme").textContent=THEMES[S.week];
  const cur=currentSlot();
  document.getElementById("dbtns").innerHTML=DAYS.map((d,i)=>{
   const isToday=!cur.pre&&!cur.post&&cur.w===S.week&&cur.d===i;
   return `<button class="db ${i===S.day?"on":""}" onclick="setDay(${i})">${d}${isToday?'<span class="dot">🟢</span>':""}</button>`;}).join("");
}
function renderMain(){
  const el=document.getElementById("content");
  if(S.view==="plan")el.innerHTML=viewPlan();
  else if(S.view==="overview")el.innerHTML=viewOverview();
  else if(S.view==="tips")el.innerHTML=viewTips();
  else if(S.view==="pantry")el.innerHTML=viewPantry();
  else if(S.view==="shop")el.innerHTML=viewShop(S.week);
}
function renderToday(){
  document.getElementById("startDate").value=getStart();
  document.getElementById("proSel").value=S.proK;
  const c=currentSlot();
  const el=document.getElementById("todayLbl");
  if(c.pre)el.textContent="Starts in "+(-c.n)+" days";
  else if(c.post)el.textContent="Plan complete 🎉";
  else el.textContent="Week "+(c.w+1)+" · "+DAYS[c.d];
}
function renderAll(){renderNav();renderToday();renderSelectors();renderMain();}
load();getStart();
(function(){const c=currentSlot();if(!c.pre&&!c.post&&S.week===0&&S.day===0){S.week=c.w;S.day=c.d;}})();
renderAll();

</script>
</body>
</html>
