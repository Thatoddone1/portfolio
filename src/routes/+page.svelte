<script>
    import About from "./About.svelte";

    import Contact from "./Contact.svelte";

    import Introduction from "./Introduction.svelte";

    import Projects from "./Projects.svelte";

    import Langs from "./Langs.svelte";

    import BlogAd from "./BlogAd.svelte";
</script>

<html lang="en">
    <head>
        <title>Joshua's Portfolio</title>
        <meta
            name="description"
            content="Explore Joshua's portfolio showcasing innovative web development projects and free tools to enhance your coding journey. Discover, learn, and collaborate!"
        />
    </head>
    <style></style>
    <body class="bg-white dark:bg-black w-auto h-auto">
        <div class="grid grid-cols-1 gap-4 lg:grid-cols-4 p-2 pt-4">
            <Introduction></Introduction>
            <Contact></Contact>
            <About></About>
            <Langs></Langs>
            <div
                class="col-span-2 lg:col-span-1 dark:text-white rounded-md bg-gradient-to-r from-pink-400 to-orange-400 dark:from-pink-700 dark:to-orange-700 justify-center font-bold text-4xl pt-5 pb-5"
            >
                <p class="text-center">My Projects</p>
                <p class="text-center">↓</p>
                <p class="text-center font-medium text-xl py-10 p-3">
                    P.S. Not everything down there is finished, or ever will be.
                    It is just a space for me to test out my wacky ideas, which
                    might get turned into real products, and be bumped up that
                    list
                </p>
            </div>
        </div>
        <Projects></Projects>
        <BlogAd></BlogAd>
    </body>
</html>
