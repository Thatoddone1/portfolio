<script>
    import BlogCard from "./BlogCard.svelte";
</script>

<head>
    <title>Joshua's Portfolio - Blogs</title>
</head>
<h1 class="text-center font-bold text-4xl">Blogs</h1>
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-3 p-2">
    <BlogCard
        title="First Blog"
        url="/blog/first-blog"
        description="My first blog. A quick article on how I built the blogging system"
    ></BlogCard>
    <BlogCard
        title="Warp: The Terminal of the Future?"
        url="/blog/warp"
        description="A dive into the Warp terminal application. Is it worth your time, and money?"
    ></BlogCard>
</div>
