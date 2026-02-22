<script>
    let {
        src, alt, caption, size } = $props();
</script>

<div class="featured-pic" class:size-full={size === 'full'} class:size-large={size === 'large'} class:size-medium={size === 'medium'} class:size-small={size === 'small'}>
    <a href={src} target="_blank" rel="noopener noreferrer">
        <img src={src} alt={alt} class="image" />
    </a>
    {#if caption}
        <p class="caption">{caption}</p>
    {/if}
</div>

<style>
    .featured-pic {
        display: block;
        border-radius: 8px;
        background-color: var(--color-light-gray);
        margin: var(--spacing-lg) 0;
        text-align: center;
    }
    .image {
        width: 100%;
        aspect-ratio: 1 / 1; /* square image */
        object-fit: cover;
        border-radius: 4px;
        padding: var(--spacing-sm);
        box-shadow: 0 2px 8px var(--color-shadow);
        border-color: var(--color-black);
        border-width: 2px;
        border-style: solid;
        cursor: pointer;
        transition: filter 0.2s ease;
    }

    .image:hover {
        filter: brightness(0.75);
    }
    .caption {
        margin-top: var(--spacing-sm);
        padding: 8px;
        font-size: var(--font-size-sm);
        color: var(--color-medium-gray);
    }

</style>