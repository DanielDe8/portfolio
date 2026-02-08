<script>
    export let name
    export let description
    export let imgSrc
</script>

<div class="m-7 flex space-x-20 items-center">
    <img src="{imgSrc}" alt="{name}" class="flex-none w-30 h-30 object-contain">
    
    <div class="flex-auto">
        <h3 class="text-5xl font-semibold">{name}</h3>
        <p class="text-2xl m-3">{@html description}</p>
    </div>
</div>