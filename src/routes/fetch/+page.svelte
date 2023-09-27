<script>
	import { error } from "@sveltejs/kit";

    async function getNow(){
        const res = await fetch(`https://worldtimeapi.org/api/timezone/Asia/Tokyo`);
        const text = await res.text()

        console.log(text)

        if (res.ok){
            return text;
        }else{
            throw new Error(text);
        }
    }

    let promise = getNow();

    function handleClick(){
        promise = getNow();
    }
</script>

<button on:click={handleClick}>get not time</button>

{#await promise}
    <p>...waiting</p>
{:then t}
    <p>time is {t}</p>
{:catch error}
    <p>{error}</p>
{/await}
