<script>
  import { templeData } from "../data.js";
</script>

<div class=" grid grid-cols-1 md:grid-cols-2 gap-5">
  {#each templeData as temple}
    <div
      class=" w-full flex p-3 gap-5 shadow-md mb-4 bg-white md:p-3 rounded-md"
    >
      <img
        src={temple.image}
        alt=""
        class=" w-[100px] h-[100px] md:w-[100px] md:h-[100px]"
      />
      <div class="">
        <h2 class=" font-semibold text-[14px] md:text-[16px]">
          {temple.title}
        </h2>
        <h3 class=" text-[10px] md:text-[13px] pt-1 pb-2">
          {temple.location}
        </h3>
      </div>
    </div>
  {/each}
</div>
