<script lang="ts">
  import '../app.css';
  import favicon from '$lib/assets/favicon.svg';
  import Menu from '$lib/components/Menu.svelte';
  import Footer from '$lib/components/Footer.svelte';
  import { MenuItem } from '$lib/enum';
  import { page } from '$app/stores';

  let { children, data } = $props();

  let menuChoosen = $derived($page.url.pathname === '/' ? MenuItem.Home : MenuItem.Settings);
</script>

<svelte:head>
  <link rel="icon" href={favicon} />
  <title>Beautiful Blossom Garden</title>
  <meta name="description" content="Beautiful Blossom Garden" />
  <meta name="keywords" content="Beautiful Blossom Garden, Garden, Flowers" />
  <meta name="author" content="theeasternfurry" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="robots" content="index, follow" />
  <meta name="googlebot" content="index, follow" />
</svelte:head>

<div class="flex h-screen">
  <Menu {menuChoosen} />

  <div class="flex-1">
    <div class="py-30">
      {@render children?.()}
    </div>

    <Footer />
  </div>
</div>
