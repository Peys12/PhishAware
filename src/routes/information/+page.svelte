<script>
  let scrolled = false;

  const handleScroll = () => {
    scrolled = window.scrollY > 10;
  };
</script>

<svelte:window on:scroll={handleScroll} />

<div class="min-h-screen">
  <!-- navbar -->
  <nav class="fixed top-0 w-full transition-all duration-300 z-30 {scrolled ? 'bg-[#FFB103]/80 backdrop-blur shadow-md' : 'bg-transparent'}">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between h-16">
        <div class="space-x-8 py-3">
          <a href="/" class="font-sans font-extrabold px-3 text-3xl {scrolled ? 'text-black' : 'text-[#E67E22]'}">PhishAware</a>
        </div>
        <div class="flex py-3 space-x-3">
          <a href="about" class="px-3 py-2 {scrolled ? 'text-black hover:bg-[#F5C948] hover:border-b-4 hover:border-[#E67E22]' : 'hover:border-b-4 hover:border-[#E67E22] text-[#812E88]'} rounded-md text-base font-sans font-medium">About</a>
        </div>
      </div>
    </div>
  </nav>

  <!-- Hero Card -->
  <div class="card flex items-center w-full">
    <div class="card-body bg-[#8E45AE] mt-20 h-40 rounded-4xl w-full max-w-[1200px]">
      <h1 class="text-white font-extrabold text-5xl flex justify-center items-center text-center">Phishing Awareness</h1>
      <p class="text-white font-semibold text-lg flex justify-center items-center text-center">Pelajari ancaman phishing dan cara menghindarinya untuk menjaga keamanan digital Anda.</p>
    </div>
  </div>

  <!-- Cards untuk Konten Phishing -->
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-10 space-y-8">
    <!-- Card 1: Apa itu Phishing? -->
    <div class="card bg-white shadow-lg rounded-lg p-6">
      <div class="card-body">
        <h2 class="card-title text-2xl font-bold text-[#8E45AE]">🧠 1. Apa itu Phishing?</h2>
        <p class="text-gray-700 mt-4">
          Phishing adalah metode penipuan digital yang digunakan untuk mencuri informasi sensitif seperti kata sandi, data pribadi, atau informasi keuangan dengan menyamar sebagai pihak yang terpercaya. Pelaku phishing biasanya memanfaatkan rasa panik, takut, atau tergesa-gesa agar korban melakukan tindakan tanpa berpikir panjang.
        </p>
        <p class="text-gray-700 mt-2">
          Phishing tidak selalu berbentuk email. Serangan ini dapat muncul melalui website palsu, pesan singkat, media sosial, hingga iklan online yang tampak meyakinkan.
        </p>
      </div>
    </div>

    <!-- Card 2: Bagaimana Cara Kerja Phishing? -->
    <div class="card bg-white shadow-lg rounded-lg p-6">
      <div class="card-body">
        <h2 class="card-title text-2xl font-bold text-[#8E45AE]">🎣 2. Bagaimana Cara Kerja Phishing?</h2>
        <p class="text-gray-700 mt-4">
          Secara umum, phishing bekerja melalui beberapa tahapan:
        </p>
        <ul class="list-disc list-inside text-gray-700 mt-2 space-y-1">
          <li>Pelaku membuat tampilan palsu yang menyerupai layanan asli.</li>
          <li>Korban diarahkan ke halaman tersebut melalui tautan atau pesan.</li>
          <li>Korban memasukkan data pribadi tanpa menyadari bahwa halaman tersebut palsu.</li>
          <li>Data yang dimasukkan kemudian disalahgunakan oleh pelaku.</li>
        </ul>
        <p class="text-gray-700 mt-4">
          Karena tampilannya mirip dengan situs resmi, banyak pengguna tidak menyadari bahwa mereka sedang menjadi target phishing.
        </p>
      </div>
    </div>

    <!-- Card 3: Metode Phishing yang Sering Digunakan -->
    <div class="card bg-white shadow-lg rounded-lg p-6">
      <div class="card-body">
        <h2 class="card-title text-2xl font-bold text-[#8E45AE]">🧪 3. Metode Phishing yang Sering Digunakan</h2>
        <div class="mt-4 space-y-4">
          <div>
            <h3 class="font-semibold text-gray-800">📧 Email Phishing</h3>
            <p class="text-gray-700">Pelaku mengirim email yang seolah berasal dari institusi resmi, seperti bank atau layanan digital. Email biasanya berisi peringatan palsu atau permintaan untuk segera mengklik tautan tertentu.</p>
          </div>
          <div>
            <h3 class="font-semibold text-gray-800">🌐 Website Palsu</h3>
            <p class="text-gray-700">Korban diarahkan ke website tiruan yang sangat mirip dengan situs asli. Tujuannya adalah membuat korban memasukkan data login tanpa curiga.</p>
          </div>
          <div>
            <h3 class="font-semibold text-gray-800">📱 Phishing melalui Pesan & Media Sosial</h3>
            <p class="text-gray-700">Pesan dikirim melalui SMS, WhatsApp, atau media sosial dengan iming-iming hadiah, ancaman akun diblokir, atau permintaan bantuan mendesak.</p>
          </div>
          <div>
            <h3 class="font-semibold text-gray-800">🎯 Spear Phishing</h3>
            <p class="text-gray-700">Serangan phishing yang ditargetkan ke individu tertentu. Informasi korban sering digunakan agar pesan terlihat lebih meyakinkan dan personal.</p>
          </div>
        </div>
      </div>
    </div>

    <!-- Card 4: Tanda-tanda Phishing yang Perlu Diwaspadai -->
    <div class="card bg-white shadow-lg rounded-lg p-6">
      <div class="card-body">
        <h2 class="card-title text-2xl font-bold text-[#8E45AE]">🚨 4. Tanda-tanda Phishing yang Perlu Diwaspadai</h2>
        <p class="text-gray-700 mt-4">
          Beberapa ciri umum phishing antara lain:
        </p>
        <ul class="list-disc list-inside text-gray-700 mt-2 space-y-1">
          <li>Bahasa yang mendesak atau mengancam</li>
          <li>Permintaan data pribadi secara tiba-tiba</li>
          <li>Alamat website yang terlihat aneh atau berbeda</li>
          <li>Kesalahan ejaan atau tata bahasa</li>
          <li>Tawaran hadiah yang terlalu menggiurkan</li>
        </ul>
      </div>
    </div>

    <!-- Card 5: Cara Menghindari Phishing -->
    <div class="card bg-white shadow-lg rounded-lg p-6">
      <div class="card-body">
        <h2 class="card-title text-2xl font-bold text-[#8E45AE]">🛡️ 5. Cara Menghindari Phishing</h2>
        <p class="text-gray-700 mt-4">
          Untuk menghindari phishing, pengguna disarankan untuk:
        </p>
        <ul class="list-disc list-inside text-gray-700 mt-2 space-y-1">
          <li>Selalu memeriksa alamat website dengan teliti</li>
          <li>Tidak mengklik tautan mencurigakan</li>
          <li>Tidak membagikan kata sandi kepada siapa pun</li>
          <li>Menggunakan autentikasi dua faktor (2FA)</li>
          <li>Meningkatkan literasi keamanan digital</li>
        </ul>
      </div>
    </div>

    <!-- Penutup -->
    <div class="card bg-gradient-to-r from-[#8E45AE] to-[#FFB103] shadow-lg rounded-lg p-6 text-white">
      <div class="card-body text-center">
        <h2 class="card-title text-3xl font-bold">✨ Penutup</h2>
        <p class="text-lg mt-4">
          Phishing memanfaatkan kelengahan manusia, bukan kelemahan teknologi. Dengan pemahaman yang baik, ancaman ini dapat dikenali dan dihindari sebelum menimbulkan kerugian.
        </p>
      </div>
    </div>
  </div>

  <!-- footer -->
  <div>
    <footer class="footer sm:footer-horizontal bg-neutral text-neutral-content items-center p-2">
      <aside class="grid-flow-col items-center">
        <!-- instagram -->
        <svg width="36" height="36" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" fill-rule="evenodd" clip-rule="evenodd" class="fill-current">
          <path d="M22.672 15.226l-2.432.811.841 2.515c.33 1.019-.209 2.127-1.23 2.456-1.15.325-2.148-.321-2.463-1.226l-.84-2.518-5.013 1.677.84 2.517c.391 1.203-.434 2.542-1.831 2.542-.88 0-1.601-.564-1.86-1.314l-.842-2.516-2.431.809c-1.135.328-2.145-.317-2.463-1.229-.329-1.018.211-2.127 1.231-2.456l2.432-.809-1.621-4.823-2.432.808c-1.355.384-2.558-.59-2.558-1.839 0-.817.509-1.582 1.327-1.846l2.433-.809-.842-2.515c-.33-1.02.211-2.129 1.232-2.458 1.02-.329 2.13.209 2.461 1.229l.842 2.515 5.011-1.677-.839-2.517c-.403-1.238.484-2.553 1.843-2.553.819 0 1.585.509 1.85 1.326l.841 2.517 2.431-.81c1.02-.33 2.131.211 2.461 1.229.332 1.018-.21 2.126-1.23 2.456l-2.433.809 1.622 4.823 2.433-.809c1.242-.401 2.557.484 2.557 1.838 0 .819-.51 1.583-1.328 1.847m-8.992-6.428l-5.01 1.675 1.619 4.828 5.011-1.674-1.62-4.829z"></path>
        </svg>
        <p>Copyright © {new Date().getFullYear()} - All right reserved</p>
      </aside>
      <nav class="grid-flow-col gap-3 md:place-self-center md:justify-self-end pr-3">
        <a href="https://www.instagram.com/zhoksd/?hl=id">
          <!-- Instagram -->
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" class="w-6 h-6 fill-current">
            <path d="M7.8 2h8.4C19.6 2 22 4.4 22 7.8v8.4C22 19.6 19.6 22 16.2 22H7.8C4.4 22 2 19.6 2 16.2V7.8C2 4.4 4.4 2 7.8 2zm0 1.6C5.5 3.6 3.6 5.5 3.6 7.8v8.4c0 2.3 1.9 4.2 4.2 4.2h8.4c2.3 0 4.2-1.9 4.2-4.2V7.8c0-2.3-1.9-4.2-4.2-4.2H7.8zM12 7.4a4.6 4.6 0 1 1 0 9.2 4.6 4.6 0 0 1 0-9.2zm0 1.6a3 3 0 1 0 0 6 3 3 0 0 0 0-6zm5.6-2.2a1.2 1.2 0 1 1 0 2.4 1.2 1.2 0 0 1 0-2.4z"/>
          </svg>
        </a>
        <a href="https://www.tiktok.com/@zhoksd">
          <!-- Tiktok -->
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" class="w-6 h-6 fill-current">
            <path d="M14.5 3c.4 2.3 1.8 4 4 4.4v2.2c-1.7 0-3.3-.6-4.5-1.7v7c0 3-2.4 5.4-5.4 5.4A5.4 5.4 0 0 1 8.6 9.5c.5 0 1 .1 1.5.2v2.3a3 3 0 1 0 2.3 2.9V3h2.1z"/>
          </svg>
        </a>
      </nav>
    </footer>
  </div>
</div>