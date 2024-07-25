<script>
    import { onMount } from "svelte";
    import { marked } from "marked";
    let markdownText = "";
    let htmlContent = "";
    export let filename;
    // Function to fetch the Markdown file
    async function fetchMarkdown() {
        const res = await fetch(filename); // Adjust the path if needed
        if (res.ok) {
            markdownText = await res.text();
            htmlContent = marked(markdownText);
        } else {
            console.error("Error fetching the markdown file:", res.statusText);
        }
    }

    // Call the fetch function when the component mounts
    onMount(() => {
        fetchMarkdown();
    });
</script>

<div class="markdownblog">{@html htmlContent}</div>

<style>
    /* Basic styles for Markdown headings */
    :global(.markdownblog h1) {
        font-size: 2.5em;
        margin-top: 1em;
        margin-bottom: 0.5em;
        font-weight: bold;
        color: #333;
    }

    :global(.markdownblog h2) {
        font-size: 2em;
        margin-top: 1em;
        margin-bottom: 0.5em;
        font-weight: bold;
        color: #444;
    }

    :global(.markdownblog h3) {
        font-size: 1.75em;
        margin-top: 1em;
        margin-bottom: 0.5em;
        font-weight: bold;
        color: #555;
    }

    /* Additional styles for paragraphs, lists, and links */
    :global(.markdownblog p) {
        margin-bottom: 1em;
        line-height: 1.6;
        color: #666;
    }

    :global(.markdownblog ul) {
        list-style-type: disc;
        padding-left: 1.5em;
        margin-bottom: 1em;
        color: #666;
    }

    :global(.markdownblog a) {
        color: blue;
        text-decoration: underline;
    }
    :global(.markdownblog code) {
        background-color: #ebebebe8;
        color: #2594c7;
        padding: 0.2em 0.4em;
        border-radius: 3px;
        font-family: "Courier New", Courier, monospace;
        font-size: 0.95em;
    }

    /* Styles for code blocks */
    :global(.markdownblog pre) {
        background-color: #f5f5f5;
        color: #333;
        padding: 1em;
        border-radius: 5px;
        overflow-x: auto;
        font-family: "Courier New", Courier, monospace;
        font-size: 0.95em;
        margin-bottom: 1em;
        border: 1px solid #ddd;
    }

    :global(.markdownblog pre code) {
        background-color: transparent;
        color: inherit;
        padding: 0;
        border-radius: 0;
        font-size: inherit;
    }
    :global(.markdownblog ol) {
        list-style-type: decimal;
        padding-left: 1.5em;
        margin-bottom: 1em;
    }

    :global(.markdownblog ol li) {
        margin-bottom: 0.5em;
        color: #666;
    }
</style>
