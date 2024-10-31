<script>
    import Title from '$lib/header.svelte';
</script>

<header>
    <Title title="svelte"/>
</header>

<main>
    <slot><!-- optional fallback --></slot>
</main>

<footer>
    <h3>Property of Agustin Salas-Vaca</h3>
</footer>