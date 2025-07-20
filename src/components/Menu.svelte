<script>
  import { BookOpenIcon, HomeIcon } from '@lucide/svelte';
</script>

<ul class="menu h-fit bg-base-200 rounded-box">
  <li>
    <a class="tooltip tooltip-right" data-tip="Home" href="/">
      <HomeIcon class="w-5 h-5" />
    </a>
  </li>
  <li>
    <a class="tooltip tooltip-right" data-tip="Journey" href="/journey">
      <BookOpenIcon class="w-5 h-5" />
    </a>
  </li>
</ul>
