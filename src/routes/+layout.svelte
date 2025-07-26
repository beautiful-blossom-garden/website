<script>
  import Footer from '../components/Footer.svelte';
  import Menu from '../components/Menu.svelte';
  import '../style.css';
  import '@fontsource/noto-sans';

  let { children } = $props();
</script>

<div class="flex">
  <Menu />

  <div class="w-full">
    <div class="w-full p-10">
      {@render children()}
    </div>


  </div>
</div>
<Footer />
