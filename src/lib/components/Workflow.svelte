<script>
    import { checklistItems } from "$lib/data/data.js";
    import {CheckCircle2 } from "@lucide/svelte"
     import codeImg from '$lib/assets/code.jpg'
</script>

<div id="workflow" class="mt-20">
    <h2 class="text-3xl sm:text-5xl lg:text-6xl text-center mt-6 tracking-wide">Acclerate your {" "} 
        <span class="bg-gradient-to-r from-orange-500 to-orange-800 text-transparent bg-clip-text">coading workflow.</span></h2>

    <div class="flex flex-wrap justify-center">
        <div class="pt-12 w-full lg:w-1/2">
            <img alt="coading" src={codeImg} /> 
        </div>

        <div class="pt-12 w-full lg:w-1/2">
            {#each checklistItems as items}
            <div class="flex mb-12">
                <div class="text-green-400 mx-6 bg-neutral-900 h-10 w-10 p-2 justify-center items-center rounded-full">
                    <div> <CheckCircle2  /></div>
                </div>

                <div>
                    <h5 class="mt-1 mb-2 text-xl">{items.title}</h5>
                    <p class="text-md text-neutral-500">{items.description}</p>
                </div>
                </div>
            {/each}
        </div>

    </div>
</div>
