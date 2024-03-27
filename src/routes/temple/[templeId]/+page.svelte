<script>
  import { templeDetails } from "../../../data.js";
  import { page } from "$app/stores";
  import Slider from "../../../components/Slider.svelte";
  const templeId = $page.params.templeId;

  import { onMount } from "svelte";

  let specialFeaturesVisible = {};

  function toggleSpecialFeatures(featureName) {
    specialFeaturesVisible[featureName] = !specialFeaturesVisible[featureName];
  }
</script>

<section class=" min-h-screen py-10 w-[90%] mx-auto">
  <Slider />

  <div class=" flex items-center justify-between">
    <div class="">
      <h1 class=" text-xl">{templeDetails.name}</h1>
      <h3 class=" text-[16px]">{templeDetails.godName}</h3>
    </div>

    <div class=" flex items-center gap-3">
      <button class=" flex flex-col items-center gap-2">
        <i class="fa-solid fa-hands-praying"></i>
        <h3>Visited</h3>
      </button>
      <button class=" flex flex-col items-center gap-2">
        <i class="fa-solid fa-heart"></i>
        Favorite
      </button>
    </div>
  </div>

  <div class=" flex flex-col lg:flex-row gap-4 mt-10">
    <div class=" basis-[70%] flex flex-col gap-3">
      <div class="">
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <!-- svelte-ignore a11y-no-noninteractive-element-interactions -->
        <h1
          class=" text-xl cursor-pointer"
          on:click={() => toggleSpecialFeatures(0)}
        >
          {#if specialFeaturesVisible[0]}
            <i class="fa-solid fa-angle-down"></i>
          {/if}
          {#if !specialFeaturesVisible[0]}
            <i class="fa-solid fa-chevron-right"></i>
          {/if}
          Special Features
        </h1>
        {#if specialFeaturesVisible[0]}
          <p class=" text-[16px]">
            {templeDetails.specialFeatures}
          </p>
        {/if}
      </div>
      <div class="">
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <!-- svelte-ignore a11y-no-noninteractive-element-interactions -->
        <h1
          class=" text-xl cursor-pointer"
          on:click={() => toggleSpecialFeatures(1)}
        >
          {#if specialFeaturesVisible[1]}
            <i class="fa-solid fa-angle-down"></i>
          {/if}
          {#if !specialFeaturesVisible[1]}
            <i class="fa-solid fa-chevron-right"></i>
          {/if}
          Special Features
        </h1>
        {#if specialFeaturesVisible[1]}
          <p class=" text-[16px]">
            {templeDetails.specialFeatures}
          </p>
        {/if}
      </div>
      <div class="">
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <!-- svelte-ignore a11y-no-noninteractive-element-interactions -->
        <h1
          class=" text-xl cursor-pointer"
          on:click={() => toggleSpecialFeatures(2)}
        >
          {#if specialFeaturesVisible[2]}
            <i class="fa-solid fa-angle-down"></i>
          {/if}
          {#if !specialFeaturesVisible[2]}
            <i class="fa-solid fa-chevron-right"></i>
          {/if}
          Festvails
        </h1>
        {#if specialFeaturesVisible[2]}
          <p class=" text-[16px]">
            {templeDetails.specialFeatures}
          </p>
        {/if}
      </div>
    </div>

    <div class=" basis-[30%] border font-semibold rounded-md">
      <div class=" p-5">
        <h1 class=" text-xl font-semibold">Location</h1>

        <h3>MDR782, Agarapettai, Tamil Nadu 613104, India</h3>
      </div>

      <div class=" mt-5">
        <!-- svelte-ignore a11y-missing-attribute -->
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m26!1m12!1m3!1d3944310.4159974633!2d76.15116885034523!3d15.11073200049566!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!4m11!3e6!4m5!1s0x3bcb99daeaebd2c7%3A0xae93b78392bafbc2!2sHyderabad%2C%20Telangana!3m2!1d17.406498!2d78.47724389999999!4m3!3m2!1d12.8467884!2d79.7001106!5e0!3m2!1sen!2sin!4v1711525746385!5m2!1sen!2sin"
          class=" w-full h-[300px]"
          style="border:0;"
          allowfullscreen=""
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"
        ></iframe>
      </div>

      <div class=" mt-5 p-5">
        <h1 class=" text-xl">Open Timiings</h1>
        <p>Alldays : 05:30 am - 10:00 pm</p>
      </div>

      <div class=" mt-5 p-5">
        <h1>Contact Details</h1>

        <p>Name</p>
        <p>Phone +91- 44-2722 2084</p>
        <p>Website</p>
      </div>
    </div>
  </div>
</section>
