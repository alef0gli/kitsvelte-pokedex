<script context="module">
    export async function load(ctx) {
        const id = ctx.params.id
        const url = `https://pokeapi.co/api/v2/pokemon/${id}`
        const res = await fetch(url)
        const pokeman = await res.json()
        return {props: {pokeman}}
    }
</script>
<script>
    export let pokeman
    const type = pokeman.types[0].type.name
 
    let type2 = pokeman.types[1]

    if(!type2) {
        type2 = ""
} else {
    type2 = pokeman.types[1].type.name
}




</script>
<div class="flex flex-col items-center">
<h1 class="text-4xl text-center my-8 uppercase"><a href="/">⟸</a> {pokeman.name}</h1>
<p>Type: <strong>{type} {type2}</strong> | Height: <strong>{pokeman.height/10}m</strong>
    | Weight: <strong>{pokeman.weight/10}kg</strong>
</p>

<img class="h-40" src={pokeman.sprites['front_default']} 
alt={pokeman.name}/>
</div>