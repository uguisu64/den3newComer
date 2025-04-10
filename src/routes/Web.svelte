<script>
    import Card from "$lib/component/Card.svelte";

    const blogs = [
        {
            "title": "Svelteはいいぞ",
            "link": "http://den3.net/activity_diary/2025/03/18/7105/",
            "description": "実はこの新歓ページもSvelteで作ってます"
        },
        {
            "title": "【新歓ブログリレー】Hasuraのデータ取得の仕組みがよくできている",
            "link": "http://den3.net/activity_diary/2024/04/04/6658/",
            "description": "このブログの著者は面白いブログが多いので見てみてください．"
        },
        {
            "title": "電子計算機研究会のHPを作ってみた",
            "link": "http://den3.net/activity_diary/2019/11/23/59/",
            "description": "このサイトでの最古のブログ記事です．"
        },
    ]
</script>

<h3>Web系</h3>

<img src="/den3newComer/web1.jpg" alt="web画像1"/>

<p>Web系の部員はWebアプリ開発や，ブログの管理などを行っています．アプリ開発ではバックエンド，フロントエンドどちらも開発している部員がいます．</p>

<h4>ブログ一覧(抜粋)</h4>

{#each blogs as blog}
    <Card title={blog.title} link={blog.link} description={blog.description}></Card>
{/each}

<style>
    img {
        margin-left: auto;
        margin-right: auto;
        display: block;
        width: 80%;
    }
</style>