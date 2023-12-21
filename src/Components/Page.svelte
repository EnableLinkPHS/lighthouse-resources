<script context="module">
    import data from "../Assets/data.json";
</script>
<script>
    export let current = "home"; // defaults to homepage
</script>
<p>{data[current].flavor}</p>