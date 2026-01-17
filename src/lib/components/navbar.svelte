<script lang="ts">
  import { m } from "$lib/paraglide/messages.js";
  import { getLocale } from "$lib/paraglide/runtime";
  import LocaleSwitcher from "./locale-switcher.svelte";
  import MobileMenu from "./mobile-menu.svelte";
  let locale = getLocale();
  const links = [
    { href: `/${locale}#about`, title: m["navbar.about"]() },
    { href: `/${locale}#values`, title: m["navbar.values"]() },
    { href: `/${locale}#whatwedo`, title: m["navbar.whatwedo"]() },
    { href: `/${locale}#contact`, title: m["navbar.contact"]() },
  ];
</script>

<header class="sticky top-0 z-50 w-full bg-white shadow-sm">
  <div class="flex items-center justify-center">
    <div class="flex h-16 items-center justify-between px-4 md:px-20 w-full">
      <a href="/" class="flex items-center gap-2 w-36 overflow-hidden">
        <enhanced:img src="$lib/images/logo_text.webp" alt="Bonani Logo" />
        <span class="sr-only">Bonani Drop in Centre</span>
      </a>
      <nav class="hidden gap-6 text-sm font-medium md:flex min-w-122.5">
        <LocaleSwitcher />
        {#each links as link (link.href)}
          <a
            href={link.href}
            class="inline-flex items-center gap-1 transition-colors hover:text-gray-900"
          >
            {link.title}
          </a>
        {/each}
      </nav>
      <div class="flex items-center gap-4 md:hidden">
        <div class="md:hidden">
          <LocaleSwitcher />
        </div>
        <MobileMenu />
      </div>
    </div>
  </div>
</header>
