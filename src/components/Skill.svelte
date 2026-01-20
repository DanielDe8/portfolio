<script>
    export let name
    export let description
</script>

<div class="m-7">
    <h3 class="text-5xl font-semibold">{name}</h3>
    <p class="text-2xl m-2">{@html description}</p>
</div>