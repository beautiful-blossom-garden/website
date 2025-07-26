<script>
  import Display from '../components/Display.svelte';
  import Footer from '../components/Footer.svelte';
  import Menu from '../components/Menu.svelte';
  import '../style.css';
  import '@fontsource/noto-sans';

  let { children } = $props();
</script>

<div class="flex">
  <Menu />

  <Display>{@render children()}</Display>
</div>
<Footer />
