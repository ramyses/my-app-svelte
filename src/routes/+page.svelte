<script>
    
    
</script>

<h1> inicio</h1>







 <!-- <script>
    const idade = 23;
    if(idade == 23){
        // .....
    }else{
        // .....
    }

    const lista = [
        'joao', 
        'mateus',
        ' lukas'
    ]
    const lista2 = [
        {nome: 'Joao', idade: 23},
        {nome: 'ana', idade: 25},
        {nome: 'pedro', idade: 32},
    ]
    for(let nome of lista){
        console.log(nome);
    }

</script>

<h1>inicio</h1>

{#if idade == 23} 
    <p>Idade é 23!</p>

{:else}
    <p>Idade nao esta entre 20 e 30 anos</p>
{/if}



{#each lista as nome}
    <p>{nome}</p>
{/each}

{#each lista2 as {nome, idade}}{nome, idade} e uma destruturing de um objeto 
    <p>{nome} tem {idade}</p>
{/each}
 --> 