<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>696 PARTY</title>
  <style>
    body {
      font-family: "Poppins", sans-serif;
      background: linear-gradient(135deg, #0d0d2b, #1a1a40);
      color: #f5f5f5;
      margin: 0;
      padding: 0;
    }
    header {
      background: linear-gradient(90deg, #7209b7, #3a0ca3, #4361ee);
      padding: 25px;
      text-align: center;
      color: #fff;
      box-shadow: 0 0 25px rgba(114, 9, 183, 0.8);
      border-bottom: 3px solid #7209b7;
    }
    header h1 {
      margin: 0;
      font-size: 30px;
      text-shadow: 0 0 8px #fff, 0 0 15px #00d4ff;
      letter-spacing: 2px;
    }
    header p {
      margin: 5px 0 0;
      font-size: 15px;
      color: #ddd;
      letter-spacing: 1px;
    }
    .party-container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
      gap: 20px;
      padding: 20px;
    }
    .hero-card {
      background: linear-gradient(180deg, #1e1e2f, #2a2a4a);
      border-radius: 15px;
      border: 2px solid transparent;
      overflow: hidden;
      cursor: pointer;
      box-shadow: 0 0 15px rgba(0, 212, 255, 0.2);
      transition: transform 0.3s ease, box-shadow 0.3s ease, border 0.3s ease;
    }
    .hero-card:hover {
      transform: translateY(-8px) scale(1.05);
      border: 2px solid #00d4ff;
      box-shadow: 0 0 20px #00d4ff, 0 0 40px #7209b7;
    }
    .hero-card img {
      width: 100%;
      height: 150px;
      object-fit: cover;
      border-bottom: 2px solid rgba(0, 212, 255, 0.5);
    }
    .hero-info {
      padding: 12px;
      text-align: center;
    }
    .hero-info h3 {
      margin: 5px 0;
      font-size: 18px;
      color: #00d4ff;
      text-shadow: 0 0 6px #00d4ff;
    }
    .hero-info p {
      margin: 0;
      font-size: 14px;
      font-weight: bold;
      color: #ffcc70;
      text-shadow: 0 0 6px #ffcc70;
      letter-spacing: 1px;
    }

    /* === POPUP MODAL === */
    .modal {
      display: none;
      position: fixed;
      z-index: 1000;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      background: rgba(0,0,0,0.8);
      backdrop-filter: blur(3px);
      justify-content: center;
      align-items: center;
    }
    .modal-content {
      background: linear-gradient(180deg, #1e1e2f, #2a2a4a);
      padding: 20px;
      border-radius: 15px;
      box-shadow: 0 0 20px #00d4ff;
      text-align: center;
      max-width: 350px;
      animation: pop 0.3s ease;
    }
    @keyframes pop {
      from { transform: scale(0.7); opacity: 0; }
      to { transform: scale(1); opacity: 1; }
    }
    .modal-content img {
      width: 100%;
      border-radius: 10px;
      margin-bottom: 10px;
    }
    .modal-content h2 {
      margin: 10px 0;
      color: #00d4ff;
      text-shadow: 0 0 8px #00d4ff;
    }
    .modal-content p {
      margin: 5px 0;
      font-size: 14px;
    }
    .close {
      margin-top: 15px;
      padding: 8px 16px;
      background: #ff004c;
      border: none;
      color: #fff;
      border-radius: 8px;
      cursor: pointer;
      transition: 0.3s;
    }
    .close:hover {
      background: #ff3366;
      box-shadow: 0 0 10px #ff004c;
    }

    /* === PRESTASI === */
    .prestasi {
      padding: 30px 20px;
      text-align: center;
      background: linear-gradient(180deg, #1a1a40, #0d0d2b);
      border-top: 2px solid #7209b7;
      box-shadow: 0 -5px 20px rgba(114,9,183,0.5);
    }
    .prestasi h2 {
      font-size: 24px;
      margin-bottom: 20px;
      color: #ffcc70;
      text-shadow: 0 0 8px #ffcc70, 0 0 15px #ff6600;
    }
    .prestasi-list {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 15px;
      max-width: 900px;
      margin: 0 auto;
    }
    .prestasi-item {
      background: linear-gradient(180deg, #2a2a4a, #1e1e2f);
      border: 2px solid transparent;
      border-radius: 12px;
      padding: 15px;
      box-shadow: 0 0 10px rgba(0,212,255,0.3);
      transition: 0.3s ease;
    }
    .prestasi-item:hover {
      border: 2px solid #00d4ff;
      box-shadow: 0 0 20px #00d4ff, 0 0 30px #7209b7;
      transform: scale(1.05);
    }
    .prestasi-item h3 {
      margin: 0;
      color: #00d4ff;
      text-shadow: 0 0 6px #00d4ff;
      font-size: 18px;
    }
    .prestasi-item p {
      margin: 5px 0 0;
      font-size: 14px;
      color: #ddd;
    }
  </style>
</head>
<body>
  <header>
    <h1>696 PARTY</h1>
    <p>ANGGOTA PARTY - MOBILE LEGENDS</p>
  </header>

  <!-- ANGGOTA PARTY -->
  <section class="party-container">
    <div class="hero-card" onclick="openModal('ZYAT','XP LANE','CICI','Power: Curtain Call','https://i.supaimg.com/e4ac05a6-0058-4ddb-a569-2dbeb6f0a9c6.jpg')">
      <img src="https://i.supaimg.com/e4ac05a6-0058-4ddb-a569-2dbeb6f0a9c6.jpg" alt="ZYAT">
      <div class="hero-info">
        <h3>ZYAT</h3>
        <p>XP LANE</p>
      </div>
    </div>
    <div class="hero-card" onclick="openModal('CALVINE','JUNGLER','Julian','Power: Chain','https://i.supaimg.com/360bdef9-24bf-4a3f-ac77-d6a8aaa11afc.jpg')">
      <img src="https://i.supaimg.com/360bdef9-24bf-4a3f-ac77-d6a8aaa11afc.jpg" alt="CALVINE">
      <div class="hero-info">
        <h3>CALVINE</h3>
        <p>JUNGLER</p>
      </div>
    </div>
    <div class="hero-card" onclick="openModal('KENZYSKY','GOLD LANE','Granger','Power: Death Sonata','https://i.supaimg.com/5041dd79-6986-401b-8bff-417ba1c4ee67.jpg')">
      <img src="https://i.supaimg.com/5041dd79-6986-401b-8bff-417ba1c4ee67.jpg" alt="KENZYSKY">
      <div class="hero-info">
        <h3>KENZYSKY</h3>
        <p>GOLD LANE</p>
      </div>
    </div>
    <div class="hero-card" onclick="openModal('FRICILLA','MAGE','Kagura','Power: Yin Yang Overturn','https://i.supaimg.com/72db14c4-3634-4e61-8737-bf9af4ad5604.jpg')">
      <img src="https://i.supaimg.com/72db14c4-3634-4e61-8737-bf9af4ad5604.jpg" alt="FRICILLA">
      <div class="hero-info">
        <h3>FRICILLA</h3>
        <p>MAGE</p>
      </div>
    </div>
    <div class="hero-card" onclick="openModal('SUPER DREAM','XP LANE','Lapu-Lapu','Power: Homeland Defender','https://i.supaimg.com/797ce193-0ed3-4e18-856b-923231f5cca8.jpg')">
      <img src="https://i.supaimg.com/797ce193-0ed3-4e18-856b-923231f5cca8.jpg" alt="AL VIRLY">
      <div class="hero-info">
        <h3>SUPER DREAM</h3>
        <p>XP LANE</p>
      </div>
    </div>
    <div class="hero-card" onclick="openModal('masgliez','XP LANE','yuzhong','Power: black dragon from','https://i.supaimg.com/458a2a91-d780-44d3-9f1e-3ac8b352b20a.jpg')">
      <img src="https://i.supaimg.com/458a2a91-d780-44d3-9f1e-3ac8b352b20a.jpg" alt="AGLIZ">
      <div class="hero-info">
        <h3>masgliez</h3>
        <p>XP LANE</p>
      </div>
    </div>
    <div class="hero-card" onclick="openModal('AINZZ','ROAM','jonshon','Power: rapid tou','https://i.supaimg.com/7c42dcee-43d1-4e77-adce-a81bdad0dd91.jpg')">
      <img src="https://i.supaimg.com/7c42dcee-43d1-4e77-adce-a81bdad0dd91.jpg" alt="WIRIA">
      <div class="hero-info">
        <h3>AINZZ</h3>
        <p>ROAM</p>
      </div>
    </div>
    <div class="hero-card" onclick="openModal('cheys','JUNGLER','lancelot','Power: phantom execution','https://i.supaimg.com/2d81db97-8749-43f9-89ce-e4563cd6cc7f.jpg')">
      <img src="https://i.supaimg.com/2d81db97-8749-43f9-89ce-e4563cd6cc7f.jpg" alt="FIKRY">
      <div class="hero-info">
        <h3>cheys</h3>
        <p>JUNGLER</p>
      </div>
    </div>
  </section>

  <!-- PRESTASI -->
  <section class="prestasi">
    <h2>🏆 MAU BAI ONE??? have fun? HUBUNGI NOMER DI
    BAWAH INI FREE KOK GUYS</h2>
    <div class="prestasi-list">
      <div class="prestasi-item">
        <h3>ADMIN </h3>
        <p>0895 0776 0714</p>
      </div>
      <div class="prestasi-item">
        <h3></h3>
        <p></p>
      </div>
      <div class="prestasi-item">
        <h3></h3>
        <p></p>
      </div>
      <div class="prestasi-item">
        <h3></h3>
        <p></p>
      </div>
    </div>
  </section>

  <!-- Modal -->
  <div id="heroModal" class="modal">
    <div class="modal-content">
      <img id="heroImg" src="" alt="Hero">
      <h2 id="heroName"></h2>
      <p><b>Role:</b> <span id="heroRole"></span></p>
      <p><b>Hero:</b> <span id="heroHero"></span></p>
      <p><b>Special:</b> <span id="heroPower"></span></p>
      <button class="close" onclick="closeModal()">Tutup</button>
    </div>
  </div>

  <script>
    function openModal(name, role, hero, power, img) {
      document.getElementById("heroName").innerText = name;
      document.getElementById("heroRole").innerText = role;
      document.getElementById("heroHero").innerText = hero;
      document.getElementById("heroPower").innerText = power;
      document.getElementById("heroImg").src = img;
      document.getElementById("heroModal").style.display = "flex";
    }
    function closeModal() {
      document.getElementById("heroModal").style.display = "none";
    }
  </script>
</body>
</html>
