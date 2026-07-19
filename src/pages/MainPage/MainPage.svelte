<script lang="ts">
  import BentoGrid from "../../widgets/bento-grid/BentoGrid.svelte";
  import Footer from "../../shared/ui/Footer/Footer.svelte";
</script>

<main class="page">
  <BentoGrid />
  <Footer />
</main>

<style>
  .page {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 100%;
  }
</style>
