<script>
    import Card from "$lib/component/Card.svelte";

    const blogs = [
        {
            "title": "楽に背景が描きたい",
            "link": "http://den3.net/activity_diary/2025/02/28/7048/",
            "description": "イラストを描いている人のブログ記事となります"
        },
        {
            "title": "【初心者、電卓アプリ作りに挑戦！",
            "link": "http://den3.net/activity_diary/2021/08/28/4604/",
            "description": "こちらはアンドロイドアプリの作成記事ですね"
        },
    ]
</script>

<h3>その他</h3>

<p>上記のグループ以外でも，スマホアプリ作成や，イラスト制作をしている人もいます．</p>

<h4>ブログ一覧(抜粋)</h4>

{#each blogs as blog}
    <Card title={blog.title} link={blog.link} description={blog.description}></Card>
{/each}