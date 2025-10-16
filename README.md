# PRAKTIKUM 4: CSS LAYOUT

# MEMBUAT BOX ELEMENT 

  Buat file baru dengan nama ```lab4_box.html```, lalu tambahkan code seperti ini pada VSCode


```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Box Element</title>
    <style>
        div {
            float:left;
            padding: 10px;  
        }
        .div1 {
            background: red;
        }
        .div2 {
            background: yellow;
        }
        .div3 {
            background: green;
        }
        .div4 {
            background: blue;
            clear: left;
            float: none;
        }
    </style>
</head>
<body>
    <header>
        <h1>Box Element</h1>
    </header>
    <section>
        <div class="div1">Div 1</div>
        <div class="div2">Div 2</div>
        <div class="div3">Div 3</div>
        <div class="div4">Div 4 (Clearfix)</div>
    </section>
</body>
</html>
```

    Berikut hasil pada browser 

<img width="1365" height="335" alt="Screenshot 2025-10-16 134148" src="https://github.com/user-attachments/assets/65c6e3db-3a6d-4681-9b3c-c6a2cea32365" />


# MEMBUAT LAYOUT SEDERHANA 

   Pada bagian ```<header>``` digunakan untuk menampilkan judul halaman. kemudian ```<nav>``` berisi menu navigasi agar pengguna dapat berpindah antarhalaman seperti home, artikel, abaout dan kontak. Lalu pada bagian ```<section id="hero">``` digunakan sebagai area tampilan pembuka atau benner utama yang berisi teks dan tombol. Selanjutnya ada area utama halaman ```<section id="wrapper">```, yang terdiri dari ```<main>``` sebagai tempat konten utama (berisi beberapa kotak dan artikel), serta ```<aside>``` yang berfungsi sebagai sidebar untuk menampilkan widget link dan teks tambahan. Dan di bagian bawah 
   Pada bagian ```<header>``` digunakan untuk menampilkan judul halaman. kemudian ```<nav>``` berisi menu navigasi agar pengguna dapat berpindah antarhalaman seperti home, artikel, abaout dan kontak. Lalu pada bagian ```<section id="hero">``` digunakan sebagai area tampilan pembuka atau benner utama yang berisi teks dan tombol. Selanjutnya ada area utama halaman ```<section id="wrapper">```, yang terdiri dari ```<main>``` sebagai tempat konten utama (berisi beberapa kotak dan artikel), serta ```<aside>``` yang berfungsi sebagai sidebar untuk menampilkan widget link dan teks tambahan. Dan di bagian bawah terdapat ```<footer>``` yang menampilkan informasi hak cipta website.
Seluruh elemen dibungkus dalam ```<div id="container">``` agar tata letaknya dapat diatur dengan mudah menggunakan CSS. 





```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Layout Sederhana</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="container">
        <header>
            <h1>Layout Sederhana</h1>
        </header>

        <nav>
            <a href="home.html" class="active">Home</a>
            <a href="artikel.html">Artikel</a>
            <a href="about.html">About</a>
            <a href="kontak.html">Kontak</a>
        </nav>

        <section id="hero">
            <h1>Hello World!</h1>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis.</p>
            <a href="home.html" class="btn btn-large">Learn more &raquo;</a>
        </section>

        <section id="wrapper">
            <section id="main">
                <div class="row">
                    <div class="box">
                        <img src="https://dummyimage.com/120/db7d25/fff.png" alt="" class="image-circle">
                        <h3>Heading</h3>
                        <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
                        <a href="#" class="btn btn-default">View detail</a>
                    </div>
                    <div class="box">
                        <img src="https://dummyimage.com/120/3e73e6/fff.png" alt="" class="image-circle">
                        <h3>Heading</h3>
                        <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
                        <a href="#" class="btn btn-default">View detail</a>
                    </div>
                    <div class="box">
                        <img src="https://dummyimage.com/120/71e6d4/fff.png" alt="" class="image-circle">
                        <h3>Heading</h3>
                        <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
                        <a href="#" class="btn btn-default">View detail</a>
                    </div>
                </div>

                <hr class="divider">

                <article class="entry">
                    <h2>First featurette heading.</h2>
                    <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="">
                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla.</p>
                </article>

                <hr class="divider">

                <article class="entry">
                    <h2>Second featurette heading.</h2>
                    <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="" class="right-img">
                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu.</p>
                </article>
            </section>

            <aside id="sidebar">
                <div class="widget-box">
                    <h3 class="title">Widget Header</h3>
                    <ul>
                        <li><a href="#">Widget Link</a></li>
                        <li><a href="#">Widget Link</a></li>
                        <li><a href="#">Widget Link</a></li>
                        <li><a href="#">Widget Link</a></li>
                        <li><a href="#">Widget Link</a></li>
                    </ul>
                </div>

                <div class="widget-box">
                    <h3 class="title">Widget Text</h3>
                    <p>Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla.</p>
                </div>
            </aside>
        </section>

        <footer>
            <p>&copy; 2021 - Universitas Pelita Bangsa</p>
        </footer>
    </div>
</body>
</html>
```


# CSS STYLE 

  File style.css ini berfungsi untuk mengatur tampilan dari halaman web layout sederhana agar terlihat rapi, seimbang, dan menarik. Pada bagian awal digunakan @import untuk mengambil font dari Google Fonts yaitu Open Sans dan Open Sans Condensed, agar tulisan terlihat lebih modern. Kemudian terdapat reset CSS menggunakan tanda * untuk menghilangkan margin dan padding bawaan browser, supaya setiap elemen memiliki tampilan yang seragam.




  
```
/* import google font */ 
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400;0,600;0,700;0,800;1,300;1,400;1,600;1,700;1,800&display=swap'); 
@import url('https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:ital,wght@0,300;0,700;1,300&display=swap'); 

/* Reset CSS */ 
* { 
    margin: 0; 
    padding: 0; 
} 

body { 
    line-height:1; 
    font-size:100%; 
    font-family:'Open Sans', sans-serif; 
    color:#5a5a5a; 
} 

#container { 
    width: 980px; 
    margin: 0 auto; 
    box-shadow: 0 0 1em #cccccc; 
} 

/* header */ 
header { 
    padding: 20px; 
} 

header h1 { 
    margin: 20px 10px; 
    color: #b5b5b5; 
} 

/* navigasi */ 
nav { 
    display: block; 
    background-color: #1f5faa; 
} 

nav a { 
    padding: 15px 30px; 
    display: inline-block; 
    color: #ffffff; 
    font-size: 14px; 
    text-decoration: none; 
    font-weight: bold; 
} 

nav a.active, 
nav a:hover { 
    background-color: #2b83ea; 
} 

/* Hero Panel */ 
#hero { 
    background-color: #e4e4e5; 
    padding: 50px 20px; 
    margin-bottom: 20px; 
} 

#hero h1 { 
    margin-bottom: 20px; 
    font-size: 35px; 
} 

#hero p { 
    margin-bottom: 20px; 
    font-size: 18px; 
    line-height: 25px; 
} 

/* main content */ 
#wrapper { 
    margin: 0; 
} 

#main { 
    float: left; 
    width: 640px; 
    padding: 20px; 
} 

/* sidebar area */ 
#sidebar { 
    float: left; 
    width: 260px; 
    padding: 20px; 
} 

/* widget */ 
.widget-box { 
    border:1px solid #eee; 
    margin-bottom:20px; 
} 

.widget-box  .title { 
    padding:10px 16px; 
    background-color:#428bca; 
    color:#fff; 
} 

.widget-box ul { 
    list-style-type:none; 
} 

.widget-box li { 
    border-bottom:1px solid #eee; 
} 

.widget-box li a { 
    padding:10px 16px; 
    color:#333; 
    display:block; 
    text-decoration:none; 
} 

.widget-box li:hover a { 
    background-color:#eee; 
} 

.widget-box p { 
    padding:15px; 
    line-height:25px; 
} 

/* footer */ 
footer { 
    clear:both; 
    background-color:#1d1d1d; 
    padding:20px; 
    color:#eee; 
} 

/* box */ 
.box { 
    display:block; 
    float:left; 
    width:33.333333%; 
    box-sizing:border-box; 
    -moz-box-sizing:border-box; 
    -webkit-box-sizing:border-box; 
    padding:0 10px; 
    text-align:center; 
} 

.box h3 { 
    margin: 15px 0; 
} 

.box p { 
    line-height: 20px; 
    font-size: 14px; 
    margin-bottom: 15px; 
} 

box img { 
    border: 0; 
    vertical-align: middle; 
} 

.image-circle { 
    border-radius: 50%; 
} 

.row { 
    margin: 0 -10px; 
    box-sizing: border-box; 
    -moz-box-sizing: border-box; 
    -webkit-box-sizing: border-box; 
} 

.row:after, .row:before, 
.entry:after, .entry:before { 
    content:''; 
    display:table; 
} 

.row:after, 
.entry:after { 
    clear:both; 
} 

.divider { 
    border:0; 
    border-top:1px solid #eeeeee; 
    margin:40px 0; 
} 

/* entry */ 
.entry { 
    margin: 15px 0; 
} 

.entry h2 { 
    margin-bottom: 20px; 
} 

.entry p { 
    line-height: 25px; 
} 

.entry img { 
    float: left; 
    border-radius: 5px; 
    margin-right: 15px; 
} 

.entry .right-img { 
    float: right; 
}
```


    Berikut hasil nya pada browser 

<img width="711" height="609" alt="Screenshot 2025-10-16 213509" src="https://github.com/user-attachments/assets/2bb9bf14-de53-4056-afa5-2c05dfcb0df4" />



# MEMBUAT TAMPILAN ABOUT

  Code ini merupakan halaman About atau Tentang Kami dari website layout sederhana. Halaman ini menggunakan struktur HTML5 dengan bantuan CSS untuk mengatur tampilannya. Bagian atas halaman menggunakan elemen ```<header>``` yang menampilkan judul “Tentang Kami”. Di bawahnya terdapat ```<nav>``` sebagai menu navigasi agar pengguna dapat berpindah antarhalaman seperti Home, About, Artikel, dan Kontak. Tautan About diberi kelas active sehingga tampil dengan warna berbeda sebagai tanda bahwa halaman ini sedang dibuka.





```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tentang Kami</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="container">
        <header>
            <h1>Tentang Kami</h1>
        </header>

        <nav>
            <a href="home.html">Home</a>
            <a href="about.html" class="active">About</a>
            <a href="artikel.html">Artikel</a>
            <a href="kontak.html">Kontak</a>
        </nav>

        <section id="main">
            <h2>Deskripsi</h2>
            <p>Website ini dibuat sebagai latihan dasar layout menggunakan HTML5 dan CSS Float.</p>

            <h2>Portfolio</h2>
            <ul>
                <li>Project 1 - Desain Web</li>
                <li>Project 2 - Sistem Informasi Penjualan</li>
                <li>Project 3 - Aplikasi kalkulator</li>
            </ul>
        </section>

        <footer>
            <p>&copy; 2025 - Universitas Pelita Bangsa</p>
        </footer>
    </div>
</body>
</html>
```

   Berikut hasil pada browser

<img width="1354" height="689" alt="Screenshot 2025-10-16 214041" src="https://github.com/user-attachments/assets/c89c3042-313a-4f1d-8fee-a01e8988f47f" />


# MEMBUAT TAMPILAN ARTIKEL 

   Bagian utama halaman ditempatkan di dalam ```<section id="wrapper">``` yang terbagi menjadi dua bagian, yaitu ```<section id="main">``` untuk konten utama dan ```<aside id="sidebar">``` untuk area samping. Pada bagian utama (#main), terdapat dua artikel yang masing-masing elemen <article> dan diberi kelas entry. Artikel pertama berjudul “Judul Artikel Pertama” yang berisi gambar di sebelah kiri serta teks penjelasan. Artikel ini menggunakan elemen ```<article>``` yang merupakan bagian dari elemen semantik HTML5 untuk menandai isi konten utama. Setelah itu terdapat garis pemisah ``<hr class="divider">``` untuk memisahkan antarartikel. Artikel kedua berjudul “Judul Artikel Kedua” dengan gambar di sisi kanan dan teks di sebelah kiri. Penempatan gambar diatur menggunakan kelas CSS right-img agar posisinya sejajar di sisi kanan.





```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Artikel</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div id="container">
    <header>
      <h1>Layout Sederhana</h1>
    </header>

    <nav>
      <a href="home.html">Home</a>
      <a href="artikel.html" class="active">Artikel</a>
      <a href="about.html">About</a>
      <a href="kontak.html">Kontak</a>
    </nav>

    <section id="wrapper">
      <section id="main">
        <article class="entry">
          <h2>Judul Artikel Pertama</h2>
          <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="">
          <p>
            Ini adalah contoh artikel pertama. Kamu bisa menuliskan isi artikel atau berita di sini.
            Artikel ini menggunakan elemen <code>&lt;article&gt;</code> yang termasuk bagian dari HTML5 semantic element.
          </p>
        </article>

        <hr class="divider">

        <article class="entry">
          <h2>Judul Artikel Kedua</h2>
          <img src="https://dummyimage.com/150/3e73e6/fff.png" alt="" class="right-img">
          <p>
            Ini adalah contoh artikel kedua. Kamu bisa menambahkan gambar dan teks sesuai kebutuhan.
            Gambar bisa berada di kiri atau kanan sesuai kelas CSS yang digunakan.
          </p>
        </article>
      </section>

      <aside id="sidebar">
        <div class="widget-box">
          <h3 class="title">Artikel Lain</h3>
          <ul>
            <li><a href="#">Tips Desain Web</a></li>
            <li><a href="#">Belajar CSS Layout</a></li>
            <li><a href="#">Responsive Design</a></li>
          </ul>
        </div>
      </aside>
    </section>

    <footer>
      <p>&copy; 2025 - Universitas Pelita Bangsa</p>
    </footer>
  </div>
</body>
</html>
```

   Berikut hasil pada browser

<img width="1299" height="717" alt="Screenshot 2025-10-16 214857" src="https://github.com/user-attachments/assets/88e3fdf4-334d-4198-bbdc-0460d04040dc" />


# MEMBUAT TAMPILAN KONTAK 

  Bagian utama halaman berada di dalam elemen ```<section id="main">```. Di dalamnya terdapat subjudul “Hubungi Kami” dan sebuah formulir kontak yang dibuat menggunakan tag ```<form>```. Formulir ini terdiri dari beberapa elemen input, yaitu:
* Kolom Nama untuk mengisi nama pengirim menggunakan ```<input type="text">```.
* Kolom Email untuk menuliskan alamat email dengan ```<input type="email">```.
* Kolom Pesan untuk menulis isi pesan menggunakan <textarea>.

Sebuah tombol Kirim dengan tag ```<button type="submit">``` yang berfungsi untuk mengirimkan data formulir. Setiap bagian input disusun secara berurutan dan diberi jarak agar tampak rapi serta mudah diisi oleh pengguna. Semua elemen ini ditempatkan dalam ```<section id="main">``` agar posisinya sesuai dengan layout utama yang diatur melalui CSS.





```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kontak Kami</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="container">
        <header>
            <h1>Kontak Kami</h1>
        </header>

        <nav>
            <a href="home.html">Home</a>
            <a href="artikel.html">Artikel</a>
            <a href="about.html">About</a>
            <a href="kontak.html" class="active">Kontak</a>
        </nav>

        <section id="main">
            <h2>Hubungi Kami</h2>
            <form>
                <label>Nama:</label><br>
                <input type="text" name="nama" placeholder="Masukkan nama"><br><br>

                <label>Email:</label><br>
                <input type="email" name="email" placeholder="Masukkan email"><br><br>

                <label>Pesan:</label><br>
                <textarea name="pesan" rows="5" placeholder="Tulis pesan Anda..."></textarea><br><br>

                <button type="submit">Kirim</button>
            </form>
        </section>

        <footer>
            <p>&copy; 2025 - Universitas Pelita Bangsa</p>
        </footer>
    </div>
</body>
</html>
```


    Berikut hasil pada browser

<img width="1302" height="685" alt="Screenshot 2025-10-16 215725" src="https://github.com/user-attachments/assets/12b30c7d-765d-45b8-a5b8-a923c4438a5c" />


# PERTANYAAN DAN TUGAS  

JAWABAN 1. 





```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tentang Kami</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="container">
        <header>
            <h1>Tentang Saya</h1>
        </header>

        <nav>
            <a href="home.html">Home</a>
            <a href="about.html" class="active">About</a>
            <a href="artikel.html">Artikel</a>
            <a href="kontak.html">Kontak</a>
        </nav>

        <section id="main">
            <h2>Deskripsi</h2>
            <p>Hai perkenalkan nama saya Adinda Aulia Nabila Putri, saya mahasiswi Universitas Pelita Bangsa fakultas teknik program studi teknik informatika.</p>

            <h2>Hobi saya</h2>
            <ul>
                <li>Menonton film</li>
                <li>Mendengarkan musik</li>
            </ul>
        </section>

        <footer>
            <p>&copy; 2025 - Universitas Pelita Bangsa</p>
        </footer>
    </div>
</body>
</html>
```


   Berikut hasil pada browser 

<img width="1082" height="483" alt="Screenshot 2025-10-16 220109" src="https://github.com/user-attachments/assets/ce3f2281-2974-40d1-84e6-ec8843a11dfb" />


JAWABAN 2 





```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kontak Kami</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="container">
        <header>
            <h1>Kontak Saya dibawah ini</h1>
        </header>

        <nav>
            <a href="home.html">Home</a>
            <a href="artikel.html">Artikel</a>
            <a href="about.html">About</a>
            <a href="kontak.html" class="active">Kontak</a>
        </nav>

        <section id="main">
            <h2>Formulir Kontak</h2>
            <form>
                <label>Nama:</label><br>
                <input type="text" name="nama" placeholder="Masukkan nama"><br><br>

                <label>Email:</label><br>
                <input type="email" name="email" placeholder="Masukkan email"><br><br>

                <label>Pesan:</label><br>
                <textarea name="pesan" rows="5" placeholder="Tulis pesan Anda..."></textarea><br><br>

                <button type="submit">Kirim</button>
            </form>
        </section>

        <footer>
            <p>&copy; 2025 - Universitas Pelita Bangsa</p>
        </footer>
    </div>
</body>
</html>
```

  Berikut hasil pada browser 

<img width="1032" height="599" alt="Screenshot 2025-10-16 220603" src="https://github.com/user-attachments/assets/9c4a7f48-f0bb-4705-8e14-c94bf8441034" />

