<script lang="ts">
    import {formatDate} from '$lib/utils'

    export let data
</script>

<article>
    <hgroup class="flex flex-col">
        <h1 class='text-2xl font-bold mb-1'>{data.meta.title}</h1>
        <p class='italic text-sm mb-4'>Published on {formatDate(data.meta.date)}</p>
    </hgroup>

    <div class='my-2 flex flex-wrap'>
        {#each data.meta.tags as tag}
            <span class="mx-0.5 p-2 border-2 rounded-2xl text-xs font-semibold cursor-pointer">&num;{tag}</span>
        {/each}
    </div>

    <div class='divider'></div>

    <!-- The prose class is from Tailwind Typography so we don't need to define -->
    <div class="prose">
        <svelte:component this={data.content}/>
    </div>
</article>
