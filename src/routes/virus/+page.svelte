<script>
  let scrolled = false;

  const handleScroll = () => {
    scrolled = window.scrollY > 10;
  };
</script>

<svelte:window on:scroll={handleScroll} />

<div class="min-h-screen ">
  <!-- navbar -->
  <nav class="fixed top-0 w-full transition-all duration-300 z-30 {scrolled ? 'bg-[#FFB103]/90 backdrop-blur-md shadow-lg' : 'bg-transparent'}">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between h-16">
        <div class="space-x-8 py-3">
          <a href="/" class="font-sans font-extrabold px-3 text-3xl {scrolled ? 'text-black' : 'text-[#E67E22]'} hover:scale-105 transition-transform">PhishAware</a>
        </div>
        <div class="flex py-3 space-x-3">
          <a href="about" class="px-3 py-2 {scrolled ? 'text-black hover:bg-[#F5C948] hover:border-b-4 hover:border-[#E67E22]' : 'hover:border-b-4 hover:border-[#E67E22] text-[#812E88]'} rounded-md text-base font-sans font-medium transition-all">About</a>
        </div>
      </div>
    </div>
  </nav>

  <!-- Hero Card -->
  <div class="flex items-center justify-center w-full pt-20 pb-10">
    <div class="card-body bg-gradient-to-r from-[#8E45AE] to-[#D291BC] mt-10 h-48 rounded-3xl w-full max-w-[1200px] shadow-2xl hover:shadow-3xl transition-shadow duration-500">
      <h1 class="text-white font-extrabold text-5xl flex justify-center items-center text-center animate-fade-in">Virus & Malware</h1>
      <p class="text-white font-semibold text-lg flex justify-center items-center text-center mt-4 animate-fade-in delay-200">Ancaman malware terus berkembang. Pemahaman dasar diperlukan untuk menjaga keamanan perangkat dan data.</p>
    </div>
  </div>

  <!-- Cards Section -->
  <div class="flex flex-wrap justify-evenly items-center  pt-4 pb-12 px-4">
    <!-- Virus Card -->
    <div class="flex justify-center items-center mt-7">
      <div class="w-[350px] h-[400px] perspective-1000">
        <div class="relative w-full h-full transition-transform duration-700 transform-style-preserve-3d hover:rotate-y-180 cursor-pointer">
          <div class="absolute inset-0 backface-hidden shadow-2xl rounded-3xl overflow-hidden bg-gradient-to-b from-white to-gray-100">
            <img src="virus.png"  class="w-full h-[320px] object-cover rounded-t-3xl">
            <div class="bg-gradient-to-r from-[#8E45AE] to-[#D291BC] h-[80px] flex items-center justify-center rounded-b-3xl">
              <h2 class="text-white font-bold text-3xl">Virus</h2>
            </div>
          </div>
          <div class="absolute inset-0 backface-hidden rotate-y-180 bg-gradient-to-br from-[#F5C948] to-[#FFB103] rounded-3xl shadow-xl flex items-center justify-center px-6 text-center">
            <p class="text-[#812E88] font-semibold text-[15px] leading-relaxed">
              Virus adalah program berbahaya yang menempel pada file atau aplikasi lain dan menyebar ketika file tersebut dijalankan. Setelah aktif, virus dapat merusak sistem operasi, memperlambat kinerja perangkat, menghapus atau mengubah data, bahkan menyebabkan sistem tidak bisa digunakan. Virus biasanya menyebar melalui file unduhan ilegal, flashdisk, email berbahaya, atau software bajakan. Tanpa perlindungan keamanan, virus dapat menyebar dengan cepat ke banyak perangkat.
            </p>
          </div>
        </div>
      </div>
    </div>

    <!-- Trojan Card -->
    <div class="flex justify-center items-center mt-7">
      <div class="w-[350px] h-[400px] perspective-1000">
        <div class="relative w-full h-full transition-transform duration-700 transform-style-preserve-3d hover:rotate-y-180 cursor-pointer">
          <div class="absolute inset-0 backface-hidden shadow-2xl rounded-3xl overflow-hidden bg-gradient-to-b from-white to-gray-100">
            <img src="trojan.png"  class="w-full h-[320px] object-cover rounded-t-3xl">
            <div class="bg-gradient-to-r from-[#8E45AE] to-[#D291BC] h-[80px] flex items-center justify-center rounded-b-3xl">
              <h2 class="text-white font-bold text-3xl">Trojan</h2>
            </div>
          </div>
          <div class="absolute inset-0 backface-hidden rotate-y-180 bg-gradient-to-br from-[#F5C948] to-[#FFB103] rounded-3xl shadow-xl flex items-center justify-center px-6 text-center">
            <p class="text-[#812E88] font-semibold text-[15px] leading-relaxed">
              Trojan adalah malware yang menyamar sebagai aplikasi normal atau berguna, seperti game, software gratis, atau file dokumen. Berbeda dengan virus, Trojan tidak menyebar sendiri, tetapi mengandalkan pengguna untuk menjalankannya. Setelah aktif, Trojan dapat membuka akses ilegal ke sistem, mencuri data sensitif, memasang malware lain, atau memungkinkan penyerang mengendalikan perangkat dari jarak jauh tanpa sepengetahuan pengguna.
            </p>
          </div>
        </div>
      </div>
    </div>

    <!-- Ransomware Card -->
    <div class="flex justify-center items-center mt-7">
      <div class="w-[350px] h-[400px] perspective-1000">
        <div class="relative w-full h-full transition-transform duration-700 transform-style-preserve-3d hover:rotate-y-180 cursor-pointer">
          <div class="absolute inset-0 backface-hidden shadow-2xl rounded-3xl overflow-hidden bg-gradient-to-b from-white to-gray-100">
            <img src="ransom.png"  class="w-full h-[320px] object-cover rounded-t-3xl">
            <div class="bg-gradient-to-r from-[#8E45AE] to-[#D291BC] h-[80px] flex items-center justify-center rounded-b-3xl">
              <h2 class="text-white font-bold text-3xl">Ransomware</h2>
            </div>
          </div>
          <div class="absolute inset-0 backface-hidden rotate-y-180 bg-gradient-to-br from-[#F5C948] to-[#FFB103] rounded-3xl shadow-xl flex items-center justify-center px-6 text-center">
            <p class="text-[#812E88] font-semibold text-[15px] leading-relaxed">
              Ransomware merupakan jenis malware yang sangat berbahaya karena mengenkripsi atau mengunci data korban sehingga tidak dapat diakses. Setelah itu, korban diminta membayar tebusan agar data dapat dipulihkan. Serangan ransomware sering menargetkan individu, perusahaan, hingga institusi penting seperti rumah sakit. Meskipun tebusan dibayar, tidak ada jaminan data akan kembali, sehingga pencegahan dan backup data menjadi langkah perlindungan yang sangat penting.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- Footer -->
  <footer class="footer sm:footer-horizontal bg-neutral text-neutral-content items-center p-4 mt-10">
    <aside class="grid-flow-col items-center">
      <svg width="36" height="36" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" fill-rule="evenodd" clip-rule="evenodd" class="fill-current">
        <path d="M22.672 15.226l-2.432.811.841 2.515c.33 1.019-.209 2.127-1.23 2.456-1.15.325-2.148-.321-2.463-1.226l-.84-2.518-5.013 1.677.84 2.517c.391 1.203-.434 2.542-1.831 2.542-.88 0-1.601-.564-1.86-1.314l-.842-2.516-2.431.809c-1.135.328-2.145-.317-2.463-1.229-.329-1.018.211-2.127 1.231-2.456l2.432-.809-1.621-4.823-2.432.808c-1.355.384-2.558-.59-2.558-1.839 0-.817.509-1.582 1.327-1.846l2.433-.809-.842-2.515c-.33-1.02.211-2.129 1.232-2.458 1.02-.329 2.13.209 2.461 1.229l.842 2.515 5.011-1.677-.839-2.517c-.403-1.238.484-2.553 1.843-2.553.819 0 1.585.509 1.85 1.326l.841 2.517 2.431-.81c1.02-.33 2.131.211 2.461 1.229.332 1.018-.21 2.126-1.23 2.456l-2.433.809 1.622 4.823 2.433-.809c1.242-.401 2.557.484 2.557 1.838 0 .819-.51 1.583-1.328 1.847m-8.992-6.428l-5.01 1.675 1.619 4.828 5.011-1.674-1.62-4.829z"></path>
      </svg>
      <p class="ml-2">Copyright © {new Date().getFullYear()} - All right reserved</p>
    </aside>
    <nav class="grid-flow-col gap-3 md:place-self-center md:justify-self-end pr-3">
      <a href="https://www.instagram.com/zhoksd/?hl=id" class="hover:scale-110 transition-transform">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" class="w-6 h-6 fill-current">
          <path d="M7.8 2h8.4C19.6 2 22 4.4 22 7.8v8.4C22 19.6 19.6 22 16.2 22H7.8C4.4 22 2 19.6 2 16.2V7.8C2 4.4 4.4 2 7.8 2zm0 1.6C5.5 3.6 3.6 5.5 3.6 7.8v8.4c0 2.3 1.9 4.2 4.2 4.2h8.4c2.3 0 4.2-1.9 4.2-4.2V7.8c0-2.3-1.9-4.2-4.2-4.2H7.8zM12 7.4a4.6 4.6 0 1 1 0 9.2 4.6 4.6 0 0 1 0-9.2zm0 1.6a3 3 0 1 0 0 6 3 3 0 0 0 0-6zm5.6-2.2a1.2 1.2 0 1 1 0 2.4 1.2 1.2 0 0 1 0-2.4z"/>
        </svg>
      </a>
      <a href="https://www.tiktok.com/@zhoksd" class="hover:scale-110 transition-transform">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" class="w-6 h-6 fill-current">
          <path d="M14.5 3c.4 2.3 1.8 4 4 4.4v2.2c-1.7 0-3.3-.6-4.5-1.7v7c0 3-2.4 5.4-5.4 5.4A5.4 5.4 0 0 1 8.6 9.5c.5 0 1 .1 1.5.2v2.3a3 3 0 1 0 2.3 2.9V3h2.1z"/>
        </svg>
      </a>
    </nav>
  </footer>
</div>

