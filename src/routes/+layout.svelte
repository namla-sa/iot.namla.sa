<script>
	import '../app.css';
	import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte';
	import { page } from '$app/stores';
	$: activeUrl = $page.url.pathname;
	let activeClass = 'text-cyan-50 bg-cyan-500 md:bg-transparent md:text-cyan-300';
	let nonActiveClass =
		'text-gray-600 hover:bg-gray-300 md:text-gray-300 md:hover:bg-transparent md:border-0 md:hover:text-cyan-500 text-gray-400';
	import {
		Footer,
		FooterCopyright,
		FooterLinkGroup,
		FooterLink,
		FooterBrand,
		FooterIcon
	} from 'flowbite-svelte';
	import { FacebookSolid, GithubSolid, DiscordSolid, TwitterSolid } from 'flowbite-svelte-icons';
</script>

<header class="absolute inset-x-0 top-0 z-50 border-b border-b-cyan-500">
	<Navbar fluid={true} class=" bg-black text-white">
		<a href="/">
			<NavBrand class="t flex flex-col items-center justify-center">
				<img src="https://cdn.namla.sa/namla.png" class="me-2 h-12 rounded-md" alt="Namla Logo" />
			</NavBrand>
		</a>
		<NavHamburger class="hover:bg-black" />

		<NavUl {activeUrl} {activeClass} {nonActiveClass}>
			<NavLi href="/">Home</NavLi>
			<NavLi href="/products">Products</NavLi>
			<!-- <NavLi href="/services">Services</NavLi> -->
			<NavLi href="/about">About</NavLi>
			<NavLi href="/research">Research</NavLi>
			<!-- <NavLi href="/blog">Blog</NavLi> -->
			<!-- <NavLi href="/careers">Careers</NavLi> -->
		</NavUl>
	</Navbar>
</header>

<slot></slot>

<footer class="border-t border-t-cyan-500">
	<Footer footerType="socialmedia" class="bg-black ">
		<div class="sm:flex sm:items-center sm:justify-between">
			<FooterCopyright href="https://namla.sa" by="namla.sa" />
			<div class="mt-4 flex space-x-6 sm:mt-0 sm:justify-center rtl:space-x-reverse">
				<FooterIcon href="https://github.com/namla-sa">
					<GithubSolid class="hover: h-5 w-5 text-gray-300 hover:text-cyan-300" />
				</FooterIcon>
				<p class=" text-cyan-50">info@namla.sa</p>
			</div>
		</div>
	</Footer>
</footer>
