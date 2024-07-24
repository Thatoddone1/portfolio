<script>
    import Introduction from "./Introduction.svelte";
</script>

<div
    class=" bg-gradient-to-r from-cyan-400 to-green-400 dark:from-cyan-600 dark:to-green-600 p-10 rounded-lg pl-20 pr-20 basis-1/2 lg:hover:basis-2/3 transition-all duration-800 ease-in-out"
>
    <h1 class="text-2xl font-bold text-center dark:text-white">Contact Me</h1>
    <div
        class="grid md:grid-cols-2 grid-cols-1 lg:grid-cols-3 gap-4 dark:text-white"
    >
        <div
            class="bg-gradient-to-r from-blue-300 to-indigo-300 dark:from-blue-500 dark:to-indigo-500 rounded-lg justify-center p-5 text-center font-semibold text-xl"
        >
            Discord: <p class="font-medium text-blue-600 dark:text-blue-200">
                thatoddone1
            </p>
        </div>
        <a
            class="bg-gradient-to-r from-sky-300 to-emerald-300 dark:from-sky-500 dark:to-emerald-500 rounded-lg justify-center p-5 text-center font-semibold text-xl hover:shadow-md hover:from-sky-500 hover:to-emerald-500 dark:hover:from-sky-700 dark:hover:to-emerald-700"
            href="https://github.com/Thatoddone1"
        >
            GitHub: <p class="font-medium text-blue-600 dark:text-blue-200">
                Thatoddone1
            </p>
        </a>
        <a
            class="bg-gradient-to-r from-lime-300 to-rose-300 dark:from-lime-500 dark:to-rose-500 rounded-lg justify-center p-5 text-center font-semibold text-lg text-wrap hover:shadow-md hover:from-lime-500 hover:to-rose-500 dark:hover:from-lime-700 dark:hover:to-rose-700"
            href="mailto:slot.visor0c@icloud.com"
        >
            Email: <p
                class="font-medium text-blue-600 text-wrap dark:text-blue-200"
            >
                slot.visor0c @icloud.com
            </p>
        </a>
    </div>
</div>
