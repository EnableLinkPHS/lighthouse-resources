<script>
    import data from "../Assets/data.json";
    export let current = "home";
</script>
<main class="Page">
    <p>{data[current].flavor}</p>
</main>
<style>
    .Page {
        position: relative;
    }
</style>