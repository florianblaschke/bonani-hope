<script lang="ts">
  import { SheetTrigger, Sheet, SheetContent } from "$lib/components/ui/sheet";
  import { Button } from "$lib/components/ui/button";
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
    <Button variant="outline" size="icon" class="hover:bg-primary md:hidden">
      <MenuIcon />
      <span class="sr-only">Toggle navigation</span>
    </Button>
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
