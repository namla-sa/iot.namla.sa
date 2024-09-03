<script>
	import '../app.css';
	import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte';
</script>

<Navbar>
	<NavBrand>
		<img src="/logo.png" class="me-3 h-6" alt="Company Logo">
		<span></span>
	</NavBrand>
</Navbar>

<slot></slot>
