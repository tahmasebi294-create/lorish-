<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Lorish Shop — Ästhetik & Beauty</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,500;0,600;0,700;1,400;1,500&family=Outfit:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css" rel="stylesheet">
<!-- Poe Embed Script (offiziell) -->
<script src="https://cdn.poe.com/embed/poe-embed.js" defer></script>
<style>
/* ===== Deine bestehenden Styles ===== */
:root {
  --bg: #FAF7F4;
  --bg-card: #FFFFFF;
  --bg-elevated: #F5F0EB;
  --bg-overlay: rgba(58,42,36,0.55);
  --text: #2E2220;
  --text-sec: #7A6B63;
  --text-muted: #B5A89F;
  --accent: #9C6B4A;
  --accent-rich: #7B4F32;
  --accent-light: #D4A984;
  --accent-glow: rgba(156,107,74,0.15);
  --rose: #C4727F;
  --rose-soft: #F6E3E6;
  --gold: #C9A84C;
  --gold-soft: #FBF3DC;
  --sage: #7A9E7E;
  --sage-soft: #E4F0E5;
  --border: #E8E0D8;
  --border-light: #F0EBE5;
  --shadow-sm: 0 2px 8px rgba(46,34,32,0.06);
  --shadow-md: 0 6px 24px rgba(46,34,32,0.08);
  --shadow-lg: 0 12px 40px rgba(46,34,32,0.12);
  --shadow-xl: 0 20px 60px rgba(46,34,32,0.16);
  --radius: 16px;
  --radius-sm: 10px;
  --radius-xs: 6px;
  --transition: 0.3s cubic-bezier(0.4,0,0.2,1);
}
html.dark {
  --bg: #1A1514;
  --bg-card: #231E1C;
  --bg-elevated: #2C2522;
  --bg-overlay: rgba(0,0,0,0.7);
  --text: #F0E8E2;
  --text-sec: #A89890;
  --text-muted: #6B5E58;
  --accent: #C4925E;
  --accent-rich: #D4A46E;
  --accent-light: #8B6840;
  --accent-glow: rgba(196,146,94,0.12);
  --rose: #D4889A;
  --rose-soft: #2D1F22;
  --gold: #D4B35C;
  --gold-soft: #2A2418;
  --sage: #8AB08E;
  --sage-soft: #1C261D;
  --border: #3A322E;
  --border-light: #2C2522;
  --shadow-sm: 0 2px 8px rgba(0,0,0,0.2);
  --shadow-md: 0 6px 24px rgba(0,0,0,0.25);
  --shadow-lg: 0 12px 40px rgba(0,0,0,0.3);
  --shadow-xl: 0 20px 60px rgba(0,0,0,0.4);
}
*{margin:0;padding:0;box-sizing:border-box;}
body{font-family:'Outfit',sans-serif;background:var(--bg);color:var(--text);min-height:100vh;overflow-x:hidden;line-height:1.5;}
h1,h2,h3,.serif{font-family:'Cormorant Garamond',serif;}
::-webkit-scrollbar{width:6px;}
::-webkit-scrollbar-track{background:transparent;}
::-webkit-scrollbar-thumb{background:var(--border);border-radius:3px;}
.navbar{position:sticky;top:0;z-index:100;background:var(--bg);border-bottom:1px solid var(--border);backdrop-filter:blur(16px);-webkit-backdrop-filter:blur(16px);}
.nav-inner{max-width:1100px;margin:0 auto;padding:14px 20px;display:flex;align-items:center;justify-content:space-between;gap:12px;}
.nav-brand{display:flex;align-items:center;gap:10px;text-decoration:none;color:var(--text);}
.nav-logo{width:38px;height:38px;border-radius:50%;background:linear-gradient(135deg,var(--accent),var(--rose));display:flex;align-items:center;justify-content:center;color:#fff;font-family:'Cormorant Garamond',serif;font-size:20px;font-weight:700;flex-shrink:0;}
.nav-brand-text{display:flex;flex-direction:column;}
.nav-brand-name{font-family:'Cormorant Garamond',serif;font-size:22px;font-weight:700;line-height:1.1;letter-spacing:0.5px;}
.nav-brand-tag{font-size:10px;text-transform:uppercase;letter-spacing:2px;color:var(--text-muted);font-weight:500;}
.nav-actions{display:flex;align-items:center;gap:6px;}
.nav-btn{width:42px;height:42px;border-radius:50%;border:1.5px solid var(--border);background:var(--bg-card);color:var(--text-sec);cursor:pointer;display:flex;align-items:center;justify-content:center;font-size:16px;transition:var(--transition);position:relative;}
.nav-btn:hover{border-color:var(--accent);color:var(--accent);background:var(--accent-glow);}
.cart-badge{position:absolute;top:-2px;right:-2px;background:var(--rose);color:#fff;font-size:10px;font-weight:700;width:18px;height:18px;border-radius:50%;display:flex;align-items:center;justify-content:center;border:2px solid var(--bg);transform:scale(0);transition:var(--transition);}
.cart-badge.show{transform:scale(1);}
.hero{max-width:1100px;margin:0 auto;padding:40px 20px 20px;text-align:center;animation:fadeUp .7s ease;}
.hero-badge{display:inline-flex;align-items:center;gap:6px;padding:6px 16px;background:var(--gold-soft);border:1px solid var(--gold);border-radius:50px;font-size:12px;font-weight:600;color:var(--gold);margin-bottom:16px;letter-spacing:0.5px;}
.hero h1{font-size:clamp(32px,6vw,52px);font-weight:600;line-height:1.1;margin-bottom:12px;letter-spacing:-0.5px;}
.hero h1 .accent{color:var(--accent);font-style:italic;}
.hero p{font-size:16px;color:var(--text-sec);max-width:500px;margin:0 auto 24px;line-height:1.6;}
.hero-actions{display:flex;gap:10px;justify-content:center;flex-wrap:wrap;}
.btn{padding:12px 28px;border-radius:50px;border:none;font-family:'Outfit',sans-serif;font-size:14px;font-weight:600;cursor:pointer;transition:var(--transition);display:inline-flex;align-items:center;gap:8px;text-decoration:none;letter-spacing:0.3px;}
.btn-primary{background:linear-gradient(135deg,var(--accent),var(--accent-rich));color:#fff;box-shadow:0 4px 16px rgba(156,107,74,0.3);}
.btn-primary:hover{transform:translateY(-1px);box-shadow:0 6px 24px rgba(156,107,74,0.4);}
.btn-outline{background:transparent;border:1.5px solid var(--border);color:var(--text);}
.btn-outline:hover{border-color:var(--accent);color:var(--accent);}
.categories{max-width:1100px;margin:0 auto;padding:8px 20px 20px;display:flex;gap:8px;overflow-x:auto;scrollbar-width:none;-ms-overflow-style:none;animation:fadeUp .7s ease .1s both;}
.categories::-webkit-scrollbar{display:none;}
.cat-chip{padding:8px 18px;border-radius:50px;border:1.5px solid var(--border);background:var(--bg-card);color:var(--text-sec);font-size:13px;font-weight:500;cursor:pointer;white-space:nowrap;transition:var(--transition);flex-shrink:0;}
.cat-chip:hover,.cat-chip.active{background:var(--accent);color:#fff;border-color:var(--accent);}
.section-header{max-width:1100px;margin:0 auto;padding:24px 20px 12px;display:flex;align-items:baseline;justify-content:space-between;animation:fadeUp .7s ease .15s both;}
.section-header h2{font-size:28px;font-weight:600;}
.section-header span{font-size:13px;color:var(--text-muted);}
.product-grid{max-width:1100px;margin:0 auto;padding:0 20px 32px;display:grid;grid-template-columns:repeat(auto-fill,minmax(220px,1fr));gap:16px;animation:fadeUp .7s ease .2s both;}
.product-card{background:var(--bg-card);border:1px solid var(--border-light);border-radius:var(--radius);overflow:hidden;cursor:pointer;transition:var(--transition);position:relative;}
.product-card:hover{transform:translateY(-4px);box-shadow:var(--shadow-lg);border-color:var(--border);}
.product-img{width:100%;aspect-ratio:3/3.5;display:flex;align-items:center;justify-content:center;position:relative;overflow:hidden;}
.product-img-bg{width:100%;height:100%;display:flex;align-items:center;justify-content:center;font-size:48px;transition:transform .5s ease;}
.product-card:hover .product-img-bg{transform:scale(1.05);}
.product-tag{position:absolute;top:10px;left:10px;padding:4px 10px;border-radius:50px;font-size:10px;font-weight:700;text-transform:uppercase;letter-spacing:0.5px;}
.tag-new{background:var(--sage-soft);color:var(--sage);}
.tag-sale{background:var(--rose-soft);color:var(--rose);}
.tag-best{background:var(--gold-soft);color:var(--gold);}
.product-wish{position:absolute;top:10px;right:10px;width:32px;height:32px;border-radius:50%;background:var(--bg-card);border:1px solid var(--border);display:flex;align-items:center;justify-content:center;font-size:13px;color:var(--text-muted);cursor:pointer;transition:var(--transition);opacity:0;transform:scale(0.8);}
.product-card:hover .product-wish{opacity:1;transform:scale(1);}
.product-wish.liked{opacity:1;transform:scale(1);color:var(--rose);background:var(--rose-soft);border-color:var(--rose);}
.product-body{padding:14px 16px 16px;}
.product-brand{font-size:11px;text-transform:uppercase;letter-spacing:1px;color:var(--text-muted);font-weight:600;margin-bottom:4px;}
.product-name{font-family:'Cormorant Garamond',serif;font-size:18px;font-weight:600;line-height:1.2;margin-bottom:6px;}
.product-desc{font-size:12px;color:var(--text-sec);line-height:1.4;margin-bottom:10px;display:-webkit-box;-webkit-line-clamp:2;-webkit-box-orient:vertical;overflow:hidden;}
.product-footer{display:flex;align-items:center;justify-content:space-between;}
.product-price{font-size:18px;font-weight:700;color:var(--accent);}
.product-price .old{font-size:13px;color:var(--text-muted);text-decoration:line-through;font-weight:400;margin-left:6px;}
.add-cart-btn{width:36px;height:36px;border-radius:50%;border:1.5px solid var(--accent);background:transparent;color:var(--accent);font-size:14px;cursor:pointer;display:flex;align-items:center;justify-content:center;transition:var(--transition);}
.add-cart-btn:hover,.add-cart-btn.added{background:var(--accent);color:#fff;}
.cart-overlay{position:fixed;inset:0;background:var(--bg-overlay);z-index:200;opacity:0;pointer-events:none;transition:opacity .3s ease;}
.cart-overlay.open{opacity:1;pointer-events:all;}
.cart-drawer{position:fixed;top:0;right:0;bottom:0;width:min(400px,92vw);background:var(--bg);z-index:201;transform:translateX(100%);transition:transform .35s cubic-bezier(.4,0,.2,1);display:flex;flex-direction:column;}
.cart-drawer.open{transform:translateX(0);}
.cart-header{padding:20px;border-bottom:1px solid var(--border);display:flex;align-items:center;justify-content:space-between;}
.cart-header h2{font-size:24px;font-weight:600;}
.cart-close{width:36px;height:36px;border-radius:50%;border:1px solid var(--border);background:var(--bg-card);color:var(--text-sec);cursor:pointer;display:flex;align-items:center;justify-content:center;font-size:16px;transition:var(--transition);}
.cart-close:hover{border-color:var(--rose);color:var(--rose);}
.cart-items{flex:1;overflow-y:auto;padding:16px 20px;}
.cart-empty{text-align:center;padding:48px 20px;color:var(--text-muted);}
.cart-empty i{font-size:40px;margin-bottom:12px;display:block;color:var(--border);}
.cart-item{display:flex;gap:14px;padding:14px 0;border-bottom:1px solid var(--border-light);animation:fadeUp .3s ease;}
.cart-item-img{width:64px;height:64px;border-radius:var(--radius-sm);display:flex;align-items:center;justify-content:center;font-size:28px;flex-shrink:0;}
.cart-item-info{flex:1;min-width:0;}
.cart-item-name{font-family:'Cormorant Garamond',serif;font-size:16px;font-weight:600;margin-bottom:2px;}
.cart-item-variant{font-size:12px;color:var(--text-muted);}
.cart-item-bottom{display:flex;align-items:center;justify-content:space-between;margin-top:8px;}
.cart-item-price{font-weight:700;color:var(--accent);font-size:15px;}
.qty-ctrl{display:flex;align-items:center;gap:0;border:1px solid var(--border);border-radius:8px;overflow:hidden;}
.qty-btn{width:28px;height:28px;border:none;background:var(--bg-elevated);color:var(--text-sec);cursor:pointer;font-size:14px;display:flex;align-items:center;justify-content:center;transition:var(--transition);}
.qty-btn:hover{background:var(--accent);color:#fff;}
.qty-val{width:32px;text-align:center;font-size:13px;font-weight:600;background:var(--bg-card);border:none;color:var(--text);}
.cart-footer{padding:20px;border-top:1px solid var(--border);}
.cart-total{display:flex;justify-content:space-between;align-items:center;margin-bottom:16px;}
.cart-total-label{font-size:14px;color:var(--text-sec);}
.cart-total-value{font-size:24px;font-weight:700;font-family:'Cormorant Garamond',serif;}
.checkout-btn{width:100%;padding:14px;border:none;border-radius:50px;background:linear-gradient(135deg,var(--accent),var(--accent-rich));color:#fff;font-family:'Outfit',sans-serif;font-size:15px;font-weight:600;cursor:pointer;transition:var(--transition);display:flex;align-items:center;justify-content:center;gap:8px;box-shadow:0 4px 16px rgba(156,107,74,0.3);}
.checkout-btn:hover{transform:translateY(-1px);box-shadow:0 6px 24px rgba(156,107,74,0.4);}
.chat-toggle{position:fixed;bottom:20px;right:20px;z-index:150;width:56px;height:56px;border-radius:50%;border:none;background:linear-gradient(135deg,var(--accent),var(--rose));color:#fff;font-size:22px;cursor:pointer;box-shadow:var(--shadow-lg);transition:var(--transition);display:flex;align-items:center;justify-content:center;}
.chat-toggle:hover{transform:scale(1.08);box-shadow:var(--shadow-xl);}
.chat-toggle.active{border-radius:16px;}
.chat-panel{position:fixed;bottom:86px;right:20px;width:min(380px,calc(100vw - 32px));height:min(520px,calc(100vh - 120px));background:var(--bg);border:1px solid var(--border);border-radius:20px;z-index:150;box-shadow:var(--shadow-xl);display:flex;flex-direction:column;opacity:0;pointer-events:none;transform:translateY(16px) scale(0.96);transition:all .3s cubic-bezier(.4,0,.2,1);overflow:hidden;}
.chat-panel.open{opacity:1;pointer-events:all;transform:translateY(0) scale(1);}
.chat-head{padding:16px;border-bottom:1px solid var(--border);display:flex;align-items:center;gap:12px;}
.chat-head-icon{width:36px;height:36px;border-radius:10px;background:linear-gradient(135deg,var(--accent),var(--rose));color:#fff;display:flex;align-items:center;justify-content:center;font-size:16px;}
.chat-head-info{flex:1;}
.chat-head-title{font-weight:700;font-size:15px;}
.chat-head-sub{font-size:11px;color:var(--text-muted);}
.chat-bot-select{padding:10px 16px;border-bottom:1px solid var(--border-light);display:flex;gap:6px;}
.chat-bot-chip{flex:1;padding:8px 10px;border-radius:var(--radius-xs);border:1.5px solid var(--border);background:var(--bg-card);cursor:pointer;text-align:center;transition:var(--transition);font-size:12px;font-weight:600;color:var(--text-sec);}
.chat-bot-chip:hover{border-color:var(--accent);}
.chat-bot-chip.active{border-color:var(--accent);background:var(--accent-glow);color:var(--accent);}
.chat-bot-chip .chip-icon{font-size:16px;display:block;margin-bottom:2px;}
.chat-messages{flex:1;overflow-y:auto;padding:16px;display:flex;flex-direction:column;gap:12px;}
.chat-msg{max-width:85%;padding:10px 14px;border-radius:14px;font-size:14px;line-height:1.5;animation:fadeUp .3s ease;word-break:break-word;white-space:pre-wrap;}
.chat-msg.bot{align-self:flex-start;background:var(--bg-elevated);border:1px solid var(--border-light);border-bottom-left-radius:4px;}
.chat-msg.user{align-self:flex-end;background:var(--accent);color:#fff;border-bottom-right-radius:4px;}
.chat-msg.error{align-self:flex-start;background:var(--rose-soft);color:var(--rose);border:1px solid var(--rose);font-size:13px;}
.typing-indicator{display:flex;gap:4px;padding:12px 16px;align-self:flex-start;}
.typing-indicator span{width:7px;height:7px;border-radius:50%;background:var(--text-muted);animation:typingBounce 1.2s ease-in-out infinite;}
.typing-indicator span:nth-child(2){animation-delay:.15s;}
.typing-indicator span:nth-child(3){animation-delay:.3s;}
.chat-input-area{padding:12px 16px;border-top:1px solid var(--border);display:flex;gap:8px;align-items:flex-end;}
.chat-input{flex:1;padding:10px 14px;border-radius:12px;border:1.5px solid var(--border);background:var(--bg-card);color:var(--text);font-family:'Outfit',sans-serif;font-size:14px;resize:none;outline:none;max-height:80px;line-height:1.4;min-height:40px;transition:border-color .2s;}
.chat-input::placeholder{color:var(--text-muted);}
.chat-input:focus{border-color:var(--accent);}
.chat-send{width:40px;height:40px;border-radius:50%;border:none;background:var(--accent);color:#fff;cursor:pointer;display:flex;align-items:center;justify-content:center;font-size:15px;transition:var(--transition);flex-shrink:0;}
.chat-send:hover{background:var(--accent-rich);}
.chat-send:disabled{opacity:0.5;cursor:not-allowed;}
.toast{position:fixed;bottom:90px;left:50%;transform:translateX(-50%) translateY(20px);background:var(--text);color:var(--bg);padding:10px 22px;border-radius:50px;font-size:13px;font-weight:600;z-index:300;opacity:0;pointer-events:none;transition:all .3s ease;white-space:nowrap;display:flex;align-items:center;gap:8px;}
.toast.show{opacity:1;transform:translateX(-50%) translateY(0);}
.modal-overlay{position:fixed;inset:0;background:var(--bg-overlay);z-index:500;display:flex;align-items:center;justify-content:center;padding:20px;opacity:0;pointer-events:none;transition:opacity .3s;}
.modal-overlay.open{opacity:1;pointer-events:all;}
.modal-box{background:var(--bg);border:1px solid var(--border);border-radius:var(--radius);padding:28px;max-width:400px;width:100%;box-shadow:var(--shadow-xl);transform:scale(0.95);transition:transform .3s;text-align:center;}
.modal-overlay.open .modal-box{transform:scale(1);}
.modal-box h3{font-family:'Cormorant Garamond',serif;font-size:24px;margin-bottom:8px;}
.modal-box p{font-size:14px;color:var(--text-sec);margin-bottom:20px;line-height:1.5;}
.modal-actions{display:flex;gap:10px;justify-content:center;}
@keyframes fadeUp{from{opacity:0;transform:translateY(16px);}to{opacity:1;transform:translateY(0);}}
@keyframes typingBounce{0%,80%,100%{transform:scale(0.6);opacity:0.4;}40%{transform:scale(1);opacity:1;}}
@keyframes cartPop{0%{transform:scale(1);}50%{transform:scale(1.25);}100%{transform:scale(1);}}
.cart-pop{animation:cartPop .4s ease;}
@media(max-width:600px){
  .hero{padding:24px 16px 12px;}
  .product-grid{grid-template-columns:repeat(2,1fr);gap:10px;padding:0 12px 24px;}
  .categories{padding:8px 12px 16px;}
  .section-header{padding:20px 12px 10px;}
  .product-body{padding:10px 12px 12px;}
  .product-name{font-size:15px;}
  .product-price{font-size:15px;}
  .product-desc{display:none;}
  .nav-inner{padding:12px 12px;}
  .nav-brand-tag{display:none;}
  .chat-panel{bottom:76px;right:12px;width:calc(100vw - 24px);}
  .chat-toggle{bottom:14px;right:14px;width:50px;height:50px;font-size:20px;}
  .toast{bottom:76px;}
}
</style>
</head>
<body>

<!-- NAVBAR -->
<nav class="navbar">
  <div class="nav-inner">
    <a class="nav-brand" href="javascript:void(0)">
      <div class="nav-logo">L</div>
      <div class="nav-brand-text">
        <span class="nav-brand-name">Lorish Shop</span>
        <span class="nav-brand-tag">Ästhetik & Beauty</span>
      </div>
    </a>
    <div class="nav-actions">
      <button class="nav-btn" onclick="scrollToProducts()" title="Suche"><i class="fas fa-search"></i></button>
      <button class="nav-btn" onclick="toggleCart()" title="Warenkorb" id="cartNavBtn">
        <i class="fas fa-shopping-bag"></i>
        <span class="cart-badge" id="cartBadge">0</span>
      </button>
    </div>
  </div>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-badge"><i class="fas fa-sparkles"></i> Premium Beauty Kollektion 2026</div>
  <h1>Entdecke deine <span class="accent">natürliche Schönheit</span></h1>
  <p>Handverlesene Ästhetik- und Beauty-Produkte für strahlende Haut, luxuriöse Pflege und zeitlose Eleganz.</p>
  <div class="hero-actions">
    <button class="btn btn-primary" onclick="scrollToProducts()"><i class="fas fa-arrow-down"></i> Jetzt entdecken</button>
    <button class="btn btn-outline" onclick="toggleChat()"><i class="fas fa-wand-magic-sparkles"></i> KI-Beratung</button>
  </div>
</section>

<!-- CATEGORIES -->
<div class="categories" id="categories">
  <button class="cat-chip active" data-cat="all" onclick="filterCategory(this)">Alle</button>
  <button class="cat-chip" data-cat="skincare" onclick="filterCategory(this)">Hautpflege</button>
  <button class="cat-chip" data-cat="serum" onclick="filterCategory(this)">Seren</button>
  <button class="cat-chip" data-cat="mask" onclick="filterCategory(this)">Masken</button>
  <button class="cat-chip" data-cat="lips" onclick="filterCategory(this)">Lippen</button>
  <button class="cat-chip" data-cat="fragrance" onclick="filterCategory(this)">Düfte</button>
  <button class="cat-chip" data-cat="tools" onclick="filterCategory(this)">Tools</button>
</div>

<!-- PRODUCTS SECTION (mit ID für Scroll) -->
<div class="section-header" id="productsSection">
  <h2 class="serif">Unsere Produkte</h2>
  <span id="productCount"></span>
</div>
<div class="product-grid" id="productGrid"></div>

<!-- CART OVERLAY -->
<div class="cart-overlay" id="cartOverlay" onclick="toggleCart()"></div>
<div class="cart-drawer" id="cartDrawer">
  <div class="cart-header">
    <h2 class="serif">Warenkorb</h2>
    <button class="cart-close" onclick="toggleCart()"><i class="fas fa-times"></i></button>
  </div>
  <div class="cart-items" id="cartItems"></div>
  <div class="cart-footer" id="cartFooter" style="display:none;">
    <div class="cart-total">
      <span class="cart-total-label">Gesamtbetrag</span>
      <span class="cart-total-value" id="cartTotal">€0,00</span>
    </div>
    <button class="checkout-btn" onclick="showCheckoutModal()"><i class="fas fa-lock"></i> Zur Kasse</button>
  </div>
</div>

<!-- CHAT TOGGLE -->
<button class="chat-toggle" id="chatToggle" onclick="toggleChat()" title="KI Beauty-Beraterin">
  <i class="fas fa-wand-magic-sparkles"></i>
</button>

<!-- CHAT PANEL -->
<div class="chat-panel" id="chatPanel">
  <div class="chat-head">
    <div class="chat-head-icon"><i class="fas fa-wand-magic-sparkles"></i></div>
    <div class="chat-head-info">
      <div class="chat-head-title">Lorish Beauty-Beraterin</div>
      <div class="chat-head-sub">Frag mich zu Produkten & Pflege-Tipps</div>
    </div>
  </div>
  <div class="chat-bot-select">
    <div class="chat-bot-chip active" data-bot="Claude-Sonnet-4.5" onclick="selectChatBot(this)">
      <span class="chip-icon">🟠</span>Claude 4.5
    </div>
    <div class="chat-bot-chip" data-bot="Gemini-3-Pro" onclick="selectChatBot(this)">
      <span class="chip-icon">🔵</span>Gemini 3 Pro
    </div>
  </div>
  <div class="chat-messages" id="chatMessages">
    <div class="chat-msg bot">Willkommen bei Lorish Shop! 💫 Ich bin deine Beauty-Beraterin. Frag mich zu Hautpflege, Produktempfehlungen oder Pflege-Routinen!</div>
  </div>
  <div class="chat-input-area">
    <textarea class="chat-input" id="chatInput" placeholder="Frag mich etwas…" rows="1" onkeydown="handleChatKey(event)" oninput="autoGrow(this)"></textarea>
    <button class="chat-send" id="chatSendBtn" onclick="sendChatMessage()"><i class="fas fa-paper-plane"></i></button>
  </div>
</div>

<!-- TOAST -->
<div class="toast" id="toast"></div>

<!-- MODAL -->
<div class="modal-overlay" id="modalOverlay">
  <div class="modal-box">
    <h3 class="serif" id="modalTitle"></h3>
    <p id="modalText"></p>
    <div class="modal-actions" id="modalActions"></div>
  </div>
</div>

<script>
// ─── DARK MODE ───
if(window.matchMedia&&window.matchMedia('(prefers-color-scheme:dark)').matches){document.documentElement.classList.add('dark');}
window.matchMedia('(prefers-color-scheme:dark)').addEventListener('change',e=>{e.matches?document.documentElement.classList.add('dark'):document.documentElement.classList.remove('dark');});

// ─── PRODUCT DATA ───
const products=[
  {id:1,name:"Rosé Glow Serum",brand:"LORISH",cat:"serum",price:49.90,oldPrice:null,tag:"best",tagLabel:"Bestseller",emoji:"🌹",bg:"linear-gradient(135deg,#F9E4E8,#F5D0D6)",desc:"Vitamin-C-Serum für strahlenden Teint und ebenmäßige Haut."},
  {id:2,name:"Hyaluron Feuchtigkeitscreme",brand:"LORISH",cat:"skincare",price:38.50,oldPrice:45.00,tag:"sale",tagLabel:"-15%",emoji:"💧",bg:"linear-gradient(135deg,#E0EFF6,#C8E3F0)",desc:"72h Tiefenfeuchtigkeit mit dreifach Hyaluronsäure-Komplex."},
  {id:3,name:"Gold Kollagen Maske",brand:"LORISH LUXE",cat:"mask",price:24.90,oldPrice:null,tag:"new",tagLabel:"Neu",emoji:"✨",bg:"linear-gradient(135deg,#FBF3DC,#F0E4B8)",desc:"24K Gold-Infusion für sofort sichtbare Straffung und Glow."},
  {id:4,name:"Samt Lippenpflege",brand:"LORISH",cat:"lips",price:18.90,oldPrice:null,tag:null,emoji:"💋",bg:"linear-gradient(135deg,#F5D5D5,#E8B8B8)",desc:"Reichhaltige Pflege mit Sheabutter und Wildrosenöl."},
  {id:5,name:"Retinol Nachtserum",brand:"LORISH PRO",cat:"serum",price:54.90,oldPrice:62.00,tag:"sale",tagLabel:"-11%",emoji:"🌙",bg:"linear-gradient(135deg,#D8D0E8,#C0B4D8)",desc:"0.5% verkapseltes Retinol für Zellerneuerung über Nacht."},
  {id:6,name:"Eau de Lorish — Blossom",brand:"LORISH",cat:"fragrance",price:79.00,oldPrice:null,tag:"best",tagLabel:"Bestseller",emoji:"🌸",bg:"linear-gradient(135deg,#FCE4EC,#F8BBD0)",desc:"Florale Note mit Jasmin, Pfingstrose und sanftem Moschus."},
  {id:7,name:"Jade Gua Sha Stein",brand:"LORISH TOOLS",cat:"tools",price:22.50,oldPrice:null,tag:"new",tagLabel:"Neu",emoji:"💎",bg:"linear-gradient(135deg,#E4F0E5,#C8E0CA)",desc:"Echter Jade-Stein für Lymphdrainage und Gesichtskonturierung."},
  {id:8,name:"Niacinamid Klärendes Tonic",brand:"LORISH",cat:"skincare",price:26.90,oldPrice:null,tag:null,emoji:"🧴",bg:"linear-gradient(135deg,#E8F0E4,#D0E0CA)",desc:"10% Niacinamid für verfeinerte Poren und ausgeglichene Haut."},
  {id:9,name:"Kollagen Lip Boost",brand:"LORISH LUXE",cat:"lips",price:32.00,oldPrice:39.00,tag:"sale",tagLabel:"-18%",emoji:"👄",bg:"linear-gradient(135deg,#FDDEDE,#F0B8B8)",desc:"Peptid-Komplex für sichtbar vollere und definierte Lippen."},
  {id:10,name:"Detox Tonerde Maske",brand:"LORISH",cat:"mask",price:19.90,oldPrice:null,tag:null,emoji:"🍃",bg:"linear-gradient(135deg,#E2EDE4,#C4D8C6)",desc:"Grüne Tonerde mit Teebaum für porentief reine Haut."},
  {id:11,name:"Rosenquarz Roller",brand:"LORISH TOOLS",cat:"tools",price:28.00,oldPrice:null,tag:"best",tagLabel:"Bestseller",emoji:"🩷",bg:"linear-gradient(135deg,#FDEAF0,#F4CED8)",desc:"Doppelseitiger Roller für Micro-Circulation und Entspannung."},
  {id:12,name:"Eau de Lorish — Noir",brand:"LORISH",cat:"fragrance",price:89.00,oldPrice:null,tag:"new",tagLabel:"Neu",emoji:"🖤",bg:"linear-gradient(135deg,#D8D4D0,#B8B0AA)",desc:"Tiefe Oud-Akkorde mit Amber, Vanille und Sandelholz."},
];

let cart=[];
let currentCat='all';
let chatBot='Claude-Sonnet-4.5';
let chatOpen=false;
let isSending=false;
let poeReady = false;

// ─── Warten auf Poe-API ───
function waitForPoe(cb) {
  if (window.Poe && typeof window.Poe.sendUserMessage === 'function') {
    poeReady = true;
    cb();
  } else {
    setTimeout(() => waitForPoe(cb), 200);
  }
}

// ─── RENDER PRODUCTS ───
function renderProducts(){
  const grid=document.getElementById('productGrid');
  const filtered=currentCat==='all'?products:products.filter(p=>p.cat===currentCat);
  document.getElementById('productCount').textContent=filtered.length+' Produkte';
  grid.innerHTML=filtered.map(p=>`
    <div class="product-card" data-id="${p.id}">
      <div class="product-img">
        <div class="product-img-bg" style="background:${p.bg}">${p.emoji}</div>
        ${p.tag?`<span class="product-tag tag-${p.tag}">${p.tagLabel}</span>`:''}
        <button class="product-wish" onclick="event.stopPropagation();toggleWish(this)" title="Merken"><i class="far fa-heart"></i></button>
      </div>
      <div class="product-body">
        <div class="product-brand">${p.brand}</div>
        <div class="product-name">${p.name}</div>
        <div class="product-desc">${p.desc}</div>
        <div class="product-footer">
          <span class="product-price">€${p.price.toFixed(2).replace('.',',')}${p.oldPrice?`<span class="old">€${p.oldPrice.toFixed(2).replace('.',',')}</span>`:''}</span>
          <button class="add-cart-btn" onclick="event.stopPropagation();addToCart(${p.id},this)" title="In den Warenkorb"><i class="fas fa-plus"></i></button>
        </div>
      </div>
    </div>
  `).join('');
}

function filterCategory(el){
  document.querySelectorAll('.cat-chip').forEach(c=>c.classList.remove('active'));
  el.classList.add('active');
  currentCat=el.dataset.cat;
  renderProducts();
}

function scrollToProducts(){
  document.getElementById('productsSection').scrollIntoView({behavior:'smooth'});
}

function toggleWish(btn){
  btn.classList.toggle('liked');
  const icon=btn.querySelector('i');
  if(btn.classList.contains('liked')){
    icon.classList.remove('far');icon.classList.add('fas');
    showToast('Zur Wunschliste hinzugefügt ♥');
  } else {
    icon.classList.remove('fas');icon.classList.add('far');
  }
}

// ─── CART ───
function addToCart(id,btn){
  const p=products.find(x=>x.id===id);
  if(!p)return;
  const existing=cart.find(x=>x.id===id);
  if(existing){existing.qty++;}else{cart.push({...p,qty:1});}
  updateCartUI();
  btn.classList.add('added');
  btn.innerHTML='<i class="fas fa-check"></i>';
  setTimeout(()=>{btn.classList.remove('added');btn.innerHTML='<i class="fas fa-plus"></i>';},1200);
  showToast(p.name+' hinzugefügt');
  const badge=document.getElementById('cartBadge');
  badge.classList.add('show');
  document.getElementById('cartNavBtn').classList.add('cart-pop');
  setTimeout(()=>document.getElementById('cartNavBtn').classList.remove('cart-pop'),400);
}

function updateCartUI(){
  const badge=document.getElementById('cartBadge');
  const totalQty=cart.reduce((s,i)=>s+i.qty,0);
  badge.textContent=totalQty;
  if(totalQty>0)badge.classList.add('show');else badge.classList.remove('show');

  const container=document.getElementById('cartItems');
  const footer=document.getElementById('cartFooter');
  if(cart.length===0){
    container.innerHTML='<div class="cart-empty"><i class="fas fa-shopping-bag"></i><p>Dein Warenkorb ist leer</p></div>';
    footer.style.display='none';
    return;
  }
  footer.style.display='block';
  container.innerHTML=cart.map((item,i)=>`
    <div class="cart-item">
      <div class="cart-item-img" style="background:${item.bg};border-radius:10px;">${item.emoji}</div>
      <div class="cart-item-info">
        <div class="cart-item-name">${item.name}</div>
        <div class="cart-item-variant">${item.brand}</div>
        <div class="cart-item-bottom">
          <span class="cart-item-price">€${(item.price*item.qty).toFixed(2).replace('.',',')}</span>
          <div class="qty-ctrl">
            <button class="qty-btn" onclick="changeQty(${i},-1)">−</button>
            <span class="qty-val">${item.qty}</span>
            <button class="qty-btn" onclick="changeQty(${i},1)">+</button>
          </div>
        </div>
      </div>
    </div>
  `).join('');
  const total=cart.reduce((s,i)=>s+i.price*i.qty,0);
  document.getElementById('cartTotal').textContent='€'+total.toFixed(2).replace('.',',');
}

function changeQty(index,delta){
  cart[index].qty+=delta;
  if(cart[index].qty<=0)cart.splice(index,1);
  updateCartUI();
}

function toggleCart(){
  const overlay=document.getElementById('cartOverlay');
  const drawer=document.getElementById('cartDrawer');
  const isOpen=drawer.classList.contains('open');
  if(isOpen){overlay.classList.remove('open');drawer.classList.remove('open');}
  else{overlay.classList.add('open');drawer.classList.add('open');}
}

function showCheckoutModal(){
  const total=cart.reduce((s,i)=>s+i.price*i.qty,0);
  showModal(
    'Bestellung aufgeben',
    'Gesamtbetrag: €'+total.toFixed(2).replace('.',',')+'. Diese Demo simuliert den Checkout-Prozess. Möchtest du fortfahren?',
    [
      {label:'Abbrechen',style:'outline',action:()=>closeModal()},
      {label:'Bestellen',style:'primary',action:()=>{cart=[];updateCartUI();toggleCart();closeModal();showToast('Bestellung erfolgreich aufgegeben! 🎉');}}
    ]
  );
}

// ─── MODAL (mit sauberer Event-Handling) ───
function showModal(title,text,buttons){
  document.getElementById('modalTitle').textContent=title;
  document.getElementById('modalText').textContent=text;
  const actionsDiv=document.getElementById('modalActions');
  actionsDiv.innerHTML='';
  buttons.forEach((btn,idx)=>{
    const buttonEl=document.createElement('button');
    buttonEl.className=`btn btn-${btn.style}`;
    buttonEl.textContent=btn.label;
    buttonEl.onclick=()=>{ btn.action(); closeModal(); };
    actionsDiv.appendChild(buttonEl);
  });
  document.getElementById('modalOverlay').classList.add('open');
}
function closeModal(){document.getElementById('modalOverlay').classList.remove('open');}

// ─── TOAST ───
function showToast(msg){
  const t=document.getElementById('toast');
  t.innerHTML='<i class="fas fa-check-circle"></i> '+msg;
  t.classList.add('show');
  setTimeout(()=>t.classList.remove('show'),2500);
}

// ─── CHAT ───
function toggleChat(){
  chatOpen=!chatOpen;
  document.getElementById('chatPanel').classList.toggle('open',chatOpen);
  const btn=document.getElementById('chatToggle');
  btn.innerHTML=chatOpen?'<i class="fas fa-times"></i>':'<i class="fas fa-wand-magic-sparkles"></i>';
}

function selectChatBot(el){
  document.querySelectorAll('.chat-bot-chip').forEach(c=>c.classList.remove('active'));
  el.classList.add('active');
  chatBot=el.dataset.bot;
}

function autoGrow(el){
  el.style.height='auto';
  el.style.height=Math.min(el.scrollHeight,80)+'px';
}

function handleChatKey(e){
  if(e.key==='Enter'&&!e.shiftKey){e.preventDefault();sendChatMessage();}
}

function addChatMsg(text,type){
  const msgs=document.getElementById('chatMessages');
  const div=document.createElement('div');
  div.className='chat-msg '+type;
  div.textContent=text;
  msgs.appendChild(div);
  msgs.scrollTop=msgs.scrollHeight;
  return div;
}

function showTyping(){
  const msgs=document.getElementById('chatMessages');
  const div=document.createElement('div');
  div.className='typing-indicator';
  div.id='typingIndicator';
  div.innerHTML='<span></span><span></span><span></span>';
  msgs.appendChild(div);
  msgs.scrollTop=msgs.scrollHeight;
}

function removeTyping(){
  const el=document.getElementById('typingIndicator');
  if(el)el.remove();
}

// Poe-Handler registrieren (wird nach Laden der API ausgeführt)
function registerPoeHandler(){
  if(window.Poe && typeof window.Poe.registerHandler === 'function'){
    window.Poe.registerHandler('lorish-chat-handler',(result)=>{
      const msg=result.responses[0];
      removeTyping();
      if(msg.status==='error'){
        addChatMsg('Entschuldigung, es ist ein Fehler aufgetreten: '+(msg.statusText||'Unbekannt'),'error');
        isSending=false;
        document.getElementById('chatSendBtn').disabled=false;
        return;
      }
      let existingBot=document.querySelector('.chat-msg.bot.streaming');
      if(msg.status==='incomplete'){
        if(!existingBot){
          existingBot=addChatMsg(msg.content,'bot');
          existingBot.classList.add('streaming');
        } else {
          existingBot.textContent=msg.content;
        }
        document.getElementById('chatMessages').scrollTop=document.getElementById('chatMessages').scrollHeight;
      } else if(msg.status==='complete'){
        if(existingBot){
          existingBot.textContent=msg.content;
          existingBot.classList.remove('streaming');
        } else {
          addChatMsg(msg.content,'bot');
        }
        isSending=false;
        document.getElementById('chatSendBtn').disabled=false;
        document.getElementById('chatMessages').scrollTop=document.getElementById('chatMessages').scrollHeight;
      }
    });
  }
}

async function sendChatMessage(){
  if(isSending) return;
  if(!poeReady){
    addChatMsg('Beauty-Beraterin wird geladen. Bitte versuche es gleich noch einmal. 🌸','error');
    return;
  }
  const input=document.getElementById('chatInput');
  const text=input.value.trim();
  if(!text) return;

  addChatMsg(text,'user');
  input.value='';
  input.style.height='auto';
  isSending=true;
  document.getElementById('chatSendBtn').disabled=true;
  showTyping();

  const productList=products.map(p=>p.name+' (€'+p.price.toFixed(2)+') — '+p.desc).join('\n');
  const systemPrompt=`Du bist die freundliche KI-Beauty-Beraterin von Lorish Shop, einem Onlineshop für Ästhetik und Beauty Produkte. Antworte hilfsbereit, warmherzig und professionell auf Deutsch. Halte Antworten knapp (max 150 Wörter). Hier sind unsere aktuellen Produkte:\n${productList}\n\nKundenanfrage:`;

  try{
    await window.Poe.sendUserMessage(
      '@'+chatBot+' '+systemPrompt+'\n'+text,
      {handler:'lorish-chat-handler',stream:true,openChat:false,parameters:{}}
    );
  }catch(err){
    removeTyping();
    isSending=false;
    document.getElementById('chatSendBtn').disabled=false;
    if(err&&err.errorType==='USER_REJECTED_CONFIRMATION'){
      addChatMsg('Nachricht wurde abgebrochen.','error');
    } else {
      addChatMsg('Fehler: '+(err.message||String(err)),'error');
    }
  }
}

// ─── INIT ───
renderProducts();
updateCartUI();

// Poe-API abwarten und Handler registrieren
waitForPoe(()=>{
  registerPoeHandler();
  console.log('Poe API bereit');
});
</script>
</body>
</html>
