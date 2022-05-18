<script>
    export let pokeman
    import {fade} from 'svelte/transition'
</script>

<a class="p-6 flex flex-col items-center text-center shadow-sm hover:shadow-lg text-gray-800 bg-gray-100 rounded-md" href={`/pokemon/${pokeman.id}`} transition:fade>
<img class="h-40 w-40" src={pokeman.image} alt={pokeman.name}>
<h2 class="uppercase text-2xl font-semibold">{pokeman.id}. {pokeman.name}</h2>
<p>{pokeman.type}</p>
</a>

