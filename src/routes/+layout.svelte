<script>
  import "../app.css";
  import { page } from "$app/stores";

  function url_for(path) {
    const baseUrl = $page.url.origin;
    const url = new URL(path, baseUrl);
    return url.href;
  }
  let homeURL = url_for("/");
  let blogURL = url_for("/blog");
</script>

<div
  class="fixed top-1 right-1 w-16 hover:w-48 group rounded-3xl m-3 bg-blue-400 p-3 transition-all ease-in-out duration-800"
>
  <div class="flex flex-auto flex-row gap-3">
    <!-- svelte-ignore a11y-img-redundant-alt -->
    <img
      src="/profilepicture.jpeg"
      alt="My Profile Picture"
      class="rounded-full size-10"
    />
    <a
      class="invisible group-hover:visible p-1 rounded-md bg-slate-100 flex justify-center items-center font-semibold text-md"
      href={homeURL}
    >
      Home
    </a>
    <a
      class="invisible group-hover:visible p-1 rounded-md bg-slate-100 flex justify-center items-center font-semibold text-md"
      href={blogURL}
    >
      Blogs
    </a>
  </div>
</div>
<slot />
