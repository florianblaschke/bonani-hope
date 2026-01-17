<script lang="ts">
  import { m } from "$lib/paraglide/messages.js";
  import {
    TooltipProvider,
    TooltipContent,
    TooltipTrigger,
    Tooltip,
  } from "$lib/components/ui/tooltip";
  import Separator from "./ui/separator/separator.svelte";
  import { Mail, Map, Phone, Instagram } from "@lucide/svelte";
</script>

<footer class="bg-gray-100 py-6">
  <div
    class="md:px-20 w-full flex flex-col items-center justify-between gap-4 px-4 sm:flex-row sm:gap-0"
  >
    <div class="flex w-full flex-col items-center gap-2 sm:flex-row sm:gap-4">
      <a
        href="/imprint"
        class="text-sm font-medium text-gray-500 hover:text-gray-900"
      >
        {m["footer.impressum"]()}
      </a>
      <Separator orientation="vertical" class="hidden sm:block" />
      <a
        href="/privacy"
        class="text-sm font-medium text-gray-500 hover:text-gray-900"
      >
        {m["footer.privacy"]()}
      </a>
    </div>
    <div class="flex items-center gap-6 md:gap-12">
      <TooltipProvider>
        <Tooltip>
          <TooltipTrigger>
            <a
              target="_blank"
              href="https://www.google.de/maps/place/Kalinyanga,+Südafrika/@-31.6952403,28.0240882,12.69z/data=!4m6!3m5!1s0x1e604ecfbeae89f1:0xf591f11855426ac2!8m2!3d-31.6853943!4d28.0504864!16s%2Fg%2F1wz3bd5k?entry=ttu"
              class="text-gray-500 hover:text-gray-900"
            >
              <Map />
              <span class="sr-only">{m["footer.location"]()}</span>
            </a>
          </TooltipTrigger>
          <TooltipContent class="tracking-tight text-sm leading-snug">
            {m["footer.location"]()}
          </TooltipContent>
        </Tooltip>
      </TooltipProvider>
      <TooltipProvider>
        <Tooltip>
          <TooltipTrigger>
            <a
              href="tel:+27791357657"
              class="text-gray-500 hover:text-gray-900"
            >
              <Phone />
              <span class="sr-only">{m["footer.phone"]()}</span>
            </a>
          </TooltipTrigger>
          <TooltipContent class="tracking-tight text-sm leading-snug">
            {m["footer.phone"]()}
          </TooltipContent>
        </Tooltip>
      </TooltipProvider>
      <TooltipProvider>
        <Tooltip>
          <TooltipTrigger>
            <a
              href="mailto:bonaniengcobo@gmail.com"
              class="text-gray-500 hover:text-gray-900"
            >
              <Mail />
              <span class="sr-only">{m["footer.mail"]()}</span>
            </a>
          </TooltipTrigger>
          <TooltipContent class="tracking-tight text-sm leading-snug">
            {m["footer.mail"]()}
          </TooltipContent>
        </Tooltip>
      </TooltipProvider>
      <TooltipProvider>
        <Tooltip>
          <TooltipTrigger>
            <a
              target="_blank"
              href="https://www.instagram.com/bonani.ngcobo/"
              class="text-gray-500 hover:text-gray-900"
            >
              <Instagram />
              <span class="sr-only">{m["footer.insta"]()}</span>
            </a>
          </TooltipTrigger>
          <TooltipContent class="tracking-tight text-sm leading-snug">
            {m["footer.insta"]()}
          </TooltipContent>
        </Tooltip>
      </TooltipProvider>
    </div>
  </div>
</footer>
