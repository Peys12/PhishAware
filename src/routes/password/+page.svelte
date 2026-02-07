<script>
  let scrolled = false;
  let password = '';
  let strength = 0; 
  let criteria = [
    { text: '8 Karakter', met: false },
    { text: 'Huruf Besar', met: false },
    { text: 'Angka', met: false },
    { text: 'Simbol', met: false }
  ];

  const handleScroll = () => {
    scrolled = window.scrollY > 10;
  };


  function checkPasswordStrength() {
    let score = 0;
    criteria[0].met = password.length >= 8; 
    criteria[1].met = /[A-Z]/.test(password); 
    criteria[2].met = /\d/.test(password);
    criteria[3].met = /[!@#$%^&*(),.?":{}|<>]/.test(password); 

    score = criteria.filter(c => c.met).length;
    strength = score;
  }

  $: if (password !== undefined) checkPasswordStrength();
</script>

<svelte:window on:scroll={handleScroll} />

<div class="min-h-screen">
  <!-- navbar -->
  <nav class="fixed top-0 w-full z-10 transition-all duration-300 z-30 {scrolled ? 'bg-[#FFB103]/80 backdrop-blur shadow-md' : 'bg-transparent'}">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between h-16">
        <div class="space-x-8 py-3">
          <a href="/" class="font-sans font-extrabold tracking-[0.1em] px-3 text-3xl {scrolled ? 'text-black' : 'text-[#E67E22]'}">PhishAware</a>
        </div>
        <div class="flex py-3 space-x-3">
          <a href="about" class="px-3 py-2 {scrolled ? 'text-black hover:bg-[#F5C948] hover:border-b-4 hover:border-[#E67E22]' : 'hover:border-b-4 hover:border-[#E67E22] text-[#812E88]'} rounded-md text-base font-sans font-medium">About</a>
        </div>
      </div>
    </div>
  </nav>

  <!-- gasss -->
  <div class="min-h-screen flex justify-center items-center">
    <div class="card w-[650px] absolute z-10 rounded-4xl bg-[#8E45AE] h-[165px] top-[100px]">
      <div class="card-body rounded-full justify-center space-y-2 my-2 text-center">
        <h1 class="text-4xl text-white font-bold text-center font-sans">Password Strength Checker</h1>
        <p class="font-semibold text-sm">Banyak serangan phishing berhasil karena password lemah. Pastikan password kamu aman sebelum digunakan.</p>
      </div>
    </div>

    <div class="card w-[800px] bg-white h-[400px]">
      <div class="card-body rounded-4xl shadow-2xl flex justify-center items-center font-black text-center">
      </div>
    </div>

    <div class="card w-[650px] absolute z-10 rounded-4xl bg-transparent h-[165px]">
      <div class="card-body flex items-center justify-center">
        <div class="font-black text-center">
          <input type="text" class="input w-[350px] -top-8 bg-transparent text-black font-semibold border-3 border-[#E67E22]" placeholder="Masukan Password" bind:value={password}>
        </div>
        <div class="w-[350px] absolute top-22 bg-gray-200 rounded-full top-10 transition-all duration-500">
          <div class="h-3 rounded-full transition-all duration-500 {strength === 0 ? 'bg-red-500' : strength === 1 ? 'bg-orange-500' : strength === 2 ? 'bg-yellow-500' : strength === 3 ? 'bg-blue-500' : 'bg-green-500'}" style="width: {strength * 25}%"></div>
        </div>

        <div class="card w-[360px] absolute z-20 top-[90px] bg-transparent h-[165px]">
          <div class="card-body">
            <ul class="list-disc">
              {#each criteria as criterion}
                <li class="text-black {criterion.met ? 'text-green-600 line-through' : ''}">{criterion.met ? '✓' : '✗'} {criterion.text}</li>
              {/each}
            </ul>
          </div>
        </div>
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
          <!-- Tiktok -->
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" class="w-6 h-6 fill-current">
            <path d="M7.8 2h8.4C19.6 2 22 4.4 22 7.8v8.4C22 19.6 19.6 22 16.2 22H7.8C4.4 22 2 19.6 2 16.2V7.8C2 4.4 4.4 2 7.8 2zm0 1.6C5.5 3.6 3.6 5.5 3.6 7.8v8.4c0 2.3 1.9 4.2 4.2 4.2h8.4c2.3 0 4.2-1.9 4.2-4.2V7.8c0-2.3-1.9-4.2-4.2-4.2H7.8zM12 7.4a4.6 4.6 0 1 1 0 9.2 4.6 4.6 0 0 1 0-9.2zm0 1.6a3 3 0 1 0 0 6 3 3 0 0 0 0-6zm5.6-2.2a1.2 1.2 0 1 1 0 2.4 1.2 1.2 0 0 1 0-2.4z"/>
          </svg>
        </a>
        <a href="https://www.tiktok.com/@zhoksd">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" class="w-6 h-6 fill-current">
            <path d="M14.5 3c.4 2.3 1.8 4 4 4.4v2.2c-1.7 0-3.3-.6-4.5-1.7v7c0 3-2.4 5.4-5.4 5.4A5.4 5.4 0 0 1 8.6 9.5c.5 0 1 .1 1.5.2v2.3a3 3 0 1 0 2.3 2.9V3h2.1z"/>
          </svg>
        </a>
      </nav>
    </footer>
  </div>
</div>