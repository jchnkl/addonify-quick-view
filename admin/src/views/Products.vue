<script setup>
	import Navigation from "../components/layouts/Navigation.vue";
	const { __ } = wp.i18n;
</script>

<template>
	<section class="adfy-container">
		<main class="adfy-columns main-content">
			<aside class="adfy-col start aside secondary">
				<Navigation />
			</aside>
			<section class="adfy-col end site-primary">
				<p>{{ __("Coming soon.....", "addonify-quick-view") }}</p>
			</section>
		</main>
	</section>
</template>
