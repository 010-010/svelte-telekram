<script lang="ts">

  import { onMount, onDestroy } from 'svelte';
  import { createKaiNavigator, KaiNavigator } from '../../../utils/navigation';

  export let chat: any = {};
  export let message: any = {};
  export let parentNavInstance: typeof KaiNavigator;
  export let callButtonCallback: Function = (id, callback) => {}
  export let fetchMessageCallback: Function = (id: number) => {}

  onMount(() => {
    // console.log(message);
  });

</script>

<div class="MessageActionEmpty">
  <p>{message.action.className}</p>
</div>

<style>
  .MessageActionEmpty {
    box-sizing: border-box;
    margin: 0px;
    padding: 0px;
  }
  .MessageActionEmpty > p {
    margin: 0px;
    padding: 0px;
    font-style: italic;
  }
</style>
