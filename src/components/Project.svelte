<script>
    export let name
    export let description
    export let imgSrc
    export let imgWidth
    export let evenProject // every second project has image on the left and a different bg
</script>

<div class="px-25 py-10 flex space-x-15" class:bg-base-100={!evenProject} class:bg-base-200={evenProject}>
    {#if evenProject}
        <img src="{imgSrc}" alt="{name}" class="flex-none w-{imgWidth}">
    {/if}

    <div class="flex-auto">
        <h3 class="text-5xl font-semibold">{ name }</h3>
        <p class="mt-5 text-2xl">
            {@html description}
        </p>
    </div>

    {#if !evenProject}
        <img src="{imgSrc}" alt="{name}" class="flex-none w-{imgWidth}">
    {/if}
</div>