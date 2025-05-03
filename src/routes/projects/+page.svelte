<script lang="ts">
    import { page } from '$app/state'
    let { value } = $props()
</script>
Hello!
{page.url.pathname}