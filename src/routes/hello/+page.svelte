<svelte:head>
    <title>Hello</title>
    <meta name="description" content="Initial tutorial page" />
</svelte:head>

<script>
    import MyComponent from "../../components/MyComponent.svelte";
    let greet = "Hello"
    let name = "World".toUpperCase();
    let src = "https://picsum.photos/seed/picsum/200/300"
</script>

<h1>{greet.toUpperCase()} {name}!</h1>
<img {src} alt="{name} image" height=300 width=200 />
<p>styled text</p>
<MyComponent name="aaa"/>
<MyComponent />

<style>
    p {
        color: purple;
        font-family: monospace;
        font-size: 2rem;
    }
</style>