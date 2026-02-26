# mie_legend
mie nya enak kali lee\
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <title>Mie Legend</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            animation: rgbBackground 10s infinite alternate;
            transition: background 1s linear;
        }

        /* ANIMASI RGB */
        @keyframes rgbBackground {
            0%   { background: rgb(255, 99, 71); }
            25%  { background: rgb(255, 0, 255); }
            50%  { background: rgb(0, 191, 255); }
            75%  { background: rgb(0, 255, 127); }
            100% { background: rgb(255, 165, 0); }
        }

        #intro {
            position: fixed;
            width: 100%;
            height: 100vh;
            background: black;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            color: white;
            z-index: 9999;
        }

        #intro button {
            padding: 15px 30px;
            font-size: 18px;
            border: none;
            border-radius: 8px;
            background: white;
            color: red;
            cursor: pointer;
        }

        header {
            background-color: rgba(0,0,0,0.6);
            color: white;
            text-align: center;
            padding: 30px;
        }

        header img {
            width: 200px;
            border-radius: 10px;
            margin-top: 10px;
        }

        section {
            padding: 40px;
            text-align: center;
        }

        table {
            width: 80%;
            margin: auto;
            border-collapse: collapse;
            background-color: rgba(255,255,255,0.9);
        }

        th, td {
            border: 1px solid #ddd;
            padding: 12px;
            text-align: center;
        }

        th {
            background-color: #2500ad;
            color: white;
        }

        table img {
            width: 100px;
            border-radius: 8px;
        }

        .link-btn {
            display: inline-block;
            margin-top: 20px;
            padding: 10px 20px;
            background-color: red;
            color: white;
            text-decoration: none;
            border-radius: 5px;
        }

        footer {
            background-color: rgba(0,0,0,0.7);
            color: white;
            text-align: center;
            padding: 15px;
            margin-top: 40px;
        }
    </style>
</head>
<body>

<audio id="bgm"></audio>

<div id="intro">
    <h1>🍜 Mie Legend</h1>
    <button onclick="masukWebsite()">🎵 Klik Untuk Masuk</button>
</div>

<header>
    <h1>Mie Legend</h1>
    <p>Pusat Kuliner Favorit Anda ala ala kelapa gading ayak ding</p>
    <img src="bener jual mie.jpg">
</header>

<section>
    <h2>Daftar Menu</h2>

    <table>
        <tr>
            <th>Nama Menu</th>
            <th>Harga</th>
            <th>Gambar</th>
        </tr>
        <tr>
            <td>Mie Goreng Polos</td>
            <td>Rp 10.000</td>
            <td><img src="mie goreng polos.jpg"></td>
        </tr>
        <tr>
            <td>Mie Kuah</td>
            <td>Rp 10.000</td>
            <td><img src="mie kuah.jpg"></td>
        </tr>
        <tr>
            <td>Mie Goreng Telur</td>
            <td>Rp 15.000</td>
            <td><img src="telur.jpg"></td>
        </tr>
        <tr>
            <td>Mie Goreng Spesial</td>
            <td>Rp 25.000</td>
            <td><img src="mie sepesial.jpg"></td>
        </tr>
        <tr>
            <td>Mie Bihun</td>
            <td>Rp 15.000</td>
            <td><img src="bihun.webp"></td>
        </tr>
        <tr>
            <td>Mie Kwetiau</td>
            <td>Rp 18.000</td>
            <td><img src="kuetiau.jpg"></td>
        </tr>
    </table>

    <a href="https://www.instagram.com/ugaaa_gaaaa?igsh=ZmQ3b2Z4bHd0aG50" target="_blank" class="link-btn">
        Kunjungi Foodcourt
    </a>
</section>

<footer>
    <p>&copy; 2029 yoga pratama</p>
</footer>

<script>
    const playlist = [
        "https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3",
        "https://www.soundhelix.com/examples/mp3/SoundHelix-Song-2.mp3",
        "https://www.soundhelix.com/examples/mp3/SoundHelix-Song-3.mp3"
    ];

    let currentSong = 0;
    const music = document.getElementById("bgm");

    function playMusic() {
        music.src = playlist[currentSong];
        music.play();
    }

    music.addEventListener("ended", function() {
        currentSong++;
        if (currentSong >= playlist.length) {
            currentSong = 0;
        }
        playMusic();
    });

    function masukWebsite() {
        playMusic();
        document.getElementById("intro").style.display = "none";
    }
</script>

</body>
</html>
