<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Lapengatti Motors</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #0d0d0d;
      color: white;
    }

    header {
      text-align: center;
      padding: 30px 20px;
      background: #111;
      border-bottom: 2px solid #444;
    }

    header h1 {
      margin: 0 0 5px;
      letter-spacing: 2px;
    }

    header p {
      margin: 0;
      color: #bbb;
    }

    .top-nav {
      text-align: center;
      padding: 10px 0;
      background: #151515;
      border-bottom: 1px solid #333;
    }

    .top-nav button {
      background: #222;
      color: #eee;
      border: 1px solid #444;
      padding: 8px 16px;
      margin: 0 5px;
      border-radius: 20px;
      cursor: pointer;
      font-size: 0.9rem;
      transition: 0.2s;
    }

    .top-nav button:hover {
      background: #2e2e2e;
      transform: translateY(-1px);
    }

    .model-grid, .trim-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
      padding: 30px 20px 50px;
      max-width: 1100px;
      margin: 0 auto;
    }

    .model-card, .trim-card {
      background: #1a1a1a;
      padding: 20px;
      border-radius: 12px;
      cursor: pointer;
      transition: 0.2s;
      border: 1px solid #333;
      box-shadow: 0 8px 18px rgba(0,0,0,0.4);
    }

    .model-card:hover, .trim-card:hover {
      transform: translateY(-4px);
      background: #222;
      border-color: #666;
    }

    .model-card h2, .trim-card h3 {
      margin-top: 0;
    }

    .badge {
      display: inline-block;
      padding: 3px 10px;
      border-radius: 999px;
      font-size: 0.7rem;
      text-transform: uppercase;
      letter-spacing: 1px;
      margin-bottom: 8px;
      background: #262626;
      color: #ccc;
    }

    .price {
      font-size: 1.1rem;
      font-weight: bold;
      margin-top: 5px;
      color: #7dd56f;
    }

    .cta {
      margin-top: 12px;
      font-size: 0.85rem;
      color: #aaa;
    }

    .hidden {
      display: none;
    }

    .section-title {
      text-align: center;
      margin: 25px 0 5px;
      font-size: 1.4rem;
      color: #f5f5f5;
    }

    .section-sub {
      text-align: center;
      margin: 0 0 20px;
      font-size: 0.9rem;
      color: #999;
    }

    .back-link {
      text-align: center;
      margin-top: 10px;
    }

    .back-link button {
      background: transparent;
      border: none;
      color: #aaa;
      cursor: pointer;
      font-size: 0.85rem;
      text-decoration: underline;
    }

    .popup {
      position: fixed;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: rgba(0,0,0,0.7);
      display: flex;
      justify-content: center;
      align-items: center;
      z-index: 10;
    }

    .popup-box {
      background: #222;
      padding: 25px 30px 20px;
      border-radius: 12px;
      text-align: center;
      max-width: 320px;
      width: 90%;
      border: 1px solid #444;
      box-shadow: 0 10px 25px rgba(0,0,0,0.6);
    }

    .popup-box h2 {
      margin-top: 0;
    }

    .popup-box p {
      margin: 8px 0;
    }

    .popup-box button {
      margin-top: 15px;
      padding: 8px 18px;
      border-radius: 20px;
      border: none;
      cursor: pointer;
      background: #3b82f6;
      color: white;
      font-weight: 600;
      transition: 0.2s;
    }

    .popup-box button:hover {
      background: #2563eb;
    }

    footer {
      text-align: center;
      padding: 15px 10px 25px;
      font-size: 0.8rem;
      color: #666;
      border-top: 1px solid #222;
      background: #050505;
    }
  </style>
</head>
<body>

  <header>
    <h1>Lapengatti Motors</h1>
    <p>Performance. Precision. Presence.</p>
  </header>

  <div class="top-nav">
    <button onclick="showHome()">Models</button>
    <button onclick="fakeLink()">Build &amp; Price</button>
    <button onclick="fakeLink()">Find a Dealer</button>
  </div>

  <!-- HOME / MODEL LIST -->
  <section id="homeSection">
    <h2 class="section-title">Choose Your Lapengatti</h2>
    <p class="section-sub">Tap a model to explore trims and pricing.</p>

    <div class="model-grid">
      <div class="model-card" onclick="openModel('spektral')">
        <span class="badge">EV</span>
        <h2>Spektral</h2>
        <p>Electric • Sleek • Silent Power</p>
        <p class="price">From $49,995</p>
        <p class="cta">View trims &amp; details →</p>
      </div>

      <div class="model-card" onclick="openModel('testaback')">
        <span class="badge">Hybrid</span>
        <h2>Testaback</h2>
        <p>Twin‑Turbo Hybrid • Track Ready</p>
        <p class="price">From $68,500</p>
        <p class="cta">View trims &amp; details →</p>
      </div>

      <div class="model-card" onclick="openModel('evermore')">
        <span class="badge">Luxury</span>
        <h2>Evermore</h2>
        <p>Luxury • Comfort • Endless Range</p>
        <p class="price">From $55,000</p>
        <p class="cta">View trims &amp; details →</p>
      </div>
    </div>
  </section>

  <!-- MODEL DETAIL / TRIMS -->
  <section id="modelSection" class="hidden">
    <h2 id="modelName" class="section-title"></h2>
    <p id="modelTagline" class="section-sub"></p>

    <div id="trimList" class="trim-grid"></div>

    <div class="back-link">
      <button onclick="showHome()">← Back to all models</button>
    </div>
  </section>

  <!-- POPUP -->
  <div id="popup" class="popup hidden">
    <div class="popup-box">
      <h2 id="popupTitle"></h2>
      <p id="popupPrice"></p>
      <p style="font-size:0.85rem;color:#aaa;">
        This is a fictional Lapengatti configuration.<br>
        No payment. Just vibes.
      </p>
      <button onclick="closePopup()">Close</button>
    </div>
  </div>

  <footer>
    Lapengatti Motors · A fictional brand experience · © 2026
  </footer>

  <script>
    // MODEL DATA
    const models = {
      spektral: {
        name: "Lapengatti Spektral",
        tagline: "Electric • Silent • Deadly Smooth",
        trims: [
          { name: "Base", price: "$49,995" },
          { name: "Dual Motor", price: "$59,995" },
          { name: "Spektral RS", price: "$74,995" }
        ]
      },

      testaback: {
        name: "Lapengatti Testaback",
        tagline: "Twin‑Turbo Hybrid • Track Weapon",
        trims: [
          { name: "Sport", price: "$68,500" },
          { name: "Track Pack", price: "$82,900" },
          { name: "V2 Prototype", price: "Not For Sale" }
        ]
      },

      evermore: {
        name: "Lapengatti Evermore",
        tagline: "Luxury • Comfort • Infinite Range",
        trims: [
          { name: "Comfort", price: "$55,000" },
          { name: "Prestige", price: "$69,000" },
          { name: "Evermore Elite", price: "$89,000" }
        ]
      }
    };

    const homeSection = document.getElementById("homeSection");
    const modelSection = document.getElementById("modelSection");
    const modelNameEl = document.getElementById("modelName");
    const modelTaglineEl = document.getElementById("modelTagline");
    const trimListEl = document.getElementById("trimList");
    const popupEl = document.getElementById("popup");
    const popupTitleEl = document.getElementById("popupTitle");
    const popupPriceEl = document.getElementById("popupPrice");

    function showHome() {
      modelSection.classList.add("hidden");
      homeSection.classList.remove("hidden");
    }

    function openModel(key) {
      const model = models[key];
      if (!model) return;

      homeSection.classList.add("hidden");
      modelSection.classList.remove("hidden");

      modelNameEl.textContent = model.name;
      modelTaglineEl.textContent = model.tagline;
      trimListEl.innerHTML = "";

      model.trims.forEach(trim => {
        const card = document.createElement("div");
        card.className = "trim-card";
        card.innerHTML = `
          <h3>${trim.name}</h3>
          <p class="price">${trim.price}</p>
          <p class="cta">Select trim →</p>
        `;
        card.onclick = () => openPopup(trim);
        trimListEl.appendChild(card);
      });
    }

    function openPopup(trim) {
      popupTitleEl.textContent = trim.name;
      popupPriceEl.textContent = `Configured price: ${trim.price}`;
      popupEl.classList.remove("hidden");
    }

    function closePopup() {
      popupEl.classList.add("hidden");
    }

    function fakeLink() {
      alert("In the full Lapengatti universe, this would open a full configurator or dealer locator. For now, this is a demo.");
    }
  </script>
</body>
</html>
