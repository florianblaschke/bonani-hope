<script lang="ts">
  import { m } from "$lib/paraglide/messages";
  import {
    Carrot,
    GraduationCap,
    Paintbrush,
    PersonStanding,
  } from "@lucide/svelte";
</script>

<section class="space-y-4 w-full" id="whatwedo">
  <h2 class="text-3xl font-bold tracking-tight sm:text-4xl md:text-5xl">
    {m["whatwedo.title"]()}
  </h2>
  <div class="space-y-6">
    <div class="grid md:grid-cols-2 gap-8 lg:gap-12 w-full md:min-h-69">
      <div
        class="flex flex-col items-start gap-4 p-6 rounded-lg shadow-md hover:scale-[102%] transition-all duration-150 ease-in-out"
      >
        <div
          class="bg-primary rounded-md flex items-center justify-center aspect-square w-12"
        >
          <GraduationCap class="size-6 text-secondary-foreground" />
        </div>
        <h3 class="text-xl font-semibold">
          {m["whatwedo.school_title"]()}
        </h3>
        <p class="text-gray-500">{m["whatwedo.school_text"]()}</p>
      </div>
      <div
        class="flex flex-col items-start gap-4 p-6 bg-white rounded-lg shadow-md hover:scale-[102%] transition-all duration-150 ease-in-out"
      >
        <div
          class="bg-accent rounded-md flex items-center justify-center aspect-square w-12"
        >
          <Carrot class="size-6 text-primary-foreground" />
        </div>
        <h3 class="text-xl font-semibold">
          {m["whatwedo.kitchen_title"]()}
        </h3>
        <p class="text-gray-500">{m["whatwedo.kitchen_text"]()}</p>
      </div>
    </div>
    <div class="grid md:grid-cols-2 lg:gap-12 gap-8 w-full md:min-h-69">
      <div
        class="flex flex-col items-start gap-4 p-6 bg-white rounded-lg shadow-md hover:scale-[102%] transition-all duration-150 ease-in-out"
      >
        <div
          class="bg-secondary rounded-md flex items-center justify-center aspect-square w-12"
        >
          <PersonStanding class="size-6 text-primary-foreground" />
        </div>
        <h3 class="text-xl font-semibold">
          {m["whatwedo.family_title"]()}
        </h3>
        <p class="text-gray-500">{m["whatwedo.family_text"]()}</p>
      </div>
      <div
        class="flex flex-col items-start gap-4 p-6 bg-white rounded-lg shadow-md hover:scale-[102%] transition-all duration-150 ease-in-out"
      >
        <div
          class="bg-[#F29D38] rounded-md flex items-center justify-center aspect-square w-12"
        >
          <Paintbrush class="size-6 text-primary-foreground" />
        </div>
        <h3 class="text-xl font-semibold">
          {m["whatwedo.arts_title"]()}
        </h3>
        <p class="text-gray-500">{m["whatwedo.arts_text"]()}</p>
      </div>
    </div>
  </div>
</section>
