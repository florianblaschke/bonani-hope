<script>
  import Contact from "$lib/components/contact.svelte";
  import CookieBanner from "$lib/components/cookie-banner.svelte";
  import Goals from "$lib/components/goals.svelte";
  import Hero from "$lib/components/hero.svelte";
  import SectionLeft from "$lib/components/section-left.svelte";
  import SectionRight from "$lib/components/section-right.svelte";
  import Value from "$lib/components/value.svelte";
  import Whatwedo from "$lib/components/whatwedo.svelte";
</script>

<svelte:head>
  <title>Bonani Ngcobo</title>
</svelte:head>

<Hero />
<SectionLeft />
<SectionRight />
<Goals />
<Value />
<Whatwedo />
<Contact />
<CookieBanner />
