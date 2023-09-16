
<script>
    let count = 0

    $: doubleCount = count * 2;

    let maybeNotChange = count * 2;

    function countUp(){
        count++;
    }
</script>

<button on:click={countUp}>Count UP!</button>
<p>COUNT : {count}</p>
<p>WCOUNT : {doubleCount}</p>
<p>not change : {maybeNotChange}</p>

<style>
    p {
        text-align: center;
        font-size: 5rem;
    }
</style>