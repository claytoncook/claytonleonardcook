<script lang="ts">
  import type { TypeIcons } from "@/types/icons";

  import Bluesky from "./icons/Bluesky.svelte";
  import Github from "./icons/Github.svelte";
  import Calendar from "./icons/Calendar.svelte";
  import LinkedIn from "./icons/LinkedIn.svelte";
  import NotDefined from "./icons/NotDefined.svelte";

  let className = "transition fill-ctp-blue hover:brightness-110";

  export let icon: TypeIcons | undefined;
</script>

{#if icon === "bluesky"}
  <Bluesky class={className} {...$$restProps} />
{:else if icon === "github"}
  <Github class={className} {...$$restProps} />
{:else if icon === "calendar"}
  <Calendar class={className} {...$$restProps} />
{:else if icon === "linkedin"}
  <LinkedIn class={className} {...$$restProps} />
{:else}
  <NotDefined class={className} {...$$restProps} />
{/if}
