<script>
  import { templeData } from "../data.js";
</script>

<div class=" mb-10">
  <div class=" h-[50vh] flex gap-10 overflow-x-scroll no-scrollbar">
    {#each templeData as temple}
      <img src={temple.image} alt="" class=" w-[100%] rounded-md" />
    {/each}
  </div>
</div>
