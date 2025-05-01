<script lang="ts">
    import { Navigation } from '@skeletonlabs/skeleton-svelte';
    import { base } from '$app/paths';
    import IconFolder from '@lucide/svelte/icons/folder';
	import IconImage from '@lucide/svelte/icons/image';
	import IconMusic from '@lucide/svelte/icons/music';
	import IconVideo from '@lucide/svelte/icons/video';
</script>

<Navigation.Tile id="" labelExpanded="About Me" label="About" href="{base}/">
    <IconFolder />
</Navigation.Tile>
<Navigation.Tile id="projects" labelExpanded="Projects" label="Projects">
    <IconImage />
</Navigation.Tile>
<Navigation.Tile id="certifications" labelExpanded="Certifications" label="Certs">
    <IconMusic />
</Navigation.Tile>
<Navigation.Tile id="contact" labelExpanded="Contact" label="Contact">
    <IconVideo />
</Navigation.Tile>