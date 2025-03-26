<script>
    import Card from "$lib/component/Card.svelte";

    const blogs = [
        {
            "title": "【新歓ブログリレー】自作キーボードを作ってみないか",
            "link": "http://den3.net/activity_diary/2024/04/03/6659/",
            "description": "自作キーボードの作成記録"
        },
        {
            "title": "【新歓ブログリレー】LEDの抵抗値の決め方",
            "link": "http://den3.net/activity_diary/2023/03/24/6373/",
            "description": "IoT初心者向けの記事"
        }
    ]
</script>

<h3>IoT制作</h3>

<p>IoT班では、主にラズベリーパイなどを用いて電子工作などを行っています！部室の温度や人がいるかどうかなどを外部から確認できるようにしたり、スピーカーの自作やファイルサーバーなどを作成したりなど電算の活動をより円滑にするためのものも作成しています！電子工作に興味がある、家をIoTにしたい人は大歓迎です！</p>

<h4>ブログ一覧(抜粋)</h4>

{#each blogs as blog}
    <Card title={blog.title} link={blog.link} description={blog.description}></Card>
{/each}