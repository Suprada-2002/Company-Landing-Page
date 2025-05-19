<script>
    import logo from '$lib/assets/logo.png';
    import {navItems} from '$lib/data/data.js';
    import {Menu, X} from '@lucide/svelte';

    let mobileDrawerOpen = false;

    function toggleNavbar() {
        mobileDrawerOpen = !mobileDrawerOpen;
    }
</script>

<nav class="sticky top-0 z-50 py-3 backdrop-blur-lg border-b border-neutral-700/80">
   <div class="container px-4 mx-auto relative lg:text-sm">

        <div class="flex justify-between items-center">
            <div class="hidden lg:flex items-center flex-shrink-0">
                <img class="h-10 w-10 mr-2" alt="navbar-logo" src={logo} />
                <span class="text-xl tracking-tight">VirtualR</span>
            </div>
      

        <ul class="hidden lg:flex ml-14 space-x-12">
            {#each navItems as item}
            <li><a href={item.href}>{item.label}</a></li>
            {/each}
        </ul>

        <div class="hidden lg:flex justify-center space-x-12 items-center">
            <a href="www.google.com" class="py-2 px-3 border rounded-md">Sign In</a>
             <a href="www.google.com" class="bg-gradient-to-tr from-orange-500 to-orange-800 py-2 px-3 rounded-md"> Create an account</a>
        </div>
      </div>

        <div class="lg:hidden md:flex flex-col justify-end">
            <button onclick={toggleNavbar}>
                {#if mobileDrawerOpen}
                 <X />
                {:else}
                 <Menu />
                {/if}
            </button>
        </div>
   </div>

   {#if mobileDrawerOpen}
        <div class="fixed right-0 z-20 bg-neutral-900 w-full p-12 flex flex-col justify-center items-center lg:hidden">
           <ul>
                {#each navItems as item}
                <li class="py-4"><a href={item.href}>{item.label}</a></li>
                {/each}
          </ul>
          <div class="flex space-x-6">
                <a href="www.google.com" class="py-2 px-3 border rounded-md">Sign In</a>
             <a href="www.google.com" class="bg-gradient-to-tr from-orange-500 to-orange-800 py-2 px-3 rounded-md"> Create an account</a>
          </div>
        </div>
   {/if}
</nav>
