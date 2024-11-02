<script>
    import { page } from "$app/stores";
    function url_for(path) {
    const baseUrl = $page.url.origin;
    const url = new URL(path, baseUrl);
    return url.href;
  }
  let blogURL = url_for("/blog");
  </script>
<div class="grid grid-cols-2 gap-4 m-4">
<div
    class="bg-gradient-to-r from-cyan-300 to-red-300 dark:from-cyan-700 dark:to-red-700 rounded-lg p-4 col-span-2"
>
    <h1 class="text-center font-bold text-4xl pb-3 dark:text-white">
        Read my blog!
    </h1>
    <div class="justify-center items-center flex">
    <div class="flex flex-col items-center">
        <a href={blogURL} class="p-3 m-5 bg-teal-500 rounded-md hover:shadow-lg hover:bg-teal-600 font-semibold dark:bg-teal-300 dark:hover:bg-teal-400">
            Read it here!
        </a>
        <p class="text-sm text-gray-400">(it's cool, right?)</p>
    </div>
</div>
</div>
</div>