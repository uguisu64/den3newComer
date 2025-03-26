<script>
    let { title, description, link } = $props()
</script>

<a class="card" href={link} target="_blank">
    <div class="card-content">
    <h4>{title}</h4>
    <p>{description}</p>
    </div>
</a>

<style>
    .card {
        display: block;
        background: #fff;
        border: 1px solid #ddd;
        border-radius: 8px;
        overflow: hidden;
        text-decoration: none;
        transition: transform 0.2s ease, box-shadow 0.2s ease;
    }
    .card:hover {
        transform: translateY(-4px);
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    }
    .card-content {
        padding: 1rem;
    }
    .card-content h4 {
        margin: 0 0 0.5rem;
    }
    .card-content p {
        margin: 0;
        color: #555;
        font-size: medium;
    }
</style>