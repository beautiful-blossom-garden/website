<script lang="ts">
  let { children, class: className = '' } = $props();
</script>

<h1 class="text-3xl {className}">{@render children()}</h1>
