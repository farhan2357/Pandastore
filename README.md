<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Panda Store - Pulsa & Voucher Game</title>
  <style>
    body {
      font-family: 'Segoe UI', Arial, sans-serif;
      margin: 0;
      padding: 0;
      background: #eef6fb;
    }
    header {
      background: linear-gradient(135deg, #0077cc, #005fa3);
      color: white;
      padding: 30px 20px;
      text-align: center;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 15px;
    }
    header img {
      width: 60px;
      height: 60px;
      border-radius: 50%;
      background: white;
      padding: 5px;
    }
    header h1 {
      margin: 0;
      font-size: 2rem;
    }
    nav {
      background: #004f87;
      padding: 12px;
      text-align: center;
      position: sticky;
      top: 0;
      z-index: 100;
    }
    nav a {
      color: white;
      margin: 0 15px;
      text-decoration: none;
      font-weight: bold;
      transition: 0.3s;
    }
    nav a:hover {
      color: #ffd700;
    }
    .container {
      padding: 25px;
      max-width: 1000px;
      margin: auto;
    }
    .card {
      background: white;
      padding: 20px;
      border-radius: 15px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
      margin: 20px 0;
      transition: transform 0.2s;
    }
    .card:hover {
      transform: translateY(-5px);
    }
    .card h3 {
      margin-top: 0;
    }
    footer {
      background: #0077cc;
      color: white;
      text-align: center;
      padding: 20px;
      margin-top: 40px;
    }
    /* Form Style */
    form {
      display: flex;
      flex-direction: column;
      gap: 12px;
      margin-top: 15px;
    }
    input, select {
      padding: 12px;
      border: 1px solid #ccc;
      border-radius: 10px;
      font-size: 1rem;
    }
    button {
      background: #28a745;
      color: white;
      padding: 12px;
      border: none;
      border-radius: 10px;
      font-size: 1rem;
      cursor: pointer;
      transition: 0.3s;
    }
    button:hover {
      background: #218838;
    }

    /* Table Style */
    table {
      width: 100%;
      border-collapse: collapse;
      margin-top: 15px;
      font-size: 0.95rem;
    }
    table th, table td {
      border: 1px solid #ddd;
      padding: 12px;
      text-align: center;
    }
    table th {
      background: #0077cc;
      color: white;
    }
    table tr:nth-child(even) {
      background: #f9f9f9;
    }

    /* Modal */
    .modal {
      display: none;
      position: fixed;
      z-index: 999;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      background: rgba(0,0,0,0.6);
      display: flex;
      justify-content: center;
      align-items: center;
    }
    .modal-content {
      background: white;
      padding: 25px;
      border-radius: 15px;
      text-align: center;
      max-width: 400px;
      box-shadow: 0 5px 20px rgba(0,0,0,0.3);
      animation: fadeIn 0.4s ease;
    }
    .modal-content h2 {
      color: #28a745;
      margin-top: 0;
    }
    .close-btn {
      margin-top: 15px;
      padding: 10px 20px;
      background: #0077cc;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      transition: 0.3s;
    }
    .close-btn:hover {
      background: #005fa3;
    }
    @keyframes fadeIn {
      from { transform: scale(0.9); opacity: 0; }
      to { transform: scale(1); opacity: 1; }
    }
  </style>
</head>
<body>

  <header>
    <!-- Logo Panda -->
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/0f/Panda_icon.svg/512px-Panda_icon.svg.png" alt="Logo Panda">
    <div>
      <h1>Panda Store</h1>
      <p>Pulsa & Voucher Game Online</p>
    </div>
  </header>

  <nav>
    <a href="#">Beranda</a>
    <a href="#pulsa">Pulsa</a>
    <a href="#voucher">Voucher Game</a>
    <a href="#kontak">Kontak</a>
  </nav>

  <div class="container">
    <h2>Produk Populer</h2>

    <!-- Pulsa -->
    <div class="card" id="pulsa">
      <h3>Pulsa Telkomsel</h3>
      <p>Isi ulang pulsa Telkomsel dengan mudah & cepat.</p>

      <!-- Tabel Harga Pulsa -->
      <table>
        <tr>
          <th>Nominal</th>
          <th>Harga</th>
        </tr>
        <tr><td>Rp 10.000</td><td>Rp 11.000</td></tr>
        <tr><td>Rp 25.000</td><td>Rp 26.500</td></tr>
        <tr><td>Rp 50.000</td><td>Rp 52.000</td></tr>
        <tr><td>Rp 100.000</td><td>Rp 102.000</td></tr>
      </table>

      <form class="form-pulsa">
        <label>Nomor HP:</label>
        <input type="text" placeholder="08xxxxxx" required>

        <label>Pilih Nominal:</label>
        <select required>
          <option value="">-- Pilih --</option>
          <option value="10k">Rp 10.000</option>
          <option value="25k">Rp 25.000</option>
          <option value="50k">Rp 50.000</option>
          <option value="100k">Rp 100.000</option>
        </select>

        <button type="submit">Beli Pulsa</button>
      </form>
    </div>

    <!-- Voucher Game -->
    <div class="card" id="voucher">
      <h3>Voucher Mobile Legends</h3>
      <p>Dapatkan diamond Mobile Legends dengan harga murah.</p>

      <!-- Tabel Harga Diamond -->
      <table>
        <tr>
          <th>Paket Diamond</th>
          <th>Harga</th>
        </tr>
        <tr><td>86 Diamond</td><td>Rp 20.000</td></tr>
        <tr><td>172 Diamond</td><td>Rp 40.000</td></tr>
        <tr><td>257 Diamond</td><td>Rp 60.000</td></tr>
        <tr><td>514 Diamond</td><td>Rp 115.000</td></tr>
      </table>

      <form class="form-voucher">
        <label>ID Player:</label>
        <input type="text" placeholder="Masukkan ID ML" required>

        <label>Pilih Paket:</label>
        <select required>
          <option value="">-- Pilih --</option>
          <option value="86dm">86 Diamond</option>
          <option value="172dm">172 Diamond</option>
          <option value="257dm">257 Diamond</option>
          <option value="514dm">514 Diamond</option>
        </select>

        <button type="submit">Beli Voucher</button>
      </form>
    </div>
  </div>

  <footer id="kontak">
    <p>&copy; 2025 Panda Store. Semua Hak Dilindungi.</p>
    <p>WhatsApp: 08xxxxxxxxxx | Email: pandastore@gmail.com</p>
  </footer>

  <!-- Modal -->
  <div id="successModal" class="modal">
    <div class="modal-content">
      <h2>✅ Transaksi Berhasil!</h2>
      <p id="orderDetail"></p>
      <button class="close-btn">Tutup</button>
    </div>
  </div>

  <script>
    const modal = document.getElementById("successModal");
    const detailText = document.getElementById("orderDetail");
    const closeBtn = document.querySelector(".close-btn");

    function showModal(message) {
      detailText.innerText = message;
      modal.style.display = "flex";
    }

    closeBtn.addEventListener("click", () => {
      modal.style.display = "none";
    });

    // Form Pulsa
    document.querySelector(".form-pulsa").addEventListener("submit", function(e) {
      e.preventDefault();
      const nomor = this.querySelector("input").value;
      const nominal = this.querySelector("select").value;
      if(nomor && nominal){
        showModal("Nomor: " + nomor + "\nNominal: " + nominal);
        this.reset();
      }
    });

    // Form Voucher
    document.querySelector(".form-voucher").addEventListener("submit", function(e) {
      e.preventDefault();
      const idPlayer = this.querySelector("input").value;
      const paket = this.querySelector("select").value;
      if(idPlayer && paket){
        showModal("ID Player: " + idPlayer + "\nPaket: " + paket);
        this.reset();
      }
    });
  </script>

</body>
</html>
