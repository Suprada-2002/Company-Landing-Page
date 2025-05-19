<script>
    import { testimonials } from '$lib/data/data.js'
</script>

<div id="testimonials" class="mt-20 tracking-wide">
    <h2 class="text-3xl sm:text-5xl lg:text-6xl text-center my-10 lg:my-20">What People are saying</h2>

    <div class="flex flex-wrap justify-center">
        {#each testimonials as testimoni}
            <div class="w-full sm:w-1/2 lg:w-1/3 px-4 py-2">
                <div class="bg-neutral-900 rounded-md p-6 text-md border border-neutral-800 font-thin">
                    <p>{testimoni.text}</p>
                    <div class="flex mt-8 items-start">
                        <img class="w-12 h-12 mr-6 rounded-full border border-neutral-300"
                        alt="testimony-image" src={testimoni.image} />
                    
                        <div>
                            <h6>{testimoni.user}</h6>
                            <span class="text-sm font-normal italic text-neutral-600">{testimoni.company}</span>
                        </div>
                    </div>
                </div>
            </div>
        {/each}

    </div>

</div>
