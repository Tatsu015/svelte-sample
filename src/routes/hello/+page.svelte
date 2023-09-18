<svelte:head>
    <title>Hello</title>
    <meta name="description" content="Initial tutorial page" />
</svelte:head>

<script>
    import MyComponent from "../../components/MyComponent.svelte";
    let greet = "Hello"
    let name = "World".toUpperCase();
    let src = "https://picsum.photos/seed/picsum/200/300"
    const myComponentProps = {
        id:1,
        name:'spread',
        description:'spreadspreadspread',
    }
</script>

<h1>{greet.toUpperCase()} {name}!</h1>
<img {src} alt="{name} image" height=300 width=200 />
<p>styled text</p>
<MyComponent />
<MyComponent id={10} name="aaa" description="aaaaaaaaaaaaaaaaaa"/>
<MyComponent {...myComponentProps} />

<style>
    p {
        color: purple;
        font-family: monospace;
        font-size: 2rem;
    }
</style>