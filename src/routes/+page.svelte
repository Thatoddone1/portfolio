<script>
    import Contact from "./Contact.svelte";

    import Introduction from "./Introduction.svelte";

    import Projects from "./Projects.svelte";
</script>

<html lang="eng">
    <head></head>
    <style></style>
    <body class="bg-white dark:bg-black w-auto h-auto">
        <div class="flex flex-row flex-auto p-2 pt-4">
            <Introduction></Introduction>
            <Contact></Contact>
        </div>
        <div
            class="flex flex-row flex-auto dark:text-white rounded-md bg-gradient-to-r from-pink-400 to-orange-400 dark:from-pink-700 dark:to-orange-700 p-4 pb-10 pt-10 m-4 justify-center font-bold text-4xl w-2/3 mx-auto"
        >
            My Projects
        </div>
        <Projects></Projects>
    </body>
</html>
