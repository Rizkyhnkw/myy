<script>
    export let y;
    export let tabs = [
        {name: "project", link:"#project"},
        {name: "About Me", link: "#about"}
    ];
</script>

<header class={"sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border-b border-solid"
+
        (y > 0
            ? " py-4 bg-gray-950 border-sky-950"
            : " py-6 bg-transparent border-transparent")}>
    <h1 class="font-medium">
      <b class="font-bold poppins">Rizky</b> <span> Ramadhan</span> 
    </h1>
    <div class="sm:flex ml-auto pr-4 gap-4 items-center hidden">
        {#each tabs as tab,index }           
        <a href={tab.link} class="duration-200 hover:text-sky-400"> <p>{tab.name}</p></a>
       
        {/each}
   
    <!-- button-->
    <button 
    class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-white text-gray-950"
>
    <div
        class="absolute top-0 right-full w-full h-full bg-sky-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
    />
    <h4 class="relative z-9">Get in touch</h4>
</button> </div>
</header>