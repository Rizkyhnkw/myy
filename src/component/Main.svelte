<script>
    import Step from "./Step.svelte";
    let steps = [
        {name: 'BookShelf',icon:'fas fa-book-open'},
        {name: 'Qr code generator',icon:'fa-solid fa-qrcode'},
        {name: 'ContactAddress',icon:'fa-solid fa-address-book'}
    ];
    let benefits = [
        {name: 'Good Teammate', description: ' Effective communication, listening to others opinions, and willing to help teammates Unselfish and willing to share knowledge and experience.'},
        {name: 'Openness to Feedback and Continuous Learning', description: ' Accept criticism with a positive attitude and see it as an opportunity to grow.Constantly learning and keeping up with the latest technology.Take the initiative to learn new skills and apply them on the job.'},
        {name: 'c', description: 'lorem'},
    ]
</script>

<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
<div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
<h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
    Hi I'm <span class="poppins text-sky-500">Rizky</span> Ramadhan.<br>Junior <span class="poppins text-sky-500">Developer</span>
</h2>
<p class="text-base sm:text-lg md:text-xl">
    My <span class="text-sky-400"> favorite tech</span> includes JavaScript
    (ExpressJS or SvelteKit),Python(ScikitLearn or TensorFlow) TailwindCSS, Node.js + & MongoDB
</p>
<a  class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full  bg-white text-slate-950 cursor-pointer" href="#" target="_blank">
    <div
        class="absolute top-0 right-full w-full h-full bg-sky-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
    />
    <h4 class="relative z-9">Get in touch &rarr;</h4>
</a>
</div>
<!-- pics -->
<!-- <div class="relative shadow-2xl grid place-items-center">
    <img src="" alt="profile image" class="object-cover z-[2] max-h-[70vh]">
</div>     -->
</section>
<section id="project" class="py-20 lg:py-32 flex flex-col gap-24">
    <div class="flex flex-col gap-2 text-center">
        <h6 class="text-lg sm:text-xl md:text-2xl">
a few of my hardwork
        </h6>
        <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
            Curious to <span class="poppins text-sky-400">see</span> my work?
        </h3></div>
        <a href="" target="_blank" class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center 
        gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-sky-700 duration-200">
    <i class="fa-regular fa-circle-play"/>
<p>watch the vid</p></a>
<div class="bg-gray-800 grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
    <Step step={steps[0]}>
        <p>A simple REST API to store a books created with<strong class="text-sky-400"> NodeJS + Hapi.js</strong></p>
        <div
        class="ml-auto cursor-pointer hover:text-gray-950 duration-200 relative after:absolute after:top-0 after:h-0 after:right-full
         after:bg-white after:w-full after:h-full after:duration-200 hover:after:translate-x-full after:z-[-1] overflow-hidden"
    >
    <p class="z-4"><a href="https://github.com/Rizkyhnkw">Go to &rarr;</a></p>
    </div>
    </Step>
    <Step step={steps[1]}>
<p>A simple web to generate QR code</p>
    </Step>
    <Step step={steps[2]}>
<p>A simple web app to save contacts created with <strong class="text-sky-400">NodeJS+ExpressJS</strong></p>
    </Step>
</div></section>
<section id="about" class="py-20 pt-10 lg:pt-16 lg:py32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
    <div class="flex  flex-col gap-2 text-center relative before:absolute before:top-0 
    before:left-0 before:w-2/3 before:h-1.5 before:bg-sky-700 after:absolute after:bottom-0
     after:right-0 after:w-2/3 after:h-1.5 after:bg-sky-700 py-4">
    <h6 class="text-lg sm:text-xl md-text-2xl">Want to know more?</h6>
<h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">A bit <span class="poppins text-sky-400">about </span>me.
</h3>
</div>
<p class="mx-auto poppins fonr-semibold text-lg sm:text-xl md:text-2xl">I am . . .</p>
<div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
    {#each  benefits as benefit, index }
    <div class="flex gap-6 sm:gap-8">
        <p class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold">
            0{index + 1}
        </p>
        <div class="flex flex-col gap-6 sm:gap-8">
            <h3 class="text-2xl sm:text-3xl md:text-5xl">
                {benefit.name}
            </h3>
            <p>{benefit.description}</p>
        </div>
    </div>       
    {/each}
</div>
<!-- <h5 class="text-2xl sm:text-3xl font-semibold text-center poppins">The <span class="text-sky-400">Complete </span>Package</h5>
<div class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full">
    <table class="bg-white text-slate-700 rounded text-center">
        <thead class="border-b border-solid border-slate-200">
            <tr class="">
                <th></th>
                <th class="whitespace-nowrap p-2 px-4">Candidate #1</th>
                <th class="whitespace-nowrap p-2 px-4">Candidate #2</th>
                <th class="whitespace-nowrap p-2 px-4">Candidate #3</th>
                <th class="whitespace-nowrap bg-sky-700 text-white p-4 px-8 ">Me</th>
            </tr>
        </thead>
        <tbody>
            <tr class="border-b border-solid border-slate-200">
                <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap">
                    Dedication</td>
                    <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                    <td><i class="fa-solid fa-check text-slate-500"></i></td>
                    <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                    <td><i class="fa-solid fa-check text-slate-500"></i></td>
            </tr>
        </tbody>
        <tbody>
            <tr class="border-b border-solid border-slate-200">
                <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap">
                    Interpersonal Skills</td>
                    <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                    <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                    <td><i class="fa-solid fa-check text-slate-500"></i></td>
                    <td><i class="fa-solid fa-check text-slate-500"></i></td>
            </tr>
        </tbody>
        <tbody>
            <tr class="border-b border-solid border-slate-200">
                <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap">
                    Programing ability</td>
                    <td><i class="fa-solid fa-check text-slate-500"></i></td>
                    <td><i class="fa-solid fa-check text-slate-500"></i></td>
                    <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                    <td><i class="fa-solid fa-check text-slate-500"></i></td>
            </tr>
        </tbody>
        <tbody>
            <tr class="border-b border-solid border-slate-200">
                <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap">
                    Critical thought</td>
                    <td><i class="fa-solid fa-check text-slate-500"></i></td>
                    <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                    <td><i class="fa-solid fa-check text-slate-500"></i></td>
                    <td><i class="fa-solid fa-check text-slate-500"></i></td>
            </tr>
        </tbody>
    </table>
</div>
<div class="mx-auto -mt-12 italic sm:hidden opacity-50">
    <p class="mx-auto">Scroll to see more &rAarr;</p>
</div> -->
</section>
</main>