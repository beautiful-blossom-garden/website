<script lang="ts">
  import { CopyIcon } from '@lucide/svelte';
  import H1 from '../../../components/H1.svelte';
  import { v4 as uuidv4 } from 'uuid';

  let uuid_value = $state(uuidv4());
  let is_copied = $state(false);


  function generateUUID() {
    uuid_value = uuidv4();
  }

  function copyToClipboard() {
    navigator.clipboard.writeText(uuid_value);
    is_copied = true;
    setTimeout(() => {
      is_copied = false;
    }, 2000);
  }
</script>

<div class="w-full flex flex-col gap-y-6 items-center justify-center">
  <div class="flex flex-col gap-y-6 items-center w-full justify-center">
    <H1>UUID Random Generator</H1>

    <div class="flex flex-row gap-x-2 items-center">
      <p>{uuid_value}</p>
      <button class="btn btn-ghost transition-all duration-300" onclick={copyToClipboard}>
        <CopyIcon class="w-4 h-4" /> {is_copied ? 'Copied' : 'Copy'}
      </button>
    </div>

    <button class="btn btn-primary" onclick={generateUUID}>
      Generate
    </button>
  </div>
</div>
