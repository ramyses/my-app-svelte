<script lang="ts">
import { page } from '$app/stores';

    //const items = $page.data.items
    export let data;
    
    let currentCategory: String = 'Todos'
    let portfolioItems = data.items;

    function changeCategory(newCategory: String){
        currentCategory = newCategory;
        filterPortfolio();
    }

    function filterPortfolio(){
        portfolioItems = data.items.filter(item => {
            return item.category === currentCategory || currentCategory === 'Todos';
        })
    }
</script>

<section class="bg-white dark:bg-gray-900">
    <div class="container px-6 mx-auto">
        


        <div class="flex py-4 mt-4 overflow-x-auto overflow-y-hidden md:justify-center dark:border-gray-700">
           {#each data.categories as category}
                {#if currentCategory === category}
                    <button
                    
                        class="h-12 px-8 py-2 -mb-px text-sm text-center text-blue-600 bg-transparent border-b-2 border-blue-500 sm:text-base dark:border-blue-400 dark:text-blue-300 whitespace-nowrap focus:outline-none">
                        {category}
                    </button>
                {:else}
                    <button
                        on:click={
                            () => {changeCategory(category)}
                        }
                        class="h-12 px-8 py-2 -mb-px text-sm text-center text-blue-600 bg-transparent border-b-2 border-blue-500 sm:text-base dark:border-blue-400 dark:text-blue-300 whitespace-nowrap focus:outline-none">
                        {category}
                    </button>
                {/if}
           {/each}     

            
        </div>
        
       
        <section class="mt-8 space-y-8 lg:mt-12">
            {#each portfolioItems as {slug, title,category,image}}
            <section class="lg:flex lg:items-center">
                <div class="lg:w-1/2 ">
                    <p class="text-lg tracking-wider text-blue-500 uppercase dark:text-blue-400 ">{category}</p>
                    <h2 class="mt-2 text-2xl font-semibold text-gray-800 capitalize dark:text-white">{title}</h2>
                </div>
    
                <div class="mt-4 lg:w-1/2 lg:mt-0">
                   <a href={`/portifolio/${slug}`}>
                        <img class="object-cover w-full h-64 rounded-lg md:h-96"
                        src={image}
                        alt="">
                   </a>
                </div>
            </section>
            {/each}
            
        </section>
    </div>
</section>