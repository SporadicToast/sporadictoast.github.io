<script lang="ts">
    import { Accordion } from "@skeletonlabs/skeleton-svelte";

    import {Smile, Briefcase} from '@lucide/svelte';

    let value = $state(['about', 'prog'])
    
</script>
<div class="m-5 flex flex-wrap overflow-x-hidden max-w-full">
<Accordion {value} onValueChange={(e) => (value = e.value)} multiple classes="max-w-full">
    <Accordion.Item value="about">
        {#snippet lead()}<Smile/>{/snippet}
        {#snippet control()}About Me{/snippet}

        {#snippet panel()}
        <p>Welcome to my website! I love embracing challenges and always make it a point that I learn as much as an I whenever I can. I usually love tinkering around and trying new things! I've had a passion for programming ever since I was young and in my free time I repair and refurbish electronics to give them a second life.</p>
        {/snippet}
    </Accordion.Item>
    <Accordion.Item value="prog">
        {#snippet lead()}<Briefcase/>{/snippet}
        {#snippet control()}Proficiencies{/snippet}

        {#snippet panel()}
        <div class="flex flex-wrap gap-2 w-full max-w-full">
            <button type="button" class="chip preset-filled-primary-500">Web Technologies</button>
            <button type="button" class="chip preset-filled-secondary-500">Database Management</button>
            <button type="button" class="chip preset-filled-tertiary-500">Tools and Management</button>
            <button type="button" class="chip preset-filled-warning-500">Data Engineering and Visualization</button>
            <button type="button" class="chip preset-filled-surface-500">Hardware Technologies</button>
        </div>
        
        <div class="flex flex-wrap gap-2 w-full max-w-fullap-4 my-5">
            <button type="button" class="chip preset-filled-primary-500">Typescript</button>
            <button type="button" class="chip preset-filled-primary-500">Javascript</button>
            <button type="button" class="chip preset-filled-primary-500">SvelteKit</button>
            <button type="button" class="chip preset-filled-primary-500">NodeJS</button>
            <button type="button" class="chip preset-filled-primary-500">Tailwind</button>

            <button type="button" class="chip preset-filled-secondary-500">PostgreSQL</button>
            <button type="button" class="chip preset-filled-secondary-500">MongoDB</button>
            <button type="button" class="chip preset-filled-secondary-500">SQLite</button>

            <button type="button" class="chip preset-filled-tertiary-500">Docker</button>
            <button type="button" class="chip preset-filled-tertiary-500">Figma</button>
            <button type="button" class="chip preset-filled-tertiary-500">Github CI</button>
            <button type="button" class="chip preset-filled-tertiary-500">Git</button>
            <button type="button" class="chip preset-filled-tertiary-500">Knime Workflow</button>

            <button type="button" class="chip preset-filled-warning-500">DAX PowerBI</button>
            <button type="button" class="chip preset-filled-warning-500">Python</button>
            <button type="button" class="chip preset-filled-warning-500">MATLAB</button>

            <button type="button" class="chip preset-filled-surface-500">C</button>
            <button type="button" class="chip preset-filled-surface-500">ESP32</button>
            <button type="button" class="chip preset-filled-surface-500">Arduino</button>
            <button type="button" class="chip preset-filled-surface-500">Digital Electronics & Circuitry</button>
        </div>
        {/snippet}
    </Accordion.Item>
</Accordion>
</div>