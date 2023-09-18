
<script>
    let count = 0
    let debug = false
    let maybeNotChange = count * 2;
    let nums = [1,2,3,4]

    $: doubleCount = count * 2;
    $: {
        if (debug === true){
            console.log('[DEBUG]', count)
        }
    }
    $: sum = nums.reduce((t, n)=>t+n,0)

    function countUp(){
        count++;
    }
    
    function toggleDebug(){
        debug = !debug
    }

    function addNum(){
        console.log(nums)
        nums.push(nums.length+1)
    }
    function addNumUpdatable(){
        console.log(nums)
        nums.push(nums.length+1)
        nums = nums
    }
    function addNumByIndex(){
        console.log(nums)
        nums[nums.length] = nums.length+1
    }

</script>

<button on:click={toggleDebug}>DEBUG : {debug}</button>
<button on:click={countUp}>Count UP!</button>
<button on:click={addNum}>Add List!!</button>
<button on:click={addNumUpdatable}>Add List with Udate!!</button>
<button on:click={addNumByIndex}>Add List by index!!</button>
<p>list total : {sum}</p>
<p>COUNT : {count}</p>
<p>WCOUNT : {doubleCount}</p>
<p>not change : {maybeNotChange}</p>
<p></p>

<style>
    p {
        text-align: center;
        font-size: 5rem;
    }
</style>