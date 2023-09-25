<script>
    let val = ""
    $: gval = val
</script>

<input type="text" bind:value={val}/>
<div>
    {#if gval.length < 4}
        password: 短すぎます    
    {:else if gval.length < 6}
        password: 普通
    {:else}
        password: 強力
    {/if}
</div>