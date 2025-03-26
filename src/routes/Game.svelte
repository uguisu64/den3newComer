<script>
    import Card from "$lib/component/Card.svelte";

    const blogs = [
        {
            "title": "進捗報告のすゝめ　＠ゲーム制作",
            "link": "http://den3.net/activity_diary/2024/12/08/6977/",
            "description": "ゲーム制作者のリアルな知見"
        },
        {
            "title": "【新歓ブログリレー】DXライブラリでゲームプログラミング",
            "link": "http://den3.net/activity_diary/2023/03/31/6422/",
            "description": "DXライブラリを使っている今となっては数少ないブログ"
        },
        {
            "title": "【芝浦祭】制作したゲームの紹介",
            "link": "http://den3.net/activity_diary/2022/11/21/6245/",
            "description": "マイコンとUnityで作った，体を動かす音ゲーの紹介記事"
        }
    ]
</script>

<h3>ゲーム班</h3>

<p>ゲーム班では，Unityを使ったゲーム作りがメインです．昔はDxLiblaryなんかも使っていたのですが，時代ですね．今は完全にUnityに移行しています．ゲームはゲームエンジンを使えば比較的簡単に動くものが作れてフィードバックをもらいやすいので，何かプログラムしたいけどやりたいことがない人におすすめ，一緒にゲームを作りましょう</p>

<h4>ブログ一覧(抜粋)</h4>

{#each blogs as blog}
    <Card title={blog.title} link={blog.link} description={blog.description}></Card>
{/each}