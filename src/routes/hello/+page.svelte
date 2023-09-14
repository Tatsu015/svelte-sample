<svelte:head>
    <title>Hello</title>
    <meta name="description" content="Initial tutorial page" />
</svelte:head>

<script>
    let greet = "Hello"
    let name = "World".toUpperCase();
</script>

<h1>{greet.toUpperCase()} {name}!</h1>