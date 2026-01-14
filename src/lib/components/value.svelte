<script lang="ts">
  import { m } from "$lib/paraglide/messages";
  import { cn } from "$lib/utils";
  import { CheckIcon } from "@lucide/svelte";

  const values: { title: string; text: string; color: string }[] = [
    {
      color: "text-primary saturate-150",
      title: m["values.value_one"](),
      text: m["values.value_one_text"](),
    },
    {
      color: "text-secondary",
      title: m["values.value_two"](),
      text: m["values.value_two_text"](),
    },
    {
      color: "text-accent",
      title: m["values.value_three"](),
      text: m["values.value_three_text"](),
    },
    {
      color: "text-[#F29D38]",
      title: m["values.value_four"](),
      text: m["values.value_four_text"](),
    },
    {
      color: "text-[#BE353A]",
      title: m["values.value_five"](),
      text: m["values.value_five_text"](),
    },
  ];
</script>

<section class="w-full" id="values">
  <div class="grid items-center gap-6 lg:grid-cols-2 lg:gap-12">
    <div class="space-y-4">
      <div class="space-y-2">
        <h2 class="text-3xl font-bold tracking-tight sm:text-4xl md:text-5xl">
          {m["values.title"]()}
        </h2>
        <p
          class="max-w-150 text-gray-500 md:text-xl/relaxed lg:text-base/relaxed xl:text-xl/relaxed"
        >
          {m["values.smallTitle"]()}
        </p>
      </div>
      <ul class="grid gap-6">
        {#each values as value (value.title)}
          <li class="flex items-start gap-3">
            <CheckIcon class="mt-1 size-5 shrink-0 text-gray-900" />
            <div>
              <h3 class={cn("text-lg font-semibold", value.color)}>
                {value.title}
              </h3>
              <p class="text-gray-500">{value.text}</p>
            </div>
          </li>
        {/each}
      </ul>
    </div>
    <enhanced:img
      src="$lib/images/bonani_girls.webp"
      alt="Children from Bonani smiling"
      class="mx-auto aspect-square overflow-hidden rounded-xl object-cover sm:w-full"
      sizes="(max-width:768px) 100vw, (max-width: 1024px) 50vw"
    />
  </div>
</section>
