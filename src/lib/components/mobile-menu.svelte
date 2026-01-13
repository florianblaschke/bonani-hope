<script lang="ts">
  import { SheetTrigger, Sheet, SheetContent } from "$lib/components/ui/sheet";
  import { MenuIcon } from "@lucide/svelte";
  import { m } from "$lib/paraglide/messages";

  const links = [
    { href: "#about", title: m["navbar.about"]() },
    { href: "#values", title: m["navbar.values"]() },
    { href: "#whatwedo", title: m["navbar.whatwedo"]() },
    { href: "#contact", title: m["navbar.contact"]() },
  ];

  let open = $state(false);
</script>

<Sheet bind:open>
  <SheetTrigger>
    <MenuIcon />
    <span class="sr-only">Toggle navigation</span>
  </SheetTrigger>
  <SheetContent side="right">
    <nav class="grid gap-6 text-lg font-medium">
      {#each links as link (link.href)}
        <a
          onclick={() => (open = false)}
          href={link.href}
          class="inline-flex items-center gap-1 transition-colors hover:text-gray-900 dark:hover:text-gray-50"
        >
          {link.title}
        </a>
      {/each}
    </nav>
  </SheetContent>
</Sheet>
