<script lang="ts">
  let {
    elementName = "Element Name", 
    value = $bindable()
  }: { elementName: string, value: number } = $props();
</script>

<div class="input-field-container">
  <span class="label">{elementName}</span>
  <input 
      type="number" 
      placeholder="0"
      bind:value="{value}"
  />
</div>

<style>
  div.input-field-container {
    position: relative;
    background: mistyrose;
    margin-bottom: 24px;
    height: fit-content;
    width: fit-content;
  }

  input {
    border: 2px solid #2f8a89;
    padding: 0 16px;
    border-radius: 4px;
    opacity: 1;
    font-size: var(--text-size);
    height: 52px;
    width: var(--width, 240px);
    text-align: right;
    box-sizing: border-box;
  }

  span.label {
    font-size: var(--label-size);
    position: absolute;
    z-index: 2;
    padding: 0 4px;
    inset-inline-start: 14px; /* 12px + 2px (border width) */
    inset-block-start: calc(-1 * var(--label-size) / 2); /* height / 2 */
    background: white;
    border-radius: 4px;
  }
  
</style>