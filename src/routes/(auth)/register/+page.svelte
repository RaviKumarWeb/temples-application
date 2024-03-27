<script></script>

<main class=" min-h-screen bg-gray-200">
  <div class="py-10 flex flex-col lg:flex-row gap-10">
    <div class=" flex items-center justify-center flex-col basis-[50%]">
      <img
        src="https://www.templesofindia.org/assets/images/tofi_logo/tofi-logo.png"
        alt=""
        class=""
      />
      <h1 class=" text-2xl md:text-4xl lg:text-6xl font-semibold tracking-wide">
        Download on Play Store
      </h1>
    </div>
    <div
      class=" w-[90%] md:w-[70%] lg:w-[100%] mx-auto shadow-md bg-gray-100 p-5 rounded-md basis-[30%]"
    >
      <div class=" flex flex-col py-10">
        <button
          class=" self-center flex justify-between items-center gap-3 bg-blue-600 rounded-md py-3 px-10 text-white transition-all duration-300 hover:bg-blue-900"
          ><i class="fa-brands fa-google"></i> Sign up with google</button
        >

        <div class=" flex items-center justify-center gap-2 py-10">
          <div class=" h-[1px] bg-gray-200 w-[50%]"></div>
          <p class=" text-[16px]">or</p>
          <div class=" h-[1px] bg-gray-200 w-[50%]"></div>
        </div>

        <form
          action=""
          class=" flex flex-col gap-5 w-[90%] mx-auto font-semibold"
        >
          <input
            type="name"
            placeholder="Name"
            class=" py-3 rounded-md px-5 bg-white shadow-md"
          />
          <input
            type="email"
            placeholder="Email"
            class=" py-3 rounded-md px-5 bg-white shadow-md"
          />

          <div class=" flex items-center gap-3">
            <select class="py-3 px-5 rounded-md" name="" id="">
              <option class=" py-2 px-5 text-[16px]" value="+91">+91</option>
              <option class=" py-2 px-5 text-[16px]" value="+72">+72</option>
              <option class=" py-2 px-5 text-[16px]" value="+73">+73</option>
              <option class=" py-2 px-5 text-[16px]" value="+63">+63</option>
            </select>
            <input
              type="phone"
              class=" py-3 px-5 w-full shadow-md rounded-md"
              placeholde="Phone"
            />
          </div>

          <input
            type="password"
            placeholder="Password"
            class=" py-3 rounded-md px-5 bg-white shadow-md"
          />

          <button
            class=" self-center py-3 px-8 rounded-full text-white bg-[#ff4678] text-[16px] font-semibold transition-all duration-300 hover:bg-sky-800"
            >Signup</button
          >
        </form>

        <p class=" flex justify-between items-center py-8 font-semibold">
          Already have and account? <a
            href="/login"
            class=" transition-all duration-300 hover:underline">Login</a
          >
        </p>
      </div>
    </div>
  </div>
</main>
