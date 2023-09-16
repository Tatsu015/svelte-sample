
<script>
    let count = 0
    let debug = false
    $: doubleCount = count * 2;
    $: {
        if (debug === true){
            console.log('[DEBUG]', count)
        }
    }

    let maybeNotChange = count * 2;

    function countUp(){
        count++;
    }
    function toggleDebug(){
        debug = !debug
    }
</script>

<button on:click={toggleDebug}>DEBUG : {debug}</button>
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