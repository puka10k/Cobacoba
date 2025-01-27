<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Fade Transition Pages</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background-color: #f5f5f5;
      overflow-y: auto;
      background-attachment: fixed;
      backgrooun-size: cover;
    }
    .page {
      position: absolute;
      width: 100%;
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background: linear-gradient(to bottom right, #000000, #ffc0cb);
      opacity: 0;
      transition: opacity 1s ease-in-out;
      color: white;
      text-align: center;
    }
    .page.active {
      opacity: 1;
      z-index: 1;
    }
    .hidden {
      display: none;
    }
    button {
      margin-top: 20px;
      padding: 10px 20px;
      font-size: 16px;
      cursor: pointer;
      background-color: #2575fc;
      color: white;
      border: none;
      border-radius: 5px;
      transition: background-color 0.3s;
    }
    button:hover {
      background-color: #1a5bb8;
    }
    input {
      padding: 10px;
      font-size: 16px;
      border: 1px solid #ccc;
      border-radius: 5px;
      width: 80%;
      max-width: 300px;
    }
    p {
    text-shadow: 
      -1px -1px 0 #000, /* Outline hitam */
      1px -1px 0 #000,
      -1px 1px 0 #000,
      1px 1px 0 #000;
      
    }
  </style>
</head>
<body>
  <!-- Halaman Input Kode -->
  <div id="inputPage" class="page active">
    <div>
      <p>Masukkan kode untuk membuka halaman:</p>
      <input type="password" id="codeInput" placeholder="Masukkan kode" />
      <button onclick="checkCode()">Submit</button>
      <p id="error" style="color: red; display: none;">Kode salah!</p>
    </div>
  </div>

  <!-- Halaman 1 -->
  <div id="page1" class="page hidden">
    <div>
      <h2> </h1>
      <p> haii...<p>
      <button onclick="goToNextPage('page2')">Selanjutnya</button>
    </div>
  </div>

  <!-- Halaman 2 -->
  <div id="page2" class="page hidden">
    <div>
      <h2></h1>
      <p>Gimana kabarnya? Pasti kamu baik baik aja kan. Kmu emng bisa tanpa aku ya. Ga kaya aku hehe <p>
      <button onclick="goToNextPage('page3')">Selanjutnya</button>
      <button onclick="goToNextPage('page1')">kembali</button>
    </div>
  </div>

  <!-- Halaman 3 -->
  <div id="page3" class="page hidden">
    <div>
      <h1> </h1>
      <p> Aku mau minta maaf sama kamu. Kemaren emng lagi ga tepat aja waktu berantemya. Aku lagi cape karna kerjaan, Kmu juga cape karna tugas kuliah. Sama sama gede egonya, sama sama gabisa ngertiin satu sama lain.Allhasil jadi asing lagi<p>
      <button onclick="goToNextPage('page4')">Selanjutnya</button>
<button onclick="goToNextPage('page2')">kembali</button>
    </div>
  </div>
  

  <!-- Halaman 1 -->
  <div id="page4" class="page hidden">
    <div>
      <h2> </h1>
      <p> disaat aku mikirin kamu, tetep jaga hati buat kamu. Berharap bisa jadi rumah kamu. Nyatanya tempat kmu pulang bukan aku<p>
      <button onclick="goToNextPage('page5')">Selanjutnya</button>
      <button onclick="goToNextPage('page3')">kembali</button>
    </div>
  </div>

  <!-- Halaman 2 -->
  <div id="page5" class="page hidden">
    <div>
      <h2></h1>
      <p>Yah Lagi pula dari dulu emng aku gapernah ngerasa bisa menang dari dia. Bahkan kebnyakan sebab kita berantem tuh pasti karna  dia. Tapi aku gabisa nyalahin dia juga. Karna mungkin ada sesuatu yang kamu cari ada di dia, yang gada di diri aku. Selama ini aku bareng kmu. mungkin aku punya raga kamu, tapi aku ga punya hati kamu. Kaya lagu aja ya.. Hha <p>
      <button onclick="goToNextPage('page6')">Selanjutnya</button>
      <button onclick="goToNextPage('page4')">kembali</button>
    </div>
  </div>

  <!-- Halaman 3 -->
  <div id="page6" class="page hidden">
    <div>
      <h1> </h1>
      <p> Mungkin akunya aja yang terlalu terobsesi sama kamu. Sampe aku ga sadar klo selama ini yang kmu mau tuh bukan aku<p>
<button onclick="goToNextPage('page7')">Selanjutnya</button>
      <button onclick="goToNextPage('page5')">kembali</button>
    </div>
  </div>
  
  
<div id="page7" class="page hidden">
    <div>
      <h2>.</h1>
      <p>Bisa bisanya aku percaya  klo kmu bisa nglepas dia dari hidup kamu. Bahkan bodohnya aku. Entah berapa kali aku percaya sama hal itu, pada akhirnya. kamu emang gabisa lepasin dia sampai kapanpun<p>
      <button onclick="goToNextPage('page8')">Selanjutnya</button>
      <button onclick="goToNextPage('page6')">kembali</button>
    </div>
  </div>

  <!-- Halaman 3 -->
  <div id="page8" class="page hidden">
    <div>
      <h1> </h1>
      <p> Sekarang aku tau. aku bukan tempat buat kamu pulang. Maaf aku gabisa bisa bikin kamu bahagia dan ngerasa nyaman layaknya rumah.  Dia emng lebih pantes bareng kamu dari pada aku<p>
      <button onclick="goToNextPage('page9')">Selanjutnya</button>
<button onclick="goToNextPage('page7')">kembali</button>
    </div>
  </div>
  

  <!-- Halaman 1 -->
  <div id="page9" class="page hidden">
    <div>
      <h2> </h1>
      <p> tapi Aku juga sadar klo aku tuh ga jelek jelek amat. Masih ada cewe yang mau sama aku. Mungkin diluar sana masih ada cewe yang nerima sifat manja aku. Yang ga bilang aku alay, yang gabilang aku lebay, yang ga bilang aku miskin, yang bisa nurut sama perkataan aku. Dan Yang terpenting bisa ngejaga perasaan aku. Selama ini aku terlalu bodoh buat cinta sama cewe yang bahkan bukan aku cowo yang cewe itu mau<p>
      <button onclick="goToNextPage('page10')">Selanjutnya</button>
      <button onclick="goToNextPage('page8')">kembali</button>
    </div>
  </div>

  <!-- Halaman 2 -->
  <div id="page10" class="page hidden">
    <div>
      <h2></h1>
      <p> Kamu cantik, Lucu, gemesin, wajar aja kmu bisa tanpa aku. sampsi saat ini hati aku masih sepenuhnya terisi sama kamu. Tapi aku percaya. Waktu bisa nuntun aku buat lepasin kamu<p>
      <button onclick="goToNextPage('page11')">Selanjutnya</button>
      <button onclick="goToNextPage('page9')">kembali</button>
    </div>
  </div>
  
<div id="page11" class="page hidden">
    <div>
      <h2></h1>
      <p>Aku maafin semua yang kamu pernah lakuin. Aku juga minta maaf buat semua yang pernah aku lakuin. Makasih ya buat waktunya. jaga diri kamu ya, jangan sampe ketemu sama cowo kaya aku lagi<p>
      <button onclick="goToNextPage('page12')">Selanjutnya</button>
      <button onclick="goToNextPage('page10')">kembali</button>
    </div>
  </div>

  <!-- Halaman 3 -->
  <div id="page12" class="page hidden">
    <div>
      <h1></h1>
      <p> semoga suatu saat kita bisa ketemu lagi<p>
      <button onclick="goToNextPage('page11')">kembali</button>
    </div>
  </div>
  

  <!-- Halaman 1 
  <div id="page4" class="page hidden">
    <div>
      <h2> .</h1>
      <p> <p>
      <button onclick="goToNextPage('page5')">Selanjutnya</button>
      <button onclick="goToNextPage('page3')">kembali</button>
    </div>
  </div>

  <!-- Halaman 2 
  <div id="page5" class="page hidden">
    <div>
      <h2>.</h1>
      <p> <p>
      <button onclick="goToNextPage('page6')">Selanjutnya</button>
      <button onclick="goToNextPage('page4')">kembali</button>
    </div>
  </div>-->


  <script>
    function checkCode() {
      const code = document.getElementById('codeInput').value;
      const error = document.getElementById('error');
      if (code === 'asu') {
        showPage('page1');
        hidePage('inputPage');
      } else {
        error.style.display = 'block';
      }
    }

    function showPage(pageId) {
      const page = document.getElementById(pageId);
      page.classList.add('active');
      page.classList.remove('hidden');
    }

    function hidePage(pageId) {
      const page = document.getElementById(pageId);
      page.classList.remove('active');
      setTimeout(() => {
        page.classList.add('hidden');
      }, 1000);
    }

    function showPage(pageId) {
      const activePage = document.querySelector('.page.active');
      const nextPage = document.getElementById(pageId);

      if (activePage) {
        // Hilangkan halaman aktif dengan efek memudar
        activePage.classList.remove('active');
        setTimeout(() => {
          activePage.classList.add('hidden');
        }, 1000); // Sesuai durasi transisi
      }

      // Tampilkan halaman berikutnya
      nextPage.classList.remove('hidden');
      setTimeout(() => {
        nextPage.classList.add('active');
      }, 10); // Sedikit jeda untuk transisi
    }

    function goToNextPage(nextPageId) {
      showPage(nextPageId);
    }
  </script>
</body>
</html>
