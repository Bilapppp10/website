<!DOCTYPE html>  <html lang="id">  
<head>  
<meta charset="UTF-8">  
<meta name="viewport" content="width=device-width, initial-scale=1.0">  
<title>Tugasku</title>  <style>  
* {  
    box-sizing: border-box;  
    margin: 0;  
    padding: 0;  
    font-family: Arial, sans-serif;  
}  
  
body {  
    background: #f3f6fb;  
    color: #222;  
    padding-bottom: 80px;  
}  
  
header {  
    background: #2563eb;  
    color: white;  
    padding: 22px;  
    border-radius: 0 0 25px 25px;  
}  
  
header h1 {  
    font-size: 26px;  
}  
  
header p {  
    margin-top: 5px;  
    opacity: .9;  
}  
  
.container {  
    padding: 18px;  
}  
  
.page {  
    display: none;  
}  
  
.page.active {  
    display: block;  
}  
  
.card {  
    background: white;  
    padding: 18px;  
    margin-bottom: 15px;  
    border-radius: 15px;  
    box-shadow: 0 3px 12px rgba(0,0,0,.08);  
}  
  
.card h3 {  
    margin-bottom: 8px;  
}  
  
.info {  
    color: #666;  
    font-size: 14px;  
    margin: 5px 0;  
}  
  
input, select, textarea {  
    width: 100%;  
    padding: 12px;  
    margin: 7px 0 13px;  
    border: 1px solid #ddd;  
    border-radius: 10px;  
    outline: none;  
}  
  
textarea {  
    height: 90px;  
    resize: none;  
}  
  
button {  
    border: none;  
    padding: 12px 16px;  
    border-radius: 10px;  
    background: #2563eb;  
    color: white;  
    font-weight: bold;  
    cursor: pointer;  
}  
  
button:hover {  
    opacity: .9;  
}  
  
.btn-danger {  
    background: #dc2626;  
}  
  
.btn-green {  
    background: #16a34a;  
}  
  
.success {  
    display: none;  
    background: #dcfce7;  
    color: #166534;  
    padding: 13px;  
    border-radius: 10px;  
    margin-bottom: 15px;  
}  
  
.empty {  
    text-align: center;  
    color: #777;  
    padding: 30px;  
}  
  
.bottom-nav {  
    position: fixed;  
    bottom: 0;  
    left: 0;  
    right: 0;  
    height: 70px;  
    background: white;  
    display: flex;  
    justify-content: space-around;  
    align-items: center;  
    box-shadow: 0 -3px 15px rgba(0,0,0,.12);  
    z-index: 100;  
}  
  
.nav-btn {  
    background: none;  
    color: #777;  
    font-size: 12px;  
    padding: 7px;  
}  
  
.nav-btn.active {  
    color: #2563eb;  
}  
  
.nav-icon {  
    display: block;  
    font-size: 22px;  
    margin-bottom: 3px;  
}  
  
.file-box {  
    background: #f1f5f9;  
    padding: 12px;  
    border-radius: 10px;  
    margin: 10px 0;  
    word-break: break-word;  
}  
  
.viewer {  
    display: none;  
    position: fixed;  
    inset: 0;  
    background: rgba(0,0,0,.8);  
    z-index: 999;  
    padding: 20px;  
}  
  
.viewer-content {  
    background: white;  
    width: 100%;  
    height: 100%;  
    border-radius: 15px;  
    overflow: hidden;  
    position: relative;  
}  
  
.viewer iframe {  
    width: 100%;  
    height: 100%;  
    border: none;  
}  
  
.viewer img {  
    width: 100%;  
    height: 100%;  
    object-fit: contain;  
}  
  
.close-viewer {  
    position: absolute;  
    top: 10px;  
    right: 10px;  
    z-index: 10;  
    background: #dc2626;  
    border-radius: 50%;  
    width: 40px;  
    height: 40px;  
    padding: 0;  
}  
  
.back-btn {  
    background: #64748b;  
    margin-bottom: 15px;  
}  
</style>  </head>  <body>  <header>  
    <h1>📚 TUGASKU</h1>  
    <p>Aplikasi Pengumpulan Tugas</p>  
</header>  <div class="container">  <!-- BERANDA -->  
<div id="home" class="page active">  

    <div class="card">  
        <h2>👋 Selamat Datang!</h2>  
        <p style="margin-top:8px;">  
            Kelola dan kumpulkan tugas sekolah dengan mudah.  
        </p>  
    </div>  

    <div class="card">  
        <h3>📌 Tugas Terbaru</h3>  

        <div class="card">  
            <h3>💻 Pemrograman</h3>  
            <p class="info">Membuat program sederhana</p>  
            <p class="info">Deadline: 10 September 2026</p>  
        </div>  

        <div class="card">  
            <h3>📖 Bahasa Indonesia</h3>  
            <p class="info">Membuat teks laporan</p>  
            <p class="info">Deadline: 12 September 2026</p>  
        </div>  

        <div class="card">  
            <h3>🧮 Matematika</h3>  
            <p class="info">Latihan soal aljabar</p>  
            <p class="info">Deadline: 15 September 2026</p>  
        </div>  
    </div>  

</div>  


<!-- DAFTAR TUGAS -->  
<div id="tasks" class="page">  

    <div class="card">  
        <h2>📋 Daftar Tugas</h2>  
    </div>  

    <div class="card">  
        <h3>💻 Pemrograman</h3>  
        <p class="info">Membuat program sederhana</p>  
        <p class="info">Deadline: 10 September 2026</p>  
        <button onclick="bukaKirim('Pemrograman','Membuat program sederhana')">  
            📤 Kumpulkan  
        </button>  
    </div>  

    <div class="card">  
        <h3>📖 Bahasa Indonesia</h3>  
        <p class="info">Membuat teks laporan</p>  
        <p class="info">Deadline: 12 September 2026</p>  
        <button onclick="bukaKirim('Bahasa Indonesia','Membuat teks laporan')">  
            📤 Kumpulkan  
        </button>  
    </div>  

    <div class="card">  
        <h3>🧮 Matematika</h3>  
        <p class="info">Latihan soal aljabar</p>  
        <p class="info">Deadline: 15 September 2026</p>  
        <button onclick="bukaKirim('Matematika','Latihan soal aljabar')">  
            📤 Kumpulkan  
        </button>  
    </div>  

</div>  


<!-- KIRIM TUGAS -->  
<div id="submit" class="page">  

    <div class="card">  
        <h2>📤 Kirim Tugas</h2>  
        <p class="info">Isi data dengan lengkap.</p>  
    </div>  

    <div id="success" class="success">  
        ✅ Tugas berhasil dikirim!  
    </div>  

    <div class="card">  

        <label>Nama</label>  
        <input type="text" id="nama" placeholder="Masukkan nama">  

        <label>Kelas</label>  
        <input type="text" id="kelas" placeholder="Contoh: X PPLG 1">  

        <label>Mata Pelajaran</label>  
        <select id="mapel">  
            <option value="">-- Pilih Mapel --</option>  
            <option>Pemrograman</option>  
            <option>Bahasa Indonesia</option>  
            <option>Matematika</option>  
            <option>Bahasa Inggris</option>  
            <option>Informatika</option>  
        </select>  

        <label>Nama Tugas</label>  
        <input type="text" id="namaTugas" placeholder="Nama tugas">  

        <label>Pilih File</label>  
        <input type="file" id="file">  

        <label>Catatan</label>  
        <textarea id="catatan" placeholder="Tambahkan catatan..."></textarea>  

        <button onclick="kirimTugas()" style="width:100%;">  
            🚀 KIRIM TUGAS  
        </button>  

    </div>  

</div>  


<!-- TUGAS TERKIRIM -->  
<div id="submitted" class="page">  

    <div class="card">  
        <h2>📂 Tugas Terkirim</h2>  
        <p class="info">  
            Berikut adalah tugas yang sudah kamu kirim.  
        </p>  
    </div>  

    <div id="daftarTerkirim"></div>  

</div>  


<!-- DETAIL TUGAS -->  
<div id="detail" class="page">  

    <button class="back-btn" onclick="showPage('submitted')">  
        ← Kembali  
    </button>  

    <div id="detailTugas"></div>  

</div>

</div>  <!-- VIEWER FILE -->  <div class="viewer" id="viewer">  <div class="viewer-content">  

    <button class="close-viewer" onclick="tutupViewer()">  
        ✕  
    </button>  

    <div id="viewerContent"></div>  

</div>

</div>  <!-- NAVIGASI -->  <div class="bottom-nav">  <button class="nav-btn active" onclick="showPage('home', this)">  
    <span class="nav-icon">🏠</span>  
    Home  
</button>  

<button class="nav-btn" onclick="showPage('tasks', this)">  
    <span class="nav-icon">📋</span>  
    Tugas  
</button>  

<button class="nav-btn" onclick="showPage('submit', this)">  
    <span class="nav-icon">📤</span>  
    Kirim  
</button>  

<button class="nav-btn" onclick="showPage('submitted', this); tampilkanTugas()">  
    <span class="nav-icon">📂</span>  
    Terkirim  
</button>

</div>  <script>  
  
/* =========================  
   PINDAH HALAMAN  
========================= */  
  
function showPage(page, button) {  
  
    document.querySelectorAll(".page").forEach(function(p) {  
        p.classList.remove("active");  
    });  
  
    document.getElementById(page).classList.add("active");  
  
    if (button) {  
  
        document.querySelectorAll(".nav-btn").forEach(function(btn) {  
            btn.classList.remove("active");  
        });  
  
        button.classList.add("active");  
    }  
  
    if (page === "submitted") {  
        tampilkanTugas();  
    }  
  
    window.scrollTo(0, 0);  
}  
  
  
/* =========================  
   BUKA FORM DARI DAFTAR  
========================= */  
  
function bukaKirim(mapel, tugas) {  
  
    showPage("submit");  
  
    document.getElementById("mapel").value = mapel;  
    document.getElementById("namaTugas").value = tugas;  
}  
  
  
/* =========================  
   KIRIM TUGAS  
========================= */  
  
function kirimTugas() {  
  
    let nama = document.getElementById("nama").value.trim();  
    let kelas = document.getElementById("kelas").value.trim();  
    let mapel = document.getElementById("mapel").value;  
    let namaTugas = document.getElementById("namaTugas").value.trim();  
    let fileInput = document.getElementById("file");  
    let catatan = document.getElementById("catatan").value.trim();  
  
    if (!nama || !kelas || !mapel || !namaTugas || !fileInput.files.length) {  
  
        alert("⚠️ Lengkapi semua data dan pilih file terlebih dahulu!");  
  
        return;  
    }  
  
    let file = fileInput.files[0];  
  
    /*  
       Batas file 10 MB agar localStorage  
       tidak cepat penuh.  
    */  
  
    if (file.size > 10 * 1024 * 1024) {  
  
        alert("❌ Ukuran file maksimal 10 MB.");  
  
        return;  
    }  
  
    let reader = new FileReader();  
  
    reader.onload = function(e) {  
  
        let data = JSON.parse(  
            localStorage.getItem("tugasTerkirim") || "[]"  
        );  
  
        let tugas = {  
  
            id: Date.now(),  
  
            nama: nama,  
  
            kelas: kelas,  
  
            mapel: mapel,  
  
            namaTugas: namaTugas,  
  
            fileName: file.name,  
  
            fileType: file.type,  
  
            fileSize: file.size,  
  
            fileData: e.target.result,  
  
            catatan: catatan,  
  
            waktu: new Date().toLocaleString("id-ID")  
  
        };  
  
        data.push(tugas);  
  
        try {  
  
            localStorage.setItem(  
                "tugasTerkirim",  
                JSON.stringify(data)  
            );  
  
        } catch (error) {  
  
            alert(  
                "❌ Penyimpanan penuh. Coba gunakan file yang lebih kecil."  
            );  
  
            return;  
        }  
  
        document.getElementById("success").style.display = "block";  
  
        alert("✅ Tugas berhasil dikirim!");  
  
        document.getElementById("nama").value = "";  
        document.getElementById("kelas").value = "";  
        document.getElementById("mapel").value = "";  
        document.getElementById("namaTugas").value = "";  
        document.getElementById("file").value = "";  
        document.getElementById("catatan").value = "";  
  
        tampilkanTugas();  
  
        setTimeout(function() {  
  
            document.getElementById("success").style.display = "none";  
  
        }, 3000);  
    };  
  
    reader.readAsDataURL(file);  
}  
  
  
/* =========================  
   MENAMPILKAN TUGAS  
========================= */  
  
function tampilkanTugas() {  
  
    let container = document.getElementById("daftarTerkirim");  
  
    let data = JSON.parse(  
        localStorage.getItem("tugasTerkirim") || "[]"  
    );  
  
    if (data.length === 0) {  
  
        container.innerHTML = `  
            <div class="card empty">  
                <h3>📭 Belum ada tugas</h3>  
                <p style="margin-top:8px;">  
                    Tugas yang kamu kirim akan muncul di sini.  
                </p>  
            </div>  
        `;  
  
        return;  
    }  
  
    container.innerHTML = "";  
  
    data.slice().reverse().forEach(function(item) {  
  
        let card = document.createElement("div");  
  
        card.className = "card";  
  
        card.innerHTML = `  
  
            <h3>📚 ${escapeHTML(item.namaTugas)}</h3>  
  
            <p class="info">  
                📖 ${escapeHTML(item.mapel)}  
            </p>  
  
            <p class="info">  
                👤 ${escapeHTML(item.nama)}  
            </p>  
  
            <p class="info">  
                🏫 ${escapeHTML(item.kelas)}  
            </p>  
  
            <p class="info">  
                🕐 ${escapeHTML(item.waktu)}  
            </p>  
  
            <div class="file-box">  
                📎 ${escapeHTML(item.fileName)}  
            </div>  
  
            <button  
                class="btn-green"  
                onclick="lihatDetail(${item.id})">  
                👀 LIHAT TUGAS  
            </button>  
  
            <button  
                class="btn-danger"  
                onclick="hapusTugas(${item.id})"  
                style="margin-left:5px;">  
                🗑️ HAPUS  
            </button>  
        `;  
  
        container.appendChild(card);  
  
    });  
}  
  
  
/* =========================  
   DETAIL TUGAS  
========================= */  
  
function lihatDetail(id) {  
  
    let data = JSON.parse(  
        localStorage.getItem("tugasTerkirim") || "[]"  
    );  
  
    let item = data.find(function(t) {  
        return t.id === id;  
    });  
  
    if (!item) {  
  
        alert("Tugas tidak ditemukan.");  
  
        return;  
    }  
  
    let detail = document.getElementById("detailTugas");  
  
    detail.innerHTML = `  
  
        <div class="card">  
  
            <h2>📄 Detail Tugas</h2>  
  
            <br>  
  
            <p><b>Nama:</b></p>  
            <p class="info">${escapeHTML(item.nama)}</p>  
  
            <p><b>Kelas:</b></p>  
            <p class="info">${escapeHTML(item.kelas)}</p>  
  
            <p><b>Mata Pelajaran:</b></p>  
            <p class="info">${escapeHTML(item.mapel)}</p>  
  
            <p><b>Nama Tugas:</b></p>  
            <p class="info">${escapeHTML(item.namaTugas)}</p>  
  
            <p><b>Waktu Kirim:</b></p>  
            <p class="info">${escapeHTML(item.waktu)}</p>  
  
            <p><b>Catatan:</b></p>  
            <div class="file-box">  
                ${item.catatan  
                    ? escapeHTML(item.catatan)  
                    : "Tidak ada catatan."  
                }  
            </div>  
  
            <p><b>File:</b></p>  
  
            <div class="file-box">  
                📎 ${escapeHTML(item.fileName)}  
            </div>  
  
            <button  
                class="btn-green"  
                onclick="bukaFile(${item.id})"  
                style="width:100%;">  
                👀 LIHAT FILE  
            </button>  
  
        </div>  
    `;  
  
    showPage("detail");  
}  
  
  
/* =========================  
   BUKA FILE  
========================= */  
  
function bukaFile(id) {  
  
    let data = JSON.parse(  
        localStorage.getItem("tugasTerkirim") || "[]"  
    );  
  
    let item = data.find(function(t) {  
        return t.id === id;  
    });  
  
    if (!item || !item.fileData) {  
  
        alert("File tidak ditemukan.");  
  
        return;  
    }  
  
    let viewer = document.getElementById("viewer");  
  
    let content = document.getElementById("viewerContent");  
  
    let type = item.fileType || "";  
  
    /*  
       Jika gambar  
    */  
  
    if (type.startsWith("image/")) {  
  
        content.innerHTML = `  
            <img src="${item.fileData}" alt="File tugas">  
        `;  
  
    }  
  
    /*  
       Jika PDF  
    */  
  
    else if (type === "application/pdf") {  
  
        content.innerHTML = `  
            <iframe src="${item.fileData}"></iframe>  
        `;  
  
    }  
  
    /*  
       File lain  
    */  
  
    else {  
  
        content.innerHTML = `  
  
            <div style="  
                padding:30px;  
                text-align:center;  
            ">  
  
                <h2>📎 File Tugas</h2>  
  
                <p style="margin:15px 0;">  
                    ${escapeHTML(item.fileName)}  
                </p>  
  
                <p style="  
                    color:#666;  
                    margin-bottom:20px;  
                ">  
                    Format file ini tidak dapat ditampilkan  
                    langsung di aplikasi.  
                </p>  
  
                <a  
                    href="${item.fileData}"  
                    download="${escapeHTML(item.fileName)}"  
                    style="  
                        display:inline-block;  
                        background:#2563eb;  
                        color:white;  
                        padding:12px 18px;  
                        border-radius:10px;  
                        text-decoration:none;  
                        font-weight:bold;  
                    ">  
                    ⬇️ DOWNLOAD FILE  
                </a>  
  
            </div>  
        `;  
    }  
  
    viewer.style.display = "block";  
}  
  
  
/* =========================  
   TUTUP VIEWER  
========================= */  
  
function tutupViewer() {  
  
    document.getElementById("viewer").style.display = "none";  
  
    document.getElementById("viewerContent").innerHTML = "";  
}  
  
  
/* =========================  
   HAPUS TUGAS  
========================= */  
  
function hapusTugas(id) {  
  
    if (!confirm("Yakin ingin menghapus tugas ini?")) {  
        return;  
    }  
  
    let data = JSON.parse(  
        localStorage.getItem("tugasTerkirim") || "[]"  
    );  
  
    data = data.filter(function(item) {  
        return item.id !== id;  
    });  
  
    localStorage.setItem(  
        "tugasTerkirim",  
        JSON.stringify(data)  
    );  
  
    tampilkanTugas();  
  
    alert("🗑️ Tugas berhasil dihapus.");  
}  
  
  
/* =========================  
   MENCEGAH HTML INJECTION  
========================= */  
  
function escapeHTML(text) {  
  
    if (!text) return "";  
  
    return text  
        .replace(/&/g, "&amp;")  
        .replace(/</g, "&lt;")  
        .replace(/>/g, "&gt;")  
        .replace(/"/g, "&quot;")  
        .replace(/'/g, "&#039;");  
}  
  
</script>  </body>  
</html>