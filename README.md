
<!DOCTYPE html>
<html lang="en"><head><meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Windows 11 Web</title>
<style>
:root{--win:#fff;--tx:#1b1b1f;--bar:rgba(243,243,243,.92);--bd:#d0d4dc;--ac:#0067c0;--hv:rgba(0,0,0,.07);--in:#f6f7f9;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media(prefers-color-scheme:dark){:root:not([data-theme=light]){--win:#2b2b2f;--tx:#f3f3f3;--bar:rgba(32,32,36,.92);--bd:#46464c;--hv:rgba(255,255,255,.1);--in:#38383d}}
:root[data-theme=dark]{--win:#2b2b2f;--tx:#f3f3f3;--bar:rgba(32,32,36,.92);--bd:#46464c;--hv:rgba(255,255,255,.1);--in:#38383d}
*{box-sizing:border-box}
html,body{height:100%;margin:0;overflow:hidden;font-family:"Segoe UI",system-ui,sans-serif;color:var(--tx);background:#16213e;font-size:14px}
body{display:flex;flex-direction:column}
#desk{flex:1;position:relative;overflow:hidden;background:linear-gradient(135deg,#7ec8ff,#2a5bd7 55%,#1b2a6b)}
#icons{position:absolute;inset:8px;display:flex;flex-direction:column;flex-wrap:wrap;align-content:flex-start;gap:4px;pointer-events:none}
.ic{width:80px;padding:6px 2px;text-align:center;color:#fff;text-shadow:0 1px 3px #000a;border-radius:6px;cursor:default;pointer-events:auto;font-size:12px}
.ic span{display:block;font-size:32px}.ic:hover,.ic.s{background:#fff3}
.w{position:absolute;background:var(--win);border:1px solid var(--bd);border-radius:8px;box-shadow:0 10px 36px #0006;display:flex;flex-direction:column;overflow:hidden;min-width:250px;min-height:170px;resize:both}
.w.max{inset:0!important;width:auto!important;height:auto!important;border-radius:0;resize:none}
.th{display:flex;align-items:center;height:34px;padding-left:10px;background:var(--bar);cursor:move;user-select:none;touch-action:none;flex:none}
.th b{flex:1;font-weight:400;font-size:12.5px;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;padding-left:4px}
.th button{width:42px;height:34px;border:0;background:none;color:inherit;cursor:pointer;font-size:13px}
.th button:hover{background:var(--hv)}.th .x:hover{background:#c42b1c;color:#fff}
.bd{flex:1;overflow:auto;display:flex;flex-direction:column;min-height:0}
.tl{display:flex;flex-wrap:wrap;gap:4px;padding:6px;border-bottom:1px solid var(--bd);align-items:center;flex:none}
.tl button,.tl select{border:1px solid var(--bd);background:var(--in);color:inherit;border-radius:5px;padding:4px 9px;cursor:pointer;font:inherit}
.tl button:hover{background:var(--hv)}
.pth{margin-left:auto;font-size:12px;opacity:.7}
.row{flex:1;display:flex;min-height:0}
.sd{width:130px;border-right:1px solid var(--bd);padding:6px;flex:none}
.sd div{padding:6px 8px;border-radius:5px;cursor:pointer}.sd div:hover{background:var(--hv)}
.ls{flex:1;padding:8px;display:flex;flex-wrap:wrap;align-content:flex-start;gap:6px;overflow:auto}
.it{width:92px;padding:8px 4px;text-align:center;border-radius:6px;font-size:12px;word-break:break-word;cursor:default;border:1px solid transparent}
.it span{display:block;font-size:34px}.it:hover{background:var(--hv)}.it.s{background:#0067c033;border-color:var(--ac)}
.pp{flex:1;margin:12px auto;width:min(720px,94%);background:#fff;color:#111;padding:28px 34px;box-shadow:0 1px 8px #0003;outline:0;overflow:auto;font:16px/1.5 Georgia,serif}
.ad{flex:1;min-width:120px;border:1px solid var(--bd)!important;background:var(--in);color:inherit;border-radius:16px!important;padding:5px 12px}
iframe{flex:1;border:0;background:#fff;width:100%}
.hm{margin:auto;text-align:center;padding:20px}.hm h2{font-weight:300;font-size:30px;margin:0 0 14px}
.hm input{width:min(420px,90%);padding:10px 16px;border-radius:24px;border:1px solid var(--bd);background:var(--in);color:inherit;font:inherit}
.hm a{display:inline-block;margin:12px 8px 0;color:var(--ac);cursor:pointer}
.nb{padding:5px 10px;font-size:12px;background:var(--in);border-bottom:1px solid var(--bd)}.nb a{color:var(--ac)}
.cd{display:grid;grid-template-columns:repeat(4,1fr);gap:4px;padding:8px;flex:1}
.cd button{border:0;border-radius:6px;background:var(--in);color:inherit;font-size:18px;cursor:pointer}.cd button:hover{background:var(--hv)}.cd .eq{background:var(--ac);color:#fff}
.dp{padding:14px 16px;font-size:30px;text-align:right;min-height:64px;word-break:break-all}
canvas{max-width:100%;background:#fff;touch-action:none;cursor:crosshair;margin:auto}
.st{padding:16px;display:flex;flex-direction:column;gap:12px}.st button{margin-right:6px;padding:7px 12px;border:1px solid var(--bd);background:var(--in);color:inherit;border-radius:6px;cursor:pointer}
#tb{height:48px;flex:none;background:var(--bar);border-top:1px solid var(--bd);display:flex;align-items:center;justify-content:center;position:relative;backdrop-filter:blur(20px);z-index:9999}
#tbar{display:flex;gap:4px}
.tbi{width:42px;height:40px;border:0;border-radius:6px;background:none;font-size:20px;cursor:pointer;color:inherit;position:relative}
.tbi:hover{background:var(--hv)}.tbi.on::after{content:"";position:absolute;left:14px;right:14px;bottom:2px;height:3px;border-radius:2px;background:var(--ac)}
.lg{display:grid;grid-template-columns:7px 7px;gap:2px}.lg i{width:7px;height:7px;background:#0a84ff;display:block}
#clk{position:absolute;right:10px;text-align:right;font-size:12px;line-height:1.3}
#sm{position:absolute;left:50%;bottom:56px;transform:translateX(-50%);width:min(420px,96vw);background:var(--bar);backdrop-filter:blur(24px);border:1px solid var(--bd);border-radius:12px;padding:18px;display:none;z-index:9998;box-shadow:0 10px 40px #0006}
#sm h4{margin:0 0 10px;font-weight:600}.pg{display:grid;grid-template-columns:repeat(3,1fr);gap:6px}
.pg div{padding:10px 4px;text-align:center;border-radius:8px;cursor:pointer;font-size:12px}.pg div:hover{background:var(--hv)}.pg span{display:block;font-size:30px}
#sm footer{margin-top:14px;padding-top:10px;border-top:1px solid var(--bd);display:flex;justify-content:space-between;align-items:center}
#sm footer button{border:1px solid var(--bd);background:var(--in);color:inherit;border-radius:6px;padding:5px 10px;cursor:pointer}
.md{position:fixed;inset:0;background:#0006;display:flex;align-items:center;justify-content:center;z-index:99999}
.md>div{background:var(--win);padding:16px 18px;border-radius:10px;min-width:260px;box-shadow:0 10px 40px #0008}
.md input{width:100%;padding:7px;border:1px solid var(--bd);background:var(--in);color:inherit;border-radius:5px}.md button{padding:5px 14px;margin-right:6px;cursor:pointer}
</style></head><body>
<div id="desk"><div id="icons"></div></div>
<div id="sm"><h4>Pinned</h4><div class="pg" id="pin"></div><footer><span>👤 Guest user</span><button id="rs">⟳ Restart</button></footer></div>
<div id="tb"><div id="tbar"><button class="tbi" id="sb" title="Start"><div class="lg" style="margin:auto"><i></i><i></i><i></i><i></i></div></button></div><div id="clk"></div></div>
<script>
const $=s=>document.querySelector(s);
let fs={Desktop:{},Documents:{'Welcome.doc':'<h2>Welcome to Windows 11 Web</h2><p>Edit this document, then press Save. Create folders and files in File Explorer.</p>'},Downloads:{},Pictures:{}};
try{const s=localStorage.getItem('w11fs');if(s)fs=JSON.parse(s)}catch(e){}
const persist=()=>{try{localStorage.setItem('w11fs',JSON.stringify(fs))}catch(e){}};
const dirAt=p=>p.reduce((d,k)=>d[k],fs);
function ask(t,d,cb){const m=document.createElement('div');m.className='md';m.innerHTML=`<div><p>${t}</p><input><p><button>OK</button><button>Cancel</button></p></div>`;document.body.append(m);const i=m.querySelector('input'),bs=m.querySelectorAll('button');i.value=d;i.focus();i.select();const go=ok=>{m.remove();if(ok&&i.value.trim())cb(i.value.trim())};bs[0].onclick=()=>go(1);bs[1].onclick=()=>go(0);i.onkeydown=e=>e.key=='Enter'&&go(1)}
let z=10,wins=[];
function win(title,icon,w,h,build){
 const el=document.createElement('div');el.className='w';const n=wins.length%6;
 el.style.cssText=`left:${40+n*28}px;top:${24+n*28}px;width:${Math.min(w,innerWidth-8)}px;height:${Math.min(h,innerHeight-70)}px;z-index:${++z}`;
 el.innerHTML=`<div class=th><span>${icon}</span><b>${title}</b><button class=m>–</button><button class=mx>▢</button><button class=x>✕</button></div><div class=bd></div>`;
 $('#desk').append(el);
 const tb=document.createElement('button');tb.className='tbi';tb.textContent=icon;tb.title=title;$('#tbar').append(tb);
 const o={el,tb};wins.push(o);
 const focus=()=>{el.style.display='flex';el.style.zIndex=++z;wins.forEach(q=>q.tb.classList.toggle('on',q===o))};
 el.addEventListener('pointerdown',focus);
 tb.onclick=()=>{if(el.style.display=='none'||!tb.classList.contains('on'))focus();else{el.style.display='none';tb.classList.remove('on')}};
 el.querySelector('.m').onclick=e=>{e.stopPropagation();el.style.display='none';tb.classList.remove('on')};
 const mx=()=>el.classList.toggle('max');el.querySelector('.mx').onclick=mx;
 el.querySelector('.x').onclick=()=>{el.remove();tb.remove();wins=wins.filter(q=>q!==o)};
 const th=el.querySelector('.th');let dr=null;
 th.addEventListener('dblclick',mx);
 th.addEventListener('pointerdown',e=>{if(e.target.tagName=='BUTTON'||el.classList.contains('max'))return;dr=[e.clientX-el.offsetLeft,e.clientY-el.offsetTop];th.setPointerCapture(e.pointerId)});
 th.addEventListener('pointermove',e=>{if(dr){el.style.left=Math.max(-100,e.clientX-dr[0])+'px';el.style.top=Math.max(0,e.clientY-dr[1])+'px'}});
 th.addEventListener('pointerup',()=>dr=null);
 if(innerWidth<640)el.classList.add('max');
 build(el.querySelector('.bd'),o);focus();return o}
const apps={
files:{n:'File Explorer',i:'📁',f:explorer},docs:{n:'Documents',i:'📝',f:docs,w:680,h:480},edge:{n:'Microsoft Edge',i:'🌐',f:edge,w:760,h:480},
calc:{n:'Calculator',i:'🧮',f:calc,w:300,h:420},paint:{n:'Paint',i:'🎨',f:paint,w:620,h:460},set:{n:'Settings',i:'⚙️',f:settings,w:460,h:340}};
function open(id,a){const p=apps[id];win(p.n,p.i,p.w||600,p.h||400,(b,o)=>p.f(b,o,a))}
function explorer(b,o){
 let p=['Documents'],sel=null;
 b.innerHTML=`<div class=tl><button data-a=up>⬆ Up</button><button data-a=nd>＋ Folder</button><button data-a=nf>＋ Document</button><button data-a=rn>Rename</button><button data-a=del>🗑 Delete</button><span class=pth></span></div><div class=row><div class=sd></div><div class=ls></div></div>`;
 const ls=b.querySelector('.ls'),sd=b.querySelector('.sd');
 sd.innerHTML=Object.keys(fs).map(k=>`<div data-k="${k}">📁 ${k}</div>`).join('');
 function render(){sel=null;const d=dirAt(p);b.querySelector('.pth').textContent='This PC > '+p.join(' > ');o.el.querySelector('.th b').textContent=p[p.length-1]+' – File Explorer';
  const ks=Object.keys(d);ls.innerHTML=ks.length?ks.map(k=>`<div class=it data-n="${k}"><span>${typeof d[k]=='object'?'📁':'📄'}</span>${k}</div>`).join(''):'<p style="opacity:.6;padding:10px">This folder is empty.</p>'}
 sd.onclick=e=>{const k=e.target.dataset.k;if(k){p=[k];render()}};
 ls.onclick=e=>{const it=e.target.closest('.it');ls.querySelectorAll('.s').forEach(x=>x.classList.remove('s'));if(it){it.classList.add('s');sel=it.dataset.n}else sel=null};
 ls.ondblclick=e=>{const it=e.target.closest('.it');if(!it)return;const v=dirAt(p)[it.dataset.n];if(typeof v=='object'){p.push(it.dataset.n);render()}else open('docs',{path:[...p,it.dataset.n]})};
 b.querySelector('.tl').onclick=e=>{const a=e.target.dataset.a,d=dirAt(p);if(!a)return;
  if(a=='up'&&p.length>1){p.pop();render()}
  if(a=='nd')ask('New folder name','New folder',v=>{d[v]={};persist();render()});
  if(a=='nf')ask('Document name','Untitled.doc',v=>{d[v]='';persist();render()});
  if(a=='rn'&&sel)ask('Rename to',sel,v=>{d[v]=d[sel];delete d[sel];persist();render()});
  if(a=='del'&&sel){delete d[sel];persist();render()}};
 render()}
function docs(b,o,a){
 let path=a&&a.path;
 b.innerHTML=`<div class=tl><button data-c=bold><b>B</b></button><button data-c=italic><i>I</i></button><button data-c=underline><u>U</u></button><button data-c=insertUnorderedList>• List</button><button data-c=justifyLeft>Left</button><button data-c=justifyCenter>Center</button><select><option value=3>Normal</option><option value=2>Small</option><option value=5>Large</option><option value=6>Huge</option></select><button data-c=save>💾 Save</button><span class=pth></span></div><div class=pp contenteditable>${path?dirAt(path.slice(0,-1))[path[path.length-1]]:'<p>Start typing…</p>'}</div>`;
 const pp=b.querySelector('.pp'),st=b.querySelector('.pth'),ttl=()=>o.el.querySelector('.th b').textContent=(path?path[path.length-1]:'Untitled')+' – Documents';ttl();
 b.querySelector('.tl').onmousedown=e=>{if(e.target.tagName!='SELECT')e.preventDefault()};
 b.querySelector('.tl').onclick=e=>{const c=e.target.closest('button')?.dataset.c;if(!c)return;
  if(c!='save')return document.execCommand(c);
  const w=n=>{path=['Documents',n];fs.Documents[n]=pp.innerHTML;persist();ttl();st.textContent='Saved'};
  if(path)dirAt(path.slice(0,-1))[path[path.length-1]]=pp.innerHTML,persist(),st.textContent='Saved';else ask('Save as','Untitled.doc',w)};
 b.querySelector('select').onchange=e=>{pp.focus();document.execCommand('fontSize',false,e.target.value)}}
function edge(b){
 b.innerHTML=`<div class=tl><button data-a=h>🏠</button><input class="ad" placeholder="Search or enter web address"><button data-a=g>Go</button></div><div class=hm><h2>Microsoft Edge</h2><input placeholder="Search the web or type a URL"><div><a data-u="wikipedia.org">Wikipedia</a><a data-u="openstreetmap.org">OpenStreetMap</a><a data-u="example.com">Example</a></div></div>`;
 const ad=b.querySelector('.ad');
 const go=v=>{v=v.trim();if(!v)return;const url=/^https?:\/\//.test(v)?v:/^[\w-]+(\.[\w-]+)+(\/.*)?$/.test(v)?'https://'+v:'https://duckduckgo.com/?q='+encodeURIComponent(v);ad.value=url;
  b.querySelectorAll('iframe,.nb,.hm').forEach(x=>x.remove());
  b.insertAdjacentHTML('beforeend',`<div class=nb>Blank page? Many sites block embedding. <a href="${url}" target=_blank rel=noopener>Open in a new browser tab</a></div><iframe src="${url}"></iframe>`)};
 b.onclick=e=>{const a=e.target.dataset;if(a.u)go(a.u);if(a.a=='g')go(ad.value);if(a.a=='h')edge(b)};
 b.onkeydown=e=>{if(e.key=='Enter'&&e.target.tagName=='INPUT')go(e.target.value)}}
function calc(b){
 b.innerHTML=`<div class=dp>0</div><div class=cd></div>`;const dp=b.querySelector('.dp');let s='';
 '7 8 9 ÷ 4 5 6 × 1 2 3 − 0 . C +  ( ) ⌫ ='.split(' ').filter(Boolean).forEach(k=>{const x=document.createElement('button');x.textContent=k;if(k=='=')x.className='eq';
  x.onclick=()=>{if(k=='C')s='';else if(k=='⌫')s=s.slice(0,-1);else if(k=='='){try{const e=s.replace(/×/g,'*').replace(/÷/g,'/').replace(/−/g,'-');if(/^[\d+\-*/.() ]+$/.test(e))s=String(+Function('return '+e)().toFixed(10))}catch(_){s='Error'}}else s+=k;dp.textContent=s||'0'};b.querySelector('.cd').append(x)})}
function paint(b){
 b.innerHTML=`<div class=tl><input type=color value="#0067c0"><input type=range min=1 max=30 value=4><button>Clear</button></div><canvas width=560 height=340></canvas>`;
 const c=b.querySelector('canvas'),x=c.getContext('2d'),[col,sz]=b.querySelectorAll('input');let d=0;
 const cl=()=>{x.fillStyle='#fff';x.fillRect(0,0,560,340)};cl();b.querySelector('button').onclick=cl;
 const pt=e=>{const r=c.getBoundingClientRect();return[(e.clientX-r.left)*560/r.width,(e.clientY-r.top)*340/r.height]};
 c.onpointerdown=e=>{d=1;c.setPointerCapture(e.pointerId);const[a,y]=pt(e);x.beginPath();x.moveTo(a,y)};
 c.onpointermove=e=>{if(!d)return;const[a,y]=pt(e);x.strokeStyle=col.value;x.lineWidth=sz.value;x.lineCap='round';x.lineTo(a,y);x.stroke()};
 c.onpointerup=()=>d=0}
function settings(b){
 b.innerHTML=`<div class=st><b>Theme</b><div><button data-t=light>Light</button><button data-t=dark>Dark</button></div><b>Wallpaper</b><div><button data-w="linear-gradient(135deg,#7ec8ff,#2a5bd7 55%,#1b2a6b)">Bloom</button><button data-w="linear-gradient(135deg,#ffb88c,#de6262)">Sunset</button><button data-w="linear-gradient(135deg,#134e5e,#71b280)">Forest</button></div><p style="opacity:.7">Windows 11 Web · files are saved in this browser only.</p></div>`;
 b.onclick=e=>{const d=e.target.dataset;if(d.t)document.documentElement.dataset.theme=d.t;if(d.w)$('#desk').style.background=d.w}}
Object.entries(apps).forEach(([id,a])=>{
 $('#icons').insertAdjacentHTML('beforeend',`<div class=ic data-id=${id}><span>${a.i}</span>${a.n}</div>`);
 $('#pin').insertAdjacentHTML('beforeend',`<div data-id=${id}><span>${a.i}</span>${a.n}</div>`)});
$('#icons').ondblclick=e=>{const i=e.target.closest('.ic');if(i)open(i.dataset.id)};
$('#icons').onclick=e=>{const i=e.target.closest('.ic');document.querySelectorAll('.ic.s').forEach(x=>x.classList.remove('s'));if(i){i.classList.add('s');if(matchMedia('(pointer:coarse)').matches)open(i.dataset.id)}};
$('#pin').onclick=e=>{const i=e.target.closest('[data-id]');if(i){open(i.dataset.id);$('#sm').style.display='none'}};
$('#sb').onclick=e=>{e.stopPropagation();const m=$('#sm');m.style.display=m.style.display=='block'?'none':'block'};
document.addEventListener('pointerdown',e=>{if(!e.target.closest('#sm,#sb'))$('#sm').style.display='none'});
$('#rs').onclick=()=>{wins.slice().forEach(w=>w.el.querySelector('.x').click());$('#sm').style.display='none'};
const tick=()=>{const d=new Date();$('#clk').innerHTML=d.toLocaleTimeString([],{hour:'numeric',minute:'2-digit'})+'<br>'+d.toLocaleDateString()};tick();setInterval(tick,15000);
open('files');
</script></body></html>

