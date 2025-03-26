<script>
    import ZoomMeeting from "./ZoomMeeting.svelte";
    import Activity from "./Activity.svelte";
</script>

<header>
    <h1>電子計算機研究会 新歓ページ</h1>
<p>芝浦工業大学公認サークル</p>
</header>

<div class="container">

    <section>
        <h2>電子計算機研究会とは</h2>
        <p>情報系の技術に興味を持った芝浦工業大学の学生が運営する大学公認サークルです．</p>
        <p><a href="https://x.com/sit_densan" target="_blank">▶︎ 電算公式Twitterアカウント</a></p>
    </section>

    <section>
        <ZoomMeeting></ZoomMeeting>
    </section>

    <section>
        <Activity></Activity>
    </section>

</div>

<svelte:head>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@300;400;700&display=swap');
        body {
            font-family: "Noto Sans JP", sans-serif;
        }
    </style>
</svelte:head>

<style>
    header {
        background-color: #007BFF;
        padding: 2rem;
        text-align: center;
        color: white;
    }

    h1 {
        margin-bottom: 0.5rem;
        font-size: 2rem;
        
    }

    .container {
        max-width: 800px;
        margin: auto;
        padding: 2rem;
    }

    section {
        background-color: white;
        padding: 1.5rem;
        margin-bottom: 1.5rem;
        border-radius: 12px;
        box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    }

    a {
        color: #007BFF;
        text-decoration: none;
        transition: color 0.2s;
    }

    a:hover {
        color: #0056b3;
        text-decoration: underline;
    }

    h2 {
        border-left: 5px solid #007BFF;
        padding-left: 0.5rem;
        margin-bottom: 1rem;
    }
</style>