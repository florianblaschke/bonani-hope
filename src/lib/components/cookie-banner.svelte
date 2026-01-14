<script lang="ts">
  import { m } from "$lib/paraglide/messages";
  import {
    Card,
    CardContent,
    CardFooter,
    CardHeader,
    CardTitle,
  } from "$lib/components/ui/card";
  import { CookieIcon } from "@lucide/svelte";
  import { Button, buttonVariants } from "./ui/button";
  import { Label } from "./ui/label";
  let consent = false;
  // action={async () => {
  //   cookies().set("language_consent", "true", {
  //     maxAge: 60 * 60 * 24 * 30,
  //   });
  // }}
</script>

{#if consent}
  <div class="w-full px-4 md:px-8 fixed bottom-4 md:bottom-8 left-0 z-50">
    <Card
      class="bg-white md:max-w-md animate-in slide-in-from-bottom-20 fade-in-50 duration-700"
    >
      <CardHeader class="pb-1">
        <div class="flex items-center">
          <CookieIcon class="mr-2" />
          <CardTitle>{m["cookie.title"]()}</CardTitle>
        </div>
      </CardHeader>
      <CardContent class="space-y-4 pt-4">
        <div class="flex justify-between items-start space-y-2">
          <div>
            <Label for="essential">{m["cookie.label"]()}</Label>
            <p class="text-dark-gray-500 text-sm">
              {m["cookie.text"]()}
            </p>
          </div>
        </div>
      </CardContent>
      <CardFooter class="p-4 gap-4 flex-wrap md:flex-nowrap">
        <a
          class={buttonVariants({
            variant: "default",
            class: "text-secondary-foreground",
          })}
          type="submit"
          href="/privacy"
        >
          {m["cookie.link"]()}
        </a>
        <form>
          <Button type="submit" class="text-secondary-foreground">
            {m["cookie.button"]()}
          </Button>
        </form>
      </CardFooter>
    </Card>
  </div>
{/if}
