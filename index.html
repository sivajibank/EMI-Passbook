<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<meta name="robots" content="noindex, nofollow">
<meta name="referrer" content="no-referrer">
<meta name="theme-color" content="#12331F">
<title>EMI Passbook</title>
<meta property="og:type" content="website">
<meta property="og:site_name" content="Sivaji Bank">
<meta property="og:title" content="Sivaji Bank — EMI Passbook">
<meta property="og:description" content="உங்கள் EMI தவணை விவரங்கள் · Your EMI instalments and dues">
<meta property="og:image" content="https://sivajibank.github.io/passbook/p/card.jpg">
<meta property="og:image:width" content="1200">
<meta property="og:image:height" content="630">
<meta name="twitter:card" content="summary_large_image">
<!--
  EMI instalment passbook — v3 (Sivaji Bank Pawnshop Manager 3.12)
  Opens:
    • E1.<hdr>.<salt>.<nonce>.<ct>.<tag>  — encrypted link (6-digit PIN). Nothing in the
      link can be read without the PIN; the live-record key travels inside.
    • L.<b64u worker>.<id>.<key>.<snapshot>  — older live link
    • <LZString snapshot>                   — oldest plain link
  All data stays in the link and this page; nothing is sent anywhere except the
  optional fetch of the shop's encrypted live record.
-->
<style>
:root{--ink:#1F2A22;--ink2:#14301F;--muted:#6B7C70;--line:#E3E9E3;--bg:#F4F7F2;--card:#fff;--gold:#C9A84C;--green:#1A7A3C;--red:#B42318;--amber:#B4520F;--blue:#1A4A8C}
*{box-sizing:border-box}
html,body{margin:0;background:var(--bg);color:var(--ink);font-family:system-ui,-apple-system,"Segoe UI",Roboto,"Noto Sans Tamil","Nirmala UI",sans-serif;-webkit-font-smoothing:antialiased}
.wrap{max-width:560px;margin:0 auto;padding:16px 16px 40px}
.hero{background:linear-gradient(135deg,#0F2A1A,#1A5C34 60%,#2C1F0A);color:#F6E7B8;border-radius:18px;padding:18px 18px 16px;box-shadow:0 10px 30px rgba(15,42,26,.25)}
.hero .s{font-weight:800;font-size:17px;letter-spacing:.2px}
.hero .st{font-size:13px;opacity:.85;margin-top:2px}
.hero .cn{font-size:20px;font-weight:800;color:#fff;margin-top:10px}
.hero .meta{font-size:12.5px;opacity:.85;margin-top:4px}
.langbar{display:flex;justify-content:flex-end;gap:6px;margin:0 0 10px}
.langbar button{border:1px solid var(--line);background:#fff;border-radius:999px;padding:5px 12px;font:inherit;font-size:12.5px;font-weight:700;color:var(--muted);cursor:pointer}
.langbar button.on{background:var(--ink2);color:#F6E7B8;border-color:var(--ink2)}
.card{background:var(--card);border:1px solid var(--line);border-radius:16px;padding:16px;margin-top:12px}
.gate{text-align:center}
.gate h2{margin:4px 0 6px;font-size:18px}
.gate p{margin:0 0 14px;color:var(--muted);font-size:13.5px;line-height:1.45}
#pin{width:100%;max-width:240px;text-align:center;font:inherit;font-family:ui-monospace,Consolas,monospace;font-size:26px;font-weight:800;letter-spacing:10px;padding:12px;border:2px solid #D8E2D8;border-radius:12px;outline:none}
#pin:focus{border-color:var(--gold)}
.btn{display:inline-flex;align-items:center;justify-content:center;gap:6px;border:0;border-radius:12px;padding:12px 18px;font:inherit;font-weight:800;font-size:15px;cursor:pointer;background:linear-gradient(135deg,#1A5C34,#12331F);color:#F6E7B8;text-decoration:none}
.btn.wide{width:100%;max-width:240px;margin-top:12px}
.err{color:var(--red);font-size:13px;font-weight:700;min-height:18px;margin-top:10px}
.bad{background:#FFF4F2;border:1px solid #F3C7C0;color:var(--red);border-radius:14px;padding:18px;margin-top:14px;font-weight:700;text-align:center}
.live{border-radius:10px;padding:8px 12px;font-size:12.5px;font-weight:700;margin-top:12px;display:none}
.grid{display:grid;grid-template-columns:1fr 1fr;gap:10px}
.k{background:#F8FBF7;border:1px solid var(--line);border-radius:12px;padding:12px}
.k .l{font-size:11px;font-weight:800;text-transform:uppercase;letter-spacing:.5px;color:var(--muted)}
.k .v{font-size:19px;font-weight:800;margin-top:3px;font-variant-numeric:tabular-nums}
.k .v.red{color:var(--red)} .k .v.green{color:var(--green)}
.bar{height:10px;background:#E8EFE8;border-radius:6px;overflow:hidden;margin:12px 0 4px}
.bar div{height:100%;background:linear-gradient(90deg,#2E8B57,#C9A84C);border-radius:6px}
.small{font-size:12px;color:var(--muted)}
.next{display:flex;justify-content:space-between;align-items:center;gap:10px}
.next b{font-size:22px}
.pay{display:grid;grid-template-columns:repeat(4,1fr);gap:8px;margin-top:12px}
.pay a{display:block;text-align:center;border:1px solid var(--line);border-radius:10px;padding:9px 4px;font-size:12.5px;font-weight:800;color:var(--blue);text-decoration:none;background:#F7FAFF}
table{width:100%;border-collapse:collapse;font-size:13px}
th{font-size:11px;text-transform:uppercase;letter-spacing:.4px;color:var(--muted);text-align:left;padding:6px 4px;border-bottom:1px solid var(--line)}
td{padding:8px 4px;border-bottom:1px solid #F0F3F0;font-variant-numeric:tabular-nums}
td.r,th.r{text-align:right}
.chip{display:inline-block;border-radius:999px;padding:2px 8px;font-size:11px;font-weight:800}
.c2{background:#E6F6EC;color:var(--green)} .c1{background:#FFF7E6;color:var(--amber)} .c0{background:#F1F3F1;color:var(--muted)} .cx{background:#FDECEA;color:var(--red)}
.more{display:block;width:100%;margin-top:10px;border:1px dashed var(--line);background:#fff;border-radius:10px;padding:9px;font:inherit;font-weight:700;color:var(--muted);cursor:pointer}
.foot{text-align:center;color:var(--muted);font-size:11.5px;margin-top:16px;line-height:1.5}
@media print{.langbar,.pay,.more,.live{display:none!important}body{background:#fff}}
</style>
</head>
<body>
<div class="wrap">
  <div class="langbar"><button id="l-en" onclick="setLang('en')">English</button><button id="l-ta" onclick="setLang('ta')">தமிழ்</button></div>
  <div class="hero"><div class="s" id="h-shop">EMI Passbook</div><div class="st" id="h-shopta" style="display:none"></div><div class="cn" id="h-cn"></div><div class="meta" id="h-meta"></div></div>
  <div id="gate" class="card gate">
    <div style="font-size:30px">🔒</div>
    <h2 data-i="gt">Enter your PIN</h2>
    <p data-i="gp">This EMI passbook is protected. Enter the PIN given to you by the shop.</p>
    <input id="pin" type="password" inputmode="numeric" autocomplete="off" maxlength="8" aria-label="PIN" onkeydown="if(event.key==='Enter')unlock()">
    <br><button class="btn wide" id="go" onclick="unlock()" data-i="open">Open</button>
    <div class="err" id="err"></div>
  </div>
  <div id="live" class="live"></div>
  <div id="book" style="display:none"></div>
  <div class="foot" data-i="foot">Figures as on the date shown. For any difference, the shop's records apply.</div>
</div>
<script>
var LZString=function(){var r=String.fromCharCode,o="ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+/=",n="ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+-$",e={};function t(r,o){if(!e[r]){e[r]={};for(var n=0;n<r.length;n++)e[r][r.charAt(n)]=n}return e[r][o]}var i={compressToBase64:function(r){if(null==r)return"";var n=i._compress(r,6,function(r){return o.charAt(r)});switch(n.length%4){default:case 0:return n;case 1:return n+"===";case 2:return n+"==";case 3:return n+"="}},decompressFromBase64:function(r){return null==r?"":""==r?null:i._decompress(r.length,32,function(n){return t(o,r.charAt(n))})},compressToUTF16:function(o){return null==o?"":i._compress(o,15,function(o){return r(o+32)})+" "},decompressFromUTF16:function(r){return null==r?"":""==r?null:i._decompress(r.length,16384,function(o){return r.charCodeAt(o)-32})},compressToUint8Array:function(r){for(var o=i.compress(r),n=new Uint8Array(2*o.length),e=0,t=o.length;e<t;e++){var s=o.charCodeAt(e);n[2*e]=s>>>8,n[2*e+1]=s%256}return n},decompressFromUint8Array:function(o){if(null==o)return i.decompress(o);for(var n=new Array(o.length/2),e=0,t=n.length;e<t;e++)n[e]=256*o[2*e]+o[2*e+1];var s=[];return n.forEach(function(o){s.push(r(o))}),i.decompress(s.join(""))},compressToEncodedURIComponent:function(r){return null==r?"":i._compress(r,6,function(r){return n.charAt(r)})},decompressFromEncodedURIComponent:function(r){return null==r?"":""==r?null:(r=r.replace(/ /g,"+"),i._decompress(r.length,32,function(o){return t(n,r.charAt(o))}))},compress:function(o){return i._compress(o,16,function(o){return r(o)})},_compress:function(r,o,n){if(null==r)return"";var e,t,i,s={},u={},a="",p="",c="",l=2,f=3,h=2,d=[],m=0,v=0;for(i=0;i<r.length;i+=1)if(a=r.charAt(i),Object.prototype.hasOwnProperty.call(s,a)||(s[a]=f++,u[a]=!0),p=c+a,Object.prototype.hasOwnProperty.call(s,p))c=p;else{if(Object.prototype.hasOwnProperty.call(u,c)){if(c.charCodeAt(0)<256){for(e=0;e<h;e++)m<<=1,v==o-1?(v=0,d.push(n(m)),m=0):v++;for(t=c.charCodeAt(0),e=0;e<8;e++)m=m<<1|1&t,v==o-1?(v=0,d.push(n(m)),m=0):v++,t>>=1}else{for(t=1,e=0;e<h;e++)m=m<<1|t,v==o-1?(v=0,d.push(n(m)),m=0):v++,t=0;for(t=c.charCodeAt(0),e=0;e<16;e++)m=m<<1|1&t,v==o-1?(v=0,d.push(n(m)),m=0):v++,t>>=1}0==--l&&(l=Math.pow(2,h),h++),delete u[c]}else for(t=s[c],e=0;e<h;e++)m=m<<1|1&t,v==o-1?(v=0,d.push(n(m)),m=0):v++,t>>=1;0==--l&&(l=Math.pow(2,h),h++),s[p]=f++,c=String(a)}if(""!==c){if(Object.prototype.hasOwnProperty.call(u,c)){if(c.charCodeAt(0)<256){for(e=0;e<h;e++)m<<=1,v==o-1?(v=0,d.push(n(m)),m=0):v++;for(t=c.charCodeAt(0),e=0;e<8;e++)m=m<<1|1&t,v==o-1?(v=0,d.push(n(m)),m=0):v++,t>>=1}else{for(t=1,e=0;e<h;e++)m=m<<1|t,v==o-1?(v=0,d.push(n(m)),m=0):v++,t=0;for(t=c.charCodeAt(0),e=0;e<16;e++)m=m<<1|1&t,v==o-1?(v=0,d.push(n(m)),m=0):v++,t>>=1}0==--l&&(l=Math.pow(2,h),h++),delete u[c]}else for(t=s[c],e=0;e<h;e++)m=m<<1|1&t,v==o-1?(v=0,d.push(n(m)),m=0):v++,t>>=1;0==--l&&(l=Math.pow(2,h),h++)}for(t=2,e=0;e<h;e++)m=m<<1|1&t,v==o-1?(v=0,d.push(n(m)),m=0):v++,t>>=1;for(;;){if(m<<=1,v==o-1){d.push(n(m));break}v++}return d.join("")},decompress:function(r){return null==r?"":""==r?null:i._decompress(r.length,32768,function(o){return r.charCodeAt(o)})},_decompress:function(o,n,e){var t,i,s,u,a,p,c,l=[],f=4,h=4,d=3,m="",v=[],g={val:e(0),position:n,index:1};for(t=0;t<3;t+=1)l[t]=t;for(s=0,a=Math.pow(2,2),p=1;p!=a;)u=g.val&g.position,g.position>>=1,0==g.position&&(g.position=n,g.val=e(g.index++)),s|=(u>0?1:0)*p,p<<=1;switch(s){case 0:for(s=0,a=Math.pow(2,8),p=1;p!=a;)u=g.val&g.position,g.position>>=1,0==g.position&&(g.position=n,g.val=e(g.index++)),s|=(u>0?1:0)*p,p<<=1;c=r(s);break;case 1:for(s=0,a=Math.pow(2,16),p=1;p!=a;)u=g.val&g.position,g.position>>=1,0==g.position&&(g.position=n,g.val=e(g.index++)),s|=(u>0?1:0)*p,p<<=1;c=r(s);break;case 2:return""}for(l[3]=c,i=c,v.push(c);;){if(g.index>o)return"";for(s=0,a=Math.pow(2,d),p=1;p!=a;)u=g.val&g.position,g.position>>=1,0==g.position&&(g.position=n,g.val=e(g.index++)),s|=(u>0?1:0)*p,p<<=1;switch(c=s){case 0:for(s=0,a=Math.pow(2,8),p=1;p!=a;)u=g.val&g.position,g.position>>=1,0==g.position&&(g.position=n,g.val=e(g.index++)),s|=(u>0?1:0)*p,p<<=1;l[h++]=r(s),c=h-1,f--;break;case 1:for(s=0,a=Math.pow(2,16),p=1;p!=a;)u=g.val&g.position,g.position>>=1,0==g.position&&(g.position=n,g.val=e(g.index++)),s|=(u>0?1:0)*p,p<<=1;l[h++]=r(s),c=h-1,f--;break;case 2:return v.join("")}if(0==f&&(f=Math.pow(2,d),d++),l[c])m=l[c];else{if(c!==h)return null;m=i+i.charAt(0)}v.push(m),l[h++]=i+m.charAt(0),i=m,0==--f&&(f=Math.pow(2,d),d++)}}};return i}();"function"==typeof define&&define.amd?define(function(){return LZString}):"undefined"!=typeof module&&null!=module?module.exports=LZString:"undefined"!=typeof angular&&null!=angular&&angular.module("LZString",[]).factory("LZString",function(){return LZString});
const I18N = {
  gt:{en:'Enter your PIN',ta:'உங்கள் PIN-ஐ உள்ளிடவும்'},
  gp:{en:'This EMI passbook is protected. Enter the PIN given to you by the shop.',ta:'இந்த EMI பாஸ்புக் பாதுகாக்கப்பட்டது. கடையில் வழங்கிய PIN-ஐ உள்ளிடவும்.'},
  open:{en:'Open',ta:'திற'},
  wrong:{en:'Wrong PIN. Please try again.',ta:'தவறான PIN. மீண்டும் முயற்சிக்கவும்.'},
  wait:{en:'Too many wrong tries. Wait {s} seconds.',ta:'பல தவறான முயற்சிகள். {s} விநாடி காத்திருக்கவும்.'},
  bad:{en:'This link is incomplete or damaged. Please ask the shop for a new one.',ta:'இந்த இணைப்பு முழுமையாக இல்லை. கடையில் புதிய இணைப்பைக் கேளுங்கள்.'},
  nocrypto:{en:'Please open this link in Chrome or Safari (it needs a secure page).',ta:'இந்த இணைப்பை Chrome அல்லது Safari-யில் திறக்கவும்.'},
  bill:{en:'Bill',ta:'பில்'},
  paid:{en:'Paid',ta:'செலுத்தியது'}, bal:{en:'Balance',ta:'மீதம்'},
  total:{en:'Total of instalments',ta:'மொத்த தவணைகள்'},
  over:{en:'Overdue',ta:'தாமதம்'}, ofn:{en:'{a} of {b} instalments paid',ta:'{b} தவணைகளில் {a} செலுத்தப்பட்டது'},
  next:{en:'Next instalment',ta:'அடுத்த தவணை'}, due:{en:'due',ta:'கெடு'}, done:{en:'All instalments are paid. Thank you!',ta:'அனைத்து தவணைகளும் செலுத்தப்பட்டன. நன்றி!'},
  sched:{en:'Instalment schedule',ta:'தவணை அட்டவணை'},
  no:{en:'No.',ta:'எண்'}, date:{en:'Due date',ta:'கெடு தேதி'}, amt:{en:'Amount',ta:'தொகை'}, st:{en:'Status',ta:'நிலை'},
  s2:{en:'Paid',ta:'செலுத்தியது'}, s1:{en:'Part paid',ta:'பகுதி'}, s0:{en:'Pending',ta:'நிலுவை'}, sx:{en:'Overdue',ta:'தாமதம்'},
  more:{en:'Show all instalments',ta:'அனைத்தையும் காட்டு'}, late:{en:'late fee',ta:'தாமதக் கட்டணம்'},
  payNow:{en:'Pay now',ta:'இப்போது செலுத்து'},
  liveOk:{en:'● Live · updated {d}',ta:'● நேரடி · புதுப்பிக்கப்பட்டது {d}'},
  liveBusy:{en:'Checking for updates…',ta:'புதுப்பிப்பைச் சரிபார்க்கிறது…'},
  liveOff:{en:'Offline — showing the details saved in this link ({d})',ta:'இணைப்பு இல்லை — இணைப்பில் சேமித்த விவரம் ({d})'},
  amtLoan:{en:'Loan',ta:'கடன்'}, rate:{en:'Rate',ta:'வட்டி'}, start:{en:'Started',ta:'தொடக்கம்'},
  foot:{en:"Figures as on the date shown. For any difference, the shop's records apply.",ta:'காட்டப்பட்ட தேதியின் படி. வேறுபாடு இருந்தால் கடையின் பதிவே இறுதியானது.'}
};
let LANG = 'en'; try { LANG = localStorage.getItem('emi_lang') || 'en'; } catch (e) {}
function T(k, v) { let s = (I18N[k] || {})[LANG] || (I18N[k] || {}).en || k; if (v) for (const x in v) s = s.replace('{' + x + '}', v[x]); return s; }
function setLang(l) { LANG = l; try { localStorage.setItem('emi_lang', l); } catch (e) {} document.querySelectorAll('[data-i]').forEach(e => { e.textContent = T(e.dataset.i); }); document.getElementById('l-en').className = l === 'en' ? 'on' : ''; document.getElementById('l-ta').className = l === 'ta' ? 'on' : ''; if (P && OPEN) render(); }
function esc(s) { return String(s == null ? '' : s).replace(/[&<>"']/g, c => ({ '&': '&amp;', '<': '&lt;', '>': '&gt;', '"': '&quot;', "'": '&#39;' }[c])); }
const inr = (n) => '₹' + Math.round(+n || 0).toLocaleString('en-IN');
const fmtD = (d) => { if (!/^\d{4}-\d{2}-\d{2}$/.test(String(d || ''))) return d || '—'; const q = d.split('-'); return q[2] + '/' + q[1] + '/' + q[0]; };
function todayIso() { const d = new Date(), p = n => String(n).padStart(2, '0'); return d.getFullYear() + '-' + p(d.getMonth() + 1) + '-' + p(d.getDate()); }
function b64uDec(str) { str = String(str).replace(/-/g, '+').replace(/_/g, '/'); while (str.length % 4) str += '='; const bin = atob(str), out = new Uint8Array(bin.length); for (let i = 0; i < bin.length; i++) out[i] = bin.charCodeAt(i); return out; }
function cat() { let n = 0; for (const a of arguments) n += a.length; const o = new Uint8Array(n); let p = 0; for (const a of arguments) { o.set(a, p); p += a.length; } return o; }
async function hkey(raw) { return crypto.subtle.importKey('raw', raw, { name: 'HMAC', hash: 'SHA-256' }, false, ['sign']); }
async function hmac(key, msg) { return new Uint8Array(await crypto.subtle.sign('HMAC', key, msg)); }

let P = null, ENC = null, LIVE = null, OPEN = false, SHOWALL = false;

// ── E1 (same sealing as the customer passbook) ───────────────────────────────
async function decEnc(pin) {
  try {
    const te = new TextEncoder();
    const base = await crypto.subtle.importKey('raw', te.encode(pin), 'PBKDF2', false, ['deriveBits']);
    const K = new Uint8Array(await crypto.subtle.deriveBits({ name: 'PBKDF2', salt: ENC.salt, iterations: 120000, hash: 'SHA-256' }, base, 256));
    const kK = await hkey(K);
    const Ke = await hmac(kK, te.encode('enc')), Km = await hmac(kK, te.encode('mac'));
    const tag = (await hmac(await hkey(Km), cat(ENC.hdrB, ENC.nonce, ENC.ct))).subarray(0, 16);
    let diff = tag.length ^ ENC.tag.length;
    for (let i = 0; i < Math.min(tag.length, ENC.tag.length); i++) diff |= tag[i] ^ ENC.tag[i];
    if (diff) return false;
    const ke = await hkey(Ke), ct = ENC.ct, pt = new Uint8Array(ct.length), jobs = [];
    for (let off = 0, c = 0; off < ct.length; off += 32, c++) jobs.push(hmac(ke, cat(ENC.nonce, new Uint8Array([c >>> 24, c >>> 16, c >>> 8, c]))).then(ks => { for (let i = 0; i < 32 && off + i < ct.length; i++) pt[off + i] = ct[off + i] ^ ks[i]; }));
    await Promise.all(jobs);
    const obj = JSON.parse(LZString.decompressFromUint8Array(pt));
    if (!obj || !obj.p || !obj.p.b) return false;
    P = obj.p;
    if (obj.lv && obj.lv.u) LIVE = { url: obj.lv.u, id: obj.lv.id, key: obj.lv.k };
    return true;
  } catch (e) { return false; }
}

// ── boot ────────────────────────────────────────────────────────────────────

// v18 · short link  #S1.<code>.<b64u worker url>  — fetch the PIN-sealed copy kept under the code,
// put it where the long link would have it, and start exactly as a long link does.
function __pbShort(boot) {
  var f = location.hash.replace(/^#/, '');
  if (f.indexOf('S1.') !== 0) return false;
  var p = f.split('.'), code = (p[1] || '').replace(/[^0-9A-Z]/g, ''), url = '';
  try { url = new TextDecoder().decode(b64uDec(p[2] || '')); } catch (e) {}
  var gate = document.getElementById('gate');
  var tl = (typeof LANG !== 'undefined' && LANG === 'ta');
  var box = document.createElement('div'); box.id = 'pb-short';
  box.style.cssText = 'margin:28px auto;max-width:420px;padding:28px 22px;border-radius:22px;background:#fff;text-align:center;box-shadow:0 18px 40px -22px rgba(10,51,64,.45);font-size:15px;line-height:1.55;color:#14323A';
  function msg(h) { box.innerHTML = h; }
  msg('<div style="width:38px;height:38px;border:3px solid rgba(15,76,92,.18);border-top-color:#0F4C5C;border-radius:50%;margin:0 auto 14px;animation:pbsr 1s linear infinite"></div><style>@keyframes pbsr{to{transform:rotate(360deg)}}</style>'
    + (tl ? 'உங்கள் பாஸ்புக் திறக்கிறது…' : 'Opening your passbook…'));
  if (gate) { gate.style.display = 'none'; gate.parentNode.insertBefore(box, gate); }
  var fail = function (gone) {
    msg('<div style="font-size:34px;margin-bottom:8px">' + (gone ? '📭' : '📶') + '</div><b>' + (gone ? (tl ? 'இந்த இணைப்பு இனி செயல்படாது' : 'This link no longer works') : (tl ? 'உங்கள் பாஸ்புக்கை இப்போது ஏற்ற முடியவில்லை' : 'Couldn’t load your passbook')) + '</b><br>'
      + (gone ? (tl ? 'கடையில் புதிய இணைப்பை அனுப்பச் சொல்லவும்.' : 'Please ask the shop to send a new link.') : (tl ? 'இணைய இணைப்பைச் சரிபார்த்து மீண்டும் முயற்சிக்கவும்.' : 'Check your internet and try again in a few minutes.'))
      + (gone ? '' : '<br><button onclick="location.reload()" style="margin-top:14px;padding:11px 22px;border:0;border-radius:12px;background:#0F4C5C;color:#fff;font-weight:700;font-size:15px">' + (tl ? 'மீண்டும் முயற்சி' : 'Try again') + '</button>'));
  };
  if (!code || !/^https:\/\//.test(url) && !/^http:\/\/(localhost|127\.)/.test(url)) { fail(true); return true; }
  fetch(url.replace(/\/+$/, '') + '/p/S' + code, { cache: 'no-store' }).then(function (r) {
    if (r.status === 404) { fail(true); return null; }
    if (!r.ok) throw 0;
    return r.text();
  }).then(function (t) {
    if (t == null) return;
    t = String(t).trim();
    if (t.indexOf('E1.') !== 0 || t.split('.').length !== 6) { fail(true); return; }
    try { history.replaceState(null, '', location.pathname + location.search + '#' + t); } catch (e) { location.replace(location.pathname + location.search + '#' + t); return; }
    box.remove(); if (gate) gate.style.display = '';
    boot();
  }).catch(function () { fail(false); });
  return true;
}
function boot() {
  try {
    let frag = location.hash.replace(/^#/, '');
    if (frag.indexOf('E1.') === 0) {
      const parts = frag.split('.');
      if (parts.length !== 6) throw 0;
      const hdrB = b64uDec(parts[1]);
      ENC = { hdr: JSON.parse(new TextDecoder().decode(hdrB)), hdrB, salt: b64uDec(parts[2]), nonce: b64uDec(parts[3]), ct: b64uDec(parts[4]), tag: b64uDec(parts[5]) };
      if (!(window.crypto && crypto.subtle)) { document.getElementById('gate').outerHTML = '<div class="bad">' + T('nocrypto') + '</div>'; return; }
      head(ENC.hdr.sn, ENC.hdr.st, '', '');
      document.getElementById('pin').maxLength = Math.min(8, Math.max(6, +ENC.hdr.pl || 6));
    } else {
      if (frag.charAt(0) === 'L' && frag.charAt(1) === '.') {
        const parts = frag.split('.');
        if (parts.length >= 5) { try { LIVE = { url: new TextDecoder().decode(b64uDec(parts[1])), id: parts[2], key: parts[3] }; } catch (e) { LIVE = null; } frag = parts.slice(4).join('.'); }
      }
      if (!frag) throw 0;
      P = JSON.parse(LZString.decompressFromEncodedURIComponent(frag));
      if (!P || !P.b) throw 0;
      head(P.sn, P.snt, P.cn, '');
    }
  } catch (e) {
    document.getElementById('gate').outerHTML = '<div class="bad" data-i="bad">' + T('bad') + '</div>';
  }
  setLang(LANG);
  setTimeout(() => { const p = document.getElementById('pin'); if (p) p.focus(); }, 300);
}
if (!__pbShort(boot)) boot();
function head(sn, st, cn, meta) {
  document.getElementById('h-shop').textContent = '📗 ' + (sn || 'EMI Passbook');
  const e = document.getElementById('h-shopta'); if (st) { e.textContent = st; e.style.display = 'block'; } else e.style.display = 'none';
  document.getElementById('h-cn').textContent = cn || '';
  document.getElementById('h-meta').textContent = meta || '';
}

// ── PIN ─────────────────────────────────────────────────────────────────────
function lockState() { try { return JSON.parse(sessionStorage.getItem('emi_lock') || '{"n":0,"u":0}'); } catch (e) { return { n: 0, u: 0 }; } }
function setLock(s) { try { sessionStorage.setItem('emi_lock', JSON.stringify(s)); } catch (e) {} }
let busy = false;
async function unlock() {
  if (busy) return;
  const err = document.getElementById('err'), inp = document.getElementById('pin');
  const L = lockState();
  if (Date.now() < L.u) { err.textContent = T('wait', { s: Math.ceil((L.u - Date.now()) / 1000) }); return; }
  const pin = (inp.value || '').trim();
  if (!pin) return;
  busy = true; document.getElementById('go').disabled = true; err.textContent = '';
  let ok = false;
  try { ok = ENC ? await decEnc(pin) : (String(P.sec || '') !== '' && pin === String(P.sec)); } catch (e) { ok = false; }
  busy = false; document.getElementById('go').disabled = false;
  if (!ok) {
    L.n = (L.n || 0) + 1;
    if (L.n >= 5) { L.u = Date.now() + 30000; L.n = 0; err.textContent = T('wait', { s: 30 }); } else err.textContent = T('wrong');
    setLock(L); inp.value = ''; inp.focus(); return;
  }
  setLock({ n: 0, u: 0 });
  OPEN = true;
  document.getElementById('gate').style.display = 'none';
  render();
  refreshLive();
}

// ── schedule rows: [m, due, emi, paidAmount, paidDate, lateFee, status] ─────
function rows() {
  if (Array.isArray(P.s)) return P.s;
  if (P.n && P.d0) {
    const base = P.m0 != null ? P.m0 : ((P.x || []).some(r => r[0] === 0) || (P.pf || []).some(r => r[0] === 0) ? 0 : 1);
    const out = [], X = {};
    (P.x || []).forEach(r => { X[r[0]] = r; });
    const paid = (m) => (P.pf || []).some(r => m >= r[0] && m <= r[1]);
    const p = n => String(n).padStart(2, '0'), iso = d => d.getFullYear() + '-' + p(d.getMonth() + 1) + '-' + p(d.getDate());
    const at = (i) => {
      const d = new Date(P.d0 + 'T00:00:00');
      if (P.stp === 'M') { d.setMonth(d.getMonth() + i); return iso(d); }
      if (P.stp === 'm') { const day = d.getDate(); d.setDate(1); d.setMonth(d.getMonth() + i); d.setDate(Math.min(day, new Date(d.getFullYear(), d.getMonth() + 1, 0).getDate())); return iso(d); }
      d.setDate(d.getDate() + i); return iso(d);
    };
    for (let i = 0; i < P.n; i++) {
      const m = base + i, due = at(i);
      if (X[m]) out.push(X[m]); else if (paid(m)) out.push([m, due, P.de, P.de, due, 0, 2]); else out.push([m, due, P.de, 0, '', 0, 0]);
    }
    return out;
  }
  return [];
}
function render() {
  const R = rows(), t = todayIso();
  const total = R.reduce((s, r) => s + (+r[2] || 0), 0);
  const paid = R.reduce((s, r) => s + (+r[3] || 0), 0);
  const nPaid = R.filter(r => r[6] === 2).length;
  const overdue = R.filter(r => r[6] !== 2 && r[1] && r[1] < t);
  const nxt = R.find(r => r[6] !== 2);
  const pct = total ? Math.min(100, Math.round(paid / total * 100)) : 0;
  head(P.sn, P.snt, P.cn, T('bill') + ' ' + (P.b || '') + (P.tn ? ' · ' + P.tn : '') + (P.sd ? ' · ' + T('start') + ' ' + fmtD(P.sd) : ''));
  let h = '<div class="card"><div class="grid">'
    + '<div class="k"><div class="l">' + T('paid') + '</div><div class="v green">' + inr(paid) + '</div></div>'
    + '<div class="k"><div class="l">' + T('bal') + '</div><div class="v">' + inr(Math.max(0, total - paid)) + '</div></div>'
    + '<div class="k"><div class="l">' + T('total') + '</div><div class="v">' + inr(total) + '</div></div>'
    + '<div class="k"><div class="l">' + T('over') + '</div><div class="v' + (overdue.length ? ' red' : '') + '">' + overdue.length + '</div></div>'
    + '</div><div class="bar"><div style="width:' + pct + '%"></div></div><div class="small">' + T('ofn', { a: nPaid, b: R.length }) + ' · ' + pct + '%'
    + (P.am ? ' · ' + T('amtLoan') + ' ' + inr(P.am) : '') + (P.r ? ' · ' + T('rate') + ' ' + P.r + '%' : '') + '</div></div>';
  if (nxt) {
    const amt = Math.max(0, (+nxt[2] || 0) - (+nxt[3] || 0)) + (overdue.length > 1 ? overdue.slice(1).reduce((s, r) => s + Math.max(0, r[2] - r[3]), 0) : 0);
    h += '<div class="card"><div class="next"><div><div class="small">' + T('next') + ' · ' + T('due') + ' ' + fmtD(nxt[1]) + '</div><b>' + inr(Math.max(0, nxt[2] - nxt[3])) + '</b></div>'
      + (overdue.length ? '<span class="chip cx">' + overdue.length + ' ' + T('sx') + '</span>' : '') + '</div>';
    if (P.upi && P.upi.pa) {
      const q = 'pa=' + encodeURIComponent(P.upi.pa) + '&pn=' + encodeURIComponent(P.upi.pn || P.sn || '') + '&am=' + amt + '&cu=INR&tn=' + encodeURIComponent('EMI ' + (P.b || ''));
      h += '<div class="small" style="margin-top:10px;font-weight:700">' + T('payNow') + ' · ' + inr(amt) + '</div><div class="pay">'
        + '<a href="tez://upi/pay?' + q + '">GPay</a><a href="phonepe://pay?' + q + '">PhonePe</a><a href="paytmmp://pay?' + q + '">Paytm</a><a href="upi://pay?' + q + '">UPI</a></div>';
    }
    h += '</div>';
  } else h += '<div class="card" style="text-align:center;font-weight:800;color:var(--green)">✅ ' + T('done') + '</div>';
  // schedule: around the next due row unless "show all"
  let list = R, cut = false;
  if (!SHOWALL && R.length > 14) { const i = Math.max(0, R.indexOf(nxt || R[R.length - 1]) - 4); list = R.slice(i, i + 12); cut = true; }
  h += '<div class="card"><div style="font-weight:800;margin-bottom:6px">' + T('sched') + '</div><table><thead><tr><th>' + T('no') + '</th><th>' + T('date') + '</th><th class="r">' + T('amt') + '</th><th class="r">' + T('st') + '</th></tr></thead><tbody>'
    + list.map(r => {
      const late = r[6] !== 2 && r[1] && r[1] < t;
      const cls = r[6] === 2 ? 'c2' : late ? 'cx' : r[6] === 1 ? 'c1' : 'c0', lbl = r[6] === 2 ? T('s2') : late ? T('sx') : r[6] === 1 ? T('s1') : T('s0');
      return '<tr><td>' + esc(r[0]) + '</td><td>' + fmtD(r[1]) + (r[4] && r[6] ? '<div class="small">' + T('paid') + ' ' + fmtD(r[4]) + '</div>' : '') + '</td><td class="r">' + inr(r[2])
        + (r[6] === 1 ? '<div class="small">' + T('paid') + ' ' + inr(r[3]) + '</div>' : '') + (r[5] ? '<div class="small">+' + inr(r[5]) + ' ' + T('late') + '</div>' : '') + '</td><td class="r"><span class="chip ' + cls + '">' + lbl + '</span></td></tr>';
    }).join('') + '</tbody></table>' + (cut ? '<button class="more" onclick="SHOWALL=true;render()">' + T('more') + ' (' + R.length + ')</button>' : '') + '</div>';
  const b = document.getElementById('book'); b.innerHTML = h; b.style.display = 'block';
}

// ── live record (encrypted on the shop's Worker; key only inside the link) ──
function liveBanner(kind, text) {
  const el = document.getElementById('live'); el.style.display = 'block'; el.textContent = text;
  const c = { live: ['#E6F6EC', '#1A5C2C'], stale: ['#FFF7E6', '#8A5A00'], busy: ['#EEF3F8', '#3A5A7A'] }[kind];
  el.style.background = c[0]; el.style.color = c[1];
}
function refreshLive() {
  if (!LIVE || !LIVE.url || !LIVE.id || !LIVE.key || !(window.crypto && crypto.subtle)) return;
  liveBanner('busy', T('liveBusy'));
  fetch(LIVE.url.replace(/\/+$/, '') + '/p/' + encodeURIComponent(LIVE.id) + '?t=' + Date.now(), { cache: 'no-store', referrerPolicy: 'no-referrer' })
    .then(r => { if (!r.ok) throw new Error('HTTP ' + r.status); return r.text(); })
    .then(blob => { const raw = b64uDec(blob.trim()); return crypto.subtle.importKey('raw', b64uDec(LIVE.key), 'AES-GCM', false, ['decrypt']).then(k => crypto.subtle.decrypt({ name: 'AES-GCM', iv: raw.slice(0, 12) }, k, raw.slice(12))); })
    .then(pt => {
      const fresh = JSON.parse(new TextDecoder().decode(pt));
      const plan = (fresh.plans || []).find(x => String(x.b) === String(P.b));
      if (!plan) throw new Error('plan not in record');
      delete plan.sec; P = plan; render();
      const d = fresh.ts ? new Date(fresh.ts) : new Date();
      liveBanner('live', T('liveOk', { d: String(d.getDate()).padStart(2, '0') + '/' + String(d.getMonth() + 1).padStart(2, '0') + '/' + d.getFullYear() }));
    })
    .catch(() => liveBanner('stale', T('liveOff', { d: fmtD(P.gen) })));
}
</script>
</body>
</html>
