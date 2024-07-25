<script>
    export let title;
    export let url;
    export let description;
    export let image;
    import { page } from "$app/stores";

    function url_for(path) {
        const baseUrl = $page.url.origin;
        const url = new URL(path, baseUrl);
        return url.href;
    }
    let finalURL = url_for(url);
</script>

{#if image == null}
    <a class="bg-slate-200 rounded-lg p-3" href={finalURL}>
        <h1 class="text-center font-bold text-xl">{title}</h1>
        <p class="font-medium text-lg text-gray-400 text-center">
            {description}
        </p>
    </a>
{:else}
    <a
        class="bg-cover bg-center bg-no-repeat rounded-lg p-3"
        href={finalURL}
        style="background-image: {image}"
    >
        <h1 class="text-center font-bold text-xl">{title}</h1>
        <p class="font-medium text-lg text-gray-400 text-center">
            {description}
        </p>
    </a>
{/if}
