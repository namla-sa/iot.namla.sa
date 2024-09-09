<script>
	import { Card } from 'flowbite-svelte';
</script>

<div class="relative isolate px-6 pt-14 lg:px-8">
	<div
		class="absolute inset-x-0 -top-40 -z-10 transform-gpu overflow-hidden blur-3xl sm:-top-80"
		aria-hidden="true"
	>
		<div
			class="relative left-[calc(50%-11rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 rotate-[30deg] bg-gradient-to-tr from-[#80fff7] to-[#115ce7] opacity-30 sm:left-[calc(50%-30rem)] sm:w-[72.1875rem]"
			style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)"
		></div>
	</div>

	<div class="container mx-auto px-4 py-8">
		<div class="grid grid-cols-1 gap-8 sm:grid-cols-2 lg:grid-cols-3">
			<div class="single-services-box rounded-lg bg-white p-6 shadow-md">
				<div class="mb-4 flex items-center justify-center">
					<i class="flaticon-megaphone text-3xl text-blue-500"></i>
				</div>
				<h3 class="mb-2 text-xl font-semibold">
					<a href="https://bxtrack.com/services/digital-marketing" class="hover:underline"
						>Digital Marketing</a
					>
				</h3>
				<p class="mb-4 text-gray-700">
					We don't leave any stone unturned when it comes to providing you with the finest digital
					exposure. We generate the most leads with our innovative SEO techniques.
				</p>
				<a
					href="https://bxtrack.com/services/digital-marketing"
					class="learn-more-btn flex items-center text-blue-500 hover:text-blue-700"
				>
					<i class="flaticon-next-button mr-2"></i> Learn More
					<i class="flaticon-next-button ml-2"></i>
				</a>
			</div>

			<!-- Repeat the service box for other services -->
			<div class="single-services-box rounded-lg bg-white p-6 shadow-md">
				<div class="mb-4 flex items-center justify-center">
					<i class="flaticon-keywords text-3xl text-green-500"></i>
				</div>
				<h3 class="mb-2 text-xl font-semibold">
					<a href="https://bxtrack.com/services/website-development" class="hover:underline"
						>Website Development</a
					>
				</h3>
				<p class="mb-4 text-gray-700">
					Your website says a lot about your company and its mission. To keep ahead of the
					competition, you'll need a well-designed, SEO-optimized, and pixel-perfect website.
				</p>
				<a
					href="https://bxtrack.com/services/website-development"
					class="learn-more-btn flex items-center text-green-500 hover:text-green-700"
				>
					<i class="flaticon-next-button mr-2"></i> Learn More
					<i class="flaticon-next-button ml-2"></i>
				</a>
			</div>

			<!-- Continue adding the other service boxes following the same pattern -->
		</div>
	</div>
</div>
