<script lang="ts">
    import {formatDate} from '$lib/utils'

    export let data
</script>

<svelte:head>
    <title>Home</title>
</svelte:head>

<section>
    {#each data.posts as post}
        <a href={post.slug} class="flex flex-col cursor-pointer rounded-box p-2 sm:p-4 sm:my-1 hover:underline">
            <p class='font-bold text-2xl'>{post.title}</p>
            <p class='text-md'>{post.description}</p>
            <p class='italic pt-1 text-sm'>{formatDate(post.date)}</p>
        </a>
        <div class='divider'></div>
    {/each}
</section>
