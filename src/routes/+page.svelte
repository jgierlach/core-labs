<script>
	// Contact form fields
	let name = '';
	let email = '';
	let message = '';

	let showSubmissionSuccess = false;
	async function submitContactForm(event) {
		event.preventDefault();
		const response = await fetch('/api/contact-form-submission', {
			method: 'POST',
			headers: {
				'Content-Type': 'application/json'
			},
			body: JSON.stringify({
				name,
				email,
				message
			})
		});
		if (response.ok) {
			showSubmissionSuccess = true;
			name = '';
			email = '';
			message = '';
			console.log('FORM FIELDS AFTER FUNC', name, email, message, showSubmissionSuccess);
		} else {
			console.error(await response.json());
			alert('Contact form submission unsuccessful.');
			return;
		}
	}
</script>

<!-- ABOUT SECTION BEGINS -->
<div
	class="bg-gradient-to-b from-gray-50 to-gray-100 py-16 dark:from-gray-900 dark:to-gray-800"
	id="about"
>
	<div class="container mx-auto flex flex-col items-center space-y-12 px-6">
		<div class="space-y-4 text-left">
			<p class="mx-auto max-w-3xl text-lg text-gray-600 sm:text-xl dark:text-gray-400">
				Hello 👋, my name is Jan-Edward. I am a fullstack developer and business owner. Over the
				past 3 years, I’ve generated
				<span class="font-semibold text-gray-800 dark:text-white">$2.35 million</span> in revenue by
				creating and scaling digital products and services.
			</p>
		</div>

		<!-- Image with Caption -->
		<div class="flex flex-col items-center space-y-4">
			<img
				src="/stripe-revenue-screenshot-half.png"
				alt="Stripe revenue screenshot"
				class="max-w-full rounded-lg object-cover shadow-lg sm:max-w-lg lg:max-w-2xl"
			/>
			<p class="text-sm text-gray-500 dark:text-gray-400">
				Stripe revenue screenshot (last 3 years)
			</p>
		</div>

		<div class="space-y-4 text-left">
			<p class="mx-auto max-w-3xl text-left text-lg text-gray-600 sm:text-xl dark:text-gray-400">
				And in just under 3 years <span class="font-semibold text-gray-800 dark:text-white"
					>$3.88</span
				> million in revenue selling on Amazon.
			</p>
		</div>

		<!-- <div class="max-w-3xl space-y-4 text-left sm:text-left">
			<p class="text-l text-left text-gray-600 sm:text-xl dark:text-gray-400">
				And in just under 3 years <span class="font-semibold text-gray-800 dark:text-white"
					>$3.88</span
				> million selling on Amazon.
			</p>
		</div> -->

		<!-- Image with Caption -->
		<div class="flex flex-col items-center space-y-4">
			<img
				src="/amazon-revenue-screenshot.png"
				alt="Stripe revenue screenshot"
				class="max-w-full rounded-lg object-cover shadow-lg sm:max-w-lg lg:max-w-2xl"
			/>
			<p class="text-sm text-gray-500 dark:text-gray-400">Amazon revenue 1/31/2022 - 12/31/2024</p>
		</div>
	</div>
</div>
<!-- ABOUT SECTION ENDS -->

<!-- CONTACT US SECTION BEGINS -->
<section id="contact" class="bg-gradient-to-r from-blue-500 to-indigo-600 py-16 dark:bg-gray-900">
	<div class="container mx-auto px-6 lg:px-8">
		<!-- Follow Me Section -->
		<div class="mb-12 text-center">
			<h2 class="text-5xl font-extrabold text-white sm:text-5xl">Contact</h2>
			<div class="mt-6 flex justify-center space-x-6">
				<a
					href="#"
					class="text-white transition hover:text-purple-300"
					aria-label="Visit our Facebook"
				>
					<svg class="h-8 w-8 fill-current" viewBox="0 0 24 24">
						<path
							d="M22.675 0H1.325C.593 0 0 .593 0 1.326v21.348C0 23.408.593 24 1.325 24h11.495v-9.294H9.692v-3.622h3.128V8.413c0-3.1 1.894-4.787 4.659-4.787 1.325 0 2.464.098 2.794.142v3.24h-1.918c-1.504 0-1.794.715-1.794 1.762v2.309h3.588l-.467 3.622h-3.121V24h6.116C23.408 24 24 23.408 24 22.674V1.326C24 .593 23.408 0 22.675 0z"
						/>
					</svg>
				</a>
				<a
					href="#"
					class="text-white transition hover:text-purple-300"
					aria-label="Visit our Twitter"
				>
					<svg class="h-8 w-8 fill-current" viewBox="0 0 24 24">
						<path
							d="M24 4.557a9.835 9.835 0 01-2.828.775 4.92 4.92 0 002.165-2.724 9.867 9.867 0 01-3.127 1.194A4.918 4.918 0 0016.616 3c-2.724 0-4.93 2.206-4.93 4.93 0 .387.043.763.127 1.124-4.094-.205-7.72-2.165-10.141-5.144a4.935 4.935 0 00-.666 2.479c0 1.71.87 3.218 2.19 4.098a4.903 4.903 0 01-2.232-.616v.062c0 2.386 1.697 4.374 3.946 4.828a4.935 4.935 0 01-2.224.084c.628 1.958 2.444 3.383 4.6 3.422A9.863 9.863 0 010 19.54a13.94 13.94 0 007.548 2.212c9.058 0 14.009-7.504 14.009-14.009 0-.213-.005-.425-.015-.637A10.012 10.012 0 0024 4.557z"
						/>
					</svg>
				</a>
				<a
					href="#"
					class="text-white transition hover:text-purple-300"
					aria-label="Visit our LinkedIn"
				>
					<svg class="h-8 w-8 fill-current" viewBox="0 0 24 24">
						<path
							d="M22.23 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.226.792 24 1.771 24H22.23c.978 0 1.77-.774 1.77-1.729V1.729C24 .774 23.208 0 22.23 0zM7.126 20.452H3.713V9.207h3.413v11.245zM5.42 7.735C4.331 7.735 3.453 6.852 3.453 5.776c0-1.075.878-1.96 1.967-1.96 1.088 0 1.967.885 1.967 1.96 0 1.076-.88 1.96-1.967 1.96zm14.999 12.717h-3.413v-5.717c0-1.365-.025-3.118-1.902-3.118-1.903 0-2.195 1.486-2.195 3.017v5.818H9.504V9.207h3.277v1.538h.047c.456-.861 1.568-1.769 3.225-1.769 3.446 0 4.084 2.27 4.084 5.222v6.254z"
						/>
					</svg>
				</a>
			</div>
		</div>

		<!-- Contact Form -->
		<div class="flex justify-center">
			<div class="w-full max-w-xl rounded-lg bg-white p-8 shadow-lg">
				<form onsubmit={submitContactForm}>
					<div class="mb-6">
						<label for="name" class="mb-2 block text-sm font-medium text-gray-700">
							Your Name
						</label>
						<input
							bind:value={name}
							type="text"
							id="name"
							placeholder="Enter your name"
							class="w-full rounded-lg border border-gray-300 bg-gray-50 p-3 text-sm focus:border-blue-500 focus:ring focus:ring-blue-200"
							required
						/>
					</div>

					<div class="mb-6">
						<label for="email" class="mb-2 block text-sm font-medium text-gray-700">
							Your Email
						</label>
						<input
							bind:value={email}
							type="email"
							id="email"
							placeholder="Enter your email"
							class="w-full rounded-lg border border-gray-300 bg-gray-50 p-3 text-sm focus:border-blue-500 focus:ring focus:ring-blue-200"
							required
						/>
					</div>

					<div class="mb-6">
						<label for="message" class="mb-2 block text-sm font-medium text-gray-700">
							Your Message
						</label>
						<textarea
							bind:value={message}
							id="message"
							placeholder="Write your message here"
							rows="6"
							class="w-full rounded-lg border border-gray-300 bg-gray-50 p-3 text-sm focus:border-blue-500 focus:ring focus:ring-blue-200"
							required
						></textarea>
					</div>

					<button
						type="submit"
						class="w-full rounded-lg bg-purple-600 px-6 py-3 text-sm font-medium text-white transition hover:bg-purple-700 focus:outline-none focus:ring-4 focus:ring-purple-300 dark:focus:ring-purple-800"
					>
						Send Message
					</button>
				</form>
				{#if showSubmissionSuccess}
					<div
						class="mt-6 rounded-lg bg-gradient-to-r from-purple-600 to-blue-600 p-6 text-white shadow-lg"
					>
						<h1 class="text-center text-3xl font-bold">🎉 Message Sent!</h1>
						<p class="mt-4 text-center text-lg">
							Thank you for reaching out! We’ve received your message and will get back to you as
							soon as possible.
						</p>
					</div>
				{/if}
			</div>
		</div>
	</div>
</section>
<!-- CONTACT US SECTION ENDS -->
