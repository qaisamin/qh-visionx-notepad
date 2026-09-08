from pathlib import Path
import zipfile, json, re

root=Path("/mnt/data/qh-visionx-notepad-v2")
root.mkdir(exist_ok=True)

html=r'''<!doctype html>
<html lang="fa" dir="rtl">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover">
<meta name="theme-color" content="#07111f">
<meta name="description" content="QH VisionX Notepad v2 — Professional Persian RTL Notepad">
<meta name="application-name" content="QH VisionX Notepad">
<title>QH VisionX Notepad v2</title>
<link rel="manifest" href="manifest.json">
<link rel="icon" href="favicon.svg" type="image/svg+xml">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Vazirmatn:wght@400;500;600;700;800&display=swap" rel="stylesheet">
<link rel="stylesheet" href="style.css">
</head>
<body>
<div id="app">
<header class="topbar">
  <div class="brand"><div class="brand-mark">QH</div><div><strong>QH VisionX</strong><small>NOTEPAD <b>v2</b></small></div></div>
  <div class="top-search"><span>⌕</span><input id="globalSearch" placeholder="جستجو در یادداشت‌ها..." aria-label="جستجوی یادداشت‌ها"><kbd>Ctrl K</kbd></div>
  <div class="top-actions">
    <button id="mobileMenu" class="icon-btn" aria-label="منو">☰</button>
    <button id="themeBtn" class="icon-btn" aria-label="تغییر حالت">☾</button>
    <button id="backupBtn" class="text-btn">پشتیبان</button>
    <button id="newBtn" class="primary">＋ یادداشت جدید</button>
  </div>
</header>

<div class="layout">
<aside id="sidebar">
  <div class="side-head"><span>فضای یادداشت‌ها</span><button id="closeSide" class="icon-btn">×</button></div>
  <button id="newSide" class="new-side">＋ یادداشت جدید</button>
  <nav class="nav">
    <button class="nav-item active" data-filter="all">📝 <span>همه یادداشت‌ها</span><b id="allCount">0</b></button>
    <button class="nav-item" data-filter="favorite">⭐ <span>مورد علاقه‌ها</span><b id="favCount">0</b></button>
    <button class="nav-item" data-filter="trash">🗑️ <span>سطل زباله</span><b id="trashCount">0</b></button>
  </nav>
  <div class="section-title">برچسب‌ها</div>
  <div id="tags" class="tags"></div>
  <div class="side-footer">ذخیره محلی فعال است<br><small>یادداشت‌ها روی همین دستگاه نگهداری می‌شوند.</small></div>
</aside>

<section class="notes-panel">
  <div class="panel-head"><div><h2 id="listTitle">همه یادداشت‌ها</h2><small id="listSubtitle">یادداشت‌های شما</small></div><button id="sortBtn" class="select-btn">آخرین ویرایش ▾</button></div>
  <div id="noteList" class="note-list"></div>
</section>

<main class="editor">
  <div id="emptyState" class="empty">
    <div class="empty-icon">✦</div><h2>یادداشت خود را بسازید</h2>
    <p>یک یادداشت جدید ایجاد کنید یا یکی از یادداشت‌های سمت راست را انتخاب کنید.</p>
    <button id="emptyNew" class="primary">＋ یادداشت جدید</button>
  </div>
  <div id="editorView" class="editor-view hidden">
    <div class="editor-head">
      <div class="title-wrap"><input id="title" maxlength="140" placeholder="عنوان یادداشت..." aria-label="عنوان"><div id="saveState" class="save-state">ذخیره شد</div></div>
      <div class="editor-tools"><button id="favoriteBtn" class="tool" title="مورد علاقه">☆</button><button id="moreBtn" class="tool">•••</button></div>
    </div>
    <div id="moreMenu" class="more-menu hidden">
      <button id="duplicateBtn">⧉ ایجاد نسخه کپی</button>
      <button id="exportMd">⌁ خروجی Markdown</button>
      <button id="restoreBtn" class="hidden">↩ بازیابی</button>
      <button id="permanentDelete" class="danger">حذف دائمی</button>
    </div>
    <div class="editor-meta"><span id="updatedAt">—</span><span id="noteTags"></span></div>
    <div class="toolbar" aria-label="ابزار ویرایش">
      <button data-cmd="undo">↶</button><button data-cmd="redo">↷</button><i></i>
      <button data-cmd="bold"><b>B</b></button><button data-cmd="italic"><i>I</i></button><button data-cmd="underline"><u>U</u></button>
      <button data-cmd="formatBlock" data-val="h2">H</button><button data-cmd="formatBlock" data-val="blockquote">❝</button>
      <button data-cmd="insertUnorderedList">•</button><button data-cmd="insertOrderedList">1.</button><i></i>
      <button id="linkBtn">🔗</button><button id="clearFormat">Tx</button>
      <span class="toolbar-spacer"></span><button id="copyBtn">کپی</button><button id="txtBtn">TXT</button><button id="printBtn">چاپ</button>
    </div>
    <div id="editor" class="editor-area" contenteditable="true" spellcheck="true" data-placeholder="اینجا بنویسید..."></div>
    <div class="editor-footer"><span id="stats">۰ کلمه · ۰ حرف</span><span>Ctrl+S ذخیره · Ctrl+K جستجو · Ctrl+N یادداشت جدید</span></div>
  </div>
</main>
</div>
<input id="fileInput" type="file" accept=".json,application/json" hidden>
<div id="toast" role="status"></div>
</div>
<script src="app.js"></script>
</body></html>'''

css=r'''*{box-sizing:border-box}html,body{margin:0;height:100%;font-family:Vazirmatn,system-ui,sans-serif}body{background:#07111f;color:#e8f2fa;overflow:hidden}button,input{font:inherit}button{cursor:pointer;color:inherit}.topbar{height:70px;background:#091522;border-bottom:1px solid #1b3045;display:flex;align-items:center;padding:0 18px;gap:18px}.brand{display:flex;align-items:center;gap:10px;min-width:180px}.brand-mark{width:42px;height:42px;border-radius:13px;display:grid;place-items:center;font-weight:900;background:linear-gradient(135deg,#0b9cf5,#ff9e2c);color:#fff}.brand strong{display:block;font-size:14px}.brand small{display:block;font-size:9px;letter-spacing:2px;color:#7890a5}.brand small b{color:#ffad4d}.top-search{height:40px;flex:1;max-width:620px;margin:auto;display:flex;align-items:center;gap:8px;padding:0 12px;background:#0c1c2c;border:1px solid #213a51;border-radius:12px}.top-search span{font-size:22px;color:#7290a6}.top-search input{width:100%;border:0;outline:0;background:transparent;color:#fff}.top-search kbd{font-size:9px;color:#6d8498;border:1px solid #2a4257;border-radius:5px;padding:3px 5px}.top-actions{display:flex;gap:7px}.icon-btn,.text-btn,.select-btn,.tool{border:1px solid #29445b;background:#0c1e30;border-radius:9px;padding:8px 11px}.icon-btn{min-width:38px}.primary{border:0;border-radius:10px;padding:9px 14px;background:linear-gradient(135deg,#0b8fe2,#f39127);color:#fff;font-weight:700}.layout{height:calc(100vh - 70px);display:grid;grid-template-columns:225px 310px minmax(0,1fr)}aside,.notes-panel{background:#091725;border-left:1px solid #1a3045}.notes-panel{border-left:0;border-right:1px solid #1a3045;overflow:hidden}.side-head,.panel-head{height:65px;padding:12px 15px;display:flex;align-items:center;justify-content:space-between}.side-head{font-size:12px;color:#91a6b7}.side-head .icon-btn{display:none}.new-side{width:calc(100% - 26px);margin:0 13px 12px;padding:10px;border:1px solid #28506d;background:#10304a;border-radius:10px;color:#dceeff}.nav{padding:0 10px}.nav-item{width:100%;display:flex;align-items:center;gap:9px;border:0;background:transparent;padding:10px;border-radius:9px;text-align:right;color:#9eb1c1;font-size:11px}.nav-item:hover,.nav-item.active{background:#102b40;color:#fff}.nav-item span{flex:1}.nav-item b{font-size:9px;color:#6f899e}.section-title{font-size:10px;color:#637d91;padding:18px 15px 7px}.tags{padding:0 14px;display:flex;gap:6px;flex-wrap:wrap}.tag{border:1px solid #294358;background:#0d2031;color:#8da5b7;border-radius:20px;padding:4px 8px;font-size:9px}.side-footer{position:absolute;bottom:15px;padding:0 15px;color:#60798e;font-size:10px}.side-footer small{font-size:8px}.panel-head{border-bottom:1px solid #172c40}.panel-head h2{font-size:14px;margin:0}.panel-head small{font-size:9px;color:#668197}.select-btn{font-size:9px;padding:6px 8px}.note-list{height:calc(100% - 65px);overflow:auto;padding:10px}.note-card{width:100%;text-align:right;border:1px solid transparent;background:#0b1b2b;border-radius:11px;padding:12px;margin-bottom:7px}.note-card:hover,.note-card.active{border-color:#315d79;background:#102a3e}.note-card b{display:block;font-size:12px;white-space:nowrap;overflow:hidden;text-overflow:ellipsis}.note-card p{margin:5px 0;color:#72899c;font-size:10px;white-space:nowrap;overflow:hidden;text-overflow:ellipsis}.note-card footer{display:flex;justify-content:space-between;color:#526b80;font-size:8px}.editor{min-width:0;background:#07111f;position:relative}.editor-view{height:100%;display:flex;flex-direction:column}.hidden{display:none!important}.editor-head{min-height:78px;padding:12px 22px;display:flex;align-items:center;justify-content:space-between;border-bottom:1px solid #172d40}.title-wrap{min-width:0;flex:1}.title-wrap input{width:100%;border:0;outline:0;background:transparent;color:#fff;font-size:25px;font-weight:800}.save-state{font-size:9px;color:#668096;margin-top:3px}.editor-tools{display:flex;gap:6px}.tool{font-size:18px}.editor-meta{padding:7px 22px;color:#5d768a;font-size:9px;display:flex;gap:15px}.toolbar{display:flex;gap:5px;align-items:center;flex-wrap:wrap;padding:8px 20px;border-top:1px solid #13283a;border-bottom:1px solid #13283a;background:#091725}.toolbar button{min-width:31px;height:31px;border:1px solid #213b51;background:#0d2031;border-radius:7px;font-size:10px}.toolbar i{width:1px;height:20px;background:#294054}.toolbar-spacer{flex:1}.editor-area{flex:1;overflow:auto;padding:28px clamp(20px,8vw,110px);font-size:16px;line-height:2.15;outline:0;word-break:break-word}.editor-area:empty:before{content:attr(data-placeholder);color:#526b80;pointer-events:none}.editor-area h2{font-size:25px}.editor-area blockquote{border-right:3px solid #168fdb;padding-right:15px;color:#9eb3c4}.editor-footer{height:38px;border-top:1px solid #172d40;display:flex;justify-content:space-between;align-items:center;padding:0 20px;color:#587188;font-size:9px}.more-menu{position:absolute;z-index:5;top:60px;left:22px;background:#0c1d2d;border:1px solid #2b455b;border-radius:10px;padding:5px;box-shadow:0 15px 40px #0007}.more-menu button{display:block;width:180px;text-align:right;border:0;background:transparent;color:#c6d7e3;padding:9px;border-radius:7px;font-size:10px}.more-menu button:hover{background:#17334a}.danger{color:#ffaaa3!important}.empty{height:100%;display:grid;place-content:center;text-align:center;padding:30px}.empty-icon{margin:auto;width:65px;height:65px;border-radius:20px;display:grid;place-items:center;background:#102b40;color:#ff9e32;font-size:28px}.empty h2{margin:15px 0 5px;font-size:20px}.empty p{color:#6e879a;font-size:11px}.toast{position:fixed}.toast,#toast{position:fixed;bottom:55px;left:50%;transform:translate(-50%,15px);opacity:0;background:#123049;border:1px solid #38637f;padding:9px 15px;border-radius:9px;font-size:11px;transition:.25s;z-index:20}.toast.show,#toast.show{opacity:1;transform:translate(-50%,0)}body.light{background:#f4f7fa;color:#172735}body.light .topbar,body.light aside,body.light .notes-panel,body.light .toolbar{background:#fff;border-color:#d7e1e8}body.light .top-search,body.light .icon-btn,body.light .text-btn,body.light .select-btn,body.light .tool,body.light .toolbar button,.light .note-card{background:#f5f8fa;border-color:#d5e0e8;color:#213243}body.light .editor{background:#fff}body.light .title-wrap input,body.light .top-search input{color:#172735}body.light .editor-head,body.light .editor-footer,body.light .panel-head{border-color:#d7e1e8}body.light .nav-item:hover,body.light .nav-item.active{background:#e8f2f8;color:#162c3c}.mobile-only{display:none}@media(max-width:1050px){.layout{grid-template-columns:200px 280px 1fr}.brand{min-width:150px}.top-search{max-width:none}}@media(max-width:800px){body{overflow:hidden}.topbar{padding:0 10px;gap:8px}.brand{min-width:auto}.brand strong{font-size:12px}.brand small{font-size:7px}.top-search{display:none}.text-btn{display:none}.layout{display:block}.notes-panel{display:none}.notes-panel.mobile-show{display:block;position:absolute;z-index:8;right:0;top:70px;width:100%;height:calc(100vh - 70px)}aside{position:absolute;z-index:10;right:-245px;top:70px;width:225px;height:calc(100vh - 70px);transition:.25s;box-shadow:-15px 0 40px #0006}aside.open{right:0}.side-head .icon-btn{display:block}.editor-head{padding:10px 14px}.title-wrap input{font-size:20px}.toolbar{padding:7px 10px}.toolbar-spacer{display:none}.editor-area{padding:22px 15px}.editor-footer{padding:0 10px}.editor-footer span:last-child{display:none}.editor-meta{padding:6px 14px}}@media print{body{background:#fff!important;color:#000!important;overflow:visible}.topbar,aside,.notes-panel,.toolbar,.editor-footer,.editor-meta,.editor-tools,.save-state{display:none!important}.layout,.editor{display:block;height:auto}.editor-area{padding:0;font-size:13pt}.title-wrap input{color:#000;font-size:22pt}.editor-head{border:0;padding:0 0 15px}.editor-view{display:block}.editor-area:empty:before{display:none}}'''

js=r'''const STORE="qhvisionx-notepad-v2";const THEME="qhvisionx-notepad-theme";let notes=[],currentId=null,filter="all",sortNewest=true,saveTimer=null;
const $=id=>document.getElementById(id), fa=n=>Number(n||0).toLocaleString("fa-AF");
function uid(){return Date.now().toString(36)+Math.random().toString(36).slice(2,8)}
function plain(html){const d=document.createElement("div");d.innerHTML=html||"";return (d.innerText||"").replace(/\s+/g," ").trim()}
function esc(s){return String(s??"").replace(/[&<>"']/g,m=>({"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#39;"}[m]))}
function saveAll(){localStorage.setItem(STORE,JSON.stringify(notes))}
function makeNote(){const n={id:uid(),title:"یادداشت جدید",content:"",favorite:false,trash:false,tags:[],created:Date.now(),updated:Date.now()};notes.unshift(n);saveAll();openNote(n.id);setTimeout(()=>{$("title").focus();$("title").select()},40)}
function seed(){if(!notes.length){const n={id:uid(),title:"خوش آمدید به QH VisionX Notepad",content:"<h2>به Notepad v2 خوش آمدید</h2><p>این نسخه برای یادداشت‌برداری حرفه‌ای فارسی و RTL طراحی شده است.</p><ul><li>ذخیره خودکار در مرورگر</li><li>جستجو، علاقه‌مندی و سطل زباله</li><li>پشتیبان‌گیری و بازیابی JSON</li><li>خروجی TXT و Markdown</li></ul><p>برای شروع، همین متن را ویرایش کنید.</p>",favorite:true,trash:false,tags:["راهنما"],created:Date.now(),updated:Date.now()};notes=[n];saveAll()}openNote(notes.find(n=>!n.trash)?.id||notes[0]?.id)}
function load(){try{notes=JSON.parse(localStorage.getItem(STORE)||"[]")}catch{notes=[]}seed();renderAll()}
function openNote(id){const n=notes.find(x=>x.id===id);if(!n)return;currentId=id;$("emptyState").classList.add("hidden");$("editorView").classList.remove("hidden");$("title").value=n.title;$("editor").innerHTML=n.content||"";$("favoriteBtn").textContent=n.favorite?"★":"☆";$("restoreBtn").classList.toggle("hidden",!n.trash);$("updatedAt").textContent="آخرین ویرایش: "+new Date(n.updated).toLocaleString("fa-AF",{dateStyle:"medium",timeStyle:"short"});$("noteTags").textContent=n.tags?.length?"# "+n.tags.join("  # "):"";stats();renderList()}
function current(){return notes.find(n=>n.id===currentId)}
function schedule(){clearTimeout(saveTimer);$("saveState").textContent="در حال ذخیره...";saveTimer=setTimeout(commit,450)}
function commit(){const n=current();if(!n)return;n.title=$("title").value.trim()||"بدون عنوان";n.content=$("editor").innerHTML;n.updated=Date.now();saveAll();$("saveState").textContent="ذخیره شد · "+new Date().toLocaleTimeString("fa-AF",{hour:"2-digit",minute:"2-digit"});$("updatedAt").textContent="آخرین ویرایش: "+new Date(n.updated).toLocaleString("fa-AF",{dateStyle:"medium",timeStyle:"short"});renderList()}
function stats(){const t=plain($("editor").innerHTML);$("stats").textContent=`${fa(t?t.split(/\s+/).length:0)} کلمه · ${fa(t.length)} حرف`}
function renderAll(){renderList();updateCounts();renderTags()}
function renderList(){const q=$("globalSearch").value.trim().toLowerCase();let arr=notes.filter(n=>{if(filter==="favorite")return n.favorite&&!n.trash;if(filter==="trash")return n.trash;return !n.trash}).filter(n=>(n.title+" "+plain(n.content)+" "+(n.tags||[]).join(" ")).toLowerCase().includes(q));arr.sort((a,b)=>sortNewest?b.updated-a.updated:a.title.localeCompare(b.title));$("noteList").innerHTML=arr.length?arr.map(n=>`<button class="note-card ${n.id===currentId?"active":""}" data-id="${n.id}"><b>${n.favorite?"★ ":""}${esc(n.title)}</b><p>${esc(plain(n.content).slice(0,90)||"یادداشت خالی")}</p><footer><span>${n.tags?.length?"# "+esc(n.tags[0]):""}</span><span>${new Date(n.updated).toLocaleDateString("fa-AF")}</span></footer></button>`).join(""):'<div style="text-align:center;color:#60798e;padding:35px;font-size:10px">موردی پیدا نشد.</div>';document.querySelectorAll(".note-card").forEach(b=>b.onclick=()=>{openNote(b.dataset.id);closeMobile()})}
function updateCounts(){let active=notes.filter(n=>!n.trash),fav=active.filter(n=>n.favorite),trash=notes.filter(n=>n.trash);$("allCount").textContent=fa(active.length);$("favCount").textContent=fa(fav.length);$("trashCount").textContent=fa(trash.length)}
function renderTags(){const map={};notes.filter(n=>!n.trash).forEach(n=>(n.tags||[]).forEach(t=>map[t]=(map[t]||0)+1));$("tags").innerHTML=Object.entries(map).slice(0,12).map(([t,c])=>`<button class="tag" data-tag="${esc(t)}">#${esc(t)} ${c}</button>`).join("");document.querySelectorAll(".tag").forEach(b=>b.onclick=()=>{$("globalSearch").value=b.dataset.tag;renderList()})}
function toast(s){$("toast").textContent=s;$("toast").classList.add("show");setTimeout(()=>$("toast").classList.remove("show"),1800)}
function closeMobile(){$("sidebar").classList.remove("open");$("notes-panel")?.classList.remove("mobile-show")}
function download(name,text,type="text/plain"){const a=document.createElement("a");a.href=URL.createObjectURL(new Blob([text],{type}));a.download=name;a.click();setTimeout(()=>URL.revokeObjectURL(a.href),500)}
function trashCurrent(){const n=current();if(!n)return;if(n.trash){n.trash=false}else n.trash=true;n.updated=Date.now();saveAll();renderAll();openNote(n.id);toast(n.trash?"به سطل زباله منتقل شد":"یادداشت بازیابی شد")}
$("newBtn").onclick=makeNote;$("newSide").onclick=makeNote;$("emptyNew").onclick=makeNote;$("title").oninput=schedule;$("editor").oninput=()=>{stats();schedule()};$("globalSearch").oninput=renderList;
document.querySelectorAll(".nav-item").forEach(b=>b.onclick=()=>{filter=b.dataset.filter;document.querySelectorAll(".nav-item").forEach(x=>x.classList.remove("active"));b.classList.add("active");$("listTitle").textContent=filter==="all"?"همه یادداشت‌ها":filter==="favorite"?"مورد علاقه‌ها":"سطل زباله";renderList();closeMobile()});
$("favoriteBtn").onclick=()=>{const n=current();if(!n)return;n.favorite=!n.favorite;saveAll();$("favoriteBtn").textContent=n.favorite?"★":"☆";renderAll();toast(n.favorite?"به مورد علاقه‌ها اضافه شد":"از مورد علاقه‌ها حذف شد")};
$("moreBtn").onclick=()=>{$("moreMenu").classList.toggle("hidden")};document.addEventListener("click",e=>{if(!$("moreMenu").contains(e.target)&&e.target!==$("moreBtn"))$("moreMenu").classList.add("hidden")});
$("duplicateBtn").onclick=()=>{const n=current();if(!n)return;const c={...n,id:uid(),title:n.title+" — کپی",created:Date.now(),updated:Date.now(),trash:false};notes.unshift(c);saveAll();openNote(c.id);toast("نسخه کپی ساخته شد")};
$("restoreBtn").onclick=trashCurrent;
$("permanentDelete").onclick=()=>{const n=current();if(!n)return;if(!confirm("این یادداشت برای همیشه حذف شود؟"))return;notes=notes.filter(x=>x.id!==n.id);saveAll();currentId=null;$("editorView").classList.add("hidden");$("emptyState").classList.remove("hidden");renderAll();toast("برای همیشه حذف شد")};
$("copyBtn").onclick=async()=>{try{await navigator.clipboard.writeText(plain($("editor").innerHTML));toast("متن کپی شد")}catch{toast("کپی در دسترس نیست")}};
$("txtBtn").onclick=()=>{const n=current();if(n)download((n.title||"note")+".txt",plain(n.content))};
$("exportMd").onclick=()=>{const n=current();if(!n)return;let text=plain(n.content).replace(/\n/g,"\n\n");download((n.title||"note")+".md",`# ${n.title}\n\n${text}`,"text/markdown")};
$("printBtn").onclick=()=>window.print();
$("sortBtn").onclick=()=>{sortNewest=!sortNewest;$("sortBtn").textContent=sortNewest?"آخرین ویرایش ▾":"الفبایی ▾";renderList()};
$("themeBtn").onclick=()=>{document.body.classList.toggle("light");localStorage.setItem(THEME,document.body.classList.contains("light")?"light":"dark")};
$("mobileMenu").onclick=()=>{$("sidebar").classList.toggle("open")};$("closeSide").onclick=closeMobile;
document.querySelectorAll("[data-cmd]").forEach(b=>b.onclick=()=>{document.execCommand(b.dataset.cmd,false,b.dataset.val||null);$("editor").focus();schedule()});
$("clearFormat").onclick=()=>{document.execCommand("removeFormat");$("editor").focus();schedule()};
$("linkBtn").onclick=()=>{const url=prompt("آدرس لینک را وارد کنید:");if(url)document.execCommand("createLink",false,url)};
$("backupBtn").onclick=()=>download("qh-visionx-notepad-backup.json",JSON.stringify({version:2,exported:new Date().toISOString(),notes},null,2),"application/json");
$("fileInput").onchange=e=>{const f=e.target.files[0];if(!f)return;const r=new FileReader();r.onload=()=>{try{const d=JSON.parse(r.result);if(!Array.isArray(d.notes))throw 0;notes=d.notes;saveAll();currentId=notes.find(n=>!n.trash)?.id||notes[0]?.id;renderAll();if(currentId)openNote(currentId);toast("پشتیبان بازیابی شد")}catch{toast("فایل پشتیبان نامعتبر است")}};r.readAsText(f)};
$("backupBtn").addEventListener("contextmenu",e=>e.preventDefault());
document.addEventListener("keydown",e=>{if((e.ctrlKey||e.metaKey)&&e.key.toLowerCase()==="s"){e.preventDefault();commit();toast("ذخیره شد")}if((e.ctrlKey||e.metaKey)&&e.key.toLowerCase()==="n"){e.preventDefault();makeNote()}if((e.ctrlKey||e.metaKey)&&e.key.toLowerCase()==="k"){e.preventDefault();$("globalSearch").focus()}if(e.key==="Escape"){$("moreMenu").classList.add("hidden");closeMobile()}});
if(localStorage.getItem(THEME)==="light")document.body.classList.add("light");load();
'''

manifest={"name":"QH VisionX Notepad v2","short_name":"QH Notepad","start_url":"./","display":"standalone","background_color":"#07111f","theme_color":"#07111f","lang":"fa","dir":"rtl","description":"Professional Persian RTL Notepad"}
favicon='''<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 64 64"><rect width="64" height="64" rx="16" fill="#07111f"/><path d="M14 15h36v34H14z" fill="#0d8fdf"/><path d="M20 23h24M20 31h18M20 39h14" stroke="#fff" stroke-width="4" stroke-linecap="round"/></svg>'''
nojekyll=""
readme=r'''# QH VisionX Notepad v2

Professional Persian/RTL static Notepad built with HTML, CSS and vanilla JavaScript.

## Features
- Multi-note workspace
- Search
- Favorites
- Trash and restore
- Duplicate notes
- Rich text editing
- Bold / Italic / Underline
- Headings, quote and lists
- Link insertion
- Auto-save to LocalStorage
- Dark / Light mode
- TXT export
- Markdown export
- JSON backup / restore
- Print
- Word / character count
- Keyboard shortcuts
- Responsive mobile layout
- PWA manifest
- GitHub Pages / Netlify ready
- No backend required

## Privacy
Notes are stored locally in the browser using LocalStorage. They are not synchronized between devices unless a cloud backend is added.

## Deployment
The project is static. Keep `index.html` at the repository root. GitHub Pages can publish static files from a repository, and Netlify can deploy the project folder or connect directly to the Git repository.

## Keyboard shortcuts
- Ctrl/Cmd + N — new note
- Ctrl/Cmd + S — save
- Ctrl/Cmd + K — search
- Esc — close menus
'''
for name,data in {
"index.html":html,"style.css":css,"app.js":js,"manifest.json":json.dumps(manifest,ensure_ascii=False,indent=2),
"favicon.svg":favicon,"README.md":readme,".nojekyll":nojekyll}.items():
    (root/name).write_text(data,encoding="utf-8")

zip_path=Path("/mnt/data/QH-VisionX-Notepad-v2.zip")
with zipfile.ZipFile(zip_path,"w",zipfile.ZIP_DEFLATED) as z:
    for p in root.iterdir(): z.write(p,p.name)
print("created",zip_path)
print("\n".join(p.name for p in root.iterdir()))
