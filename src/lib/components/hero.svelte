<script lang="ts">
  import { m } from "$lib/paraglide/messages";
</script>

<section class="relative w-full h-[80vh] min-h-125 overflow-hidden">
  <enhanced:img
    src="$lib/images/ban_yido.webp"
    alt="Hero Image"
    class="object-cover object-center rounded-xl"
    sizes="100vw"
    placeholder="blur"
  />
  <div class="absolute inset-0 bg-black/50 z-10 rounded-xl"></div>
  <div
    class="absolute inset-0 flex flex-col items-center justify-center z-20 px-4 text-center text-white"
  >
    <h1 class="text-4xl font-bold sm:text-5xl md:text-6xl">
      {m["headline.title"]()}
    </h1>
    <p class="mt-3 text-lg/relaxed sm:text-xl/relaxed md:text-2xl/relaxed">
      {m["headline.subtitle"]()}
    </p>
  </div>
</section>
