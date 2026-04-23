
ALGO Website
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Algo Official Management</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,300;0,400;0,600;1,300;1,400&family=Raleway:wght@200;300;400;500;600&display=swap" rel="stylesheet">
<style>
:root{--white:#fff;--off-white:#F7F6F2;--light:#E8E7E3;--mid:#9A9890;--dark:#2A2A2A;--near-black:#111;--black:#050505;--fd:'Playfair Display',Georgia,serif;--fb:'Raleway',sans-serif}
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{background:var(--black);color:var(--white);font-family:var(--fb);font-weight:300;line-height:1.75;overflow-x:hidden}

/* NAV */
nav{position:fixed;top:0;left:0;right:0;z-index:100;display:flex;align-items:center;justify-content:space-between;padding:1.2rem 4rem;background:rgba(5,5,5,.96);backdrop-filter:blur(20px);border-bottom:1px solid rgba(255,255,255,.06)}
.nav-logo img{height:42px;width:auto;display:block}
.nav-links{display:flex;gap:2.5rem;list-style:none}
.nav-links a{font-size:.58rem;letter-spacing:.28em;text-transform:uppercase;color:var(--mid);text-decoration:none;transition:color .3s}
.nav-links a:hover{color:var(--white)}
.nav-cta{font-size:.58rem;letter-spacing:.22em;text-transform:uppercase;color:var(--black);background:var(--white);padding:.65rem 1.6rem;text-decoration:none;font-weight:500;transition:background .3s}
.nav-cta:hover{background:var(--off-white)}

/* HERO */
#hero{min-height:100vh;display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center;padding:9rem 2rem 5rem;position:relative;overflow:hidden}
.hero-grid{position:absolute;inset:0;background-image:linear-gradient(rgba(255,255,255,.025) 1px,transparent 1px),linear-gradient(90deg,rgba(255,255,255,.025) 1px,transparent 1px);background-size:80px 80px;mask-image:radial-gradient(ellipse 80% 80% at 50% 50%,black 0%,transparent 100%)}
.hero-rule-top{width:1px;height:60px;background:linear-gradient(to bottom,transparent,rgba(255,255,255,.2));margin:0 auto 2rem;position:relative}
.hero-logo img{height:clamp(100px,16vw,200px);width:auto;display:block;margin:0 auto 3rem}
.eyebrow{font-size:.58rem;letter-spacing:.45em;text-transform:uppercase;color:var(--mid);margin-bottom:1.8rem;position:relative}
h1{font-family:var(--fd);font-size:clamp(3.5rem,8vw,7.5rem);font-weight:300;line-height:1.03;letter-spacing:-.02em;margin-bottom:1.8rem;position:relative}
h1 em{font-style:italic}
.hero-rule{width:40px;height:1px;background:rgba(255,255,255,.25);margin:0 auto 1.8rem}
.hero-sub{font-size:.82rem;letter-spacing:.06em;color:var(--mid);max-width:440px;margin:0 auto 3rem;position:relative}
.hero-btns{display:flex;gap:1rem;justify-content:center;flex-wrap:wrap;position:relative}

/* BUTTONS */
.btn-p{background:var(--white);color:var(--black);padding:1rem 2.4rem;font-family:var(--fb);font-size:.6rem;font-weight:600;letter-spacing:.25em;text-transform:uppercase;text-decoration:none;display:inline-block;transition:background .3s,transform .2s}
.btn-p:hover{background:var(--off-white);transform:translateY(-1px)}
.btn-g{border:1px solid rgba(255,255,255,.2);color:var(--white);padding:1rem 2.4rem;font-family:var(--fb);font-size:.6rem;font-weight:400;letter-spacing:.25em;text-transform:uppercase;text-decoration:none;display:inline-block;transition:border-color .3s,background .3s}
.btn-g:hover{border-color:rgba(255,255,255,.5);background:rgba(255,255,255,.04)}

/* DIVIDER */
.rule{width:100%;height:1px;background:rgba(255,255,255,.07)}

/* STATS */
#stats{display:grid;grid-template-columns:repeat(3,1fr)}
.stat{padding:3.5rem 2rem;text-align:center;border-right:1px solid rgba(255,255,255,.07)}
.stat:last-child{border-right:none}
.stat-n{font-family:var(--fd);font-size:3.8rem;font-weight:300;line-height:1;margin-bottom:.6rem}
.stat-l{font-size:.58rem;letter-spacing:.25em;text-transform:uppercase;color:var(--mid)}

/* SECTIONS */
section{padding:7rem 2rem}
.inner{max-width:1100px;margin:0 auto}
.stag{font-size:.55rem;letter-spacing:.35em;text-transform:uppercase;color:var(--mid);margin-bottom:1.2rem;display:block}
h2{font-family:var(--fd);font-size:clamp(2rem,4vw,3.2rem);font-weight:300;line-height:1.15;margin-bottom:1.5rem}
h2 em{font-style:italic}

/* WHY */
#why{background:#0C0C0C;border-top:1px solid rgba(255,255,255,.06);border-bottom:1px solid rgba(255,255,255,.06)}
.why-grid{display:grid;grid-template-columns:1fr 1fr;gap:5rem;align-items:center;margin-top:3rem}
.why-body p{font-size:.84rem;color:var(--mid);margin-bottom:1.1rem;line-height:1.9}
.why-cards{display:grid;grid-template-columns:1fr 1fr;gap:1px;background:rgba(255,255,255,.07);border:1px solid rgba(255,255,255,.07)}
.wc{background:#0C0C0C;padding:1.8rem 1.5rem;transition:background .3s}
.wc:hover{background:#141414}
.wc-n{font-family:var(--fd);font-size:.7rem;color:var(--mid);margin-bottom:1rem;font-style:italic}
.wc h3{font-family:var(--fd);font-size:1.05rem;font-weight:400;margin-bottom:.5rem}
.wc p{font-size:.74rem;color:var(--mid);line-height:1.7}

/* PRICING */
#pricing{background:var(--black)}
.pricing-grid{display:grid;grid-template-columns:1fr 1fr;gap:1.5rem;margin-top:3rem}
.pc{border:1px solid rgba(255,255,255,.08);padding:3rem 2.5rem;position:relative}
.pc.featured{border-color:var(--white);background:rgba(255,255,255,.02)}
.pc-badge{position:absolute;top:-1px;right:2rem;background:var(--white);color:var(--black);font-size:.5rem;font-weight:600;letter-spacing:.22em;text-transform:uppercase;padding:.3rem .9rem}
.pc-type{font-size:.55rem;letter-spacing:.28em;text-transform:uppercase;color:var(--mid);margin-bottom:1rem;display:block}
.pc-amt{font-family:var(--fd);font-size:3rem;font-weight:300;line-height:1;margin-bottom:.4rem}
.pc-amt.muted{color:var(--mid)}
.pc-note{font-size:.7rem;color:var(--mid);margin-bottom:2rem}
.pc-feats{list-style:none;margin-bottom:2.5rem}
.pc-feats li{font-size:.78rem;color:var(--mid);padding:.6rem 0;border-bottom:1px solid rgba(255,255,255,.06);display:flex;align-items:center;gap:.8rem}
.pc-feats li.bright{color:var(--white)}
.pc-feats li::before{content:'';width:3px;height:3px;border-radius:50%;background:currentColor;flex-shrink:0}
.savings{grid-column:1/-1;border:1px solid rgba(255,255,255,.08);background:#0C0C0C;padding:3rem;display:flex;align-items:center;justify-content:center;gap:4rem;flex-wrap:wrap}
.sv{text-align:center}
.sv-n{font-family:var(--fd);font-size:3rem;font-weight:300;line-height:1;margin-bottom:.4rem}
.sv-n.w{color:var(--white)}
.sv-n.d{color:rgba(255,255,255,.25)}
.sv-l{font-size:.58rem;letter-spacing:.15em;text-transform:uppercase;color:var(--mid)}
.sv-sep{font-family:var(--fd);font-size:1.8rem;font-style:italic;color:rgba(255,255,255,.15)}

/* TESTIMONIALS */
#testimonials{background:#0C0C0C;border-top:1px solid rgba(255,255,255,.06);border-bottom:1px solid rgba(255,255,255,.06)}
.test-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:1.5rem;margin-top:3rem}
.tc{border:1px solid rgba(255,255,255,.08);padding:2.2rem}
.tc-stars{font-size:.6rem;letter-spacing:.1em;color:var(--white);margin-bottom:1.2rem}
.tc-q{font-family:var(--fd);font-size:1rem;font-style:italic;font-weight:300;color:var(--white);line-height:1.75;margin-bottom:1.5rem}
.tc-name{font-size:.6rem;letter-spacing:.18em;text-transform:uppercase;color:var(--mid)}

/* APPLY */
#apply{background:var(--black);border-top:1px solid rgba(255,255,255,.06)}
.apply-grid{display:grid;grid-template-columns:1fr 1.7fr;gap:5rem;align-items:start;margin-top:3rem}
.apply-left h3{font-family:var(--fd);font-size:1.5rem;font-weight:300;margin-bottom:1rem}
.apply-left p{font-size:.8rem;color:var(--mid);margin-bottom:1.5rem;line-height:1.9}
.checks{list-style:none}
.checks li{font-size:.76rem;color:var(--mid);padding:.7rem 0;border-bottom:1px solid rgba(255,255,255,.06);display:flex;gap:.8rem;align-items:flex-start}
.ck{color:var(--white);flex-shrink:0;font-size:.65rem;margin-top:.15rem}
.form-box{background:#0C0C0C;border:1px solid rgba(255,255,255,.08);padding:3rem}
.f-row{display:grid;grid-template-columns:1fr 1fr;gap:1rem}
.fg{margin-bottom:1.1rem}
.fg label{display:block;font-size:.55rem;letter-spacing:.22em;text-transform:uppercase;color:var(--mid);margin-bottom:.45rem}
.fg input,.fg select,.fg textarea{width:100%;background:rgba(255,255,255,.03);border:1px solid rgba(255,255,255,.1);color:var(--white);font-family:var(--fb);font-size:.8rem;font-weight:300;padding:.85rem 1rem;outline:none;transition:border-color .3s;appearance:none}
.fg input:focus,.fg select:focus,.fg textarea:focus{border-color:rgba(255,255,255,.4)}
.fg input::placeholder,.fg textarea::placeholder{color:rgba(255,255,255,.18)}
.fg select{cursor:pointer;background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='10' height='6' viewBox='0 0 10 6'%3E%3Cpath d='M1 1l4 4 4-4' stroke='%239A9890' stroke-width='1.2' fill='none'/%3E%3C/svg%3E");background-repeat:no-repeat;background-position:right 1rem center;padding-right:2.5rem}
.fg select option{background:#0C0C0C}
.fg textarea{resize:vertical;min-height:90px}
.f-submit{width:100%;background:var(--white);color:var(--black);border:none;padding:1.1rem;font-family:var(--fb);font-size:.6rem;font-weight:600;letter-spacing:.28em;text-transform:uppercase;cursor:pointer;transition:background .3s,transform .2s;margin-top:.5rem}
.f-submit:hover{background:var(--off-white);transform:translateY(-1px)}
.f-disc{font-size:.6rem;color:rgba(255,255,255,.2);text-align:center;margin-top:1rem;line-height:1.6}
.success{display:none;text-align:center;padding:3rem 2rem}
.s-icon{width:56px;height:56px;border:1px solid rgba(255,255,255,.3);border-radius:50%;display:flex;align-items:center;justify-content:center;margin:0 auto 1.5rem;font-size:1.2rem}
.success h3{font-family:var(--fd);font-size:1.8rem;font-weight:300;margin-bottom:.8rem}
.success p{font-size:.78rem;color:var(--mid)}

/* FOOTER */
footer{background:#0C0C0C;border-top:1px solid rgba(255,255,255,.06);padding:3rem 4rem;display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;gap:1.5rem}
.foot-logo img{height:32px;width:auto}
.foot-links{display:flex;gap:2rem;list-style:none}
.foot-links a{font-size:.58rem;letter-spacing:.18em;text-transform:uppercase;color:var(--mid);text-decoration:none;transition:color .3s}
.foot-links a:hover{color:var(--white)}
.foot-copy{font-size:.58rem;color:rgba(255,255,255,.2);letter-spacing:.05em}

/* ANIMATIONS */
@keyframes fadeUp{from{opacity:0;transform:translateY(20px)}to{opacity:1;transform:translateY(0)}}
.fu{opacity:0;animation:fadeUp .9s ease forwards}
.d1{animation-delay:.1s}.d2{animation-delay:.25s}.d3{animation-delay:.4s}.d4{animation-delay:.55s}.d5{animation-delay:.7s}

@media(max-width:900px){
  nav{padding:1rem 1.5rem}
  .nav-links{display:none}
  #stats{grid-template-columns:1fr}
  .stat{border-right:none;border-bottom:1px solid rgba(255,255,255,.07)}
  .why-grid,.pricing-grid,.apply-grid{grid-template-columns:1fr}
  .savings{gap:2rem}
  .test-grid{grid-template-columns:1fr}
  .f-row{grid-template-columns:1fr}
  .form-box{padding:2rem 1.5rem}
  footer{padding:2rem 1.5rem;flex-direction:column;align-items:flex-start}
}
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a class="nav-logo" href="#"><img src="https://i.imgur.com/placeholder.png" onerror="this.style.display='none';this.nextSibling.style.display='block'" alt=""><span style="display:block;font-family:'Playfair Display',serif;font-size:1.1rem;font-weight:300;letter-spacing:.12em;color:#fff">ALGO OFFICIAL</span></a>
  <ul class="nav-links">
    <li><a href="#why">Why Us</a></li>
    <li><a href="#pricing">Pricing</a></li>
    <li><a href="#testimonials">Creators</a></li>
    <li><a href="#apply">Apply</a></li>
  </ul>
  <a class="nav-cta" href="#apply">Apply Now</a>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-grid"></div>
  <div class="hero-rule-top"></div>
  <div class="hero-logo fu d1"><img src="https://i.imgur.com/placeholder.png" onerror="this.style.display='none'" alt="" style="height:clamp(100px,16vw,200px);display:block;margin:0 auto 3rem"></div>
  <p class="eyebrow fu d2">Premium Creator Management</p>
  <h1 class="fu d3">Your talent.<br><em>Your earnings.</em></h1>
  <div class="hero-rule"></div>
  <p class="hero-sub fu d4">We help creators grow and keep more of what they earn — without the industry's standard 50/50 split.</p>
  <div class="hero-btns fu d5">
    <a class="btn-p" href="#apply">Apply to Work With Us</a>
    <a class="btn-g" href="#why">Learn More</a>
  </div>
</section>

<div class="rule"></div>

<!-- STATS -->
<div id="stats">
  <div class="stat"><div class="stat-n">$1.5K</div><div class="stat-l">Flat Monthly Fee</div></div>
  <div class="stat"><div class="stat-n">10%</div><div class="stat-l">On Messages Only</div></div>
  <div class="stat"><div class="stat-n">0%</div><div class="stat-l">Cut on Subs, PPV &amp; Tips</div></div>
</div>

<div class="rule"></div>

<!-- WHY -->
<section id="why">
  <div class="inner">
    <span class="stag">The Algo Difference</span>
    <h2>Built for creators who <em>refuse to settle</em></h2>
    <div class="why-grid">
      <div class="why-body">
        <p>Most agencies take 50% of everything you make. That's thousands leaving your account every month — money that should be funding your life, your brand, your future.</p>
        <p>At Algo Official, we operate differently. A flat monthly fee covers your management, strategy, and growth. We only earn on direct messages — so our incentive is always aligned with yours.</p>
        <p>Your subscriptions, your PPV, your tips: entirely yours.</p>
        <a class="btn-p" href="#apply" style="margin-top:1.5rem">Start Your Application</a>
      </div>
      <div class="why-cards">
        <div class="wc"><div class="wc-n">01</div><h3>Transparent Pricing</h3><p>You always know exactly what we take. No surprises, no hidden percentages.</p></div>
        <div class="wc"><div class="wc-n">02</div><h3>Full Growth Strategy</h3><p>Account management, content strategy, and messaging optimisation — all included.</p></div>
        <div class="wc"><div class="wc-n">03</div><h3>Aligned Incentives</h3><p>We earn more when your messages grow — so we're fully invested in your success.</p></div>
        <div class="wc"><div class="wc-n">04</div><h3>Easy Onboarding</h3><p>Works for new and established creators. Direct access to your manager from day one.</p></div>
      </div>
    </div>
  </div>
</section>

<!-- PRICING -->
<section id="pricing">
  <div class="inner">
    <span class="stag">Pricing</span>
    <h2>Keep more of <em>what you earn</em></h2>
    <div class="pricing-grid">
      <div class="pc">
        <span class="pc-type">Industry Standard</span>
        <div class="pc-amt muted">50%</div>
        <p class="pc-note">of your total revenue, every month</p>
        <ul class="pc-feats">
          <li>50% of subscriptions taken</li>
          <li>50% of PPV content taken</li>
          <li>50% of tips taken</li>
          <li>50% of messages taken</li>
          <li style="opacity:.4">No earnings transparency</li>
        </ul>
      </div>
      <div class="pc featured">
        <div class="pc-badge">Algo Official</div>
        <span class="pc-type">Our Structure</span>
        <div class="pc-amt">$1,500</div>
        <p class="pc-note">flat/month + 10% on messages only</p>
        <ul class="pc-feats">
          <li class="bright">100% of subscriptions — yours</li>
          <li class="bright">100% of PPV — yours</li>
          <li class="bright">100% of tips — yours</li>
          <li class="bright">10% on direct messages only</li>
          <li class="bright">Full earnings transparency</li>
        </ul>
        <a class="btn-p" href="#apply">Apply Now</a>
      </div>
      <div class="savings">
        <div class="sv"><div class="sv-n d">$5,000</div><div class="sv-l">Typical agency cut at $10K/mo</div></div>
        <div class="sv-sep">vs</div>
        <div class="sv"><div class="sv-n w">~$1,800</div><div class="sv-l">Algo Official at $10K/mo</div></div>
        <div class="sv-sep">=</div>
        <div class="sv"><div class="sv-n w">$3,200+</div><div class="sv-l">Extra in your pocket each month</div></div>
      </div>
    </div>
  </div>
</section>

<!-- TESTIMONIALS -->
<section id="testimonials">
  <div class="inner">
    <span class="stag">Creator Stories</span>
    <h2>What our creators <em>say</em></h2>
    <div class="test-grid">
      <div class="tc"><div class="tc-stars">★ ★ ★ ★ ★</div><p class="tc-q">"Switching to Algo was the best business decision I've made. I kept over $3,000 more in my very first month."</p><div class="tc-name">— Mila Seaves, 6 months with Algo</div></div>
      <div class="tc"><div class="tc-stars">★ ★ ★ ★ ★</div><p class="tc-q">"I finally feel like my manager is actually working for me. The transparency here is unlike anything I've experienced."</p><div class="tc-name">— Jaymee, 4 months with Algo</div></div>
      <div class="tc"><div class="tc-stars">★ ★ ★ ★ ★</div><p class="tc-q">"My messaging revenue tripled in 60 days. When your manager's income is tied to yours, they truly show up."</p><div class="tc-name">— Olivia Stone, 8 months with Algo</div></div>
    </div>
  </div>
</section>

<!-- APPLY -->
<section id="apply">
  <div class="inner">
    <span class="stag">Join Algo Official</span>
    <h2>Apply to work <em>with us</em></h2>
    <div class="apply-grid">
      <div class="apply-left">
        <h3>What to expect</h3>
        <p>We review every application personally. If we're a good fit, you'll hear from us within 48 hours to schedule a no-pressure call.</p>
        <ul class="checks">
          <li><span class="ck">✦</span>Application reviewed within 48 hours</li>
          <li><span class="ck">✦</span>No long-term lock-in contracts</li>
          <li><span class="ck">✦</span>Direct access to your manager from day one</li>
          <li><span class="ck">✦</span>Full onboarding strategy session included</li>
          <li><span class="ck">✦</span>Works for new and established creators</li>
        </ul>
      </div>
      <div class="form-box" id="appForm">
        <div id="formFields">
          <div class="f-row">
            <div class="fg"><label>First Name</label><input type="text" placeholder="Your first name"></div>
            <div class="fg"><label>Last Name</label><input type="text" placeholder="Your last name"></div>
          </div>
          <div class="fg"><label>Email Address</label><input type="email" placeholder="you@example.com"></div>
          <div class="fg"><label>Instagram or OnlyFans Handle</label><input type="text" placeholder="@yourhandle"></div>
          <div class="fg">
            <label>Current Monthly Revenue</label>
            <select><option value="" disabled selected>Select range</option><option>Just starting out ($0–$500/mo)</option><option>Growing ($500–$2K/mo)</option><option>Established ($2K–$5K/mo)</option><option>Scaling ($5K–$10K/mo)</option><option>Top earner ($10K+/mo)</option></select>
          </div>
          <div class="fg">
            <label>Do you currently have a manager?</label>
            <select><option value="" disabled selected>Select one</option><option>No — I manage myself</option><option>Yes — looking to switch</option><option>Yes — but exploring options</option></select>
          </div>
          <div class="fg"><label>Tell Us About Yourself (Optional)</label><textarea placeholder="Your goals, your niche, what you're looking for in a manager..."></textarea></div>
          <button class="f-submit" onclick="submitForm()">Submit Application &rarr;</button>
          <p class="f-disc">All applications are reviewed confidentially. We respect your privacy.</p>
        </div>
        <div class="success" id="formSuccess">
          <div class="s-icon">✦</div>
          <h3>Application Received</h3>
          <p>Thank you for applying. Our team will review your application and be in touch within 48 hours.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="foot-logo"><span style="font-family:'Playfair Display',serif;font-size:1rem;font-weight:300;letter-spacing:.12em;color:#fff">ALGO OFFICIAL</span></div>
  <ul class="foot-links">
    <li><a href="#why">Why Us</a></li>
    <li><a href="#pricing">Pricing</a></li>
    <li><a href="#apply">Apply</a></li>
    <li><a href="https://www.instagram.com/algofficialmanagement/" target="_blank">Instagram</a></li>
  </ul>
  <span class="foot-copy">&copy; 2026 Algo Official Management. All rights reserved.</span>
</footer>

<script>
function submitForm(){
  var f=document.getElementById('formFields'),fn=f.querySelector('input[placeholder="Your first name"]').value,ln=f.querySelector('input[placeholder="Your last name"]').value,em=f.querySelector('input[type="email"]').value,hd=f.querySelector('input[placeholder="@yourhandle"]').value,sels=f.querySelectorAll('select'),rv=sels[0]?sels[0].value:'',mg=sels[1]?sels[1].value:'',ms=f.querySelector('textarea').value;
  var sub=encodeURIComponent('New Creator Application — Algo Official Management');
  var bod=encodeURIComponent('NEW APPLICATION\n\nName: '+fn+' '+ln+'\nEmail: '+em+'\nHandle: '+hd+'\nMonthly Revenue: '+rv+'\nCurrent Manager: '+mg+'\n\nAbout Them:\n'+ms);
  window.location.href='mailto:YOUR_EMAIL_HERE?subject='+sub+'&body='+bod;
  document.getElementById('formFields').style.display='none';
  document.getElementById('formSuccess').style.display='block';
}
var obs=new IntersectionObserver(function(e){e.forEach(function(x){if(x.isIntersecting){x.target.style.opacity='1';x.target.style.transform='translateY(0)'}})},{threshold:.1});
document.querySelectorAll('.wc,.pc,.tc').forEach(function(el){el.style.opacity='0';el.style.transform='translateY(18px)';el.style.transition='opacity .7s ease,transform .7s ease';obs.observe(el)});
</script>
</body>
</html>
