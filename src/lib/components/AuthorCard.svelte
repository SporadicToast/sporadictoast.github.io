<script lang="ts">
    import { Avatar } from '@skeletonlabs/skeleton-svelte';
	import SablayImage from '$lib/assets/sablay.jpg'
	import MedalImage from '$lib/assets/medal.jpg'
    import {RefreshCcw} from '@lucide/svelte';

    let displayPic = $state(SablayImage)
    function swapImage() {
		displayPic === MedalImage ? displayPic = SablayImage : displayPic = MedalImage
	}
</script>

<div class="flex flex-col md:flex-row items-center md:items-startmd:flex-row sm:flex-col">
    <div class="w-full md:w-auto flex justify-center md:justify-start relative">
        <Avatar name="Marc Macaraeg" src={displayPic} size="min-w-[200px] max-w-[10vw] w-full"></Avatar>
        <button onclick={(e) => {e.stopPropagation(); swapImage()}} type="button" class="btn-icon preset-filled absolute top-0 left-0"><RefreshCcw/></button>
    </div>
    <div class="mt-4 md:mt-0 md:ml-4 text-center md:text-left">
        <div class="ml-4t">
            <h1 class="text-4xl">Marc Macaraeg</h1>
            <p class="text-xl">BS Computer Science @ UP Diliman</p>
            <p class="text-xl">IT Manager @ P&amp;G</p>
        <div class="flex gap-4">
        </div>
        </div>
    </div>
</div>