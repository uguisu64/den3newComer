<script>
    import HoverButton from "$lib/component/HoverButton.svelte";

    import { onMount } from "svelte";
    import { slide } from "svelte/transition";
    const meetingDatas = [
        {
            title: "第1回",
            date: "4/3(木) 20:00~",
            content: "2025年度 電子計算機研究会 新入生説明会",
            meetingUrl: "https://shibaura-it.zoom.us/j/96109677103?pwd=APhpHOiKkXVFtgkhp0HJ5IQksP2cr6.1"
        },
        {
            title: "第2回",
            date: "4/11(金) 20:00~",
            content: "2025年度 電子計算機研究会 新入生説明会",
            meetingUrl: "https://shibaura-it.zoom.us/j/94503559378?pwd=eFSyuuyLcvk77RuDAIIBfbO7IWdsrj.1"
        },
        {
            title: "第3回",
            date: "4/20(日) 20:00~",
            content: "2025年度 電子計算機研究会 新入生説明会",
            meetingUrl: "https://shibaura-it.zoom.us/j/98604222756?pwd=Ywrk1a6ZCG5BcSl5d1MWb4Q6bys6vI.1"
        },
    ]
    let index = $state(2)
</script>


<h2>Zoom説明会日程</h2>
<p>2025年度の説明会はZoomで行います．全3回を予定</p>
<div class="buttons">
    {#each meetingDatas as meeting, i}
        <HoverButton text={meeting.title} isSelected={i === index} onclick={() => {index = i}}></HoverButton>
    {/each}
</div>
{#key index}
    <section>
        <h3>{meetingDatas[index].content}</h3>
        <p>{meetingDatas[index].date}</p>
        <a href={meetingDatas[index].meetingUrl} target="_blank">ZoomMeetingに参加する</a>
    </section>
{/key}

<p>全3回のZoom説明会は終了しました．Zoom説明会で使用した，資料を公開します．</p>

<embed src="/den3newComer/newComerSlide.pdf" type="application/pdf">


<p>電算はいつでも新入部員を歓迎します．メールで連絡いただければ，対応いたします．</p>
<p>Zoom説明会に参加できない方は相談からでも連絡いただいて大丈夫です．</p>
<div class="email-box">電算公式メールアドレス：<br><strong>den3.shibaura@gmail.com</strong></div>

<style>
    .email-box {
        background-color: #e3f2fd;
        padding: 1rem;
        border-radius: 8px;
        text-align: center;
        margin-top: 1rem;
        word-break: break-all;
    }
    
    .buttons {
        display: flex;
        justify-content: center;
        width: 100%;
        background-color: #e3f2fd;
        padding-bottom: 5px;
    }

    section {
        background-color: rgb(250, 250, 250);
        padding: 1.5rem;
        margin-bottom: 1.5rem;
    }

    h2 {
        border-left: 5px solid #007BFF;
        padding-left: 0.5rem;
        margin-bottom: 1rem;
    }

    embed {
        width: 100%;
        aspect-ratio: 16/10;
    }
</style>