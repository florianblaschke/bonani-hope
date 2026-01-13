<script>
  import { m } from "$lib/paraglide/messages";
</script>

<section class="w-full" id="about">
  <div class="grid items-center gap-8 lg:grid-cols-2 lg:gap-12">
    <div class="space-y-4">
      <div class="space-y-2">
        <div class="inline-block rounded-lg bg-primary px-3 py-1 text-sm">
          {m["about.smallTitle"]()}
        </div>
        <h2 class="text-3xl font-bold tracking-tight sm:text-4xl md:text-5xl">
          {m["about.title"]()}
        </h2>
      </div>
      <p
        class="max-w-150 text-gray-500 md:text-xl/relaxed lg:text-base/relaxed xl:text-xl/relaxed dark:text-gray-400"
      >
        {m["about.text"]()}
      </p>
    </div>
    <div class="relative">
      <enhanced:img
        src="$lib/images/annie_pratt.webp"
        alt="African Kids smiling"
        class="aspect-video overflow-hidden rounded-xl object-cover w-full"
      />
    </div>
  </div>
</section>
