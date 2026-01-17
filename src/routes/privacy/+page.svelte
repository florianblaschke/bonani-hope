<script lang="ts">
  import { m } from "$lib/paraglide/messages";
</script>

<svelte:head>
  <title>Privacy</title>
</svelte:head>

<section class="grid items-center gap-8 lg:gap-12">
  <h1 class="text-2xl font-bold tracking-tighter sm:text-3xl md:text-5xl">
    {m["privacy.title"]()}
  </h1>
  <ul class="grid gap-8 list-inside list-decimal">
    <li class="text-lg font-semibold">
      <h2>{m["privacy.introduction.title"]()}</h2>
      <p class="text-medium font-normal text-gray-500">
        {m["privacy.introduction.text"]()}
      </p>
    </li>
    <li class="text-lg font-semibold">
      <h2>{m["privacy.data.title"]()}</h2>
      <p class="text-medium font-normal text-gray-500">
        {m["privacy.data.text"]()}
      </p>
    </li>
    <li class="text-lg font-semibold">
      <h2 class="pb-6">{m["privacy.language.title"]()}</h2>
      <ul class="grid gap-6 list-disc list-inside pl-6">
        <li class="text-lg font-semibold">
          <h3>{m["privacy.language.bulletpoint_one_title"]()}</h3>
          <p class="text-medium font-normal text-gray-500">
            {m["privacy.language.bulletpoint_one"]()}
          </p>
        </li>
        <li class="text-lg font-semibold">
          <h3>{m["privacy.language.bulletpoint_two_title"]()}</h3>
          <p class="text-medium font-normal text-gray-500">
            {m["privacy.language.bulletpoint_two"]()}
          </p>
        </li>
        <li class="text-lg font-semibold">
          <h3>{m["privacy.language.bulletpoint_three_title"]()}</h3>
          <p class="text-medium font-normal text-gray-500">
            {m["privacy.language.bulletpoint_three"]()}
          </p>
        </li>
      </ul>
    </li>
    <li class="text-lg font-semibold">
      <h2>{m["privacy.security.title"]()}</h2>
      <p class="text-medium font-normal text-gray-500">
        {m["privacy.security.text"]()}
      </p>
    </li>
    <li class="text-lg font-semibold">
      <h2>{m["privacy.thirdParty.title"]()}</h2>
      <p class="text-medium font-normal text-gray-500">
        {m["privacy.thirdParty.text"]()}
      </p>
    </li>
    <li class="text-lg font-semibold">
      <h2>{m["privacy.rights.title"]()}</h2>
      <p class="text-medium font-normal text-gray-500">
        {m["privacy.rights.text"]()}
      </p>
    </li>
    <li class="text-lg font-semibold">
      <h2>{m["privacy.changes.title"]()}</h2>
      <p class="text-medium font-normal text-gray-500">
        {m["privacy.changes.text"]()}
      </p>
    </li>
    <li class="text-lg font-semibold">
      <h2>{m["privacy.contact.title"]()}</h2>
      <p class="text-medium font-normal text-gray-500">
        {m["privacy.contact.text"]()}
      </p>
    </li>
  </ul>
</section>
