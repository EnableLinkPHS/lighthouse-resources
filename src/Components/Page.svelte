<script>
    import data from "../Assets/data.json";
    import { pageContrast, fontSize, underline } from "../store.js"; // for testing
    export let current = "home";
</script>
<!-- svelte-ignore a11y-no-noninteractive-tabindex -->
<main class="Page" id="page">
    <p tabindex="0">Contrast: {$pageContrast}, Size: {$fontSize}, Underline: {$underline}</p>
    <p tabindex="0">{data[current].flavor}</p>
    {#if data[current].thead} 
        <table tabindex="0">
            <tr>
                {#each data[current].thead as header}
                    <th tabindex="0">{header}</th>
                {/each}
            </tr>
            {#each data[current].table as row}
                <tr>
                    {#each Object.values(row) as cell}
                        <td tabindex="0">{cell}</td>
                    {/each}
                </tr>
            {/each}
        </table>
    {:else}
        <p tabindex="0">Welcome to the site!</p>
    {/if}
</main>
<style>
    .Page {
		position: absolute;
		top: 10%;
		left: 25%;
	}
</style>