<script>
  import "../app.pcss";
  import Header from "$lib/Header.svelte"
  import Footer from "$lib/Footer.svelte";
</script>

<Header />


<slot />
<!-- slot renderiza o conteudo de cada pagina individual-->

<!-- o ul sera redenrizado em todas as routes -->


<Footer/>