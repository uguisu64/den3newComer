<script>
    import Game from "./Game.svelte";
    import Iot from "./Iot.svelte";
    import Ml from "./Ml.svelte";
    import Web from "./Web.svelte";
    import Other from "./Other.svelte";

    import HoverButton from "$lib/component/HoverButton.svelte";

    let index = $state(0)
    const activeList = [Game, Iot, Ml, Web, Other]
    const titleList = ["ゲーム班", "IoT班", "機械学習系", "Web系", "その他"]
    let ActiveComponent = $derived(activeList[index])
</script>

<h2>部員の活動内容</h2>

<div class="buttons">
    {#each titleList as title, i}
        <HoverButton text={title} isSelected={i === index} onclick={() => {index = i}}></HoverButton>
    {/each}
</div>

{#key index}
<ActiveComponent></ActiveComponent>
{/key}

<style>
    h2 {
        border-left: 5px solid #007BFF;
        padding-left: 0.5rem;
        margin-bottom: 1rem;
    }
    
    .buttons {
        display: flex;
        justify-content: center;
        width: 100%;
        background-color: #e3f2fd;
        padding-bottom: 5px;
    }
</style>