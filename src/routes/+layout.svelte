<script>
	import '../app.css';
	import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte';
</script>

<Navbar fluid={true} class=" bg-sky-900 text-sky-100">
<a href="/"><NavBrand>
	<img src="https://cdn.namla.sa/namla.png" class="me-3 h-6 rounded-md" alt="Namla Logo">
	<span class="self-center whitespace-nowrap text-xl font-semibold">namla.sa</span>
</NavBrand>
</a>

<NavHamburger/>
<NavUl>
	<NavLi href="/">Home</NavLi>
	<NavLi href="/products">Products</NavLi>
	<NavLi href="/services">Services</NavLi>
	<NavLi href="/about">About</NavLi>
	<NavLi href="/careers">Careers</NavLi>
</NavUl>
</Navbar>

<slot></slot>
