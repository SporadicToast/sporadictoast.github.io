<script lang="ts">
	import '../app.css';
	import { page } from '$app/state'
	import { Navigation } from '@skeletonlabs/skeleton-svelte';
	import NavTiles from '$lib/components/NavTiles.svelte';
	import AuthorCard from '$lib/components/AuthorCard.svelte';
	let { children } = $props();
	let value = $state(getCurrentSelected());

	function getCurrentSelected() {
		return page.url.pathname.substring(1)
	}
</script>

<div class="h-screen w-screen">
	<div class="flex items-center justify-center my-10">
		<!--Large Case-->
		<div class="hidden md:flex sm:hidden">
			<AuthorCard/>
		</div>
		<!--Small case-->
		<div class="md:hidden sm:flex justify-contents">
			<AuthorCard/>
		</div>
	</div>

	<div class="card border-surface-100-900 grid h-full w-full grid-cols-[auto_1fr] border-[1px]">
		<!--Large case!-->
		<div class="hidden xl:flex sm:hidden md:hidden">
			<Navigation.Rail expanded={true} {value} onValueChange={(newValue) => (value = newValue)}>
				{#snippet tiles()}
					<NavTiles />
				{/snippet}
			</Navigation.Rail>
			<div class="m-5">
				{@render children()}
			</div>
		</div>

		<!--Medium screen case!-->
		<div class="hidden sm:hidden xl:hidden md:flex">
			<!-- Component -->
			<Navigation.Rail {value} onValueChange={(newValue) => (value = newValue)}>
			{#snippet tiles()}
				<NavTiles />
			{/snippet}
			</Navigation.Rail>
			<!-- Content -->
			<div class="m-5">
				{@render children()}
			</div>
		</div>

		<!--Small screen case-->
		<div class="sm:flex md:hidden xl:hidden flex-col w-screen">
			<div class="m-5 flex-1">
				{@render children()}
			</div>
			<Navigation.Bar {value} onValueChange={(newValue) => (value = newValue)}>
				<NavTiles />
			</Navigation.Bar>
		</div>
	</div>
</div>