<script lang="ts">
  import { Navigation } from '@skeletonlabs/skeleton-svelte';
  import { House, Menu, Settings } from 'lucide-svelte';
  import { MenuItem } from '$lib/enum';

  let { menuChoosen } = $props();

  let isExpansed = $state(true);

  function toggleExpanded() {
    isExpansed = !isExpansed;
  }
</script>

<div class="h-screen">
  <Navigation.Rail expanded={isExpansed}>
    {#snippet header()}
      <Navigation.Tile labelExpanded="Menu" onclick={toggleExpanded}><Menu /></Navigation.Tile>
    {/snippet}
    {#snippet tiles()}
      <Navigation.Tile selected={menuChoosen === MenuItem.Home} labelExpanded="Trang chủ" href="/"
        ><House /></Navigation.Tile
      >
    {/snippet}
    {#snippet footer()}
      <Navigation.Tile
        selected={menuChoosen === MenuItem.Settings}
        labelExpanded="Cài đặt"
        href="/cai-dat"><Settings /></Navigation.Tile
      >
    {/snippet}
  </Navigation.Rail>
</div>
