<script lang="ts">
    import { Navbar, NavBrand, NavLi, NavUl, NavHamburger, ImagePlaceholder, Skeleton, TextPlaceholder } from 'flowbite-svelte';

    import logo from '$lib/assets/logo.jpeg'
  </script>
  
  <div class="relative px-8">
    <Navbar class="px-2 sm:px-4 py-2.5 fixed w-full z-20 top-0 start-0 border-b">
      <NavBrand href="/">
        <img src="{ logo }" class="me-3 h-6 sm:h-9" alt="Flowbite Logo" />
        <span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">The Voice of Healthcare Africa</span>
      </NavBrand>
      <NavHamburger />
      <NavUl>
        <NavLi href="/" active={true}>Home</NavLi>
        <NavLi href="/talks">Talks</NavLi>
        <NavLi href="/about">About</NavLi>
        <NavLi href="/contact">Contact</NavLi>
      </NavUl>
    </Navbar>
  </div>