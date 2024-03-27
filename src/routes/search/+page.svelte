<script>
  import SearchTemples from "../../components/SearchTemples.svelte";
  import { indiaStates } from "../../data.js";
</script>

<section class="">
  <div class=" bg-[#FFE27C4D] p-5">
    <h1 class=" text-2xl md:text-3xl lg:text-4xl font-semibold">
      Search Temples
    </h1>
  </div>

  <div class="p-5 w-[90%] mx-auto">
    <div
      class=" w-[100%] lg:w-[50%] mx-auto flex items-center justify-between gap-3 py-3 px-3 border rounded-md"
    >
      <input
        type="search"
        placeholder=" Search Temples..."
        class=" outline-none w-full"
      />
      <button>
        <i class="fa-solid fa-magnifying-glass"></i>
      </button>
    </div>

    <div class=" flex gap-5 py-20">
      <div class="hidden basis-[30%] lg:block">
        <div
          class=" flex flex-col gap-5 h-[50vh] overflow-y-scroll no-scrollbar border p-5 rounded-md"
        >
          {#each indiaStates as state}
            <div class=" flex items-center gap-2">
              <input type="checkbox" class=" w-[20px] h-[20px]" id={state.id} />
              <label for={state.id} class=" text-[14px]">{state.name}</label>
            </div>
          {/each}
        </div>
      </div>
      <div class=" ">
        <SearchTemples />
      </div>
    </div>
  </div>
</section>
