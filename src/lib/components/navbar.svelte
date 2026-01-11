<script lang="ts">
import { m } from "$lib/paraglide/messages.js";
import { getLocale } from "$lib/paraglide/runtime";
import LocaleSwitcher from "./locale-switcher.svelte";
let locale = getLocale();
const links = [
	{ href: `/${locale}#about`, title: m["navbar.about"]() },
	{ href: `/${locale}#values`, title: m["navbar.values"]() },
	{ href: `/${locale}#whatwedo`, title: m["navbar.whatwedo"]() },
	{ href: `/${locale}#contact`, title: m["navbar.contact"]() },
];
</script>

    <header class="sticky top-0 z-50 w-full bg-white shadow-sm dark:bg-gray-950 dark:text-gray-50">
      <div class="container flex h-16 items-center justify-between px-4 md:px-6">
        <a href="/" class="flex items-center gap-2 w-36 overflow-hidden">
          <img
            src="/logo_text.webp"
            height={1485}
            width={2640}
            alt="Bonani Logo"
            class="object-cover overflow-hidden"
            sizes="(max-width: 768px) 60vw, (max-width: 1024px) 40vw"
          />
          <span class="sr-only">Bonani Drop in Centre</span>
        </a>
        <nav class="hidden gap-6 text-sm font-medium md:flex min-w-[490px]">
          <LocaleSwitcher />
          {#each  links as link(link.href) }
            
            <a
              href={link.href}
              class="inline-flex items-center gap-1 transition-colors hover:text-gray-900 dark:hover:text-gray-50"
            >
              {link.title}
            </a>
          {/each}

        </nav>
        <div class="flex items-center gap-4 md:hidden">
          <div class="md:hidden">
            <LocaleSwitcher />
          </div>
       <!--   <MobileMenu />--->
        </div>
      </div>
    </header>

