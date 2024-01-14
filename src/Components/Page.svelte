<script>
    import data from "../Assets/data.json";
    export let current = "home";
</script>
<main class="Page">
    <p>{data[current].flavor}</p>
    {#if data[current].thead}
        <!-- svelte-ignore a11y-no-noninteractive-tabindex -->
        <table tabindex="0">
            <tr>{#each data[current].thead as header}
                <th>{header}</th>
                {/each}
            </tr>
            {#each data[current].table as row}
                <tr>{#each Object.values(row) as cell}<td>{cell}</td>{/each}</tr>
            {/each}
        </table>
    {:else}
        <p>Welcome to the site!</p>
    {/if}
</main>
<style>
    .Page {
		position: absolute;
		top: 10%;
		left: 25%;
	}
</style>