<script>
	import '../app.css';
	import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte';
</script>
	
<Navbar fluid={true}>
<a href="/"><NavBrand>
	<img src="/logo.png" class="me-3 h-6" alt="Namla Logo">
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
