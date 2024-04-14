<script>
  import Header from "$lib/components/Header/Header.svelte"
  import Footer from "$lib/components/Footer/Footer.svelte"
  import "../globals.sass"
</script>

<Header />
<div class="flex-1">
  <slot />
</div>
<Footer />

<style lang="sass">
    :global(html, body)
        height: 100vh
        width: 100%

    :global(body)
        display: flex
        flex-direction: column
</style>
