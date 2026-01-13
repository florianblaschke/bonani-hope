<script lang="ts">
import { page } from "$app/state";
import { locales, localizeHref } from "$lib/paraglide/runtime";
import "./layout.css";
import favicon from "$lib/assets/favicon.svg";
import Navbar from "$lib/components/navbar.svelte";
import Footer from "$lib/components/footer.svelte";

let { children } = $props();
</script>

<svelte:head><link rel="icon" href={favicon} /></svelte:head>
<Navbar/>
  <main class="px-4 md:px-8 py-5 md:py-10">
    <div class="max-w-screen-xl mx-auto flex flex-col items-center gap-12 md:gap-24 xl:gap-32">
			{@render children()}
		</div>
	</main>

<Footer/>
<div style="display:none">
	{#each locales as locale}
		<a
			href={localizeHref(page.url.pathname, { locale })}
		>
			{locale}
		</a>
	{/each}
</div>
