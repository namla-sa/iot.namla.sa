<script>
	import '../app.css';
	import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte';
	import { page } from '$app/stores';
	$: activeUrl = $page.url.pathname;
	let activeClass = 'text-sky-50 bg-cyan-700 md:bg-transparent md:text-cyan-300';
	let nonActiveClass = 'text-gray-600 hover:bg-gray-300 md:hover:bg-transparent md:border-0 md:hover:text-cyan-600 dark:text-gray-400';
</script>

<header class="absolute inset-x-0 top-0 z-50">
<Navbar fluid={true} class=" bg-black shadow-lg shadow-cyan-500/5 text-cyan-200">
<a href="/">
	<NavBrand>
	<img src="logo.png" class="me-2 h-7 rounded-md" alt="Namla Logo">
	<span class="self-center whitespace-nowrap text-xl font-semibold">namla.sa</span>
</NavBrand>
</a>

<NavHamburger class='hover:bg-black'/>
<NavUl {activeUrl} {activeClass} {nonActiveClass}>
	<NavLi href="/">Home</NavLi>
	<NavLi href="/products">Products</NavLi>
	<NavLi href="/services">Services</NavLi>
	<NavLi href="/about">About</NavLi>
	<NavLi href="/careers">Careers</NavLi>
</NavUl>

</Navbar>

</header>
<slot></slot>
