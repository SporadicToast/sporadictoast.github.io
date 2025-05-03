<script lang="ts">
    import { Navigation } from '@skeletonlabs/skeleton-svelte';
    import { base } from '$app/paths';
    import {Smile, GalleryVerticalEnd  } from '@lucide/svelte'
</script>

<Navigation.Tile id="about" labelExpanded="About Me" label="About" href="{base}/">
    <Smile />
</Navigation.Tile>
<Navigation.Tile id="projects" labelExpanded="Projects" label="Projects" href="{base}/projects">
    <GalleryVerticalEnd />
</Navigation.Tile>