<script lang="ts">
	import { buttonVariants } from "$lib/components/ui/button";
	import { m } from "$lib/paraglide/messages";
	import { cn } from "$lib/utils";
</script>

<section class="w-full grid items-center gap-8 lg:gap-12 min-h-[75vh]">
	<h1 class="text-lg font-bold tracking-tighter sm:text-3xl md:text-5xl">
		{m["imprint.title"]()}
	</h1>
	<article class="grid gap-4">
		<h2 class="text-lg font-semibold">{m["imprint.company_name"]()}</h2>
		<p class="text-medium font-normal text-gray-500">Bonani Drop in Centre</p>
		<h2 class="text-lg font-semibold">{m["imprint.address"]()}</h2>
		<p class="text-medium font-normal text-gray-500">
			Kalinyanga P.O Box 108 Engcobo, 5050, South Africa
		</p>
		<h2 class="text-lg font-semibold">{m["imprint.represented"]()}</h2>
		<p class="text-medium font-normal text-gray-500">Ayanda Mlahlwa</p>
		<h2 class="text-lg font-semibold">{m["imprint.register.title"]()}</h2>
		<p class=" text-gray-500">Social Development</p>
		<div class="flex items-center gap-2 text-medium font-normal">
			<p class="text-medium font-normal text-gray-500">287-015 NPO</p>
		</div>
	</article>
	<article>
		<h2 class="text-lg font-semibold">{m["imprint.image"]()}</h2>
		<ul class="list-inside list-disc space-y-2">
			<li class="text-medium font-normal">
				<a
					class={cn(
						buttonVariants({
							variant: "link",
						}),
						"px-0 text-base",
					)}
					target="_blank"
					href="https://unsplash.com/de/@anniespratt?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash"
				>
					Annie Spratt
				</a>{" "}
				on{" "}
				<a
					class={cn(
						buttonVariants({
							variant: "link",
						}),
						"px-0 text-base",
					)}
					target="_blank"
					href="https://unsplash.com/de/fotos/gruppe-von-kinderfotografie-cVEOh_JJmEE?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash"
				>
					Unsplash
				</a>
			</li>
			<li class="text-medium font-normal">
				<a
					class={cn(
						buttonVariants({
							variant: "link",
						}),
						"px-0 text-base",
					)}
					target="_blank"
					href="https://unsplash.com/de/@ban_yido?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash"
				>
					Ban Yido
				</a>{" "}
				on{" "}
				<a
					class={cn(
						buttonVariants({
							variant: "link",
						}),
						"px-0 text-base",
					)}
					target="_blank"
					href="https://unsplash.com/de/fotos/silhouette-von-kindern-UmC0aBfur5c?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash"
				>
					Unsplash
				</a>
			</li>
		</ul>
	</article>
	<article class="space-y-2">
		<p class="text-base font-semibold">
			Homepage and Design by Florian Blaschke
		</p>
		<div class="flex flex-col md:flex-row gap-4 md:items-center">
			<p class="flex gap-1 text-medium font-normal">
				Visit:
				<a
					href="https://florianblaschke.me"
					target="_blank"
					class="hover:underline text-gray-500"
				>
					florianblaschke.me
				</a>
			</p>
		</div>
	</article>
</section>
