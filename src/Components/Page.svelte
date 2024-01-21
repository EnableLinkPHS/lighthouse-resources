<script>
    import data from "../Assets/data.json";
    import { pageContrast, fontSize, underline } from "../store.js"; // for testing
    let linkUnderline; let textSize;
    $: linkUnderline = $underline ? "underline" : "none";
    $: textSize = $fontSize + "px";
    export let current = "home";
</script>
<!-- svelte-ignore a11y-no-noninteractive-tabindex -->
<main class="Page" id="page" style="--linkUnderline: {linkUnderline}; --textSize: {textSize}">
    <!--p tabindex="0">Contrast: {$pageContrast}, Size: {textSize}, Underline: {linkUnderline}</p-->
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
                    {#each Object.entries(row) as [key, value]}
                        {#if value}
                            {#if key.includes("Website")}
                                <td tabindex="0"><a href={value}>Visit site</a></td>
                            {:else if key.includes("Email")}
                                <td tabindex="0"><a href="mailto:{value}">{value}</a></td>
                            {:else}
                                <td tabindex="0">{value}</td>
                            {/if}
                        {:else}
                            <td tabindex="0"></td>
                        {/if}
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
        font-size: var(--textSize);
	}
    .Page a {
		text-decoration: var(--linkUnderline);
	}
    .Page table {
        overflow-x: scroll;
        overflow-y: scroll;
    }
</style>