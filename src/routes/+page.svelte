<script>
    import About from "./About.svelte";

    import Contact from "./Contact.svelte";

    import Introduction from "./Introduction.svelte";

    import Projects from "./Projects.svelte";
</script>

<html lang="eng">
    <head></head>
    <style></style>
    <body class="bg-white dark:bg-black w-auto h-auto">
        <div class="grid grid-cols-2 gap-4 lg:grid-cols-4 p-2 pt-4">
            <Introduction></Introduction>
            <Contact></Contact>
            <About></About>
            <div
                class="col-span-2 lg:col-span-1 dark:text-white rounded-md bg-gradient-to-r from-pink-400 to-orange-400 dark:from-pink-700 dark:to-orange-700 justify-center font-bold text-4xl pt-5 pb-5"
            >
                <p class="text-center">My Projects</p>
                <p class="text-center">↓</p>
            </div>
        </div>
        <Projects></Projects>
    </body>
</html>
