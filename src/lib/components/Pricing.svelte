<script>
     import {CheckCircle2 } from "@lucide/svelte"
    import { pricingOptions } from '$lib/data/data.js';
</script>

<div class="mt-20">
    <h2 class="text-3xl sm:text-5xl lg:text-6xl text-center my-8 tracking-wide">Pricing</h2>

    <div class="flex flex-wrap">
        {#each pricingOptions as priceOptn}
            <div class="w-full sm:w-1/2 lg:w-1/3 p-2">
                <div class="p-10 border border-neutral-700 rounded-xl">
                    <p class="text-4xl mb-8">
                        {priceOptn.title}
                        {#if priceOptn.title === "Pro"}
                            <span class="bg-gradient-to-r from-orange-500 to-red-400 text-transparent bg-clip-text text-xl mb-4 ml-2">
                                (Most Popular)
                            </span>
                        {/if}
                    </p>

                    <p class="mb-8">
                        <span class="text-5xl mt-6 mr-2">{priceOptn.price}</span>
                        <span class="text-netural-400 tracking-tight">/Month</span>
                    </p>

                    <ul>
                        {#each priceOptn.features as feature}
                            <li class="mt-8 flex items-center">
                            <CheckCircle2 />
                            <span class="ml-2">{feature}</span>
                            </li>
                        {/each}
                    </ul>

                    <a href="www.google.com" class="inline-flex justify-center items-center text-center w-full h-12 p-5 mt-20 tracking-tight text-xl hover:bg-orange-900 border border-orange-900 rounded-lg transition duration-200">Subscribe</a>
                </div>
            </div>
        {/each}
    </div>
</div>
