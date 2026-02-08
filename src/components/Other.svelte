<script>
    export let name
    export let description
    export let imgSrc
    export let imgWidth
</script>

<div class="m-7 flex space-x-20">
    <div class="flex-auto">
        <h3 class="text-5xl font-semibold">{name}</h3>
        <p class="text-2xl m-3">{@html description}</p>
    </div>

    <img src="{imgSrc}" alt="{name}" class="flex-none" style="width: {imgWidth * 5}px">
</div>