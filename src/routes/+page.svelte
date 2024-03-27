<script>
  import Temples from "../components/Temples.svelte";
  import { templePosts, templeTags } from "../data.js";
</script>

<main class=" min-h-screen bg-gray-100">
  <!-- Hero section -->
  <div
    class=" bg-[#FFDC60] flex flex-col items-center lg:flex-row justify-around py-10"
  >
    <img
      src="https://www.templesofindia.org/assets/images/NewHomeTemple.png"
      alt=""
      class=" order-2 lg:order-1 mt-8 w-[250px] md:w-[500px] lg:w-fit"
    />
    <div class=" lg:order-2 flex flex-col items-center text-center gap-5">
      <h1
        class=" tracking-wide text-[35px] md:text-[40px] lg:text-[45px] text-[#A4213C] w-[80%] lg:w-full"
      >
        <span class=" font-bold">7,50,000</span> Plus Temples and Counting ...
      </h1>
      <button
        class=" p-4 px-8 md:px-10 bg-[#A4213C] rounded-md font-semibold text-white text-xl transition-all duration-300 hover:bg-orange-900"
        >Add Temple</button
      >
    </div>
  </div>
  <!-- Hero section -->

  <section class="py-10">
    <div
      class=" w-[90%] mx-auto flex flex-col items-center md:items-start lg:flex-row justify-between gap-5"
    >
      <div class=" flex flex-row lg:flex-col gap-5 basis-[20%]">
        <img
          src="https://www.templesofindia.org/assets/images/newFeatured.png"
          alt=""
          class=" w-[50%] lg:w-[70%]"
        />

        <img
          src="https://www.templesofindia.org/assets/images/newRecentlyEdited.png"
          alt=""
          class=" w-[50%] lg:w-[70%]"
        />
      </div>

      <Temples />

      <div class="right-side order-2 lg:order-3 basis-[20%]">
        <div class=" mb-5">
          <h3 class=" text-2xl font-semibold tracking-wide">Posts</h3>
          <div class=" flex flex-col md:flex-row md:flex-wrap md:gap-4 gap-1">
            {#each templePosts as post}
              <a
                href="/"
                class=" border-b-[1px] border-black p-1 text-[12px] md:text-[14px] lg:text-[16px] font-[500]"
              >
                <p>{post.title}</p>
              </a>
            {/each}
          </div>
        </div>

        <div class=" flex flex-wrap items-center gap-4">
          {#each templeTags as tags}
            <a
              href="/"
              class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold"
            >
              {tags.title}
            </a>
          {/each}
        </div>
      </div>
    </div>
  </section>
</main>
