<script>
  import { page } from "$app/stores";

 
  import Logo from "./Logo.svelte";
  const items = [
    { href: '/',label: 'Home'},
    { href: '/sobre',label: 'Sobre'},
    { href: '/portifolio',label: 'portfolio'},
    { href: '/contato',label: 'contato'},
    { href: '/faq',label: 'Perguntas' },
  ]

  let text_gray = 'text-gray-800';
  
</script>
<a href="/">
    <Logo />
</a>

{#each items as {href, label}}
  {#if $page.url.pathname === href}
    <a {href} class="text-gray-800 transition-colors duration-300 transform dark:text-gray-200 border-b-2 border-blue-500 mx-1.5 sm:mx-6">{label}</a>
  {:else}
    <a {href} class="border-b-2 border-transparent hover:text-gray-800 transition-colors duration-300 transform dark:hover:text-gray-200 hover:border-blue-500 mx-1.5 sm:mx-6">{label}</a>   
  {/if}
{/each}








<!-- <a href="../" class="text-gray-800 transition-colors duration-300 transform dark:text-gray-200 border-b-2 border-blue-500 mx-1.5 sm:mx-6">Inicio</a>

<a href="../sobre" class="border-b-2 border-transparent hover:text-gray-800 transition-colors duration-300 transform dark:hover:text-gray-200 hover:border-blue-500 mx-1.5 sm:mx-6">Sobre</a>

<a href="../portifolio" class="border-b-2 border-transparent hover:text-gray-800 transition-colors duration-300 transform dark:hover:text-gray-200 hover:border-blue-500 mx-1.5 sm:mx-6">Portifolio</a>

<a href="../contato" class="border-b-2 border-transparent hover:text-gray-800 transition-colors duration-300 transform dark:hover:text-gray-200 hover:border-blue-500 mx-1.5 sm:mx-6">
   Contato
</a>
<a href="../faq" class="border-b-2 border-transparent hover:text-gray-800 transition-colors duration-300 transform dark:hover:text-gray-200 hover:border-blue-500 mx-1.5 sm:mx-6">
    Perguntas Frequentes
 </a>   -->     