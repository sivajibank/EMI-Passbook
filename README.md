
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1,maximum-scale=1,user-scalable=no">
<meta name="theme-color" content="#6B1020">
<meta name="robots" content="noindex,nofollow">
<title>EMI Passbook · தவணை பாஸ்புக்</title>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+Tamil:wght@400;600;700;800&family=DM+Serif+Display&family=Inter:wght@400;600;700;800&display=swap" rel="stylesheet">
<style>
:root{
  --maroon:#6B1020; --maroon2:#8B2030; --gold:#B8860B; --goldlt:#E8C874;
  --cream:#FDF8EE; --ink:#2A1810; --muted:#7A5A40; --line:#EADFC8;
  --green:#1A7A3C; --red:#C0392B; --blue:#1A4A8C;
}
*{box-sizing:border-box;margin:0;padding:0;-webkit-tap-highlight-color:transparent;}
body{
  font-family:'Inter','Noto Sans Tamil',Latha,system-ui,sans-serif;
  background:linear-gradient(165deg,#2A1810 0%,#4A1220 45%,#1C0E08 100%);
  background-attachment:fixed;color:var(--ink);min-height:100vh;
  padding:18px 14px 44px;display:flex;justify-content:center;
}
.wrap{width:100%;max-width:460px;}
.ta{font-family:'Noto Sans Tamil',Latha,sans-serif;}

/* ─── shared card chrome ─── */
.card{background:var(--cream);border:2px solid var(--gold);border-radius:18px;
  padding:5px;box-shadow:0 22px 60px rgba(0,0,0,.55);}
.card>.in{border:1px solid var(--goldlt);border-radius:13px;padding:20px 18px;position:relative;overflow:hidden;}
.kolam{height:8px;border-radius:4px;opacity:.5;
  background:repeating-linear-gradient(90deg,var(--gold) 0 6px,transparent 6px 12px);}

/* ─── lock screen ─── */
#lock{animation:fade .5s ease both;}
@keyframes fade{from{opacity:0;transform:translateY(14px)}to{opacity:1;transform:none}}
.lk-badge{width:62px;height:62px;margin:6px auto 12px;border-radius:50%;
  background:linear-gradient(140deg,var(--maroon),var(--maroon2));
  display:flex;align-items:center;justify-content:center;font-size:28px;
  box-shadow:0 8px 22px rgba(107,16,32,.35);}
.lk-shop{font-family:'DM Serif Display',serif;font-size:22px;color:var(--maroon);text-align:center;}
.lk-shop-ta{font-size:13px;color:var(--muted);text-align:center;margin-top:2px;}
.lk-tag{display:inline-block;background:var(--maroon);color:#F5E3B3;border-radius:16px;
  padding:4px 14px;font-size:10.5px;font-weight:700;letter-spacing:.06em;margin-top:10px;}
.lk-hi{text-align:center;font-size:14px;font-weight:700;margin:16px 0 4px;}
.lk-sub{text-align:center;font-size:11.5px;color:var(--muted);line-height:1.6;margin-bottom:16px;}
.pins{display:flex;gap:10px;justify-content:center;margin-bottom:6px;}
.pins input{width:50px;height:60px;text-align:center;font-size:26px;font-weight:800;
  border:2px solid var(--goldlt);border-radius:12px;background:#fff;color:var(--maroon);
  outline:none;transition:.18s;font-family:'Inter',sans-serif;}
.pins input:focus{border-color:var(--maroon);box-shadow:0 0 0 4px rgba(107,16,32,.12);transform:translateY(-2px);}
.pins input.ok{border-color:var(--green);}
.pins.shake{animation:shk .42s;}
@keyframes shk{0%,100%{transform:translateX(0)}20%{transform:translateX(-9px)}40%{transform:translateX(9px)}60%{transform:translateX(-5px)}80%{transform:translateX(5px)}}
.err{text-align:center;font-size:11.5px;color:var(--red);font-weight:700;height:17px;margin-top:6px;}
.hint{text-align:center;font-size:10.5px;color:#A88A60;margin-top:12px;line-height:1.6;}

/* ─── unlock animation ─── */
#unlockFx{position:fixed;inset:0;z-index:99;display:none;align-items:center;justify-content:center;
  background:rgba(28,14,8,.92);backdrop-filter:blur(6px);}
#unlockFx .ring{width:96px;height:96px;border-radius:50%;border:3px solid rgba(232,200,116,.25);
  border-top-color:var(--goldlt);animation:spin .8s linear infinite;}
#unlockFx .tick{position:absolute;font-size:38px;opacity:0;transform:scale(.4);}
@keyframes spin{to{transform:rotate(360deg)}}
@keyframes pop{to{opacity:1;transform:scale(1)}}

/* ─── passbook ─── */
#book{display:none;}
#book.show{display:block;animation:fade .55s ease both;}
.hero{background:linear-gradient(140deg,var(--maroon),var(--maroon2));border-radius:16px;
  padding:18px 16px;color:#fff;margin-bottom:12px;box-shadow:0 10px 26px rgba(107,16,32,.3);position:relative;overflow:hidden;}
.hero::after{content:'';position:absolute;top:-40px;right:-30px;width:130px;height:130px;
  border-radius:50%;background:rgba(255,255,255,.06);}
.hero .who{font-size:16px;font-weight:800;}
.hero .sub{font-size:10.5px;color:#F5C6C0;margin-top:2px;}
.hero .big{font-family:'DM Serif Display',serif;font-size:33px;margin-top:12px;line-height:1.1;}
.hero .biglbl{font-size:9.5px;letter-spacing:.11em;color:#F5E3B3;font-weight:700;}
.bar{height:8px;background:rgba(255,255,255,.2);border-radius:5px;overflow:hidden;margin-top:14px;}
.bar i{display:block;height:100%;border-radius:5px;background:linear-gradient(90deg,var(--goldlt),#fff);
  width:0;transition:width 1.1s cubic-bezier(.22,1,.36,1);}
.barlbl{display:flex;justify-content:space-between;font-size:9.5px;font-weight:700;color:#F5E3B3;margin-top:5px;}

.kpis{display:grid;grid-template-columns:1fr 1fr;gap:9px;margin-bottom:12px;}
.kpi{background:var(--cream);border:1px solid var(--goldlt);border-radius:12px;padding:11px 12px;}
.kpi .l{font-size:8.5px;font-weight:800;color:#9A7A50;text-transform:uppercase;letter-spacing:.05em;}
.kpi .l .ta{display:block;font-size:9px;font-weight:600;text-transform:none;letter-spacing:0;opacity:.9;}
.kpi .v{font-size:17px;font-weight:800;color:var(--maroon);margin-top:3px;}

.sec{background:var(--cream);border:1px solid var(--goldlt);border-radius:14px;padding:14px 14px 12px;margin-bottom:12px;}
.sec h2{font-size:11px;font-weight:800;color:var(--maroon);text-transform:uppercase;letter-spacing:.07em;
  display:flex;justify-content:space-between;align-items:baseline;margin-bottom:10px;}
.sec h2 .ta{font-size:10px;font-weight:600;text-transform:none;letter-spacing:0;color:var(--muted);}
.rw{display:flex;justify-content:space-between;align-items:baseline;padding:6px 0;
  border-bottom:1px dotted var(--line);font-size:12.5px;}
.rw:last-child{border-bottom:none;}
.rw span{color:var(--muted);font-size:11.5px;}
.rw span .ta{display:block;font-size:9.5px;opacity:.85;}
.rw b{text-align:right;}

/* installment ledger */
.ins{display:flex;align-items:center;gap:11px;padding:10px 0;border-bottom:1px dotted var(--line);}
.ins:last-child{border-bottom:none;}
.ins .n{width:32px;height:32px;flex:0 0 32px;border-radius:9px;display:flex;align-items:center;
  justify-content:center;font-size:12px;font-weight:800;background:#EFE3CB;color:var(--muted);}
.ins.paid .n{background:#D1FAE5;color:#065F46;}
.ins.part .n{background:#DBEAFE;color:#1E40AF;}
.ins.miss .n{background:#FEE2E2;color:#991B1B;}
.ins.next .n{background:linear-gradient(140deg,var(--maroon),var(--maroon2));color:#F5E3B3;
  box-shadow:0 0 0 3px rgba(107,16,32,.13);}
.ins .mid{flex:1;min-width:0;}
.ins .d{font-size:12.5px;font-weight:700;}
.ins .s{font-size:9.5px;color:var(--muted);margin-top:1px;}
.ins .amt{text-align:right;flex-shrink:0;}
.ins .amt b{font-size:13px;font-weight:800;}
.ins .chip{display:inline-block;font-size:8.5px;font-weight:800;padding:2px 7px;border-radius:8px;margin-top:2px;}
.c-paid{background:#D1FAE5;color:#065F46;} .c-part{background:#DBEAFE;color:#1E40AF;}
.c-miss{background:#FEE2E2;color:#991B1B;} .c-pend{background:#FEF3C7;color:#92400E;}

.pay{display:block;width:100%;text-align:center;text-decoration:none;border:none;cursor:pointer;
  background:linear-gradient(135deg,#1A7A3C,#0F5528);color:#fff;border-radius:13px;padding:14px;
  font-size:14px;font-weight:800;box-shadow:0 8px 20px rgba(26,122,60,.3);margin-bottom:12px;
  font-family:inherit;}
.pay small{display:block;font-size:10px;font-weight:600;opacity:.85;margin-top:2px;}
.pay:active{transform:scale(.985);}
.callbtn{display:block;width:100%;text-align:center;text-decoration:none;border:1.5px solid var(--gold);
  background:var(--cream);color:var(--maroon);border-radius:13px;padding:12px;font-size:13px;font-weight:800;margin-bottom:12px;}
.foot{text-align:center;font-size:9.5px;color:rgba(232,200,116,.6);line-height:1.7;margin-top:16px;}
.stale{background:#FEF3C7;border:1px solid #F0C060;border-radius:10px;padding:9px 11px;
  font-size:10.5px;color:#7A5A10;line-height:1.55;margin-bottom:12px;font-weight:600;}
.bad{text-align:center;padding:30px 10px;}
.bad h1{font-size:17px;color:var(--maroon);margin-bottom:8px;}
.bad p{font-size:12px;color:var(--muted);line-height:1.65;}
.diag{margin-top:14px;padding:8px 10px;background:rgba(184,134,11,.1);border-radius:8px;
  font-size:9.5px;color:#8A6D00;line-height:1.5;}
</style>
</head>
<body>

<div id="unlockFx"><div class="ring"></div><div class="tick">🔓</div></div>

<div class="wrap">

  <!-- ══ LOCK SCREEN ══ -->
  <div id="lock" class="card"><div class="in">
    <div class="kolam"></div>
    <div class="lk-badge">📘</div>
    <div class="lk-shop" id="lkShop">Sivaji Bank</div>
    <div class="lk-shop-ta ta" id="lkShopTa"></div>
    <div style="text-align:center;"><span class="lk-tag">EMI PASSBOOK <span class="ta">· தவணை பாஸ்புக்</span></span></div>
    <div class="lk-hi" id="lkHi">Enter your 4-digit PIN</div>
    <div class="lk-sub ta">உங்கள் 4 இலக்க PIN-ஐ உள்ளிடவும்</div>
    <div class="pins" id="pins">
      <input type="tel" inputmode="numeric" maxlength="1" autocomplete="off">
      <input type="tel" inputmode="numeric" maxlength="1" autocomplete="off">
      <input type="tel" inputmode="numeric" maxlength="1" autocomplete="off">
      <input type="tel" inputmode="numeric" maxlength="1" autocomplete="off">
    </div>
    <div class="err" id="err"></div>
    <div class="hint">This link works offline — your details travel inside the link itself, never on a server.<br>
      <span class="ta">இந்த இணைப்பு இணையம் இல்லாமலும் வேலை செய்யும்.</span></div>
    <div class="kolam" style="margin-top:16px;"></div>
  </div></div>

  <!-- ══ PASSBOOK ══ -->
  <div id="book"></div>

  <div class="foot" id="foot"></div>
</div>

<script>var LZString=function(){var r=String.fromCharCode,o="ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+/=",n="ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+-$",e={};function t(r,o){if(!e[r]){e[r]={};for(var n=0;n<r.length;n++)e[r][r.charAt(n)]=n}return e[r][o]}var i={compressToBase64:function(r){if(null==r)return"";var n=i._compress(r,6,function(r){return o.charAt(r)});switch(n.length%4){default:case 0:return n;case 1:return n+"===";case 2:return n+"==";case 3:return n+"="}},decompressFromBase64:function(r){return null==r?"":""==r?null:i._decompress(r.length,32,function(n){return t(o,r.charAt(n))})},compressToUTF16:function(o){return null==o?"":i._compress(o,15,function(o){return r(o+32)})+" "},decompressFromUTF16:function(r){return null==r?"":""==r?null:i._decompress(r.length,16384,function(o){return r.charCodeAt(o)-32})},compressToUint8Array:function(r){for(var o=i.compress(r),n=new Uint8Array(2*o.length),e=0,t=o.length;e<t;e++){var s=o.charCodeAt(e);n[2*e]=s>>>8,n[2*e+1]=s%256}return n},decompressFromUint8Array:function(o){if(null==o)return i.decompress(o);for(var n=new Array(o.length/2),e=0,t=n.length;e<t;e++)n[e]=256*o[2*e]+o[2*e+1];var s=[];return n.forEach(function(o){s.push(r(o))}),i.decompress(s.join(""))},compressToEncodedURIComponent:function(r){return null==r?"":i._compress(r,6,function(r){return n.charAt(r)})},decompressFromEncodedURIComponent:function(r){return null==r?"":""==r?null:(r=r.replace(/ /g,"+"),i._decompress(r.length,32,function(o){return t(n,r.charAt(o))}))},compress:function(o){return i._compress(o,16,function(o){return r(o)})},_compress:function(r,o,n){if(null==r)return"";var e,t,i,s={},u={},a="",p="",c="",l=2,f=3,h=2,d=[],m=0,v=0;for(i=0;i<r.length;i+=1)if(a=r.charAt(i),Object.prototype.hasOwnProperty.call(s,a)||(s[a]=f++,u[a]=!0),p=c+a,Object.prototype.hasOwnProperty.call(s,p))c=p;else{if(Object.prototype.hasOwnProperty.call(u,c)){if(c.charCodeAt(0)<256){for(e=0;e<h;e++)m<<=1,v==o-1?(v=0,d.push(n(m)),m=0):v++;for(t=c.charCodeAt(0),e=0;e<8;e++)m=m<<1|1&t,v==o-1?(v=0,d.push(n(m)),m=0):v++,t>>=1}else{for(t=1,e=0;e<h;e++)m=m<<1|t,v==o-1?(v=0,d.push(n(m)),m=0):v++,t=0;for(t=c.charCodeAt(0),e=0;e<16;e++)m=m<<1|1&t,v==o-1?(v=0,d.push(n(m)),m=0):v++,t>>=1}0==--l&&(l=Math.pow(2,h),h++),delete u[c]}else for(t=s[c],e=0;e<h;e++)m=m<<1|1&t,v==o-1?(v=0,d.push(n(m)),m=0):v++,t>>=1;0==--l&&(l=Math.pow(2,h),h++),s[p]=f++,c=String(a)}if(""!==c){if(Object.prototype.hasOwnProperty.call(u,c)){if(c.charCodeAt(0)<256){for(e=0;e<h;e++)m<<=1,v==o-1?(v=0,d.push(n(m)),m=0):v++;for(t=c.charCodeAt(0),e=0;e<8;e++)m=m<<1|1&t,v==o-1?(v=0,d.push(n(m)),m=0):v++,t>>=1}else{for(t=1,e=0;e<h;e++)m=m<<1|t,v==o-1?(v=0,d.push(n(m)),m=0):v++,t=0;for(t=c.charCodeAt(0),e=0;e<16;e++)m=m<<1|1&t,v==o-1?(v=0,d.push(n(m)),m=0):v++,t>>=1}0==--l&&(l=Math.pow(2,h),h++),delete u[c]}else for(t=s[c],e=0;e<h;e++)m=m<<1|1&t,v==o-1?(v=0,d.push(n(m)),m=0):v++,t>>=1;0==--l&&(l=Math.pow(2,h),h++)}for(t=2,e=0;e<h;e++)m=m<<1|1&t,v==o-1?(v=0,d.push(n(m)),m=0):v++,t>>=1;for(;;){if(m<<=1,v==o-1){d.push(n(m));break}v++}return d.join("")},decompress:function(r){return null==r?"":""==r?null:i._decompress(r.length,32768,function(o){return r.charCodeAt(o)})},_decompress:function(o,n,e){var t,i,s,u,a,p,c,l=[],f=4,h=4,d=3,m="",v=[],g={val:e(0),position:n,index:1};for(t=0;t<3;t+=1)l[t]=t;for(s=0,a=Math.pow(2,2),p=1;p!=a;)u=g.val&g.position,g.position>>=1,0==g.position&&(g.position=n,g.val=e(g.index++)),s|=(u>0?1:0)*p,p<<=1;switch(s){case 0:for(s=0,a=Math.pow(2,8),p=1;p!=a;)u=g.val&g.position,g.position>>=1,0==g.position&&(g.position=n,g.val=e(g.index++)),s|=(u>0?1:0)*p,p<<=1;c=r(s);break;case 1:for(s=0,a=Math.pow(2,16),p=1;p!=a;)u=g.val&g.position,g.position>>=1,0==g.position&&(g.position=n,g.val=e(g.index++)),s|=(u>0?1:0)*p,p<<=1;c=r(s);break;case 2:return""}for(l[3]=c,i=c,v.push(c);;){if(g.index>o)return"";for(s=0,a=Math.pow(2,d),p=1;p!=a;)u=g.val&g.position,g.position>>=1,0==g.position&&(g.position=n,g.val=e(g.index++)),s|=(u>0?1:0)*p,p<<=1;switch(c=s){case 0:for(s=0,a=Math.pow(2,8),p=1;p!=a;)u=g.val&g.position,g.position>>=1,0==g.position&&(g.position=n,g.val=e(g.index++)),s|=(u>0?1:0)*p,p<<=1;l[h++]=r(s),c=h-1,f--;break;case 1:for(s=0,a=Math.pow(2,16),p=1;p!=a;)u=g.val&g.position,g.position>>=1,0==g.position&&(g.position=n,g.val=e(g.index++)),s|=(u>0?1:0)*p,p<<=1;l[h++]=r(s),c=h-1,f--;break;case 2:return v.join("")}if(0==f&&(f=Math.pow(2,d),d++),l[c])m=l[c];else{if(c!==h)return null;m=i+i.charAt(0)}v.push(m),l[h++]=i+m.charAt(0),i=m,0==--f&&(f=Math.pow(2,d),d++)}}};return i}();"function"==typeof define&&define.amd?define(function(){return LZString}):"undefined"!=typeof module&&null!=module?module.exports=LZString:"undefined"!=typeof angular&&null!=angular&&angular.module("LZString",[]).factory("LZString",function(){return LZString});</script>
<script>
(function(){
"use strict";
var D=null, EL=function(id){return document.getElementById(id);};
var esc=function(t){return String(t==null?'':t).replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;');};
var R=function(v){return '\u20B9'+Math.round(v||0).toLocaleString('en-IN');};
var fD=function(d){if(!d)return '\u2014';var p=String(d).split('-');return p.length===3?p[2]+'/'+p[1]+'/'+p[0]:d;};
var todayISO=function(){var n=new Date();return n.getFullYear()+'-'+String(n.getMonth()+1).padStart(2,'0')+'-'+String(n.getDate()).padStart(2,'0');};

/* ── decode payload from the URL fragment ─────────────────────────────────
   Some share paths mangle the fragment on the way here: a few in-app browsers
   percent-encode it, some replace '+' with a space, and long links occasionally
   get clipped. Try the plausible repairs before giving up, and never throw —
   an uncaught error just leaves the reader staring at a blank page.          */
function readFragment(){
  var raw=(location.hash||'').replace(/^#/,'');
  if(!raw) return {frag:'', data:null};
  var tries=[raw];
  if(raw.indexOf('%')>-1){ try{ tries.push(decodeURIComponent(raw)); }catch(e){} }
  if(raw.indexOf(' ')>-1) tries.push(raw.replace(/ /g,'+'));
  for(var i=0;i<tries.length;i++){
    try{
      var s=LZString.decompressFromEncodedURIComponent(tries[i]);
      if(s){ var o=JSON.parse(s); if(o&&o.s) return {frag:raw, data:o}; }
    }catch(e){}
  }
  return {frag:raw, data:null};
}

var _read=readFragment();
D=_read.data;

if(!D){
  var body, diag='';
  if(!_read.frag){
    /* Opened bare — the page itself is fine, there is just nothing to show. */
    body='<h1>Nothing to open yet</h1><p>This page only works when it is opened '+
      'from the QR code on your receipt or passbook card, or from the link the shop sent you — '+
      'your details travel inside that link.<br><br>'+
      'Please scan the QR again, or tap the link in your message.<br><br>'+
      '<span class="ta">ரசீதில் உள்ள QR-ஐ ஸ்கேன் செய்து திறக்கவும்.</span></p>';
  } else {
    body='<h1>Link not readable</h1><p>This passbook link looks incomplete — it was probably '+
      'cut short when it was copied or forwarded. Please scan the QR on your receipt again, '+
      'or ask the shop to resend the link.<br><br>'+
      '<span class="ta">இந்த இணைப்பு முழுமையாக இல்லை. ரசீதில் உள்ள QR-ஐ மீண்டும் ஸ்கேன் செய்யவும்.</span></p>';
    diag='<div class="diag">Received '+_read.frag.length+' characters — a full link is usually 400–900. '+
      'Show this line to the shop if it keeps happening.</div>';
  }
  document.querySelector('.wrap').innerHTML=
    '<div class="card"><div class="in"><div class="bad">'+body+diag+'</div></div></div>';
  return;   /* stop cleanly — no uncaught error in the console */
}

EL('lkShop').textContent = D.sn || 'Passbook';
EL('lkShopTa').textContent = D.snt || '';
if(D.cn) EL('lkHi').textContent = 'Hello, '+D.cn;
EL('foot').innerHTML = esc(D.sn||'')+(D.sp?' \u00B7 \u260E '+esc(D.sp):'')+
  '<br>Snapshot taken '+fD(D.gen)+' \u00B7 computer-generated, valid without seal';

/* ── PIN gate ── */
var boxes=[].slice.call(document.querySelectorAll('#pins input'));
var tries=0;
boxes.forEach(function(b,i){
  b.addEventListener('input',function(){
    b.value=b.value.replace(/\D/g,'');
    if(b.value){ b.classList.add('ok'); if(i<3) boxes[i+1].focus(); else check(); }
    else b.classList.remove('ok');
  });
  b.addEventListener('keydown',function(e){
    if(e.key==='Backspace'&&!b.value&&i>0){boxes[i-1].focus();boxes[i-1].value='';boxes[i-1].classList.remove('ok');}
    if(e.key==='Enter') check();
  });
  b.addEventListener('paste',function(e){
    var t=(e.clipboardData||window.clipboardData).getData('text').replace(/\D/g,'').slice(0,4);
    if(t.length){e.preventDefault();boxes.forEach(function(x,j){x.value=t[j]||'';x.classList.toggle('ok',!!t[j]);});
      if(t.length===4) check(); else boxes[t.length].focus();}
  });
});
setTimeout(function(){ if(window.innerWidth>640) boxes[0].focus(); },350);

function check(){
  var got=boxes.map(function(b){return b.value;}).join('');
  if(got.length<4) return;
  if(String(D.sec||'')===got){ unlock(); return; }
  tries++;
  EL('pins').classList.add('shake');
  EL('err').textContent = tries>=3 ? 'Still wrong — please call the shop.' : 'Incorrect PIN. Try again.';
  setTimeout(function(){EL('pins').classList.remove('shake');},450);
  setTimeout(function(){boxes.forEach(function(b){b.value='';b.classList.remove('ok');});boxes[0].focus();},480);
}

function unlock(){
  var fx=EL('unlockFx'); fx.style.display='flex';
  setTimeout(function(){
    fx.querySelector('.ring').style.display='none';
    var t=fx.querySelector('.tick'); t.style.animation='pop .35s cubic-bezier(.2,1.4,.4,1) forwards';
  },620);
  setTimeout(function(){
    fx.style.display='none'; EL('lock').style.display='none';
    render(); EL('book').classList.add('show');
    window.scrollTo(0,0);
  },1080);
}

/* ── render the passbook ── */
function render(){
  var rows=D.s||[], today=todayISO(), n=rows.length;
  // row = [m, dueDate, emi, paidAmount, paidDate, lateFee, statusCode]
  var paidCt=0, totalDue=0, totalPaid=0, nextRow=null;
  rows.forEach(function(r){
    totalDue  += (r[2]||0)+(r[5]||0);
    totalPaid += (r[3]||0);
    if(r[6]===2) paidCt++;
    if(!nextRow && r[6]!==2) nextRow=r;
  });
  var balance=Math.max(0,totalDue-totalPaid);
  var pct=n?Math.round(paidCt/n*100):0;
  var typeLbl={reducing:'Reducing Balance',flat:'Flat Rate',bullet:'Bullet / Lump Sum'}[D.ty]||D.ty||'\u2014';

  var insHtml=rows.map(function(r){
    var overdue = r[6]!==2 && r[1] < today;
    var cls = r[6]===2?'paid':r[6]===1?'part':overdue?'miss':'';
    if(!cls && nextRow && r[0]===nextRow[0]) cls='next';
    var chip = r[6]===2?'<span class="chip c-paid">PAID \u00B7 \u0BB5\u0BB0\u0BB5\u0BC1</span>'
             : r[6]===1?'<span class="chip c-part">PART PAID</span>'
             : overdue ?'<span class="chip c-miss">OVERDUE \u00B7 \u0BA4\u0BBE\u0BAE\u0BA4\u0BAE\u0BCD</span>'
             :          '<span class="chip c-pend">DUE</span>';
    var sub = r[6]===2 ? 'Paid '+fD(r[4])
            : r[6]===1 ? 'Paid '+R(r[3])+' \u00B7 still '+R(Math.max(0,(r[2]||0)-(r[3]||0)+(r[5]||0)))
            : (r[5]>0 ? 'Late fee '+R(r[5])+' added' : 'Due '+fD(r[1]));
    return '<div class="ins '+cls+'">'+
      '<div class="n">'+r[0]+'</div>'+
      '<div class="mid"><div class="d">'+fD(r[1])+'</div><div class="s">'+sub+'</div></div>'+
      '<div class="amt"><b>'+R((r[2]||0)+(r[5]||0))+'</b><br>'+chip+'</div>'+
    '</div>';
  }).join('');

  var upiBtn='';
  if(D.upi && D.upi.pa && nextRow){
    var amt=Math.round(Math.max(0,(nextRow[2]||0)-(nextRow[3]||0)+(nextRow[5]||0)));
    var note='EMI '+(D.b||'')+' #'+nextRow[0];
    var link='upi://pay?pa='+encodeURIComponent(D.upi.pa)+'&pn='+encodeURIComponent(D.upi.pn||D.sn||'')+
             '&am='+amt+'&cu=INR&tn='+encodeURIComponent(note);
    upiBtn='<a class="pay" href="'+link+'">Pay '+R(amt)+' now \u00B7 \u0B87\u0BAA\u0BCD\u0BAA\u0BCB\u0BA4\u0BC1 \u0B9A\u0BC6\u0BB2\u0BC1\u0BA4\u0BCD\u0BA4\u0BC1'+
            '<small>Opens GPay / PhonePe / Paytm \u00B7 installment #'+nextRow[0]+'</small></a>';
  }

  var callBtn = D.sp ? '<a class="callbtn" href="tel:'+esc(D.sp)+'">\u260E Call the shop \u00B7 \u0B95\u0B9F\u0BC8\u0BAF\u0BC8 \u0B85\u0BB4\u0BC8\u0B95\u0BCD\u0B95</a>' : '';

  var ageDays = Math.round((new Date(today) - new Date(D.gen||today))/86400000);
  var staleMsg = ageDays>7 ? '<div class="stale">\u26A0\uFE0F This snapshot is '+ageDays+' days old. '+
    'Any payment made after '+fD(D.gen)+' will not appear here \u2014 please ask the shop for an updated link.<br>'+
    '<span class="ta">\u0B87\u0BA8\u0BCD\u0BA4 \u0BB5\u0BBF\u0BB5\u0BB0\u0BAE\u0BCD '+fD(D.gen)+' \u0BA8\u0BBF\u0BB2\u0BC8. \u0BAA\u0BC1\u0BA4\u0BBF\u0BAF \u0B87\u0BA3\u0BC8\u0BAA\u0BCD\u0BAA\u0BC8\u0B95\u0BCD \u0B95\u0BC7\u0B9F\u0BCD\u0B95\u0BB5\u0BC1\u0BAE\u0BCD.</span></div>' : '';

  EL('book').innerHTML =
  '<div class="hero">'+
    '<div class="who">'+esc(D.cn||'')+'</div>'+
    '<div class="sub">Pledge '+esc(D.b||'')+' \u00B7 '+esc(typeLbl)+' \u00B7 '+esc(D.r||0)+'%/mo</div>'+
    '<div class="biglbl" style="margin-top:12px;">BALANCE REMAINING \u00B7 \u0BA8\u0BBF\u0BB2\u0BC1\u0BB5\u0BC8</div>'+
    '<div class="big">'+R(balance)+'</div>'+
    '<div class="bar"><i id="pfill"></i></div>'+
    '<div class="barlbl"><span>'+paidCt+' / '+n+' installments paid \u00B7 \u0B9A\u0BC6\u0BB2\u0BC1\u0BA4\u0BCD\u0BA4\u0BBF\u0BAF\u0BA4\u0BC1</span><span>'+pct+'%</span></div>'+
  '</div>'+
  staleMsg+
  '<div class="kpis">'+
    '<div class="kpi"><div class="l">Next Due<span class="ta">\u0B85\u0B9F\u0BC1\u0BA4\u0BCD\u0BA4 \u0BA4\u0BB5\u0BA3\u0BC8</span></div><div class="v">'+(nextRow?fD(nextRow[1]):'\u2705 Done')+'</div></div>'+
    '<div class="kpi"><div class="l">Next Amount<span class="ta">\u0BA4\u0BCA\u0B95\u0BC8</span></div><div class="v">'+(nextRow?R(Math.max(0,(nextRow[2]||0)-(nextRow[3]||0)+(nextRow[5]||0))):'\u2014')+'</div></div>'+
    '<div class="kpi"><div class="l">Total Paid<span class="ta">\u0BAE\u0BCA\u0BA4\u0BCD\u0BA4 \u0B9A\u0BC6\u0BB2\u0BC1\u0BA4\u0BCD\u0BA4\u0BBF\u0BAF\u0BA4\u0BC1</span></div><div class="v" style="color:var(--green);">'+R(totalPaid)+'</div></div>'+
    '<div class="kpi"><div class="l">Plan Total<span class="ta">\u0BAE\u0BCA\u0BA4\u0BCD\u0BA4 \u0BA4\u0BBF\u0B9F\u0BCD\u0B9F\u0BAE\u0BCD</span></div><div class="v">'+R(totalDue)+'</div></div>'+
  '</div>'+
  upiBtn+
  '<div class="sec"><h2>Installment Ledger <span class="ta">\u0BA4\u0BB5\u0BA3\u0BC8 \u0BAA\u0BA4\u0BBF\u0BB5\u0BC1</span></h2>'+insHtml+'</div>'+
  '<div class="sec"><h2>Loan Details <span class="ta">\u0B95\u0B9F\u0BA9\u0BCD \u0BB5\u0BBF\u0BB5\u0BB0\u0BAE\u0BCD</span></h2>'+
    '<div class="rw"><span>Pledge No.<span class="ta">\u0B85\u0B9F\u0B95\u0BC1 \u0B8E\u0BA3\u0BCD</span></span><b>'+esc(D.b||'\u2014')+'</b></div>'+
    '<div class="rw"><span>Loan Amount<span class="ta">\u0B95\u0B9F\u0BA9\u0BCD \u0BA4\u0BCA\u0B95\u0BC8</span></span><b>'+R(D.am)+'</b></div>'+
    (D.dn?'<div class="rw"><span>Down Payment<span class="ta">\u0BAE\u0BC1\u0BA9\u0BCD\u0BAA\u0BA3\u0BAE\u0BCD</span></span><b>'+R(D.dn)+'</b></div>':'')+
    '<div class="rw"><span>Plan Type<span class="ta">\u0BA4\u0BBF\u0B9F\u0BCD\u0B9F \u0BB5\u0B95\u0BC8</span></span><b>'+esc(typeLbl)+'</b></div>'+
    '<div class="rw"><span>Tenure<span class="ta">\u0B95\u0BBE\u0BB2\u0BAE\u0BCD</span></span><b>'+n+' months</b></div>'+
    (D.sd?'<div class="rw"><span>First Installment<span class="ta">\u0BAE\u0BC1\u0BA4\u0BB2\u0BCD \u0BA4\u0BB5\u0BA3\u0BC8</span></span><b>'+fD(D.sd)+'</b></div>':'')+
  '</div>'+
  callBtn;

  setTimeout(function(){var f=EL('pfill'); if(f) f.style.width=pct+'%';},180);
}
})();
</script>
</body>
</html>
