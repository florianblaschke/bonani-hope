<script lang="ts">
import { m } from "$lib/paraglide/messages";
import {
	Select,
	SelectContent,
	SelectTrigger,
	SelectItem,
	SelectGroup,
} from "$lib/components/ui/select";
import { getLocale, locales, setLocale } from "$lib/paraglide/runtime";
let locale = getLocale();

const localesMap: Record<string, string> = {
	de: m["locales.german"](),
	en: m["locales.english"](),
	sv: m["locales.swedish"](),
};

function onValueChange(value: string) {
	setLocale(value as "de" | "en" | "sv");
	return locale;
}
</script>

    <Select
      type="single"
      bind:value={locale}
      onValueChange={onValueChange}
    >
      <SelectTrigger
        class="w-fit border-none"
        aria-label="Switch language"
        type="button"
      >
        {getLocale()}
      </SelectTrigger>
      <SelectContent>
        <SelectGroup>
          {#each locales  as locale (locale) }          
            <SelectItem value={locale} >
              {localesMap[locale]}
            </SelectItem>
          {/each}
        </SelectGroup>
      </SelectContent>
    </Select>
