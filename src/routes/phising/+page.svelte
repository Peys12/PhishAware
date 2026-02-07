<script>
  let view = 'gmail'; 
  let infected = false; 
  let showModal = false; 
  let capturedData = {}; 
  let back = false

  let email = '';
  let password = '';
  let account = '';

  function handleSubmit() {
    capturedData = { email, password, account };
    showModal = true;
    email = '';
    password = '';
    account = '';
  }
</script>

<div class="min-h-screen bg-gradient-to-br from-gray-900 to-black flex items-center justify-center p-4">
  <div class="relative w-full h-screen transform scale-100 transition-all duration-500">
    <div class="bg-gradient-to-b from-gray-700 to-gray-900 w-full h-full shadow-2xl relative border-2 border-gray-600 rounded-none">
      <div class="absolute top-2 left-1/2 transform -translate-x-1/2 w-8 h-8 bg-gray-500 rounded-full flex items-center justify-center">
        <span class="text-white text-xs font-bold">P</span>
      </div>
      <div class="absolute top-4 left-1/2 transform -translate-x-1/2 w-2 h-2 bg-black rounded-full"></div>
      <div class="absolute top-6 left-8 w-4 h-2 bg-gray-800 rounded"></div>
      <div class="absolute top-6 right-8 w-4 h-2 bg-gray-800 rounded"></div>
      <div class="absolute bottom-0 left-0 right-0 h-16 bg-gray-900 rounded-b-none">
        <div class="grid grid-cols-15 gap-1 p-2">
          {#each Array(15) as _}
            <div class="bg-gray-700 w-4 h-4 rounded"></div>
          {/each}
        </div>
      </div>
      <div class="absolute bottom-20 left-1/2 transform -translate-x-1/2 w-20 h-12 bg-gray-700 rounded cursor-pointer hover:bg-gray-600 transition"></div>
    </div>
    
    <div class="absolute top-4 left-4 right-4 bottom-20 bg-black rounded-none overflow-hidden shadow-inner {infected ? 'ring-4 ring-red-500 ' : ''}">
      {#if view === 'gmail'}
        <div class="h-full bg-white flex flex-col">
          <div class="bg-red-500 text-white p-4 flex items-center justify-between">
            <div class="flex items-center space-x-2">
              <div class="w-8 h-8 bg-white rounded-full flex items-center justify-center">
                <span class="text-red-500 font-bold">G</span>
              </div>
              <h1 class="text-lg font-bold">Gmail</h1>
            </div>
            <div class="text-sm">user@gmail.com</div>
          </div>
          <div class="flex-1 overflow-y-auto p-4">
            <div class="bg-gray-50 p-4 rounded-lg shadow-md mb-4 border-l-4 border-red-500">
              <div class="flex items-center justify-between mb-2">
                <h3 class="font-semibold text-gray-800">Bank Security Team</h3>
                <span class="text-xs text-gray-500">2 min ago</span>
              </div>
              <p class="text-sm text-gray-700 mb-2"><strong>Urgent: Verify Your Account Now!</strong></p>
              <p class="text-xs text-gray-600 mb-4">Dear Valued Customer, We detected unusual activity. Click the link below to secure your account.</p>
              <button class="btn btn-link text-blue-600 underline" on:click={() => { view = 'phishing'; infected = true; }}>Click Here to Verify</button>
            </div>
            <div class="bg-white p-4 rounded-lg shadow-md mb-4">
              <div class="flex items-center justify-between mb-2">
                <h3 class="font-semibold text-gray-800">Konco</h3>
                <span class="text-xs text-gray-500">1 hour ago</span>
              </div>
              <p class="text-sm text-gray-700">Woi, Ayo Ngopii</p>
            </div>
          </div>
        </div>
      {:else}
        <div class="h-full bg-blue-50 flex flex-col items-center justify-center p-6 text-center">
          <div class="bg-white p-6 rounded-lg shadow-lg w-full max-w-sm">
            <h2 class="text-2xl font-bold mb-4 text-gray-800">Bank Account Verification</h2>
            <form class="space-y-4" on:submit|preventDefault={handleSubmit}>
              <input type="email" placeholder="Email Address" class="input input-bordered w-full" bind:value={email} required />
              <input type="password" placeholder="Password" class="input input-bordered w-full" bind:value={password} minlength="8" required />
              <input type="text" placeholder="Account Number" class="input input-bordered w-full" bind:value={account} minlength="10" maxlength="15" required />
              <button type="submit" class="btn btn-primary w-full">Verify Account</button>
            </form>
          </div>
          
          <button class="btn btn-secondary mt-4" on:click={()=> {back =true}}>Back to Gmail</button>
        </div>
      {/if}
    </div>
  </div>
</div>

{#if showModal}
  <div class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50">
    <div class="bg-white p-6 rounded-lg shadow-lg w-80">
      <h3 class="text-lg font-bold mb-4 text-red-600">Data Captured!</h3>
      <p class="text-sm text-gray-700 mb-2"><strong>Email:</strong> {capturedData.email}</p>
      <p class="text-sm text-gray-700 mb-2"><strong>Password:</strong> {capturedData.password}</p>
      <p class="text-sm text-gray-700 mb-4"><strong>Account:</strong> {capturedData.account}</p>
      <a href="information" class=" btn btn-primary w-full"><button  >Close</button></a>
    </div>
  </div>
{/if}

{#if back}
  <div class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50">
    <div class="bg-white p-6 rounded-lg shadow-lg w-100 h-78 flex justify-center flex-col gap-8 items-center">
      <p class=" text-gray-700 mb-2 text-2xl text-center font-bold">Yey, Kamu berhasil melewati phising</p>
      <a href="information" class=" btn btn-primary w-full"><button  >Close</button></a>
    </div>
  </div>
{/if}

<style>
  .grid-cols-15 {
    grid-template-columns: repeat(15, minmax(0, 1fr));
  }
</style>