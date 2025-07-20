<script lang="ts">
  let { children } = $props();
</script>

<div class="flex flex-col gap-y-6 px-50">{@render children()}</div>
