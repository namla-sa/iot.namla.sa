<script>
	import '../app.css';
	import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte';
	import { page } from '$app/stores';
	$: activeUrl = $page.url.pathname;
	let activeClass = 'text-cyan-50 bg-cyan-500 md:bg-transparent md:text-cyan-300';
	let nonActiveClass =
		'text-gray-600 hover:bg-gray-300 md:text-gray-300 md:hover:bg-transparent md:border-0 md:hover:text-cyan-500 text-gray-400';
	import { Footer, FooterCopyright, FooterIcon } from 'flowbite-svelte';
	import { GithubSolid, EnvelopeSolid, WhatsappSolid } from 'flowbite-svelte-icons';
</script>

<header class="absolute inset-x-0 top-0 z-50 border-b border-b-cyan-500">
	<Navbar fluid={true} class=" bg-black text-white">
		<NavBrand href="/" class="z-50 flex flex-col items-center justify-center sm:mx-3 mx-2">
			<img
				src="https://cdn.namla.sa/namla.png"
				class="1 me-2 flex h-12 rounded-md"
				alt="Namla Logo"
			/>
			<span class="text-pretty">namla.sa</span>
		</NavBrand>
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
		<div>
			<div class="mt-4 flex justify-center space-x-6 sm:mt-0 rtl:space-x-reverse">
				<FooterIcon href="https://wa.me/966546207191" target="_blank">
					<WhatsappSolid class="hover: h-6 w-6 text-gray-300 hover:text-cyan-300" />
				</FooterIcon>
				<FooterIcon href="mailto:info@namla.sa" target="_blank">
					<EnvelopeSolid class="hover: h-6 w-6 text-gray-300 hover:text-cyan-300" />
				</FooterIcon>
				<FooterIcon href="https://github.com/namla-sa" target="_blank">
					<GithubSolid class="hover: h-6 w-6 text-gray-300 hover:text-cyan-300" />
				</FooterIcon>
			</div>
			<div class="flex items-center justify-center">
				<img src="https://cdn.namla.sa/namla.png" class="me-2 h-12 rounded-md" alt="Namla Logo" />
				<FooterCopyright href="https://namla.sa" by="namla.sa" />
			</div>
		</div>
	</Footer>
</footer>
