<script>
  import SearchTemples from "../../components/SearchTemples.svelte";
</script>

<section class=" min-h-screen py-10">
  <div class=" flex flex-col lg:flex-row gap-5">
    <div class=" lg:basis-[50%]">
      <!-- svelte-ignore a11y-missing-attribute -->
      <iframe
        src="https://www.google.com/maps/embed?pb=!1m16!1m12!1m3!1d121807.9652198087!2d78.44003815255019!3d17.435818921784552!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!2m1!1stemples%20in%20hyderabad%20!5e0!3m2!1sen!2sin!4v1711519130756!5m2!1sen!2sin"
        class=" h-[40vh] lg:h-screen w-full"
        style="border:0;"
        allowfullscreen=""
        loading="lazy"
        referrerpolicy="no-referrer-when-downgrade"
      ></iframe>s
    </div>
    <div class=" basis-[50%]">
      <SearchTemples />
      <SearchTemples />
    </div>
  </div>
</section>
