<script>
    import Card from "$lib/component/Card.svelte";

    const blogs = [
        {
            "title": "IntelArcが3枚あればデカいLLMも動かせる",
            "link": "http://den3.net/activity_diary/2024/11/04/6918/",
            "description": "Intel愛だけのブログ"
        },
        {
            "title": "IntelのNPUを使ってAI処理をやっていくぞ -言語モデル編-",
            "link": "http://den3.net/activity_diary/2024/04/09/6713/",
            "description": "NPUの情報があまりネットにない時から触ってました"
        },
        {
            "title": "【強化学習】コピペでスーパーマリオをクリアしよう！【PyTorch】",
            "link": "http://den3.net/activity_diary/2022/06/18/5785/",
            "description": "機械学習に初めて触れてみたい人におすすめ"
        },
        {
            "title": "PGGANを実装してanimefaceを生成したい",
            "link": "http://den3.net/activity_diary/2021/09/24/4756/",
            "description": "StableDiffusionが騒がれる前のブログですね"
        }
    ]
</script>

<h3>機械学習系</h3>

<p>機械学習系では，ゲームの強化学習や，オセロAI作成などを行っています．アルゴリズムの理解をメインにやっている人もいますが，割と利用する方に舵を切っている人もちらほら．最近では猫も杓子も生成AIの時代なのでちょっと触ってみませんか？</p>

<h4>ブログ一覧(抜粋)</h4>

{#each blogs as blog}
    <Card title={blog.title} link={blog.link} description={blog.description}></Card>
{/each}