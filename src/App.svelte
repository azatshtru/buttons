<script>
  import Button from "./Button.svelte";
</script>

<main>
  <div class="container">
    <Button buttonIcon='fa-play' />
    <Button buttonIcon='fa-pause'/>
    <Button buttonIcon='fa-heart' hueRotation='260deg' />
  </div>
  
</main>

<style>
  .container {
    display: flex;
    flex-direction: row;
    gap: 10px;
  }
</style>
