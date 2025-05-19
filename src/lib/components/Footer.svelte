<script>
    import {communityLinks, platformLinks, resourcesLinks} from '$lib/data/data.js';
</script>

<footer id="footer" class="mt-20 border-t py-10 border-neutral-700">
    <div class="grid grid-cols-2 lg:grid-cols-3 gap-4">

        <div>
            <h3 class="text-md font-semibold mb-4">Resources</h3>
            <ul class="space-y-2">
                {#each resourcesLinks as links}
                    <li>
                        <a href={links.href} class="text-neutral-300 hover:text-white">{links.text}</a>
                    </li>
                {/each}
            </ul>
        </div>


        <div>
            <h3 class="text-md font-semibold mb-4">Platform</h3>
                <ul class="space-y-2">
                {#each platformLinks as links}
                    <li>
                        <a href={links.href} class="text-neutral-300 hover:text-white">{links.text}</a>
                    </li>
                {/each}
            </ul>
        </div>

        <div>
            <h3 class="text-md font-semibold mb-4">Community</h3>
                <ul class="space-y-2">
                {#each communityLinks as links}
                    <li>
                        <a href={links.href} class="text-neutral-300 hover:text-white">{links.text}</a>
                    </li>
                {/each}
            </ul>
        </div>

    </div>
</footer>
