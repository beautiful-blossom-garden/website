<script lang="ts">
  let { children, class: className = '' } = $props();
</script>

<h2 class="text-2xl {className}">{@render children()}</h2>
