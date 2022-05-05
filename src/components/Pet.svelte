<script lang="ts">
  import Eyes from './Eyes.svelte';
</script>

<div id="pet">
  <img src="/assets/img/cat.png" alt="" />
  <Eyes />
</div>

<style lang="sass">
  #pet
    position: absolute
    left: 15px
    bottom: 0
    display: flex
</style>