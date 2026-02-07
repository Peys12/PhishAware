<script>
  let scrolled = false;

  const handleScroll = () => {
    scrolled = window.scrollY > 10;
  };
</script>

<svelte:window on:scroll={handleScroll} />

<div class="min-h-screen bg-gradient-to-br from-[#F5F7FA] to-[#E8F4F8]">
  <nav class="fixed top-0 w-full z-10 transition-all duration-300 z-30 {scrolled ? 'bg-[#FFB103]/80 backdrop-blur shadow-md' : 'bg-transparent'}">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between h-16">
        <div class="space-x-8 py-3">
          <a href="/">
            <div class="font-sans font-extrabold tracking-[0.1em] px-3 text-3xl {scrolled ? 'text-black' : 'text-[#E67E22]'}">PhishAware</div>
          </a>
        </div>
        <div class="flex py-3 space-x-3">
          <a href="about">
            <div class="px-3 py-2 {scrolled ? 'text-black hover:bg-[#F5C948] hover:border-b-4 hover:border-[#E67E22]' : 'hover:border-b-4 hover:border-[#E67E22] text-[#812E88]'} rounded-md text-base font-sans font-medium">About</div>
          </a>
        </div>
      </div>
    </div>
  </nav>

  <div class="pt-20 pb-10">
    <div class="max-w-4xl mx-auto text-center">
      <h1 class="text-5xl font-extrabold text-[#8E45AE] mb-4 animate-fade-in">Tentang Website Ini</h1>
      <p class="text-lg text-gray-700">Pelajari lebih dalam tentang misi dan tujuan website edukasi keamanan siber ini.</p>
    </div>
  </div>

  <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 space-y-12 pb-20">
    <div class="bg-white rounded-3xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-500">
      <h2 class="text-3xl font-bold text-[#8E45AE] mb-4">Gambaran Umum</h2>
      <p class="text-gray-700 leading-relaxed">
        Website ini dibuat sebagai media edukasi interaktif untuk mengenalkan berbagai jenis ancaman keamanan siber, khususnya malware dan phishing, yang sering ditemui dalam kehidupan digital sehari-hari. Melalui tampilan visual dan simulasi sederhana, pengguna dapat memahami cara kerja ancaman tersebut dengan lebih mudah. Dengan pendekatan ini, website tidak hanya memberikan informasi teoritis, tetapi juga pengalaman praktis yang membantu pengguna mengidentifikasi dan menghindari risiko secara langsung dalam aktivitas online mereka sehari-hari.
      </p>
    </div>

    <div class="bg-white rounded-3xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-500">
      <h2 class="text-3xl font-bold text-[#8E45AE] mb-4">Tujuan</h2>
      <p class="text-gray-700 leading-relaxed">
        Tujuan utama dari website ini adalah meningkatkan kesadaran pengguna terhadap bahaya serangan siber serta membantu mereka mengenali tanda-tanda ancaman sejak dini. Dengan pemahaman yang baik, pengguna diharapkan dapat lebih berhati-hati dan aman saat menggunakan internet. Selain itu, website ini bertujuan untuk membangun komunitas yang peduli terhadap keamanan digital, dengan menyediakan sumber daya yang mudah diakses dan dapat digunakan oleh semua kalangan, dari pemula hingga yang sudah berpengalaman dalam dunia teknologi.
      </p>
    </div>

    <div class="bg-white rounded-3xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-500">
      <h2 class="text-3xl font-bold text-[#8E45AE] mb-4">Kenapa Penting</h2>
      <p class="text-gray-700 leading-relaxed">
        Di era digital saat ini, serangan siber tidak hanya menargetkan perusahaan besar, tetapi juga pengguna biasa. Kurangnya pengetahuan sering kali menjadi celah utama yang dimanfaatkan oleh pelaku kejahatan digital. Oleh karena itu, edukasi keamanan siber menjadi hal yang sangat penting. Dengan meningkatnya penggunaan internet untuk berbagai keperluan, dari perbankan hingga komunikasi pribadi, risiko ancaman siber juga ikut meningkat, sehingga pendidikan yang komprehensif seperti ini diperlukan untuk melindungi data dan privasi pengguna di seluruh dunia.
      </p>
    </div>
  </div>

  <!-- footer -->
  <div>
    <footer class="footer sm:footer-horizontal bg-neutral text-neutral-content items-center p-2">
      <aside class="grid-flow-col items-center">
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

<style>
  .animate-fade-in {
    animation: fadeIn 1s ease-in-out;
  }
  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }
</style>