<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <title>Form Pendaftaran Wisata</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f8fb;
            margin: 20px;
        }
        h1 {
            text-align: center;
            color: #2c3e50;
        }
        form {
            max-width: 700px;
            margin: auto;
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        label {
            font-weight: bold;
        }
        input, select {
            width: 100%;
            padding: 8px;
            margin: 8px 0 15px 0;
            border-radius: 5px;
            border: 1px solid #ccc;
        }
        .inline {
            width: auto;
        }
        button {
            background-color: #3498db;
            color: white;
            padding: 10px;
            border: none;
            width: 100%;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #2980b9;
        }
    </style>
</head>
<body>

<h1>Form Pendaftaran Paket Wisata</h1>

<form action="#" method="post" enctype="multipart/form-data">

    <!-- Hidden ID -->
    <input type="hidden" name="id_partner" value="PARTNER12345">

    <h3>Data Keamanan</h3>
    <label>PIN 6 Digit:</label>
    <input type="password" name="pin" pattern="[0-9]{6}" placeholder="Masukkan 6 digit PIN" required>

    <h3>Lokasi Penjemputan</h3>
    <label>Pilih Lokasi:</label>
    <select name="lokasi" required>
        <option value="">-- Pilih Provinsi - Kota - Meeting Point --</option>
        <option>Jawa Barat - Bandung - Gedung Sate</option>
        <option>DKI Jakarta - Jakarta - Monas</option>
        <option>Jawa Tengah - Yogyakarta - Malioboro</option>
        <option>Bali - Denpasar - Bandara Ngurah Rai</option>
    </select>

    <h3>Detail Keberangkatan</h3>

    <label>Cari Destinasi:</label>
    <input type="search" name="destinasi" placeholder="Contoh: Labuan Bajo">

    <label>Tanggal Keberangkatan:</label>
    <input type="date" name="tanggal" required>

    <label>Jam Kumpul:</label>
    <input type="time" name="jam" required>

    <label>Jumlah Peserta (1-20 orang):</label>
    <input type="number" name="peserta" min="1" max="20" required>

    <h3>Preferensi Personal</h3>

    <label>Link Media Sosial:</label>
    <input type="url" name="sosial" placeholder="https://instagram.com/username">

    <label>Warna Kaos Grup:</label>
    <input type="color" name="warna">

    <h3>Opsi Tambahan</h3>

    <label>Metode Pembayaran:</label><br>
    <input type="radio" name="pembayaran" value="full" class="inline" required> Full Payment<br>
    <input type="radio" name="pembayaran" value="dp" class="inline"> DP 50%<br><br>

    <label>Fasilitas Ekstra:</label><br>
    <input type="checkbox" name="fasilitas[]" value="asuransi" class="inline"> Asuransi Perjalanan<br>
    <input type="checkbox" name="fasilitas[]" value="kamera" class="inline"> Sewa Kamera<br>
    <input type="checkbox" name="fasilitas[]" value="dinner" class="inline"> Dinner Romantis<br><br>

    <h3>Legalitas</h3>

    <label>Upload KTP/Paspor:</label>
    <input type="file" name="dokumen" accept=".jpg,.png,.pdf" required>

    <button type="submit">Daftar Sekarang</button>

</form>

</body>
</html>
