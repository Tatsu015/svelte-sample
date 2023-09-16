
<script>
    let count = 0
    function countUp(){
        count++;
    }
</script>

<button on:click={countUp}>Count UP!</button>
<p>{count}</p>

<style>
    p {
        text-align: center;
        font-size: 10rem;
    }
</style>