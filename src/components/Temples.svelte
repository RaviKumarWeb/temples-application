<script>
  import { templeData } from "../data.js";
</script>

<div
  class=" order-3 lg:order-2 basis-[40%] h-[100vh] overflow-y-scroll no-scrollbar"
>
  <!-- svelte-ignore a11y-missing-attribute -->
  <div class="">
    {#each templeData as temple}
      <!-- svelte-ignore a11y-missing-content -->
      <a href={`temple/${temple.id}`} class="">
        <div class=" shadow-md mb-4 bg-white p-5 rounded-md">
          <h2 class=" font-semibold text-xl">{temple.title}</h2>
          <h3 class=" text-[16px] pt-1 pb-2">{temple.location}</h3>
          <img src={temple.image} alt="" class=" w-[100%]" />
          <p class=" text-[14px] font-semibold pt-3">
            {temple.description}
          </p>
        </div>
      </a>
    {/each}
  </div>
</div>
