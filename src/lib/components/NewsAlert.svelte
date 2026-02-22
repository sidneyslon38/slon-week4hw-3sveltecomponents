<script>
    let {
        alert, // Required: News alert message text
    } = $props();
</script>

<div class = "news-alert-fixed">
    <div class="news-alert">
        <strong>BREAKING NEWS:</strong> {alert}
        <span class="news-alert-space"></span>
    </div>
</div>

<style>
    .news-alert-fixed {
        background-color: var(--color-red);
        color: white;
        padding: var(--spacing-sm);
        position: fixed;
        bottom: 0;
        left: 0;
        right: 0;
        z-index: 1000;
        overflow: hidden;
    }

    .news-alert {
        text-align: center;
        animation: scroll-text 20s linear infinite;
        white-space: nowrap;
        display: inline-block;
    }

    .news-alert-space {
        display: inline-block;
        width: 8vw;
    }

    @keyframes scroll-text {
        0% {
        transform: translateX(100%);
        }
        100% {
        transform: translateX(-100%);
        }
    }
</style>