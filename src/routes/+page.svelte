<script>
  let scrolled = false;

  const handleScroll = () => {
    scrolled = window.scrollY > 10;
  };
</script>

<svelte:window on:scroll={handleScroll} />


<div class="min-h-screen">
    <nav class=" fixed top-0 w-full z-10 transition-all duration-300 {scrolled
    ? 'bg-[#FFB103]/80 backdrop-blur shadow-md'
    : 'bg-transparent'}">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between  h-16">
                <div class=" space-x-8 py-1">
                  <h1 class="  font-sans font-extrabold tracking-[0.1em] px-3 py-2  text-3xl  {scrolled ?' text-black' : ' text-[#E67E22]'}">PhishAware</h1>
                </div>
                <div class="flex py-3 space-x-3">
                    <a href="about" class="  px-3 py-2 {scrolled ?' text-black hover:bg-[#F5C948] hover:border-b-4 hover:border-[#E67E22]' : 'hover:border-b-4 hover:border-[#E67E22] text-[#812E88] '} rounded-md text-base font-sans font-medium">About</a>
                </div>
            </div>
        </div>
    </nav>

    <!-- Konten Utama -->
    <div class=" flex flex-col items-center justify-center min-h-screen anim ">
        <h1 class="text-1xl text-[#E67E22] md:text-6xl font-bold text-center mb-8 max-w-3xl animate-fade-in">Kenali Ancaman Digital. 
          Lindungi Dirimu.</h1>
        <p class="text-lg md:text-xl text-[#E67E22] text-center max-w-2xl animate-fade-in">PhishAware adalah platform edukasi interaktif yang membantu pengguna mengenali ancaman keamanan digital seperti phishing, password lemah, dan malware melalui simulasi yang aman dan mudah dipahami.</p>
    </div>
    <!-- Body -->
     <div class=" flex justify-center mb-20">
      <h3 class="text-[25px] text-[#E67E22] font-bold"> Understanding Digital Threats Through Interactive Simulation</h3>
     </div>
     <div class=" flex justify-center min-h-[400px] pb-20 space-x-18 ">
      <div class=" card  w-96 shadow-sm  flex justify-center">
        <div class=" card-body border-2 border-[#E67E22] rounded-2xl ">
           <div class=" flex justify-center">
            <h3 class=" text-[25px] text-[#E67E22] font-bold ">Phishing Simulation</h3>
           </div>
           <hr class=" border-2 border-[#E67E22]">
           <div>
            <p class="text-[18px] text-center text-[#E67E22]">Simulasi phishing yang dirancang menyerupai kasus nyata, seperti email palsu, pesan penipuan, dan halaman login tiruan.
              Pengguna diajak untuk mengidentifikasi tanda-tanda phishing, memahami teknik manipulasi yang sering digunakan pelaku, serta belajar mengenali risiko sebelum memberikan data pribadi.
              Simulasi ini bersifat aman dan edukatif, sehingga pengguna dapat belajar dari kesalahan tanpa risiko kebocoran data.
            </p>
           </div>
           <a href="phising" class=" mt-auto btn btn-outline border-2 border-[#E67E22] text-[#E67E22] hover:bg-[#E67E22] hover:text-white text-[16px] font-bold">
                <button >
                Open Phising Simulation
              </button>
            </a>

        </div>
      </div>
      <div class=" card  w-96 shadow-sm  flex justify-center">
        <div class=" card-body border-2 border-[#E67E22] rounded-2xl ">
           <div class=" flex justify-center">
            <h3 class=" text-[25px] text-[#E67E22] font-bold ">Password Checker</h3>
           </div>
           <hr class=" border-2 border-[#E67E22]">
           <div>
             <p class="text-[18px] text-center text-[#E67E22]">Password Checker berfungsi untuk mengevaluasi kekuatan kata sandi yang digunakan pengguna.
              Fitur ini menganalisis pola kata sandi, panjang karakter, serta tingkat kompleksitas untuk menunjukkan seberapa rentan kata sandi tersebut terhadap serangan.
              Melalui fitur ini, pengguna diharapkan dapat memahami pentingnya penggunaan kata sandi yang kuat dan membentuk kebiasaan keamanan digital yang lebih baik.
            </p>
           </div>
           <a href=password class="mt-auto btn btn-outline border-2 border-[#E67E22] text-[#E67E22] hover:bg-[#E67E22] hover:text-white text-[16px] font-bold" >
              <button>
              Open Password Checker
            </button>
            </a>
        </div>
      </div>
      <div class=" card  w-96 shadow-sm  flex justify-center">
        <div class=" card-body border-2 border-[#E67E22] rounded-2xl ">
           <div class=" flex justify-center">
            <h3 class=" text-[22px] text-[#E67E22] font-bold ">Virus & Malware Awareness</h3>
           </div>
           <hr class=" border-2 border-[#E67E22]">
           <div>
             <p class="text-[18px] text-center text-[#E67E22]">Edukasi mengenai berbagai jenis malware, seperti virus, trojan, dan ransomware.
Pengguna akan diperkenalkan pada cara kerja malware, dampak yang dapat ditimbulkan, serta tanda-tanda umum perangkat yang terinfeksi.
Dengan pendekatan visual dan penjelasan sederhana, fitur ini membantu meningkatkan kesadaran pengguna terhadap ancaman malware tanpa menjalankan program berbahaya secara nyata.
            </p>
           </div>
          <a href="virus" class=" mt-auto btn btn-outline border-2 border-[#E67E22] text-[#E67E22] hover:bg-[#E67E22] hover:text-white text-[16px] font-bold">
          <button>
            Open Virus & Malware Awareness
          </button>
          </a>
  
        </div>
      </div>

    </div>

    <!-- footer -->
    <div>
      <footer class="footer sm:footer-horizontal bg-neutral text-neutral-content items-center p-2">
  <aside class="grid-flow-col items-center">
    <svg
      width="36"
      height="36"
      viewBox="0 0 24 24"
      xmlns="http://www.w3.org/2000/svg"
      fill-rule="evenodd"
      clip-rule="evenodd"
      class="fill-current">
      <path
        d="M22.672 15.226l-2.432.811.841 2.515c.33 1.019-.209 2.127-1.23 2.456-1.15.325-2.148-.321-2.463-1.226l-.84-2.518-5.013 1.677.84 2.517c.391 1.203-.434 2.542-1.831 2.542-.88 0-1.601-.564-1.86-1.314l-.842-2.516-2.431.809c-1.135.328-2.145-.317-2.463-1.229-.329-1.018.211-2.127 1.231-2.456l2.432-.809-1.621-4.823-2.432.808c-1.355.384-2.558-.59-2.558-1.839 0-.817.509-1.582 1.327-1.846l2.433-.809-.842-2.515c-.33-1.02.211-2.129 1.232-2.458 1.02-.329 2.13.209 2.461 1.229l.842 2.515 5.011-1.677-.839-2.517c-.403-1.238.484-2.553 1.843-2.553.819 0 1.585.509 1.85 1.326l.841 2.517 2.431-.81c1.02-.33 2.131.211 2.461 1.229.332 1.018-.21 2.126-1.23 2.456l-2.433.809 1.622 4.823 2.433-.809c1.242-.401 2.557.484 2.557 1.838 0 .819-.51 1.583-1.328 1.847m-8.992-6.428l-5.01 1.675 1.619 4.828 5.011-1.674-1.62-4.829z"></path>
    </svg>
    <p>Copyright © {new Date().getFullYear()} - All right reserved</p>
  </aside>
  <nav class="grid-flow-col gap-3 md:place-self-center md:justify-self-end pr-3">
    <a href="https://www.instagram.com/zhoksd/?hl=id">
      <!-- Tiktok -->
      
      <svg
          xmlns="http://www.w3.org/2000/svg"
           viewBox="0 0 24 24"
           class="w-6 h-6 fill-current">
           <path d="M7.8 2h8.4C19.6 2 22 4.4 22 7.8v8.4C22 19.6 19.6 22 16.2 22H7.8C4.4 22 2 19.6 2 16.2V7.8C2 4.4 4.4 2 7.8 2zm0 1.6C5.5 3.6 3.6 5.5 3.6 7.8v8.4c0 2.3 1.9 4.2 4.2 4.2h8.4c2.3 0 4.2-1.9 4.2-4.2V7.8c0-2.3-1.9-4.2-4.2-4.2H7.8zM12 7.4a4.6 4.6 0 1 1 0 9.2 4.6 4.6 0 0 1 0-9.2zm0 1.6a3 3 0 1 0 0 6 3 3 0 0 0 0-6zm5.6-2.2a1.2 1.2 0 1 1 0 2.4 1.2 1.2 0 0 1 0-2.4z"/>
      </svg>
    </a>
    <!-- Instagram -->
    <a href="https://www.tiktok.com/@zhoksd">
     <svg
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 24 24"
         class="w-6 h-6 fill-current">
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