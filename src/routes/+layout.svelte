<script lang="ts">
 
    import "../app.css";
    import Footer from "../component/Footer.svelte"
    import Header from "../component/Header.svelte"
  import 'iconify-icon'
    let y;
    let innerHeight = 0;
    let innerWidth = 0;

    function goTop(){
      document.body.scrollIntoView();
    }
  </script>
  <div class="container relative flex flex-col max-w-[1920px] mx-auto w-full text-sm sm:text-base min-h-screen">
    <div class={"fixed bottom-0 w-full duration-200 flex p-10 z-[10]" +    (y > 0
      ? " opacity-full pointer-events-auto"
      : " pointer-events-none opacity-0")}
    >
      <button
      on:click={goTop}
            class="ml-auto rounded-full bg-gray-900 text-sky-400 px-3 sm:px-4 hover:bg-gray-800 cursor-pointer aspect-square grid place-items-center"
      >
        <i class="fa-solid fa-arrow-up"></i>
      </button>
    </div>
    <Header {y} {innerHeight}/>
    <slot />
    <Footer/>
  </div>

  <svelte:window bind:scrollY={y} bind:innerHeight bind:innerWidth />