<script>
  import Footer from '../components/Footer.svelte';
  import Menu from '../components/Menu.svelte';
  import '../style.css';
  import '@fontsource/noto-sans';

  let { children } = $props();
</script>

<div class="w-1/2 mx-auto py-50">
  <div class="flex">
    <Menu />

    {@render children()}
  </div>
</div>

<Footer />
