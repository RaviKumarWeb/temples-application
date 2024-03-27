<script>
  // State to manage dropdown visibility

  let isDropdownOpen = false;
  let isMenuOpen = false;

  // Function to open the dropdown menu
  function openDropdown() {
    isDropdownOpen = true;
  }

  // Function to close the dropdown menu
  function closeDropdown() {
    isDropdownOpen = false;
  }

  // Function to toggle the mobile menu
  function toggleMenu() {
    isMenuOpen = !isMenuOpen;
  }

  function openPopup() {
    isPopupOpen = true;
  }

  function closePopup() {
    isPopupOpen = false;
  }
</script>

<nav class="flex items-center justify-between p-3 px-5 shadow-md">
  <div class="order-2 lg:order-1 flex items-center gap-2">
    <!-- svelte-ignore a11y-img-redundant-alt -->
    <img
      src="https://templesofindia.org/assets/images/tofi_logo/tofi-logo_navbar.png"
      alt="logo image"
      class="md:w-[50px] lg:w-[80px]"
    />
    <h2 class="font-semibold text-[16px] md:text-xl lg:text-2xl">
      Temples of India
    </h2>
  </div>

  <ul class="hidden lg:flex lg:order-1 items-center gap-5">
    <li>
      <a
        href="/"
        class="font-semibold text-xl transition-all duration-300 hover:bg-gray-300 rounded-md p-4"
        >Home</a
      >
    </li>

    <li>
      <a
        href="/search"
        class="font-semibold text-xl transition-all duration-300 hover:bg-gray-300 rounded-md p-4"
        >Search</a
      >
    </li>
    <li>
      <a
        href="/nearbyTemples"
        class="font-semibold text-xl transition-all duration-300 hover:bg-gray-300 rounded-md p-4"
        >Nearby Temples</a
      >
    </li>
    <li>
      <a
        href="/addTemple"
        class="font-semibold text-xl transition-all duration-300 hover:bg-gray-300 rounded-md p-4"
        >Add Temples</a
      >
    </li>
    <li>
      <a
        href="/about"
        class="font-semibold text-xl transition-all duration-300 hover:bg-gray-300 rounded-md p-4"
        >About us</a
      >
    </li>

    <li class="relative" on:mouseenter={openDropdown}>
      <button class="bg-blue-500 text-white px-4 py-2 rounded-md">
        Login/Register
      </button>

      {#if isDropdownOpen}
        <!-- svelte-ignore a11y-no-static-element-interactions -->
        <div
          class="absolute right-0 mt-2 w-48 bg-white rounded-md shadow-lg"
          on:mouseleave={closeDropdown}
        >
          <a
            href="/login"
            class="block px-4 py-2 text-gray-800 hover:bg-gray-200 font-semibold"
            >Login</a
          >
          <a
            href="/register"
            class="block px-4 py-2 text-gray-800 hover:bg-gray-200 font-semibold"
            >Register</a
          >
        </div>
      {/if}
    </li>
  </ul>

  <!-- Menu Button for Mobile -->
  <button class="order-1 text-2xl lg:hidden" on:click={toggleMenu}>
    <i class="fa-solid fa-bars"></i>
  </button>
  <button class="order-3 text-2xl lg:hidden">
    <i class="fa-solid fa-magnifying-glass"></i>
  </button>

  <!-- Responsive Menu -->
  <div
    class="lg:hidden h-screen flex flex-col absolute left-0 top-0 bg-white w-56 shadow-lg transform transition-transform duration-300"
    style="transform: translateX({isMenuOpen ? '0%' : '-100%'})"
  >
    <button class=" self-end text-2xl p-3" on:click={toggleMenu}>
      <i class="fa-solid fa-xmark"></i>
    </button>
    <!-- svelte-ignore a11y-no-noninteractive-element-interactions -->
    <ul class="flex flex-col items-start justify-center gap-7 p-5">
      <!-- svelte-ignore a11y-click-events-have-key-events -->
      <li
        class=" flex items-center gap-3 text-[18px] pb-4 font-semibold border-b-[1px] border-gray-200 w-full"
        on:click={toggleMenu}
      >
        <i class="fa-solid fa-house"></i>
        <a href="/" class="">Home</a>
      </li>
      <!-- svelte-ignore a11y-click-events-have-key-events -->
      <li
        class=" flex items-center gap-3 text-[18px] pb-4 font-semibold border-b-[1px] border-gray-200 w-full"
        on:click={toggleMenu}
      >
        <i class="fa-solid fa-key"></i>
        <a href="/login" class="">Login</a>
      </li>
      <!-- svelte-ignore a11y-click-events-have-key-events -->
      <li
        class=" flex items-center gap-3 text-[18px] pb-4 font-semibold border-b-[1px] border-gray-200 w-full"
        on:click={toggleMenu}
      >
        <i class="fa-solid fa-hands-praying"></i>
        <a href="/nearbyTemples" class="">Nearby Temples</a>
      </li>
      <!-- svelte-ignore a11y-click-events-have-key-events -->
      <li
        class=" flex items-center gap-3 text-[18px] pb-4 font-semibold border-b-[1px] border-gray-200 w-full"
        on:click={toggleMenu}
      >
        <i class="fa-solid fa-plus"></i>

        <a href="/addTemple" class="">Add Temples</a>
      </li>
      <!-- svelte-ignore a11y-click-events-have-key-events -->
      <li
        class=" flex items-center gap-3 text-[18px] pb-4 font-semibold border-b-[1px] border-gray-200 w-full"
        on:click={toggleMenu}
      >
        <i class="fa-solid fa-info"></i>

        <a href="/about" class="">About Us</a>
      </li>
    </ul>
  </div>
</nav>
