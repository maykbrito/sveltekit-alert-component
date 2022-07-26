<script>
    import '../app.css'
    import Alert from '../components/alert.svelte';
</script>

<header class="text-4xl font-bold shadow-md p-12 mb-12 text-center">Alert Component</header>
<main class="mx-auto container max-w-md px-6">
    <Alert/>
    <slot/>
</main>