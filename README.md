<html><meta charset='UTF-8'/><meta content='width=device-width, initial-scale=1, user-scalable=1, minimum-scale=1, maximum-scale=5' name='viewport'/><meta content='IE=edge' http-equiv='X-UA-Compatible'/>
  
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Work+Sans:wght@400;700&display=swap" rel="stylesheet">
  
  <script src="https://cdn.jsdelivr.net/npm/sweetalert2@11.0.19/dist/sweetalert2.all.min.js"></script><link href="https://feeldreams.github.io/liatnih/style.css" rel="stylesheet" type="text/css" />
  <script src="https://unpkg.com/typeit@8.6.6/dist/index.umd.js"></script><script src="https://feeldreams.github.io/liatnih/script.js"></script>
  <script src="https://kit.fontawesome.com/4f3ce16e3e.js" crossorigin="anonymous"></script>

<head>
<title>Script HTML Untukmu</title>
<!-- 
  Made with love by Rayys!
     Blog: https://PalingIT.com
     Instagram: @rayyarrr
     TikTok: @rayy4r
     Email: rayyar0703@gmail.com
  Thanks to all <3
-->
</head>
<body>
	
   <!-- Ganti Audio di sini -->
   <audio src="https://feeldreams.github.io/anotherme.mp3" id="linkmp3" class="sembunyi"></audio>
   
   <div id="bodyblur">
     <!-- Wallpaper --><img src="https://feeldreams.github.io/nordic.jpeg" id="wallpaper"/>
   </div>
   
   <div id='Content'>

     <div id="suratin" onClick="memulai();">
       <!-- Tombol Surat --><img src="https://rayyscoding.github.io/envelope.png"/>
     </div>
     <p id="ket">Klik Suratnya!</p>

     <div class="kumpulanstiker">
         <!-- Stiker untuk Konten -->
         <img src="https://feeldreams.github.io/bwa2.gif" id="fotoakhir"/>
         <img src="https://feeldreams.github.io/bunga.gif" id="fotoakhir2"/>
         <img src="https://feeldreams.github.io/peachkiss.gif" id="fotoakhir3"/>
         <img src="https://feeldreams.github.io/peachhug.gif" id="fotoakhir4"/>
     </div>
     
     <div><blockquote id='bq'>

       <!-- Konten Pembukaan -->
       <p id="kalimat">Hai, </p>
       <p id="kalimatb">Aku cuma mau bilang nih,</p>
       <p id="kalimatb2">Good Morning, <b id="namakamu"></b>! Jangan lupa mandi, sarapan, dan semangat jalani harinya <3</p>
       <p id="kalimatc">Gaboleh nyerah kalau ada masalah yaa.. 😍❤️</p>

       <!-- Konten Pilihan Kado -->
       <p id="kalimatd">Oh iya, coba pilih <b>kado</b> di bawah ini! 😆❤️</p>
       <div id="kolombaru">
         <li><img src="https://feeldreams.github.io/kadoin.png" onClick="rnkado = 1;otomatis();"/></li>
         <li><img src="https://feeldreams.github.io/kadoin.png" onClick="rnkado = 2;otomatis();"/></li>
         <li><img src="https://feeldreams.github.io/kadoin.png" onClick="rnkado = 3;otomatis();"/></li>
       </div>
       
       <!-- Konten Isi Kado -->
       <p id="kado1">Selamat pagi! Maafin aku ya kalau sebelumnya udah bikin kamu marah, Aku Sayang Kamu 😍❤️</p>
       <p id="kado2">Selamat pagi, <b id="namakamu2"></b>! Matahari boleh bersinar terik, tapi hanya <b id="namakamu3"></b> yang paling menarik 😆❤️</p>
       <p id="kado3">Selamat pagi! Jangan lupa bahagia terus ya.. Aku di sini sangat menyayangimu 😍❤️</p>
       
     </blockquote></div>

     <!-- Tombol Multifungsi -->
     <div id="Tombol">
       <a id="By" onClick="multifungsi()">
         <b id="tmbl">Lanjut</b>
       </a>
     </div>
     
     <!-- Pesan yang dikirim ke WhatsApp -->
     <span id="pesanWA" class="sembunyi">Awww, Good Morning too!</span>
	 
     <!-- Nomor WhatsApp Kamu -->
     <!-- Biarkan 628 jika Tak Perlu -->
     <span id="nomorWA">628</span>
     
   </div>

<!-- Jangan Edit Bagian Ini --><script>
  ftom=0;ftganti=0;flag=1;flagg=1;fungsi=0;fungsiAwal=0;pesanwhatsapp = pesanWA.innerHTML;Content.style = "opacity:1;margin-top:16vh;";
  
  function memulai(){if(fungsiAwal==0){audio.play();fungsiAwal=1;suratin.style="transition:all .8s ease;transform:scale(10);opacity:0";wallpaper.style="transform: scale(1.5);";ket.style="display:none";setTimeout(mulainama,700)}}
  
  async function mulainama() {
    suratin.style="display:none";ket.style="display:none";
    var { value: nama } = await swals.fire({
           title: 'Masukin nama kamu', input: 'text',
       });
       if(nama && nama.length < 11){
           window.nama = nama;namakamu.innerHTML=nama;namakamu2.innerHTML=nama;namakamu3.innerHTML=nama;
           kalimat.innerHTML+= nama + "! ❤️";
           kal1 = kalimat.innerHTML;kalimat.innerHTML="";
           kal2 = kalimatb.innerHTML;kalimatb.innerHTML="";
           kal22 = kalimatb2.innerHTML;kalimatb2.innerHTML="";
           kal3 = kalimatc.innerHTML;kalimatc.innerHTML="";
           kalimatd.style="position:absolute;opacity:0";

           Content.style = "opacity:1;margin-top:4vh";
           bodyblur.style="opacity:.4";
           wallpaper.style="transform: scale(1);";
           fotoakhir.style="display:inline-flex;";setTimeout(ftmuncul,200);
           bq.style = "position:relative;opacity:1;visibility:visible;transform: scale(1);margin-top:0";
           setTimeout(mulaiketik1,500);fungsi=1;
       } else {
           await swals.fire('Ups!', 'Nama tidak boleh kosong atau lebih dari 10 karakter, ya!');mulainama();
    }
  }
  
  function ftmuncul(){
    if(ftganti==0){fotoakhir.style="display:inline-flex;opacity:1;transform:scale(1)";}
    if(ftganti==1){fotoakhir.src = fotoakhir2.src;fotoakhir.style="display:inline-flex;opacity:1;transition:all .7s ease;transform:scale(1);";}
    if(ftganti==2){fotoakhir.src = fotoakhir3.src;fotoakhir.style="display:inline-flex;opacity:1;transition:all .7s ease;transform:scale(1);";}
    if(ftganti==3){fotoakhir.src = fotoakhir4.src;fotoakhir.style="display:inline-flex;opacity:1;transition:all .7s ease;transform:scale(1);";}
  }
  function fthilang(){fotoakhir.style="display:inline-flex;opacity:1;transition:all .7s ease;transform:scale(.1)";}
  function jjfoto(){fotoakhir.style.animation="rto .8s infinite alternate";}
  
  function tombol(){ftom=1;Tombol.style="opacity:1;transform: scale(1);";if(fungsi==2){tmbl.innerHTML="💌 Kirim";ftom=2;}} ininomorkamu = nomorWA.innerHTML;if(ininomorkamu==628){ininomorkamu = "";}
  function multifungsi(){if(ftom==1){lanjut();} if(ftom==2){menuju();}} 
  async function menuju(){window.location = "https://api.whatsapp.com/send?phone=" + ininomorkamu + "&text=" + pesanwhatsapp;}

  const body = document.querySelector("body");const swalst = Swal.mixin({timer: 2777, allowOutsideClick: false, showConfirmButton: false, timerProgressBar: true, imageHeight: 90,}); audio = new Audio('' + linkmp3.innerHTML);const swals = Swal.mixin({allowOutsideClick: false, cancelButtonColor: '#FF0040', imageWidth: 100, imageHeight: 100,}); const style = document.createElement('style'); var today = new Date();var dd = String(today.getDate()).padStart(2, '0');var mm = String(today.getMonth() + 1).padStart(2, '0');var yyyy = today.getFullYear();const monthNames = ["Januari", "Februari", "Maret", "April", "Mei", "Juni", "Juli", "Agustus", "September", "Oktober", "November", "Desember"];today = dd + ' ' + monthNames[today.getMonth()] + ' ' + yyyy;
  audio = new Audio('' + linkmp3.src);
  
  function createHeart() {const heart = document.createElement("div"); heart.className = "fas fa-heart"; heart.style.left = (Math.random() * 90)+"vw"; heart.style.animationDuration = (Math.random()*3)+2+"s"; body.appendChild(heart);} setInterval(function name(params) {var heartArr = document.querySelectorAll(".fa-heart"); if (heartArr.length > 100) {heartArr[0].remove()}},100);
</script>
<!-- Sampai Sini -->
</body>
</html>
