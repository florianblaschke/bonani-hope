<script>
  import { m } from "$lib/paraglide/messages";
  import { Cross, GraduationCap, PersonStanding } from "@lucide/svelte";
</script>

<section class="w-full">
  <div class="grid grid-cols-1 md:grid-cols-3 gap-6 md:gap-12 md">
    <div
      class="flex flex-col items-start gap-4 p-6 bg-white rounded-lg shadow-md hover:scale-[102%] transition-all duration-150 ease-in-out"
    >
      <div
        class="bg-primary rounded-md flex items-center justify-center aspect-square w-12"
      >
        <GraduationCap class="size-6" />
      </div>
      <h3 class="text-xl font-semibold">{m["education.title"]()}</h3>
      <p class="text-gray-500">{m["education.text"]()}</p>
    </div>
    <div
      class="flex flex-col items-start gap-4 p-6 bg-white rounded-lg shadow-md hover:scale-[102%] transition-all duration-150 ease-in-out"
    >
      <div
        class="bg-secondary text-primary-foreground rounded-md flex items-center justify-center aspect-square w-12"
      >
        <PersonStanding class="size-6" />
      </div>
      <h3 class="text-xl font-semibold">{m["family.title"]()}</h3>
      <p class="text-gray-500">{m["family.text"]()}</p>
    </div>
    <div
      class="flex flex-col items-start gap-4 p-6 bg-white rounded-lg shadow-md hover:scale-[102%] transition-all duration-150 ease-in-out"
    >
      <div
        class="bg-accent text-primary-foreground rounded-md flex items-center justify-center aspect-square w-12"
      >
        <Cross class="size-6" />
      </div>
      <h3 class="text-xl font-semibold">{m["health.title"]()}</h3>
      <p class="text-gray-500">{m["health.text"]()}</p>
    </div>
  </div>
</section>
