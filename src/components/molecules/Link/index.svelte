<script lang="ts">
  import type { TypeIcons } from "@/types/icons";
  import { Icon } from "@/components/atoms";

  export let href: string;
  export let target: "_self" | "_blank" | "_parent" | "_top";
  export let text: string | undefined = undefined;
  export let icon: TypeIcons | undefined = undefined;
  export let size: number = 32;
</script>

<a {href} {target} class="hover:underline active:underline">
  {#if text}
    {text}
  {/if}
  {#if icon}
    <Icon {icon} width={size} />
  {/if}
</a>
