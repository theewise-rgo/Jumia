<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Jumia Careers — Build Africa's Future</title>
<style>
/* ============ TOKENS ============ */
:root{
  --orange:#F68B1E;
  --orange-dark:#E07B10;
  --orange-soft:#FFF3E5;
  --dark:#1F1F1F;
  --ink:#282828;
  --gray:#6B6B6B;
  --gray-light:#9A9A9A;
  --line:#E8E8E8;
  --bg:#F7F7F8;
  --white:#fff;
  --green:#1FA971;
  --red:#D93025;
  --radius:14px;
  --radius-lg:20px;
  --shadow-sm:0 2px 8px rgba(0,0,0,.06);
  --shadow:0 8px 28px rgba(0,0,0,.10);
  --shadow-lg:0 24px 60px rgba(0,0,0,.18);
  --font:'Inter',-apple-system,BlinkMacSystemFont,'Segoe UI',Roboto,Helvetica,Arial,sans-serif;
}

/* ============ RESET ============ */
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0;}
html{scroll-behavior:smooth;-webkit-text-size-adjust:100%;}
body{
  font-family:var(--font);
  background:var(--bg);
  color:var(--ink);
  line-height:1.55;
  font-size:15px;
  -webkit-font-smoothing:antialiased;
}
img{max-width:100%;display:block;}
button,input,select,textarea{font-family:inherit;font-size:inherit;color:inherit;}
button{cursor:pointer;border:none;background:none;}
a{color:inherit;text-decoration:none;}
:focus-visible{outline:2px solid var(--orange);outline-offset:2px;border-radius:6px;}

/* ============ LAYOUT HELPERS ============ */
.wrap{max-width:1180px;margin:0 auto;padding:0 20px;width:100%;}
.section{padding:64px 0;}
.section-head{text-align:center;max-width:640px;margin:0 auto 40px;}
.section-head h2{font-size:clamp(24px,3.4vw,34px);font-weight:800;letter-spacing:-.5px;margin-bottom:10px;}
.section-head p{color:var(--gray);font-size:15px;}

/* ============ BUTTONS ============ */
.btn{
  display:inline-flex;align-items:center;justify-content:center;gap:8px;
  padding:12px 22px;border-radius:10px;font-weight:700;font-size:14.5px;
  transition:transform .15s ease,background .15s ease,box-shadow .15s ease,color .15s;
  white-space:nowrap;
}
.btn:active{transform:scale(.98);}
.btn.primary{background:var(--orange);color:#fff;box-shadow:0 4px 14px rgba(246,139,30,.32);}
.btn.primary:hover{background:var(--orange-dark);}
.btn.primary:disabled{background:#E4E4E4;color:#9A9A9A;box-shadow:none;cursor:not-allowed;transform:none;}
.btn.ghost{background:#fff;color:var(--ink);border:1.5px solid var(--line);}
.btn.ghost:hover{border-color:#c9c9c9;background:#fafafa;}
.btn.dark{background:var(--dark);color:#fff;}
.btn.dark:hover{background:#000;}
.btn.block{width:100%;}
.btn.sm{padding:9px 16px;font-size:13.5px;}

/* ============ NAVBAR ============ */
.nav{
  position:sticky;top:0;z-index:60;background:rgba(255,255,255,.92);
  backdrop-filter:blur(12px);border-bottom:1px solid var(--line);
}
.nav-inner{max-width:1180px;margin:0 auto;padding:0 20px;height:66px;display:flex;align-items:center;gap:28px;}
.logo{display:flex;align-items:center;gap:10px;font-weight:800;font-size:19px;letter-spacing:-.3px;flex-shrink:0;}
.logo-mark{
  width:34px;height:34px;border-radius:9px;background:var(--orange);
  display:grid;place-items:center;color:#fff;font-weight:900;font-size:17px;
  box-shadow:0 3px 10px rgba(246,139,30,.35);
}
.logo span{color:var(--gray-light);font-weight:600;}
.nav-links{display:flex;gap:26px;margin-left:auto;}
.nav-links a{font-size:14.5px;font-weight:600;color:var(--gray);transition:color .15s;}
.nav-links a:hover{color:var(--orange);}
.nav-cta{margin-left:8px;}
@media(max-width:880px){
  .nav-links{display:none;}
  .nav-cta{margin-left:auto;}
}

/* ============ HERO ============ */
.hero{
  position:relative;overflow:hidden;color:#fff;
  background:linear-gradient(140deg,#141414 0%,#241d14 55%,#3a2a15 100%);
  padding:78px 0 70px;
}
.hero::before{
  content:"";position:absolute;inset:0;
  background:radial-gradient(680px 340px at 82% 8%,rgba(246,139,30,.30),transparent 68%),
             radial-gradient(520px 300px at 8% 92%,rgba(246,139,30,.14),transparent 70%);
  pointer-events:none;
}
.hero-inner{position:relative;z-index:1;max-width:1180px;margin:0 auto;padding:0 20px;}
.pill{
  display:inline-flex;align-items:center;gap:8px;font-size:12.5px;font-weight:700;
  background:rgba(246,139,30,.16);color:#FFC078;border:1px solid rgba(246,139,30,.35);
  padding:6px 14px;border-radius:100px;margin-bottom:20px;letter-spacing:.3px;
}
.pill .dot{width:6px;height:6px;border-radius:50%;background:#3DDC97;box-shadow:0 0 0 3px rgba(61,220,151,.2);}
.hero h1{
  font-size:clamp(30px,5.2vw,52px);line-height:1.1;font-weight:800;
  letter-spacing:-1.4px;max-width:760px;margin-bottom:18px;
}
.hero h1 em{font-style:normal;color:var(--orange);}
.hero p.lead{font-size:clamp(15px,1.6vw,17px);color:rgba(255,255,255,.72);max-width:560px;margin-bottom:32px;}

/* Search */
.search{
  display:flex;gap:8px;background:#fff;padding:8px;border-radius:16px;
  max-width:640px;box-shadow:0 16px 40px rgba(0,0,0,.35);
}
.search input{
  flex:1;border:none;outline:none;padding:12px 14px;font-size:15px;
  background:transparent;color:var(--ink);min-width:0;
}
.search input::placeholder{color:#A5A5A5;}
.search .btn{border-radius:11px;padding:13px 26px;}
@media(max-width:560px){
  .search{flex-direction:column;padding:10px;}
  .search .btn{width:100%;}
}

/* Stats */
.stats{
  position:relative;z-index:1;max-width:1180px;margin:56px auto 0;padding:0 20px;
  display:grid;grid-template-columns:repeat(4,1fr);gap:16px;
}
.stat{
  background:rgba(255,255,255,.06);border:1px solid rgba(255,255,255,.10);
  border-radius:var(--radius);padding:18px 20px;backdrop-filter:blur(6px);
}
.stat strong{display:block;font-size:clamp(20px,2.6vw,26px);font-weight:800;color:#fff;letter-spacing:-.6px;}
.stat span{font-size:12.5px;color:rgba(255,255,255,.55);font-weight:600;}
@media(max-width:760px){.stats{grid-template-columns:repeat(2,1fr);margin-top:40px;}}

/* ============ FILTERS ============ */
.filters{display:flex;flex-direction:column;gap:16px;margin-bottom:28px;}
.chips{display:flex;gap:9px;overflow-x:auto;padding-bottom:4px;scrollbar-width:none;}
.chips::-webkit-scrollbar{display:none;}
.chip{
  padding:9px 17px;border-radius:100px;border:1.5px solid var(--line);background:#fff;
  font-size:13.5px;font-weight:600;color:var(--gray);white-space:nowrap;
  transition:all .15s ease;
}
.chip:hover{border-color:#d5d5d5;color:var(--ink);}
.chip.active{background:var(--dark);border-color:var(--dark);color:#fff;}
.filter-row{display:flex;gap:12px;flex-wrap:wrap;align-items:center;}
.select-wrap{position:relative;}
.select-wrap select{
  appearance:none;padding:11px 40px 11px 16px;border-radius:10px;border:1.5px solid var(--line);
  background:#fff;font-size:14px;font-weight:600;cursor:pointer;min-width:180px;
}
.select-wrap::after{
  content:"▾";position:absolute;right:15px;top:50%;transform:translateY(-50%);
  pointer-events:none;color:var(--gray);font-size:13px;
}
.result-count{margin-left:auto;font-size:13.5px;color:var(--gray);font-weight:600;}
@media(max-width:600px){.result-count{margin-left:0;width:100%;}}

/* ============ JOB GRID ============ */
.job-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(320px,1fr));gap:20px;}
@media(max-width:420px){.job-grid{grid-template-columns:1fr;}}

.job-card{
  background:#fff;border:1px solid var(--line);border-radius:var(--radius-lg);
  padding:22px;display:flex;flex-direction:column;gap:14px;
  transition:transform .2s ease,box-shadow .2s ease,border-color .2s ease;
}
.job-card:hover{transform:translateY(-4px);box-shadow:var(--shadow);border-color:#F7C88E;}

.job-top{display:flex;gap:13px;align-items:flex-start;}
.job-logo{
  width:44px;height:44px;border-radius:12px;background:var(--orange-soft);color:var(--orange-dark);
  display:grid;place-items:center;font-weight:800;font-size:18px;flex-shrink:0;
}
.job-top h3{font-size:16.5px;font-weight:700;letter-spacing:-.2px;line-height:1.3;}
.job-dept{font-size:12.5px;color:var(--gray);font-weight:600;margin-top:2px;}

.job-meta{display:flex;flex-wrap:wrap;gap:8px 16px;font-size:13px;color:var(--gray);font-weight:500;}
.job-summary{font-size:13.8px;color:var(--gray);line-height:1.6;}

.job-tags{display:flex;flex-wrap:wrap;gap:7px;}
.tag{
  font-size:11.5px;font-weight:700;padding:4px 10px;border-radius:6px;
  background:#F3F3F5;color:#666;letter-spacing:.2px;
}
.tag.salary{background:#E9F7F0;color:#12805A;}

.job-foot{
  display:flex;align-items:center;justify-content:space-between;gap:14px;
  border-top:1px dashed var(--line);padding-top:16px;margin-top:auto;
}
.fee small{display:block;font-size:11px;color:var(--gray-light);font-weight:700;text-transform:uppercase;letter-spacing:.5px;}
.fee strong{font-size:17px;font-weight:800;color:var(--orange-dark);letter-spacing:-.3px;}

/* Empty state */
.empty{
  grid-column:1/-1;text-align:center;padding:64px 20px;background:#fff;
  border:1.5px dashed var(--line);border-radius:var(--radius-lg);
}
.empty h3{font-size:17px;margin-bottom:6px;}
.empty p{color:var(--gray);font-size:14px;}

/* ============ HOW IT WORKS ============ */
.how{background:#fff;border-top:1px solid var(--line);border-bottom:1px solid var(--line);}
.how-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:22px;}
@media(max-width:860px){.how-grid{grid-template-columns:1fr;}}
.how-card{
  padding:28px 24px;border-radius:var(--radius-lg);background:var(--bg);
  border:1px solid var(--line);position:relative;overflow:hidden;
}
.how-num{
  width:38px;height:38px;border-radius:11px;background:var(--orange);color:#fff;
  display:grid;place-items:center;font-weight:800;font-size:15px;margin-bottom:16px;
  box-shadow:0 6px 16px rgba(246,139,30,.32);
}
.how-card h3{font-size:16.5px;font-weight:700;margin-bottom:8px;letter-spacing:-.2px;}
.how-card p{font-size:14px;color:var(--gray);line-height:1.65;}

/* ============ FAQ ============ */
.faq-list{max-width:760px;margin:0 auto;display:flex;flex-direction:column;gap:12px;}
details{
  background:#fff;border:1px solid var(--line);border-radius:var(--radius);
  padding:18px 22px;transition:border-color .15s;
}
details[open]{border-color:#F7C88E;}
details summary{
  font-weight:700;font-size:15px;cursor:pointer;list-style:none;
  display:flex;justify-content:space-between;align-items:center;gap:16px;
}
details summary::-webkit-details-marker{display:none;}
details summary::after{
  content:"+";font-size:20px;font-weight:400;color:var(--orange);
  transition:transform .2s ease;flex-shrink:0;
}
details[open] summary::after{transform:rotate(45deg);}
details p{margin-top:12px;font-size:14px;color:var(--gray);line-height:1.7;}

/* ============ FOOTER ============ */
footer{background:#161616;color:rgba(255,255,255,.6);padding:56px 0 32px;font-size:13.5px;}
.foot-grid{display:grid;grid-template-columns:1.6fr repeat(3,1fr);gap:36px;margin-bottom:40px;}
@media(max-width:820px){.foot-grid{grid-template-columns:1fr 1fr;gap:28px;}}
@media(max-width:520px){.foot-grid{grid-template-columns:1fr;}}
.foot-brand .logo{color:#fff;margin-bottom:14px;}
.foot-brand p{max-width:300px;line-height:1.7;}
.foot-col h4{color:#fff;font-size:13px;font-weight:700;text-transform:uppercase;letter-spacing:.8px;margin-bottom:16px;}
.foot-col a{display:block;margin-bottom:11px;transition:color .15s;}
.foot-col a:hover{color:var(--orange);}
.foot-bottom{
  border-top:1px solid rgba(255,255,255,.1);padding-top:24px;
  display:flex;justify-content:space-between;gap:16px;flex-wrap:wrap;font-size:12.5px;
}

/* ============ MODAL ============ */
.overlay{
  position:fixed;inset:0;z-index:200;background:rgba(15,15,15,.62);
  backdrop-filter:blur(4px);display:none;align-items:center;justify-content:center;padding:20px;
  animation:fadeIn .18s ease;
}
.overlay.open{display:flex;}
@keyframes fadeIn{from{opacity:0}to{opacity:1}}
@keyframes popIn{from{opacity:0;transform:translateY(14px) scale(.98)}to{opacity:1;transform:none}}

.modal{
  background:#fff;width:100%;max-width:640px;max-height:90vh;border-radius:var(--radius-lg);
  display:flex;flex-direction:column;overflow:hidden;box-shadow:var(--shadow-lg);
  animation:popIn .22s cubic-bezier(.2,.8,.3,1);
}
@media(max-width:620px){
  .overlay{padding:0;align-items:flex-end;}
  .modal{max-width:none;max-height:94vh;border-radius:22px 22px 0 0;}
}

.modal-head{
  padding:20px 24px 0;display:flex;align-items:flex-start;justify-content:space-between;gap:16px;
  flex-shrink:0;
}
.modal-head h2{font-size:18px;font-weight:800;letter-spacing:-.3px;}
.modal-head p{font-size:13px;color:var(--gray);margin-top:3px;}
.close-btn{
  width:34px;height:34px;border-radius:10px;display:grid;place-items:center;
  font-size:19px;color:var(--gray);background:#F4F4F5;flex-shrink:0;transition:all .15s;
}
.close-btn:hover{background:#E8E8EA;color:var(--ink);}

/* Steps */
.steps{display:flex;gap:6px;padding:18px 24px 0;flex-shrink:0;}
.step{flex:1;display:flex;flex-direction:column;align-items:center;gap:7px;position:relative;}
.step .dot{
  width:26px;height:26px;border-radius:50%;display:grid;place-items:center;
  font-size:12px;font-weight:800;background:#EFEFF1;color:#9A9A9A;
  transition:all .22s ease;z-index:1;
}
.step em{font-size:10.5px;font-style:normal;font-weight:700;color:var(--gray-light);letter-spacing:.2px;}
.step.active .dot{background:var(--orange);color:#fff;box-shadow:0 0 0 4px rgba(246,139,30,.18);}
.step.active em{color:var(--orange-dark);}
.step.done .dot{background:var(--green);color:#fff;}
.step.done em{color:var(--green);}
.step::before{
  content:"";position:absolute;top:13px;left:-50%;width:100%;height:2px;background:#EFEFF1;z-index:0;
}
.step:first-child::before{display:none;}
.step.done::before,.step.active::before{background:var(--green);}
.step.active::before{background:linear-gradient(90deg,var(--green),var(--orange));}

/* Modal body */
.modal-body{padding:22px 24px 24px;overflow-y:auto;flex:1;}
.modal-body::-webkit-scrollbar{width:6px;}
.modal-body::-webkit-scrollbar-thumb{background:#DCDCDE;border-radius:3px;}

/* Job summary inside modal */
.job-summary-box{
  display:flex;gap:14px;align-items:flex-start;padding:16px;border-radius:var(--radius);
  background:var(--bg);border:1px solid var(--line);margin-bottom:20px;
}
.job-summary-box .job-logo{width:46px;height:46px;font-size:19px;}
.job-summary-box h3{font-size:15.5px;font-weight:700;line-height:1.3;}
.job-summary-box .meta{font-size:12.5px;color:var(--gray);margin-top:4px;display:flex;flex-wrap:wrap;gap:4px 12px;}

/* Fee box */
.fee-box{
  border:1.5px solid #F7D9B4;background:#FFFBF6;border-radius:var(--radius);
  padding:18px;margin-bottom:18px;
}
.fee-row{display:flex;justify-content:space-between;font-size:13.5px;padding:6px 0;color:var(--gray);}
.fee-row span:last-child{font-weight:600;color:var(--ink);}
.fee-row.total{
  border-top:1.5px dashed #F2CFA3;margin-top:10px;padding-top:14px;
  font-size:16px;font-weight:800;color:var(--ink);
}
.fee-row.total span:last-child{color:var(--orange-dark);font-size:19px;font-weight:800;}

.includes{list-style:none;display:flex;flex-direction:column;gap:10px;margin-bottom:20px;}
.includes li{display:flex;gap:10px;font-size:13.8px;color:var(--gray);align-items:flex-start;}
.includes li::before{
  content:"✓";color:var(--green);font-weight:900;font-size:13px;flex-shrink:0;
  width:19px;height:19px;border-radius:50%;background:#E9F7F0;display:grid;place-items:center;
}

/* Checkbox */
.check{
  display:flex;gap:11px;align-items:flex-start;font-size:13.2px;color:var(--gray);
  padding:14px;border-radius:var(--radius);background:var(--bg);cursor:pointer;
  border:1px solid transparent;transition:border-color .15s;line-height:1.55;
}
.check:hover{border-color:var(--line);}
.check input{width:18px;height:18px;accent-color:var(--orange);margin-top:1px;flex-shrink:0;cursor:pointer;}

/* Payment methods */
.pay-methods{display:grid;grid-template-columns:repeat(3,1fr);gap:10px;margin-bottom:20px;}
@media(max-width:520px){.pay-methods{grid-template-columns:1fr;}}
.pay-method{
  padding:14px 12px;border-radius:12px;border:1.5px solid var(--line);background:#fff;
  display:flex;flex-direction:column;align-items:center;gap:6px;text-align:center;
  font-size:12.5px;font-weight:700;color:var(--gray);transition:all .15s;
}
.pay-method .ico{font-size:19px;}
.pay-method:hover{border-color:#d5d5d5;}
.pay-method.active{border-color:var(--orange);background:var(--orange-soft);color:var(--orange-dark);}

/* Forms */
.field{margin-bottom:16px;}
.field label{display:block;font-size:12.8px;font-weight:700;margin-bottom:7px;color:var(--ink);}
.field input,.field textarea,.field select{
  width:100%;padding:12px 14px;border-radius:10px;border:1.5px solid var(--line);
  background:#fff;font-size:14.5px;transition:border-color .15s,box-shadow .15s;outline:none;
}
.field input:focus,.field textarea:focus{
  border-color:var(--orange);box-shadow:0 0 0 3px rgba(246,139,30,.13);
}
.field textarea{resize:vertical;min-height:100px;line-height:1.6;}
.field-row{display:grid;grid-template-columns:1fr 1fr;gap:14px;}
@media(max-width:520px){.field-row{grid-template-columns:1fr;}}
.hint{font-size:11.8px;color:var(--gray-light);margin-top:6px;}
.err-msg{font-size:12px;color:var(--red);margin-top:6px;font-weight:600;display:none;}
.field.invalid input,.field.invalid textarea{border-color:var(--red);background:#FFF7F7;}
.field.invalid .err-msg{display:block;}

/* Upload */
.upload{
  display:flex;flex-direction:column;align-items:center;gap:6px;padding:24px;
  border:2px dashed var(--line);border-radius:var(--radius);background:var(--bg);
  cursor:pointer;transition:all .15s;text-align:center;
}
.upload:hover{border-color:var(--orange);background:var(--orange-soft);}
.upload .up-ico{font-size:22px;}
.upload span{font-size:13.5px;font-weight:700;}
.upload small{font-size:11.5px;color:var(--gray-light);}
.upload em{font-style:normal;font-size:12.5px;color:var(--green);font-weight:700;}

/* Bank transfer */
.transfer-box{
  background:var(--bg);border:1px solid var(--line);border-radius:var(--radius);
  padding:18px;margin-bottom:18px;
}
.transfer-row{
  display:flex;justify-content:space-between;align-items:center;gap:12px;
  padding:10px 0;font-size:13.5px;border-bottom:1px solid var(--line);
}
.transfer-row:last-child{border-bottom:none;}
.transfer-row span:first-child{color:var(--gray);}
.transfer-row strong{font-weight:800;letter-spacing:.4px;}
.copy-btn{
  font-size:11.5px;font-weight:800;color:var(--orange-dark);background:var(--orange-soft);
  padding:5px 11px;border-radius:7px;transition:all .15s;
}
.copy-btn:hover{background:#FFE6C9;}

/* Notice */
.notice{
  display:flex;gap:10px;font-size:12.5px;color:var(--gray);background:var(--bg);
  padding:13px 15px;border-radius:11px;line-height:1.55;align-items:flex-start;
}
.notice strong{color:var(--ink);}

/* Modal actions */
.modal-actions{
  display:flex;gap:12px;margin-top:22px;padding-top:20px;border-top:1px solid var(--line);
}
.modal-actions .btn{flex:1;}

/* Success */
.success{text-align:center;padding:12px 0 4px;}
.success-icon{
  width:76px;height:76px;border-radius:50%;background:#E9F7F0;color:var(--green);
  display:grid;place-items:center;font-size:34px;margin:0 auto 20px;
  animation:popIn .4s cubic-bezier(.2,.8,.3,1);
}
.success h2{font-size:22px;font-weight:800;margin-bottom:10px;letter-spacing:-.4px;}
.success p{color:var(--gray);font-size:14px;max-width:400px;margin:0 auto 24px;line-height:1.65;}
.ref-box{
  background:var(--bg);border:1.5px dashed var(--line);border-radius:var(--radius);
  padding:18px;margin-bottom:20px;
}
.ref-box small{display:block;font-size:11px;font-weight:800;color:var(--gray-light);text-transform:uppercase;letter-spacing:1px;margin-bottom:7px;}
.ref-box strong{font-size:19px;font-weight:800;letter-spacing:1.5px;color:var(--orange-dark);}

.next-steps{text-align:left;background:var(--bg);border-radius:var(--radius);padding:18px;margin-bottom:8px;}
.next-steps h4{font-size:13px;font-weight:800;margin-bottom:12px;text-transform:uppercase;letter-spacing:.6px;}
.next-steps ol{list-style:none;counter-reset:s;display:flex;flex-direction:column;gap:11px;}
.next-steps li{
  counter-increment:s;display:flex;gap:11px;font-size:13.5px;color:var(--gray);line-height:1.55;
}
.next-steps li::before{
  content:counter(s);flex-shrink:0;width:20px;height:20px;border-radius:50%;
  background:var(--orange);color:#fff;font-size:11px;font-weight:800;
  display:grid;place-items:center;margin-top:1px;
}

/* Spinner */
.spinner{
  width:16px;height:16px;border:2.5px solid rgba(255,255,255,.35);border-top-color:#fff;
  border-radius:50%;animation:spin .7s linear infinite;
}
@keyframes spin{to{transform:rotate(360deg)}}

/* ============ TOAST ============ */
.toast{
  position:fixed;left:50%;bottom:28px;transform:translate(-50%,120%);
  background:var(--dark);color:#fff;padding:13px 22px;border-radius:12px;
  font-size:13.5px;font-weight:600;z-index:300;box-shadow:var(--shadow-lg);
  transition:transform .3s cubic-bezier(.2,.8,.3,1);display:flex;gap:9px;align-items:center;
  max-width:calc(100vw - 40px);
}
.toast.show{transform:translate(-50%,0);}

@media(prefers-reduced-motion:reduce){
  *{animation-duration:.01ms !important;transition-duration:.01ms !important;}
}
</style>
</head>
<body>

<!-- ============ NAVBAR ============ -->
<header class="nav">
  <div class="nav-inner">
    <a href="#" class="logo">
      <span class="logo-mark">J</span>
      Jumia <span>Careers</span>
    </a>
    <nav class="nav-links">
      <a href="#jobs">Open Roles</a>
      <a href="#how">How It Works</a>
      <a href="#faq">FAQs</a>
    </nav>
    <a href="#jobs" class="btn primary sm nav-cta">Browse Jobs</a>
  </div>
</header>

<!-- ============ HERO ============ -->
<section class="hero">
  <div class="hero-inner">
    <div class="pill"><span class="dot"></span> 24 roles open across Africa</div>
    <h1>Build the future of <em>e-commerce</em> in Africa.</h1>
    <p class="lead">
      Join the team powering millions of deliveries, vendors and shoppers every day.
      Find your role, complete your application and get reviewed by our hiring team.
    </p>

    <form class="search" id="heroSearch">
      <input type="text" id="heroInput" placeholder="Search job title, skill or department…" aria-label="Search jobs">
      <button type="submit" class="btn primary">Search Jobs</button>
    </form>
  </div>

  <div class="stats">
    <div class="stat"><strong>12,000+</strong><span>Team members</span></div>
    <div class="stat"><strong>11</strong><span>Countries</span></div>
    <div class="stat"><strong>24</strong><span>Open positions</span></div>
    <div class="stat"><strong>72h</strong><span>Avg. review time</span></div>
  </div>
</section>

<!-- ============ JOBS ============ -->
<section class="section" id="jobs">
  <div class="wrap">
    <div class="section-head">
      <h2>Open Positions</h2>
      <p>Every application is screened by a human recruiter. Choose a role to begin.</p>
    </div>

    <div class="filters">
      <div class="chips" id="chips"></div>
      <div class="filter-row">
        <div class="select-wrap">
          <select id="locationFilter" aria-label="Filter by location">
            <option value="all">All locations</option>
          </select>
        </div>
        <div class="select-wrap">
          <select id="sortFilter" aria-label="Sort jobs">
            <option value="newest">Newest first</option>
            <option value="fee-low">Lowest fee</option>
            <option value="fee-high">Highest fee</option>
          </select>
        </div>
        <span class="result-count" id="resultCount"></span>
      </div>
    </div>

    <div class="job-grid" id="jobGrid"></div>
  </div>
</section>

<!-- ============ HOW IT WORKS ============ -->
<section class="section how" id="how">
  <div class="wrap">
    <div class="section-head">
      <h2>How Applying Works</h2>
      <p>Three simple steps from discovery to submission.</p>
    </div>
    <div class="how-grid">
      <div class="how-card">
        <div class="how-num">1</div>
        <h3>Find your role</h3>
        <p>Browse open positions and filter by department, location or experience level. Each listing shows the full role details and requirements.</p>
      </div>
      <div class="how-card">
        <div class="how-num">2</div>
        <h3>Pay the application fee</h3>
        <p>A small processing fee covers candidate verification, skills assessment and priority routing to the hiring manager. Pay securely by card, bank transfer or USSD.</p>
      </div>
      <div class="how-card">
        <div class="how-num">3</div>
        <h3>Submit & track</h3>
        <p>Complete your profile, attach your CV and submit. You'll receive a reference number instantly and an update from our team within 72 hours.</p>
      </div>
    </div>
  </div>
</section>

<!-- ============ FAQ ============ -->
<section class="section" id="faq">
  <div class="wrap">
    <div class="section-head">
      <h2>Frequently Asked Questions</h2>
      <p>Everything you need to know before you apply.</p>
    </div>
    <div class="faq-list">
      <details open>
        <summary>Why is there an application fee?</summary>
        <p>The fee covers administrative processing, identity verification, and the skills assessment that is sent to shortlisted candidates. It also helps us filter out spam and ensures every application is reviewed seriously.</p>
      </details>
      <details>
        <summary>Is the application fee refundable?</summary>
        <p>The fee is non-refundable once your application has been submitted and processed. If a payment is made in error before submission, contact our careers support team within 24 hours.</p>
      </details>
      <details>
        <summary>What payment methods do you accept?</summary>
        <p>We accept debit/credit cards (Verve, Mastercard, Visa), direct bank transfer, and USSD payments. All transactions are encrypted and processed by our PCI-compliant payment partner.</p>
      </details>
      <details>
        <summary>How long until I hear back?</summary>
        <p>You'll receive an acknowledgement immediately with your reference number. Our recruitment team aims to respond to every complete application within 72 hours.</p>
      </details>
      <details>
        <summary>Can I apply for more than one role?</summary>
        <p>Yes. Each application is processed separately and requires its own fee, as each role has a different hiring team and assessment process.</p>
      </details>
    </div>
  </div>
</section>

<!-- ============ FOOTER ============ -->
<footer>
  <div class="wrap">
    <div class="foot-grid">
      <div class="foot-brand">
        <div class="logo"><span class="logo-mark">J</span> Jumia</div>
        <p>Africa's leading e-commerce platform. We're building the infrastructure that connects vendors and consumers across the continent.</p>
      </div>
      <div class="foot-col">
        <h4>Careers</h4>
        <a href="#jobs">Open Roles</a>
        <a href="#how">How It Works</a>
        <a href="#faq">FAQs</a>
      </div>
      <div class="foot-col">
        <h4>Company</h4>
        <a href="#">About Us</a>
        <a href="#">Life at Jumia</a>
        <a href="#">Newsroom</a>
      </div>
      <div class="foot-col">
        <h4>Support</h4>
        <a href="#">Contact Recruiting</a>
        <a href="#">Privacy Policy</a>
        <a href="#">Terms of Use</a>
      </div>
    </div>
    <div class="foot-bottom">
      <span>© 2024 Jumia Careers. Demo interface for design purposes.</span>
      <span>Made for Africa 🌍</span>
    </div>
  </div>
</footer>

<!-- ============ MODAL ============ -->
<div class="overlay" id="overlay" role="dialog" aria-modal="true" aria-labelledby="modalTitle">
  <div class="modal" id="modal">
    <div class="modal-head">
      <div>
        <h2 id="modalTitle">Apply</h2>
        <p id="modalSub"></p>
      </div>
      <button class="close-btn" id="closeModal" aria-label="Close">✕</button>
    </div>
    <div class="steps" id="steps"></div>
    <div class="modal-body" id="modalBody"></div>
  </div>
</div>

<!-- ============ TOAST ============ -->
<div class="toast" id="toast"></div>

<script>
/* =========================================================
   DATA
   ========================================================= */
const JOBS = [
  {
    id: 1,
    title: "Senior Frontend Engineer",
    dept: "Engineering",
    location: "Lagos, Nigeria",
    type: "Full-time",
    level: "Senior",
    salary: "₦900k – ₦1.3M / month",
    fee: 2500,
    posted: "2 days ago",
    order: 1,
    summary: "Build fast, accessible shopping experiences used by millions of customers across 11 countries.",
    tags: ["React", "TypeScript", "Performance"],
    requirements: [
      "5+ years building production web applications",
      "Deep knowledge of React, TypeScript and modern build tooling",
      "Experience with performance profiling and Core Web Vitals",
      "Strong understanding of accessibility standards (WCAG)"
    ]
  },
  {
    id: 2,
    title: "Data Analyst",
    dept: "Data",
    location: "Nairobi, Kenya",
    type: "Full-time",
    level: "Mid-level",
    salary: "KES 180k – 260k / month",
    fee: 2000,
    posted: "3 days ago",
    order: 2,
    summary: "Turn millions of order events into insight that shapes pricing, logistics and vendor strategy.",
    tags: ["SQL", "Python", "Looker"],
    requirements: [
      "3+ years in an analytics role, ideally in retail or logistics",
      "Advanced SQL and strong Python (pandas) skills",
      "Experience building dashboards in Looker, Tableau or Power BI",
      "Ability to communicate findings to non-technical stakeholders"
    ]
  },
  {
    id: 3,
    title: "Warehouse Operations Supervisor",
    dept: "Operations",
    location: "Abuja, Nigeria",
    type: "Full-time",
    level: "Mid-level",
    salary: "₦350k – ₦480k / month",
    fee: 1500,
    posted: "5 days ago",
    order: 3,
    summary: "Lead a shift team through picking, packing and dispatch while hitting accuracy and SLA targets.",
    tags: ["Logistics", "Team Lead", "SLA"],
    requirements: [
      "3+ years supervising warehouse or fulfilment teams",
      "Working knowledge of WMS platforms",
      "Strong track record on inventory accuracy and dispatch SLAs",
      "Comfortable with shift rotations"
    ]
  },
  {
    id: 4,
    title: "Digital Marketing Specialist",
    dept: "Marketing",
    location: "Lagos, Nigeria",
    type: "Full-time",
    level: "Mid-level",
    salary: "₦400k – ₦600k / month",
    fee: 2000,
    posted: "1 week ago",
    order: 4,
    summary: "Own paid social and search campaigns that drive millions of monthly sessions to the marketplace.",
    tags: ["Meta Ads", "Google Ads", "CRO"],
    requirements: [
      "3+ years running performance marketing campaigns at scale",
      "Hands-on budget management of $50k+/month",
      "Strong analytical skills with GA4 and attribution modelling",
      "Experience in e-commerce or marketplaces preferred"
    ]
  },
  {
    id: 5,
    title: "Customer Experience Agent",
    dept: "Customer Service",
    location: "Accra, Ghana",
    type: "Full-time",
    level: "Entry-level",
    salary: "GHS 4,500 – 6,000 / month",
    fee: 1500,
    posted: "1 week ago",
    order: 5,
    summary: "Be the first voice customers hear — resolve delivery, payment and returns issues with empathy.",
    tags: ["Support", "Zendesk", "English"],
    requirements: [
      "1+ year in a customer-facing support role",
      "Excellent written and spoken English",
      "Comfortable with ticketing systems (Zendesk, Freshdesk)",
      "Calm under pressure and highly organised"
    ]
  },
  {
    id: 6,
    title: "Product Designer (UI/UX)",
    dept: "Design",
    location: "Remote",
    type: "Full-time",
    level: "Mid-level",
    salary: "₦600k – ₦850k / month",
    fee: 2500,
    posted: "1 week ago",
    order: 6,
    summary: "Design end-to-end flows for checkout, payments and the vendor portal used across Africa.",
    tags: ["Figma", "Design Systems", "Prototyping"],
    requirements: [
      "3+ years designing consumer or enterprise digital products",
      "A portfolio showing end-to-end product thinking",
      "Expert in Figma and design system maintenance",
      "Experience running usability tests"
    ]
  },
  {
    id: 7,
    title: "Finance Analyst",
    dept: "Finance",
    location: "Lagos, Nigeria",
    type: "Full-time",
    level: "Mid-level",
    salary: "₦450k – ₦650k / month",
    fee: 2000,
    posted: "2 weeks ago",
    order: 7,
    summary: "Support FP&A cycles, build models, and provide the numbers behind major commercial decisions.",
    tags: ["Excel", "FP&A", "Modelling"],
    requirements: [
      "3+ years in FP&A, audit or investment analysis",
      "Advanced Excel and financial modelling skills",
      "Part-qualified or qualified ACCA/ICAN/CFA is a plus",
      "High attention to detail"
    ]
  },
  {
    id: 8,
    title: "Logistics Fleet Manager",
    dept: "Logistics",
    location: "Ibadan, Nigeria",
    type: "Full-time",
    level: "Senior",
    salary: "₦550k – ₦750k / month",
    fee: 1800,
    posted: "2 weeks ago",
    order: 8,
    summary: "Own the last-mile fleet: routing, driver performance, maintenance and cost per delivery.",
    tags: ["Last-mile", "Routing", "Cost Control"],
    requirements: [
      "5+ years managing delivery fleets in a high-volume environment",
      "Strong grasp of route optimisation and driver KPIs",
      "Experience negotiating maintenance and fuel contracts",
      "Data-driven approach to cost per drop"
    ]
  },
  {
    id: 9,
    title: "Backend Engineer (Node.js)",
    dept: "Engineering",
    location: "Remote",
    type: "Full-time",
    level: "Senior",
    salary: "₦850k – ₦1.2M / month",
    fee: 2500,
    posted: "3 weeks ago",
    order: 9,
    summary: "Scale the APIs and event pipelines behind orders, payments and logistics tracking.",
    tags: ["Node.js", "PostgreSQL", "Kafka"],
    requirements: [
      "5+ years building backend services in Node.js or Go",
      "Strong PostgreSQL and distributed systems knowledge",
      "Experience with message queues (Kafka, RabbitMQ)",
      "Comfortable owning services in production"
    ]
  }
];

/* =========================================================
   HELPERS
   ========================================================= */
const $  = (sel, ctx = document) => ctx.querySelector(sel);
const $$ = (sel, ctx = document) => [...ctx.querySelectorAll(sel)];
const naira = n => "₦" + n.toLocaleString("en-NG");
const esc = s => String(s).replace(/[&<>"']/g, c => ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));

/* =========================================================
   STATE
   ========================================================= */
const state = {
  category: "all",
  location: "all",
  sort: "newest",
  query: "",
  job: null,
  step: 1,
  method: "card",
  ref: null,
  data: {}   // persisted form values
};

/* =========================================================
   JOB LISTING
   ========================================================= */
const CATEGORIES = ["all", ...new Set(JOBS.map(j => j.dept))];
const LOCATIONS  = ["all", ...new Set(JOBS.map(j => j.location))];

function buildChips() {
  $("#chips").innerHTML = CATEGORIES.map(c => `
    <button class="chip ${c === state.category ? 'active' : ''}" data-cat="${esc(c)}">
      ${c === 'all' ? 'All Roles' : esc(c)}
    </button>
  `).join("");
}

function buildLocationOptions() {
  const sel = $("#locationFilter");
  sel.innerHTML = LOCATIONS.map(l =>
    `<option value="${esc(l)}">${l === 'all' ? 'All locations' : esc(l)}</option>`
  ).join("");
}

function getFilteredJobs() {
  let list = JOBS.filter(j => {
    const catOk = state.category === "all" || j.dept === state.category;
    const locOk = state.location === "all" || j.location === state.location;
    const q = state.query.trim().toLowerCase();
    const qOk = !q || [j.title, j.dept, j.location, j.summary, ...j.tags]
      .join(" ").toLowerCase().includes(q);
    return catOk && locOk && qOk;
  });

  if (state.sort === "fee-low")  list.sort((a, b) => a.fee - b.fee);
  if (state.sort === "fee-high") list.sort((a, b) => b.fee - a.fee);
  if (state.sort === "newest")   list.sort((a, b) => a.order - b.order);

  return list;
}

function renderJobs() {
  const list = getFilteredJobs();
  const grid = $("#jobGrid");

  $("#resultCount").textContent =
    `${list.length} role${list.length === 1 ? "" : "s"} found`;

  if (!list.length) {
    grid.innerHTML = `
      <div class="empty">
        <h3>No roles match your filters</h3>
        <p>Try a different department, location or search term.</p>
      </div>`;
    return;
  }

  grid.innerHTML = list.map(j => `
    <article class="job-card">
      <div class="job-top">
        <div class="job-logo">${esc(j.dept[0])}</div>
        <div>
          <h3>${esc(j.title)}</h3>
          <p class="job-dept">${esc(j.dept)} · ${esc(j.type)} · ${esc(j.level)}</p>
        </div>
      </div>

      <div class="job-meta">
        <span>📍 ${esc(j.location)}</span>
        <span>🕒 ${esc(j.posted)}</span>
      </div>

      <p class="job-summary">${esc(j.summary)}</p>

      <div class="job-tags">
        <span class="tag salary">${esc(j.salary)}</span>
        ${j.tags.map(t => `<span class="tag">${esc(t)}</span>`).join("")}
      </div>

      <div class="job-foot">
        <div class="fee">
          <small>Application fee</small>
          <strong>${naira(j.fee)}</strong>
        </div>
        <button class="btn primary" data-apply="${j.id}">Apply Now</button>
      </div>
    </article>
  `).join("");
}

/* =========================================================
   MODAL: OPEN / CLOSE
   ========================================================= */
const overlay  = $("#overlay");
const modalBody = $("#modalBody");
const stepsEl   = $("#steps");

function openModal(jobId) {
  const job = JOBS.find(j => j.id === jobId);
  if (!job) return;

  state.job = job;
  state.step = 1;
  state.method = "card";
  state.data = {};
  state.ref = null;

  $("#modalTitle").textContent = "Apply for this role";
  $("#modalSub").textContent = "Complete the steps below to submit your application.";
  overlay.classList.add("open");
  document.body.style.overflow = "hidden";
  renderModal();
}

function closeModal() {
  overlay.classList.remove("open");
  document.body.style.overflow = "";
}

$("#closeModal").addEventListener("click", closeModal);
overlay.addEventListener("click", e => { if (e.target === overlay) closeModal(); });
document.addEventListener("keydown", e => {
  if (e.key === "Escape" && overlay.classList.contains("open")) closeModal();
});

/* =========================================================
   MODAL: RENDER
   ========================================================= */
function renderSteps() {
  const labels = ["Details", "Payment", "Application", "Done"];
  stepsEl.innerHTML = labels.map((label, i) => {
    const n = i + 1;
    const cls = n < state.step ? "done" : n === state.step ? "active" : "";
    return `<div class="step ${cls}">
      <span class="dot">${n < state.step ? "✓" : n}</span>
      <em>${label}</em>
    </div>`;
  }).join("");
}

function renderModal() {
  renderSteps();
  modalBody.scrollTop = 0;

  if (state.step === 1) renderStepDetails();
  if (state.step === 2) renderStepPayment();
  if (state.step === 3) renderStepApplication();
  if (state.step === 4) renderStepSuccess();
}

/* ---------- STEP 1: DETAILS ---------- */
function renderStepDetails() {
  const j = state.job;

  modalBody.innerHTML = `
    <div class="job-summary-box">
      <div class="job-logo">${esc(j.dept[0])}</div>
      <div>
        <h3>${esc(j.title)}</h3>
        <div class="meta">
          <span>📍 ${esc(j.location)}</span>
          <span>💼 ${esc(j.type)}</span>
          <span>🎯 ${esc(j.level)}</span>
        </div>
      </div>
    </div>

    <h4 style="font-size:13px;font-weight:800;text-transform:uppercase;letter-spacing:.6px;margin-bottom:12px;">
      Key Requirements
    </h4>
    <ul class="includes" style="margin-bottom:22px;">
      ${j.requirements.map(r => `<li>${esc(r)}</li>`).join("")}
    </ul>

    <h4 style="font-size:13px;font-weight:800;text-transform:uppercase;letter-spacing:.6px;margin-bottom:12px;">
      Fee Breakdown
    </h4>
    <div class="fee-box">
      <div class="fee-row"><span>Application processing fee</span><span>${naira(j.fee)}</span></div>
      <div class="fee-row"><span>Skills assessment & verification</span><span>Included</span></div>
      <div class="fee-row"><span>Priority recruiter routing</span><span>Included</span></div>
      <div class="fee-row total"><span>Total due today</span><span>${naira(j.fee)}</span></div>
    </div>

    <label class="check">
      <input type="checkbox" id="agreeFee">
      <span>I understand that the application fee of <strong>${naira(j.fee)}</strong> is
      non-refundable once my application is submitted, and that payment does not guarantee employment.</span>
    </label>

    <div class="modal-actions">
      <button class="btn ghost" id="cancelBtn">Cancel</button>
      <button class="btn primary" id="toPayment" disabled>Continue to Payment</button>
    </div>
  `;

  const agree = $("#agreeFee");
  const next  = $("#toPayment");

  agree.addEventListener("change", () => { next.disabled = !agree.checked; });
  $("#cancelBtn").addEventListener("click", closeModal);
  next.addEventListener("click", () => { state.step = 2; renderModal(); });
}

/* ---------- STEP 2: PAYMENT ---------- */
function renderStepPayment() {
  const j = state.job;

  modalBody.innerHTML = `
    <div class="fee-box" style="margin-bottom:20px;">
      <div class="fee-row total" style="border:none;margin:0;padding:0;">
        <span>Amount to pay</span><span>${naira(j.fee)}</span>
      </div>
    </div>

    <div class="pay-methods" id="payMethods">
      <button class="pay-method ${state.method === 'card' ? 'active' : ''}" data-method="card">
        <span class="ico">💳</span> Card
      </button>
      <button class="pay-method ${state.method === 'transfer' ? 'active' : ''}" data-method="transfer">
        <span class="ico">🏦</span> Bank Transfer
      </button>
      <button class="pay-method ${state.method === 'ussd' ? 'active' : ''}" data-method="ussd">
        <span class="ico">📱</span> USSD
      </button>
    </div>

    <div id="payBody"></div>

    <div class="modal-actions">
      <button class="btn ghost" id="backBtn">Back</button>
      <button class="btn primary" id="payBtn">Pay ${naira(j.fee)}</button>
    </div>
  `;

  renderPayBody();

  $$("#payMethods .pay-method").forEach(btn => {
    btn.addEventListener("click", () => {
      state.method = btn.dataset.method;
      $$("#payMethods .pay-method").forEach(b =>
        b.classList.toggle("active", b.dataset.method === state.method));
      renderPayBody();
    });
  });

  $("#backBtn").addEventListener("click", () => { state.step = 1; renderModal(); });
  $("#payBtn").addEventListener("click", processPayment);
}

function renderPayBody() {
  const body = $("#payBody");

  if (state.method === "card") {
    body.innerHTML = `
      <div class="field">
        <label for="cardName">Cardholder name</label>
        <input type="text" id="cardName" placeholder="e.g. Adaeze Okonkwo" autocomplete="cc-name">
        <p class="err-msg">Please enter the name on your card.</p>
      </div>
      <div class="field">
        <label for="cardNumber">Card number</label>
        <input type="text" id="cardNumber" placeholder="0000 0000 0000 0000"
               inputmode="numeric" autocomplete="cc-number" maxlength="19">
        <p class="err-msg">Enter a valid 16-digit card number.</p>
      </div>
      <div class="field-row">
        <div class="field">
          <label for="cardExpiry">Expiry</label>
          <input type="text" id="cardExpiry" placeholder="MM/YY" inputmode="numeric" maxlength="5" autocomplete="cc-exp">
          <p class="err-msg">Use MM/YY format.</p>
        </div>
        <div class="field">
          <label for="cardCvv">CVV</label>
          <input type="password" id="cardCvv" placeholder="•••" inputmode="numeric" maxlength="4" autocomplete="cc-csc">
          <p class="err-msg">Enter the 3-digit code.</p>
        </div>
      </div>
      <div class="notice">
        <span>🔒</span>
        <span><strong>Secured by Paystack.</strong> Your card details are encrypted and never stored on our servers.</span>
      </div>
    `;
    bindCardFormatting();

  } else if (state.method === "transfer") {
    body.innerHTML = `
      <div class="transfer-box">
        <div class="transfer-row">
          <span>Bank</span><strong>Wema Bank</strong>
        </div>
        <div class="transfer-row">
          <span>Account name</span><strong>Jumia Careers Ltd</strong>
        </div>
        <div class="transfer-row">
          <span>Account number</span>
          <span style="display:flex;align-items:center;gap:10px;">
            <strong>7829104455</strong>
            <button class="copy-btn" data-copy="7829104455">Copy</button>
          </span>
        </div>
        <div class="transfer-row">
          <span>Amount</span><strong>${naira(state.job.fee)}</strong>
        </div>
        <div class="transfer-row">
          <span>Reference</span><strong>JUM-${state.job.id}${Date.now().toString().slice(-5)}</strong>
        </div>
      </div>
      <div class="notice">
        <span>ℹ️</span>
        <span>Transfer the exact amount using the reference above, then tap <strong>Pay ${naira(state.job.fee)}</strong> to confirm. Verification usually takes under 2 minutes.</span>
      </div>
    `;
    bindCopyButtons();

  } else {
    body.innerHTML = `
      <div class="transfer-box" style="text-align:center;padding:28px 18px;">
        <p style="font-size:13px;color:var(--gray);margin-bottom:12px;">Dial this code on your registered phone</p>
        <p style="font-size:26px;font-weight:800;letter-spacing:1.5px;color:var(--orange-dark);margin-bottom:14px;">
          *737*000*${state.job.fee}#
        </p>
        <button class="copy-btn" data-copy="*737*000*${state.job.fee}#">Copy USSD code</button>
      </div>
      <div class="notice">
        <span>ℹ️</span>
        <span>Follow the prompts on your phone to authorise the payment, then tap <strong>Pay ${naira(state.job.fee)}</strong> below to confirm.</span>
      </div>
    `;
    bindCopyButtons();
  }
}

function bindCardFormatting() {
  const num = $("#cardNumber");
  const exp = $("#cardExpiry");

  if (num) num.addEventListener("input", e => {
    let v = e.target.value.replace(/\D/g, "").slice(0, 16);
    e.target.value = v.replace(/(.{4})/g, "$1 ").trim();
  });

  if (exp) exp.addEventListener("input", e => {
    let v = e.target.value.replace(/\D/g, "").slice(0, 4);
    e.target.value = v.length > 2 ? v.slice(0, 2) + "/" + v.slice(2) : v;
  });
}

function bindCopyButtons() {
  $$("[data-copy]").forEach(btn => {
    btn.addEventListener("click", async () => {
      try {
        await navigator.clipboard.writeText(btn.dataset.copy);
        showToast("✓ Copied to clipboard");
      } catch {
        showToast("Copy not supported in this browser");
      }
    });
  });
}

/* ---------- PAYMENT PROCESSING ---------- */
function processPayment() {
  if (state.method === "card" && !validateCard()) return;

  const btn = $("#payBtn");
  btn.disabled = true;
  btn.innerHTML = `<span class="spinner"></span> Processing…`;

  setTimeout(() => {
    state.ref = "JM-" + new Date().getFullYear() + "-" +
                Math.random().toString(36).slice(2, 7).toUpperCase();
    state.step = 3;
    renderModal();
    showToast("✓ Payment successful");
  }, 1700);
}

function validateCard() {
  let ok = true;

  const checks = [
    { id: "cardName",   test: v => v.trim().length >= 3 },
    { id: "cardNumber", test: v => v.replace(/\s/g, "").length === 16 },
    { id: "cardExpiry", test: v => /^\d{2}\/\d{2}$/.test(v) },
    { id: "cardCvv",    test: v => /^\d{3,4}$/.test(v) }
  ];

  checks.forEach(({ id, test }) => {
    const input = $("#" + id);
    if (!input) return;
    const field = input.closest(".field");
    const valid = test(input.value);
    field.classList.toggle("invalid", !valid);
    if (!valid && ok) {
      input.focus();
      ok = false;
    }
  });

  return ok;
}

/* ---------- STEP 3: APPLICATION FORM ---------- */
function renderStepApplication() {
  const d = state.data;

  modalBody.innerHTML = `
    <div class="notice" style="margin-bottom:20px;background:#E9F7F0;">
      <span>✅</span>
      <span><strong>Payment confirmed.</strong> Reference <strong>${esc(state.ref)}</strong>.
      Now complete your applicant profile.</span>
    </div>

    <div class="field">
      <label for="fullName">Full name *</label>
      <input type="text" id="fullName" placeholder="Adaeze Okonkwo" value="${esc(d.fullName || '')}">
      <p class="err-msg">Please enter your full name.</p>
    </div>

    <div class="field-row">
      <div class="field">
        <label for="email">Email address *</label>
        <input type="email" id="email" placeholder="you@example.com" value="${esc(d.email || '')}">
        <p class="err-msg">Enter a valid email address.</p>
      </div>
      <div class="field">
        <label for="phone">Phone number *</label>
        <input type="tel" id="phone" placeholder="+234 800 000 0000" value="${esc(d.phone || '')}">
        <p class="err-msg">Enter a valid phone number.</p>
      </div>
    </div>

    <div class="field">
      <label for="linkedin">LinkedIn or portfolio URL</label>
      <input type="url" id="linkedin" placeholder="https://linkedin.com/in/yourprofile" value="${esc(d.linkedin || '')}">
    </div>

    <div class="field">
      <label for="cover">Why are you a great fit? *</label>
      <textarea id="cover" placeholder="Tell us about your relevant experience in 3–5 sentences…">${esc(d.cover || '')}</textarea>
      <p class="err-msg">Please write at least 40 characters.</p>
    </div>

    <div class="field">
      <label>Attach your CV *</label>
      <label class="upload" for="cv">
        <input type="file" id="cv" accept=".pdf,.doc,.docx" hidden>
        <span class="up-ico">📄</span>
        <span>Click to upload your CV</span>
        <small>PDF, DOC or DOCX — max 5MB</small>
        <em id="fileName">${d.fileName ? esc(d.fileName) : ""}</em>
      </label>
      <p class="err-msg" id="cvErr" style="display:none;">Please attach your CV.</p>
    </div>

    <div class="modal-actions">
      <button class="btn ghost" id="backBtn">Back</button>
      <button class="btn primary" id="submitBtn">Submit Application</button>
    </div>
  `;

  // Persist values as the user types
  ["fullName", "email", "phone", "linkedin", "cover"].forEach(id => {
    const el = $("#" + id);
    if (el) el.addEventListener("input", () => { state.data[id] = el.value; });
  });

  $("#cv").addEventListener("change", e => {
    const file = e.target.files[0];
    if (!file) return;
    if (file.size > 5 * 1024 * 1024) {
      showToast("File too large — max 5MB");
      e.target.value = "";
      return;
    }
    state.data.fileName = file.name;
    $("#fileName").textContent = file.name;
    $("#cvErr").style.display = "none";
  });

  $("#backBtn").addEventListener("click", () => { state.step = 2; renderModal(); });
  $("#submitBtn").addEventListener("click", submitApplication);
}

function submitApplication() {
  let ok = true;
  const d = state.data;

  const rules = [
    { id: "fullName", valid: (d.fullName || "").trim().length >= 3 },
    { id: "email",    valid: /^[^\s@]+@[^\s@]+\.[^\s@]{2,}$/.test(d.email || "") },
    { id: "phone",    valid: (d.phone || "").replace(/\D/g, "").length >= 10 },
    { id: "cover",    valid: (d.cover || "").trim().length >= 40 }
  ];

  rules.forEach(({ id, valid }) => {
    const input = $("#" + id);
    if (!input) return;
    input.closest(".field").classList.toggle("invalid", !valid);
    if (!valid && ok) { input.focus(); ok = false; }
  });

  if (!d.fileName) {
    $("#cvErr").style.display = "block";
    ok = false;
  }

  if (!ok) {
    showToast("Please fix the highlighted fields");
    return;
  }

  const btn = $("#submitBtn");
  btn.disabled = true;
  btn.innerHTML = `<span class="spinner"></span> Submitting…`;

  setTimeout(() => {
    state.step = 4;
    renderModal();
    showToast("✓ Application submitted");
  }, 1500);
}

/* ---------- STEP 4: SUCCESS ---------- */
function renderStepSuccess() {
  const j = state.job;

  modalBody.innerHTML = `
    <div class="success">
      <div class="success-icon">✓</div>
      <h2>Application Submitted!</h2>
      <p>Thank you, ${esc((state.data.fullName || "candidate").split(" ")[0])}.
         Your application for <strong>${esc(j.title)}</strong> is now with our recruitment team.</p>

      <div class="ref-box">
        <small>Your reference number</small>
        <strong>${esc(state.ref)}</strong>
      </div>

      <div class="next-steps">
        <h4>What happens next</h4>
        <ol>
          <li>A confirmation email with your receipt has been sent to <strong>${esc(state.data.email || "your inbox")}</strong>.</li>
          <li>Our recruiters review your profile and CV within 72 hours.</li>
          <li>Shortlisted candidates receive a skills assessment link.</li>
          <li>Successful candidates are invited to a virtual interview.</li>
        </ol>
      </div>

      <div class="modal-actions">
        <button class="btn ghost" id="receiptBtn">Download Receipt</button>
        <button class="btn primary" id="doneBtn">Done</button>
      </div>
    </div>
  `;

  $("#doneBtn").addEventListener("click", closeModal);
  $("#receiptBtn").addEventListener("click", () =>
    showToast("Receipt sent to your email 📧"));
}

/* =========================================================
   TOAST
   ========================================================= */
let toastTimer;
function showToast(msg) {
  const t = $("#toast");
  t.textContent = msg;
  t.classList.add("show");
  clearTimeout(toastTimer);
  toastTimer = setTimeout(() => t.classList.remove("show"), 2800);
}

/* =========================================================
   EVENTS
   ========================================================= */
// Apply buttons (event delegation — cards are re-rendered)
$("#jobGrid").addEventListener("click", e => {
  const btn = e.target.closest("[data-apply]");
  if (btn) openModal(Number(btn.dataset.apply));
});

// Category chips
$("#chips").addEventListener("click", e => {
  const chip = e.target.closest("[data-cat]");
  if (!chip) return;
  state.category = chip.dataset.cat;
  $$("#chips .chip").forEach(c =>
    c.classList.toggle("active", c.dataset.cat === state.category));
  renderJobs();
});

// Location + sort
$("#locationFilter").addEventListener("change", e => {
  state.location = e.target.value;
  renderJobs();
});

$("#sortFilter").addEventListener("change", e => {
  state.sort = e.target.value;
  renderJobs();
});

// Hero search
$("#heroSearch").addEventListener("submit", e => {
  e.preventDefault();
  state.query = $("#heroInput").value;
  renderJobs();
  document.getElementById("jobs").scrollIntoView({ behavior: "smooth" });
});

// Live search as you type
$("#heroInput").addEventListener("input", e => {
  state.query = e.target.value;
  renderJobs();
});

/* =========================================================
   INIT
   ========================================================= */
buildChips();
buildLocationOptions();
renderJobs();
</script>
</body>
</html>