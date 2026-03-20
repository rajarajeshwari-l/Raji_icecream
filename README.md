<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Raji Ice Cream 💙</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,700;0,900;1,700&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
:root {
  --cream: #FFF8F0;
  --coral: #FF6B6B;
  --pink: #FF8FAB;
  --berry: #C084FC;
  --blue: #3B82F6;
  --lightblue: #DBEAFE;
  --dark: #2D1B13;
  --gold: #F59E0B;
  --peach: #FFCBA4;
  --mint: #6EE7B7;
}
* { margin:0; padding:0; box-sizing:border-box; }
body { font-family:'DM Sans',sans-serif; background:var(--cream); color:var(--dark); overflow-x:hidden; }

/* BG */
.bg-blobs { position:fixed; inset:0; z-index:0; overflow:hidden; pointer-events:none; }
.blob { position:absolute; border-radius:50%; filter:blur(80px); opacity:0.3; animation:blobFloat 10s ease-in-out infinite; }
.blob1 { width:500px; height:500px; background:#FFCBA4; top:-100px; left:-100px; }
.blob2 { width:400px; height:400px; background:#FF8FAB; top:40%; right:-100px; animation-delay:3s; }
.blob3 { width:350px; height:350px; background:#C084FC; bottom:-50px; left:20%; animation-delay:6s; }
.blob4 { width:300px; height:300px; background:#93C5FD; top:60%; left:-80px; animation-delay:1.5s; }
@keyframes blobFloat { 0%,100%{transform:translateY(0);} 50%{transform:translateY(-25px);} }

/* HEADER */
header { position:sticky; top:0; z-index:50; display:flex; justify-content:space-between; align-items:center; padding:0 5%; height:72px; background:rgba(255,248,240,0.85); backdrop-filter:blur(12px); border-bottom:1px solid rgba(255,107,107,0.12); }
.logo { font-family:'Playfair Display',serif; font-size:1.6rem; font-weight:900; background:linear-gradient(135deg,var(--coral),var(--berry)); -webkit-background-clip:text; -webkit-text-fill-color:transparent; }
.cart-btn { display:flex; align-items:center; gap:8px; background:linear-gradient(135deg,var(--coral),var(--pink)); color:#fff; border:none; padding:10px 20px; border-radius:50px; font-family:'DM Sans',sans-serif; font-weight:700; font-size:0.9rem; cursor:pointer; box-shadow:0 4px 15px rgba(255,107,107,0.3); transition:transform 0.2s; }
.cart-btn:hover { transform:translateY(-2px); }
.cart-badge { background:#fff; color:var(--coral); border-radius:50%; width:22px; height:22px; display:flex; align-items:center; justify-content:center; font-size:0.75rem; font-weight:800; }

/* HERO */
.hero { position:relative; z-index:5; text-align:center; padding:80px 5% 50px; }
.hero-pill { display:inline-block; background:rgba(59,130,246,0.1); border:1.5px solid rgba(59,130,246,0.3); color:var(--blue); padding:6px 20px; border-radius:50px; font-size:0.8rem; font-weight:700; letter-spacing:1px; text-transform:uppercase; margin-bottom:18px; }
.hero h1 { font-family:'Playfair Display',serif; font-size:clamp(2.8rem,6vw,5.5rem); font-weight:900; line-height:1.08; margin-bottom:20px; }
.hero h1 em { font-style:italic; background:linear-gradient(135deg,var(--coral),var(--berry)); -webkit-background-clip:text; -webkit-text-fill-color:transparent; }
.hero p { font-size:1.1rem; color:#7a5c4a; max-width:500px; margin:0 auto 32px; line-height:1.7; }
.hero-btns { display:flex; gap:14px; justify-content:center; flex-wrap:wrap; }
.btn-p { background:linear-gradient(135deg,var(--coral),var(--pink)); color:#fff; border:none; padding:14px 34px; border-radius:50px; font-family:'DM Sans',sans-serif; font-size:1rem; font-weight:700; cursor:pointer; box-shadow:0 6px 20px rgba(255,107,107,0.35); transition:transform 0.2s; text-decoration:none; display:inline-block; }
.btn-p:hover { transform:translateY(-2px); }
.float-ico { position:absolute; font-size:2.8rem; animation:floatY 4s ease-in-out infinite; pointer-events:none; }
.float-ico:nth-child(1){top:12%;left:5%;animation-delay:0s;}
.float-ico:nth-child(2){top:20%;right:6%;animation-delay:1.2s;font-size:2.2rem;}
.float-ico:nth-child(3){bottom:15%;left:7%;animation-delay:2.4s;font-size:2rem;}
.float-ico:nth-child(4){bottom:25%;right:5%;animation-delay:0.8s;}
@keyframes floatY { 0%,100%{transform:translateY(0) rotate(-5deg);} 50%{transform:translateY(-16px) rotate(5deg);} }

/* STATS */
.stats-bar { position:relative; z-index:5; background:linear-gradient(135deg,var(--coral),var(--berry)); display:flex; justify-content:center; gap:50px; flex-wrap:wrap; padding:22px 5%; }
.stat { text-align:center; color:#fff; }
.stat-n { font-family:'Playfair Display',serif; font-size:1.9rem; font-weight:900; display:block; }
.stat-l { font-size:0.75rem; opacity:0.85; text-transform:uppercase; letter-spacing:0.5px; }

/* SECTION */
.section { position:relative; z-index:5; padding:70px 5%; }
.sec-hdr { text-align:center; margin-bottom:40px; }
.sec-lbl { font-size:0.75rem; font-weight:700; letter-spacing:2px; text-transform:uppercase; color:var(--coral); display:block; margin-bottom:10px; }
.sec-title { font-family:'Playfair Display',serif; font-size:clamp(1.8rem,3.5vw,2.8rem); font-weight:900; }
.sec-title em { font-style:italic; color:var(--coral); }

/* FILTER TABS */
.tabs { display:flex; gap:10px; justify-content:center; flex-wrap:wrap; margin-bottom:40px; }
.tab { padding:9px 20px; border-radius:50px; border:2px solid rgba(45,27,19,0.12); background:transparent; font-family:'DM Sans',sans-serif; font-weight:600; font-size:0.85rem; cursor:pointer; color:var(--dark); transition:all 0.2s; }
.tab.active,.tab:hover { background:linear-gradient(135deg,var(--coral),var(--pink)); border-color:transparent; color:#fff; box-shadow:0 4px 14px rgba(255,107,107,0.3); }

/* CARDS */
.grid { display:grid; grid-template-columns:repeat(auto-fill,minmax(270px,1fr)); gap:26px; max-width:1200px; margin:0 auto; }
.card { background:#fff; border-radius:26px; overflow:hidden; box-shadow:0 4px 20px rgba(45,27,19,0.08); transition:transform 0.25s,box-shadow 0.25s; }
.card:hover { transform:translateY(-6px); box-shadow:0 14px 36px rgba(45,27,19,0.13); }
.card-img { width:100%; height:190px; display:flex; align-items:center; justify-content:center; font-size:5rem; position:relative; }
.card-bdg { position:absolute; top:12px; right:12px; background:var(--gold); color:#fff; font-size:0.68rem; font-weight:700; padding:3px 10px; border-radius:50px; text-transform:uppercase; letter-spacing:0.5px; }
.card-body { padding:20px; }
.card-name { font-family:'Playfair Display',serif; font-size:1.2rem; font-weight:700; margin-bottom:5px; }
.card-desc { font-size:0.83rem; color:#9a7060; line-height:1.6; margin-bottom:12px; }
.card-tags { display:flex; gap:6px; flex-wrap:wrap; margin-bottom:16px; }
.ctag { background:rgba(255,107,107,0.1); color:var(--coral); font-size:0.7rem; font-weight:700; padding:3px 10px; border-radius:50px; }
.card-foot { display:flex; align-items:center; justify-content:space-between; }
.price { font-family:'Playfair Display',serif; font-size:1.4rem; font-weight:900; color:var(--coral); }
.price small { font-family:'DM Sans',sans-serif; font-size:0.8rem; color:#bbb; font-weight:400; }

/* ADD / QTY BUTTONS */
.add-btn { width:44px; height:44px; border-radius:50%; background:linear-gradient(135deg,var(--coral),var(--pink)); color:#fff; border:none; font-size:1.6rem; line-height:1; cursor:pointer; box-shadow:0 4px 14px rgba(255,107,107,0.35); transition:transform 0.2s; display:flex; align-items:center; justify-content:center; }
.add-btn:hover { transform:scale(1.15); }
.qty-box { display:flex; align-items:center; gap:8px; background:rgba(255,107,107,0.08); border-radius:50px; padding:4px 8px; }
.q-btn { width:34px; height:34px; border-radius:50%; background:var(--coral); color:#fff; border:none; font-size:1.1rem; cursor:pointer; display:flex; align-items:center; justify-content:center; font-weight:700; transition:transform 0.15s; }
.q-btn:hover { transform:scale(1.12); }
.q-num { font-weight:800; font-size:1rem; min-width:20px; text-align:center; }

/* CART DRAWER */
.overlay { position:fixed; inset:0; background:rgba(0,0,0,0.4); z-index:90; opacity:0; pointer-events:none; transition:opacity 0.3s; backdrop-filter:blur(4px); }
.overlay.on { opacity:1; pointer-events:all; }
.drawer { position:fixed; top:0; right:-110%; width:min(420px,100vw); height:100%; background:#fff; z-index:91; box-shadow:-10px 0 40px rgba(0,0,0,0.12); transition:right 0.35s cubic-bezier(0.4,0,0.2,1); display:flex; flex-direction:column; }
.drawer.on { right:0; }
.drawer-hdr { padding:26px 22px 18px; border-bottom:1px solid rgba(0,0,0,0.07); display:flex; align-items:center; justify-content:space-between; }
.drawer-title { font-family:'Playfair Display',serif; font-size:1.45rem; font-weight:900; }
.x-btn { width:36px; height:36px; border-radius:50%; border:2px solid rgba(0,0,0,0.1); background:transparent; cursor:pointer; font-size:1rem; display:flex; align-items:center; justify-content:center; transition:all 0.2s; }
.x-btn:hover { background:var(--coral); border-color:var(--coral); color:#fff; }
.drawer-body { flex:1; overflow-y:auto; padding:18px 22px; }
.ci { display:flex; align-items:center; gap:12px; padding:13px 0; border-bottom:1px solid rgba(0,0,0,0.05); }
.ci-emoji { font-size:2.2rem; }
.ci-info { flex:1; }
.ci-name { font-weight:600; font-size:0.95rem; }
.ci-price { color:var(--coral); font-weight:700; font-size:0.9rem; margin-top:2px; }
.ci-qty { display:flex; align-items:center; gap:7px; background:rgba(255,107,107,0.08); border-radius:50px; padding:3px 6px; }
.cq { width:28px; height:28px; border-radius:50%; background:var(--coral); color:#fff; border:none; font-size:0.95rem; cursor:pointer; display:flex; align-items:center; justify-content:center; font-weight:700; }
.empty-box { text-align:center; padding:60px 20px; }
.empty-box span { font-size:5rem; display:block; margin-bottom:14px; }
.empty-box p { color:#bbb; }
.drawer-foot { padding:18px 22px; border-top:1px solid rgba(0,0,0,0.07); }
.total-row { display:flex; justify-content:space-between; align-items:center; margin-bottom:6px; font-size:1rem; font-weight:600; }
.total-amt { font-family:'Playfair Display',serif; font-size:1.5rem; color:var(--coral); font-weight:900; }
.del-note { font-size:0.78rem; color:#bbb; text-align:right; margin-bottom:14px; }
.checkout-btn { width:100%; background:linear-gradient(135deg,var(--coral),var(--berry)); color:#fff; border:none; padding:16px; border-radius:16px; font-family:'DM Sans',sans-serif; font-size:1rem; font-weight:700; cursor:pointer; box-shadow:0 6px 20px rgba(255,107,107,0.35); transition:transform 0.2s; }
.checkout-btn:hover { transform:translateY(-2px); }

/* ORDER SUCCESS SCREEN */
.success-screen { position:fixed; inset:0; background:linear-gradient(135deg,#FFF8F0,#FFE4F0); z-index:200; display:none; flex-direction:column; align-items:center; justify-content:center; padding:30px; text-align:center; }
.success-screen.on { display:flex; }
.success-anim { font-size:6rem; animation:bigBounce 0.7s cubic-bezier(0.34,1.56,0.64,1); margin-bottom:10px; }
@keyframes bigBounce { from{transform:scale(0) rotate(-180deg);} to{transform:scale(1) rotate(0);} }
.success-screen h2 { font-family:'Playfair Display',serif; font-size:2.5rem; font-weight:900; margin-bottom:12px; }
.success-screen h2 span { background:linear-gradient(135deg,var(--coral),var(--berry)); -webkit-background-clip:text; -webkit-text-fill-color:transparent; }
.success-screen p { color:#7a5c4a; font-size:1.05rem; line-height:1.7; max-width:380px; margin-bottom:10px; }
.order-id { background:rgba(255,107,107,0.1); border:1.5px dashed var(--coral); border-radius:12px; padding:10px 24px; font-weight:700; color:var(--coral); font-size:0.95rem; margin:12px 0 28px; display:inline-block; }
.track-steps { display:flex; gap:16px; justify-content:center; flex-wrap:wrap; margin-bottom:32px; }
.step { display:flex; flex-direction:column; align-items:center; gap:6px; }
.step-ico { width:56px; height:56px; border-radius:50%; background:#fff; box-shadow:0 4px 14px rgba(255,107,107,0.2); display:flex; align-items:center; justify-content:center; font-size:1.6rem; position:relative; }
.step.done .step-ico { background:linear-gradient(135deg,var(--coral),var(--pink)); }
.step-lbl { font-size:0.75rem; font-weight:600; color:#9a7060; }
.step-line { width:40px; height:3px; background:linear-gradient(90deg,var(--coral),var(--pink)); border-radius:3px; margin-top:28px; }
.back-btn { background:linear-gradient(135deg,var(--coral),var(--berry)); color:#fff; border:none; padding:15px 44px; border-radius:50px; font-family:'DM Sans',sans-serif; font-size:1rem; font-weight:700; cursor:pointer; box-shadow:0 6px 20px rgba(255,107,107,0.4); transition:transform 0.2s; }
.back-btn:hover { transform:translateY(-2px); }

/* TOAST */
.toast { position:fixed; bottom:28px; left:50%; transform:translateX(-50%) translateY(80px); background:var(--dark); color:#fff; padding:13px 26px; border-radius:50px; font-weight:600; font-size:0.88rem; z-index:300; transition:transform 0.3s cubic-bezier(0.34,1.56,0.64,1); white-space:nowrap; box-shadow:0 8px 24px rgba(0,0,0,0.2); }
.toast.on { transform:translateX(-50%) translateY(0); }

/* REVIEWS */
.reviews-wrap { background:linear-gradient(135deg,rgba(255,107,107,0.05),rgba(192,132,252,0.05)); padding:70px 5%; position:relative; z-index:5; }
.rev-grid { display:grid; grid-template-columns:repeat(auto-fill,minmax(270px,1fr)); gap:22px; max-width:1000px; margin:0 auto; }
.rev-card { background:#fff; border-radius:22px; padding:26px; box-shadow:0 4px 18px rgba(45,27,19,0.06); }
.stars { color:var(--gold); margin-bottom:10px; }
.rev-card p { font-size:0.92rem; color:#5a3d30; line-height:1.7; margin-bottom:14px; }
.rev-by { display:flex; align-items:center; gap:10px; }
.rev-av { width:40px; height:40px; border-radius:50%; display:flex; align-items:center; justify-content:center; font-size:1.3rem; }
.rev-name { font-weight:700; font-size:0.88rem; }
.rev-sub { font-size:0.72rem; color:#bbb; }

/* FOOTER */
footer { position:relative; z-index:5; background:var(--dark); color:#fff; padding:44px 5% 28px; text-align:center; }
.foot-logo { font-family:'Playfair Display',serif; font-size:1.9rem; font-weight:900; margin-bottom:10px; }
.foot-logo span { font-style:italic; background:linear-gradient(135deg,var(--coral),var(--berry)); -webkit-background-clip:text; -webkit-text-fill-color:transparent; }
footer p { color:rgba(255,255,255,0.45); font-size:0.82rem; margin-top:18px; }

@media(max-width:600px){ nav{display:none;} .stats-bar{gap:28px;} }
</style>
</head>
<body>

<div class="bg-blobs">
  <div class="blob blob1"></div>
  <div class="blob blob2"></div>
  <div class="blob blob3"></div>
  <div class="blob blob4"></div>
</div>

<!-- HEADER -->
<header>
  <div class="logo">Raji Ice Cream 💙</div>
  <button class="cart-btn" onclick="openCart()">
    🛒 My Cart <span class="cart-badge" id="cartCount">0</span>
  </button>
</header>

<!-- HERO -->
<section class="hero">
  <div class="float-ico">🍦</div>
  <div class="float-ico">🍨</div>
  <div class="float-ico">🍧</div>
  <div class="float-ico">🧁</div>
  <div class="hero-pill">💙 Raji's Artisan Ice Cream</div>
  <h1>Pure Joy in<br>Every <em>Scoop</em> 💙</h1>
  <p>Handcrafted with love using the finest ingredients. From classic scoops to exotic sorbet — your sweetest moments start here!</p>
  <div class="hero-btns">
    <a href="#menu" class="btn-p">🍦 Order Now</a>
  </div>
</section>

<!-- STATS -->
<div class="stats-bar">
  <div class="stat"><span class="stat-n">50+</span><span class="stat-l">Flavours</span></div>
  <div class="stat"><span class="stat-n">10K+</span><span class="stat-l">Happy Customers</span></div>
  <div class="stat"><span class="stat-n">4.9★</span><span class="stat-l">Rating</span></div>
  <div class="stat"><span class="stat-n">Free</span><span class="stat-l">Delivery ₹500+</span></div>
</div>

<!-- MENU -->
<section class="section" id="menu">
  <div class="sec-hdr">
    <span class="sec-lbl">Our Menu</span>
    <h2 class="sec-title">Choose Your <em>Scoop</em></h2>
  </div>
  <div class="tabs">
    <button class="tab active" onclick="filterItems(this,'all')">All</button>
    <button class="tab" onclick="filterItems(this,'classic')">🍦 Classic</button>
    <button class="tab" onclick="filterItems(this,'sorbet')">🍧 Sorbet</button>
    <button class="tab" onclick="filterItems(this,'premium')">✨ Premium</button>
    <button class="tab" onclick="filterItems(this,'sundae')">🍨 Sundae</button>
  </div>
  <div class="grid" id="itemGrid"></div>
</section>

<!-- REVIEWS -->
<div class="reviews-wrap" id="reviews">
  <div class="sec-hdr">
    <span class="sec-lbl">Happy Customers</span>
    <h2 class="sec-title">People <em>Love</em> Us</h2>
  </div>
  <div class="rev-grid">
    <div class="rev-card">
      <div class="stars">★★★★★</div>
      <p>"Mango Tango Sorbet is absolutely divine! Fresh, bright and so refreshing. I order every week from Raji!"</p>
      <div class="rev-by"><div class="rev-av" style="background:#FFECD2">🙋‍♀️</div><div><div class="rev-name">Priya S.</div><div class="rev-sub">Loyal customer since 2022</div></div></div>
    </div>
    <div class="rev-card">
      <div class="stars">★★★★★</div>
      <p>"Triple Choco Avalanche is unreal! My kids think I'm the best parent for ordering from Raji. Love it!"</p>
      <div class="rev-by"><div class="rev-av" style="background:#D4F4E2">👨‍👧</div><div><div class="rev-name">Ramesh K.</div><div class="rev-sub">Dad of 2 sweet tooths</div></div></div>
    </div>
    <div class="rev-card">
      <div class="stars">★★★★★</div>
      <p>"Fast delivery, beautiful packaging and flavours that taste like heaven. Zero complaints. Best in town!"</p>
      <div class="rev-by"><div class="rev-av" style="background:#EDE9FE">👩‍🎨</div><div><div class="rev-name">Deepa L.</div><div class="rev-sub">Food blogger</div></div></div>
    </div>
  </div>
</div>

<!-- FOOTER -->
<footer>
  <div class="foot-logo">Raji <span>Ice Cream</span> 💙</div>
  <p>Made with love 💙🍦 | Free delivery on orders over ₹500 | © 2026 Raji Ice Cream</p>
</footer>

<!-- CART OVERLAY + DRAWER -->
<div class="overlay" id="overlay" onclick="closeCart()"></div>
<div class="drawer" id="drawer">
  <div class="drawer-hdr">
    <span class="drawer-title">🛒 Your Cart</span>
    <button class="x-btn" onclick="closeCart()">✕</button>
  </div>
  <div class="drawer-body" id="drawerBody"></div>
  <div class="drawer-foot" id="drawerFoot" style="display:none">
    <div class="total-row"><span>Total</span><span class="total-amt" id="totalAmt">₹0</span></div>
    <div class="del-note" id="delNote"></div>
    <button class="checkout-btn" onclick="placeOrder()">Place Order 🎉</button>
  </div>
</div>

<!-- ORDER SUCCESS SCREEN -->
<div class="success-screen" id="successScreen">
  <div class="success-anim">🎉</div>
  <h2>Order <span>Placed!</span></h2>
  <p>Thank you for ordering from <strong>Raji Ice Cream 💙</strong>!</p>
  <div class="order-id" id="orderIdBox"></div>
  <p style="font-size:0.9rem;color:#9a7060;">Your delicious scoops are being prepared with love 🍦</p>
  <div class="track-steps">
    <div class="step done">
      <div class="step-ico">✅</div>
      <div class="step-lbl">Confirmed</div>
    </div>
    <div class="step-line"></div>
    <div class="step">
      <div class="step-ico">👨‍🍳</div>
      <div class="step-lbl">Preparing</div>
    </div>
    <div class="step-line"></div>
    <div class="step">
      <div class="step-ico">🛵</div>
      <div class="step-lbl">On the Way</div>
    </div>
    <div class="step-line"></div>
    <div class="step">
      <div class="step-ico">🏠</div>
      <div class="step-lbl">Delivered</div>
    </div>
  </div>
  <button class="back-btn" onclick="continueShopping()">Continue Shopping 🍦</button>
</div>

<!-- TOAST -->
<div class="toast" id="toast"></div>

<script>
// ── DATA ──────────────────────────────────────────────
const ITEMS = [
  { id:1, name:"Strawberry Bliss",        emoji:"🍓", desc:"Fresh strawberry with a hint of vanilla cream",
