<script>
    import MarkdownRenderer from "./MarkdownRenderer.svelte";
    export let filename;
    export let title;
</script>

<head>
    <title>{title}</title>
</head>
<div class="flex flex-row flex-auto justify-center">
    <div class="bg-slate-100 dark:bg-slate-800 w-5/6 rounded-lg p-10 m-5">
        <h1 class="text-3xl font-bold text-center text-black dark:text-white">{title}</h1>
        <hr />
        <MarkdownRenderer {filename}></MarkdownRenderer>
    </div>
</div>
