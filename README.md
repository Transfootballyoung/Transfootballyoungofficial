!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Excel Ananda | Official Player Profile</title>

<style>
:root {
    --bg:#f2f2f2;
    --card:#ffffff;
    --text:#000;
    --primary:#0b2a55;
}
.dark {
    --bg:#121212;
    --card:#1e1e1e;
    --text:#f2f2f2;
    --primary:#1e90ff;
}
html { scroll-behavior:smooth; }
body {
    margin:0;
    font-family:Arial, Helvetica, sans-serif;
    background:var(--bg);
    color:var(--text);
}
header {
    background:var(--primary);
    color:#fff;
    padding:15px 25px;
    display:flex;
    justify-content:space-between;
    align-items:center;
}
header button {
    background:none;
    border:none;
    color:white;
    font-size:20px;
    cursor:pointer;
}
nav {
    display:flex;
    margin:10px 15px;
    border-radius:8px;
    overflow:hidden;
    background:#e6e6e6;
}
nav a {
    flex:1;
    text-align:center;
    padding:12px;
    text-decoration:none;
    font-weight:bold;
    color:#000;
}
nav a:hover {
    background:var(--primary);
    color:white;
}
.card {
    background:var(--card);
    margin:15px;
    padding:20px;
    border-radius:10px;
}
.player {
    display:flex;
}
.player img {
    width:180px;
    border-radius:10px;
    object-fit:cover;
}
.info {
    margin-left:20px;
    flex:1;
}
.info-grid {
    display:grid;
    grid-template-columns:repeat(2,1fr);
    margin-top:10px;
}
.market {
    background:#1e90ff;
    color:white;
    display:inline-block;
    padding:10px 15px;
    border-radius:6px;
    margin-top:10px;
}
.stats-grid {
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:15px;
}
.stat {
    background:#f5f5f5;
    text-align:center;
    padding:15px;
    border-radius:8px;
}
canvas {
    width:100%;
    max-width:600px;
}
table {
    width:100%;
    border-collapse:collapse;
}
td {
    padding:10px;
    border-bottom:1px solid #ccc;
}
footer {
    text-align:center;
    padding:20px;
    color:#888;
}
@media(max-width:768px){
    .player{flex-direction:column;text-align:center;}
    .info{margin-left:0;}
    .info-grid{grid-template-columns:1fr;}
    .stats-grid{grid-template-columns:repeat(2,1fr);}
}
</style>
</head>

<body>

<header>
    <strong>Transferfootball Young – Official</strong>
    <button onclick="toggleDark()">🌙</button>
</header>

<nav>
    <a href="#profil">Profil</a>
    <a href="#statistik">Statistik</a>
    <a href="#prestasi">Prestasi</a>
    <a href="#grafik">Grafik</a>
    <a href="#data">Data</a>
</nav>

<!-- PROFIL -->
<section class="card player" id="profil">
    <img src="excel-ananda.jpg" alt="Excel Ananda">
    <div class="info">
        <h2>#7 EXCEL ANANDA 
            <span style="background:#1e90ff;color:#fff;padding:3px 6px;border-radius:4px;">C</span>
        </h2>
        <p><strong>London FC 🇬🇧</strong></p>

        <div class="info-grid">
            <p>Tanggal Lahir: 27 April 2010</p>
            <p>Kewarganegaraan: Indonesia</p>
            <p>Tinggi: 155 cm</p>
            <p>Posisi: Left Winger</p>
            <p>Agen: Open Table</p>
            <p>Pemain Internasional: Indonesia</p>
        </div>

        <div class="market">Nilai Pasar: 280 Juta</div>
        <p style="font-size:22px;">🏆 🏆 🥇 ⚽ 🏅</p>
    </div>
</section>

<!-- STATISTIK -->
<section class="card" id="statistik">
    <h2>STATISTIK MUSIM INI</h2>
    <div class="stats-grid">
        <div class="stat"><h3>12</h3><p>Pertandingan</p></div>
        <div class="stat"><h3>7</h3><p>Gol</p></div>
        <div class="stat"><h3>5</h3><p>Assist</p></div>
        <div class="stat"><h3>2</h3><p>Penghargaan</p></div>
    </div>
</section>

<!-- PRESTASI -->
<section class="card" id="prestasi">
    <h2>PRESTASI PEMAIN</h2>
    <ul>
        <li>🏆 Juara Liga Usia Dini</li>
        <li>🥇 Top Skor Turnamen Nasional U-13</li>
        <li>🏆 Juara Piala Akademi</li>
        <li>⚽ Pemain Terbaik Turnamen Regional</li>
        <li>🏆 <strong>Juara Piala London Raya U-16</strong></li>
    </ul>
</section>

<!-- GRAFIK -->
<section class="card" id="grafik">
    <h2>GRAFIK PERFORMA</h2>
    <canvas id="chart"></canvas>
</section>

<!-- DATA -->
<section class="card" id="data">
    <h2>DATA PEMAIN</h2>
    <table>
        <tr><td>Nama Lengkap</td><td>Excel Ananda</td></tr>
        <tr><td>Tempat Lahir</td><td>Bogor, Indonesia</td></tr>
        <tr><td>Bergabung</td><td>1 Januari 2023</td></tr>
        <tr><td>Klub</td><td>London FC</td></tr>
        <tr><td>Kaki Dominan</td><td>Kanan</td></tr>
        <tr><td>Brand</td><td>Glacio</td></tr>
    </table>
</section>

<footer>
    © Transferfootball Young – London FC
</footer>

<script>
function toggleDark(){
    document.body.classList.toggle("dark");
}

// Grafik sederhana
const c = document.getElementById("chart");
const ctx = c.getContext("2d");

const dataGol = [2,4,7];
const dataAssist = [1,3,5];

ctx.beginPath();
ctx.moveTo(50,200-dataGol[0]*20);
ctx.lineTo(150,200-dataGol[1]*20);
ctx.lineTo(250,200-dataGol[2]*20);
ctx.strokeStyle="blue";
ctx.stroke();

ctx.beginPath();
ctx.moveTo(50,200-dataAssist[0]*20);
ctx.lineTo(150,200-dataAssist[1]*20);
ctx.lineTo(250,200-dataAssist[2]*20);
ctx.strokeStyle="green";
ctx.stroke();
</script>

</body>
</html>
