<script>
  import { m } from "$lib/paraglide/messages";
  import {
    CreditCard,
    HeartHandshake,
    MailIcon,
    MapPinIcon,
    PhoneIcon,
  } from "@lucide/svelte";
  import {
    Popover,
    PopoverTrigger,
    PopoverContent,
  } from "$lib/components/ui/popover";
</script>

<section class="w-full" id="contact">
  <div class="grid items-center gap-6 lg:grid-cols-2 lg:gap-12">
    <enhanced:img
      src="$lib/images/lunathi_w_kids.webp"
      alt="Children from Bonani smiling"
      class="mx-auto aspect-square overflow-hidden rounded-xl object-cover sm:w-full object-top"
      sizes="(max-width:768px) 100vw, (max-width: 1024px) 50vw"
    />
    <div class="grid gap-4 space-y-4">
      <div class="space-y-2">
        <div class="inline-block rounded-lg bg-primary px-3 py-1 text-sm">
          {m["contact.smallTitle"]()}
        </div>
        <h2 class="text-3xl font-bold tracking-tight sm:text-4xl md:text-5xl">
          {m["contact.title"]()}
        </h2>
      </div>
      <ul class="grid gap-6">
        <li>
          <a
            target="_blank"
            href="https://www.google.de/maps/place/Kalinyanga,+Südafrika/@-31.6952403,28.0240882,12.69z/data=!4m6!3m5!1s0x1e604ecfbeae89f1:0xf591f11855426ac2!8m2!3d-31.6853943!4d28.0504864!16s%2Fg%2F1wz3bd5k?entry=ttu"
            class="flex items-center gap-6 hover:text-gray-900 text-gray-500 md:text-xl/relaxed lg:text-base/relaxed xl:text-xl/relaxed"
          >
            <MapPinIcon />
            <span class="">Kalinyanga, Engcobo, 5050</span>
          </a>
        </li>
        <li>
          <a
            href="tel:+27791357657"
            class="flex items-center gap-6 hover:text-gray-900 text-gray-500 md:text-xl/relaxed lg:text-base/relaxed xl:text-xl/relaxed"
          >
            <PhoneIcon />
            <span class="">+27 791357657</span>
          </a>
        </li>
        <li>
          <a
            href="mailto:bonaniengcobo@gmail.com"
            class="flex items-center gap-6 hover:text-gray-900 text-gray-500 md:text-xl/relaxed lg:text-base/relaxed xl:text-xl/relaxed"
          >
            <MailIcon />
            <span>bonaniengcobo@gmail.com</span>
          </a>
        </li>
      </ul>
      <div class="space-y-4">
        <div class="space-y-2">
          <div class="inline-block rounded-lg bg-accent px-3 py-1 text-sm">
            {m["donate.smallTitle"]()}
          </div>
          <h2 class="text-3xl font-bold tracking-tight sm:text-4xl md:text-5xl">
            {m["donate.title"]()}
          </h2>
        </div>
      </div>
      <a
        href="https://www.paypal.com/donate/?hosted_button_id=GB24WD2PTVEXQ"
        target="_blank"
        class="hover:text-gray-900 text-gray-500 md:text-xl/relaxed lg:text-base/relaxed xl:text-xl/relaxed dark:text-gray-400 flex items-center gap-6"
      >
        <HeartHandshake />
        {m["donate.paypal"]()}
      </a>
      <Popover>
        <PopoverTrigger
          class="hover:text-gray-900 text-gray-500 md:text-xl/relaxed lg:text-base/relaxed xl:text-xl/relaxed  flex items-center gap-6"
        >
          <CreditCard />
          <span>{m["donate.bank"]()}</span>
        </PopoverTrigger>
        <PopoverContent
          align="start"
          class="whitespace-nowrap w-fit text-gray-900 md:text-xl/relaxed lg:text-base/relaxed xl:text-xl/relaxed "
        >
          <p>HOSA e.V.</p>
          <p>Evangelische Kreditgenossenschaft</p>
          <p>IBAN: DE 1852 0604 1000 0080 4878</p>
          <p>BIC: GENODEF1EK1</p>
          <p>{m["donate.payment"]()}: 7100 Bonani</p>
        </PopoverContent>
      </Popover>
    </div>
  </div>
</section>
