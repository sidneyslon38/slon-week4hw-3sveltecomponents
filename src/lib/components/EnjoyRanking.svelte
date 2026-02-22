<script>
    let {
    } = $props();

    let selectedIcon = $state(null);

    function selectIcon(iconNumber) {
        selectedIcon = iconNumber;
    }
</script>

<div class="enjoy-ranking-container">
    <h3>Did you enjoy this article?</h3>
    <h4>(Click an icon to rate)</h4>
    <div class="enjoy-ranking-icons">
        <img src="icon-dissatisfied.png" alt="Enjoy Ranking Icon 1" class="ranking-icon" class:selected={selectedIcon === 1} onclick={() => selectIcon(1)} />
        <img src="icon-neutral.png" alt="Enjoy Ranking Icon 2" class="ranking-icon" class:selected={selectedIcon === 2} onclick={() => selectIcon(2)} />
        <img src="icon-satisfied.png" alt="Enjoy Ranking Icon 3" class="ranking-icon" class:selected={selectedIcon === 3} onclick={() => selectIcon(3)} />
        <img src="icon-very-satisfied.png" alt="Enjoy Ranking Icon 4" class="ranking-icon" class:selected={selectedIcon === 4} onclick={() => selectIcon(4)} />
    </div>
</div>

<style>
    .enjoy-ranking-container {
        display: flex;
        flex-direction: column;
        align-items: center;
        padding: var(--spacing-md);
        border: 2px solid var(--color-medium-gray);
        border-radius: 8px;
        background-color: var(--color-light-gray);
        width: fit-content;
        margin: 0 auto;
        margin-top: 25px;
    }

    h3 {
        margin: 0 0 var(--spacing-xs) 0;
        text-align: center;
    }

    h4 {
        margin: 0 0 var(--spacing-sm) 0;
        text-align: center;
        font-weight: normal;
        font-style: italic;
    }

    .enjoy-ranking-icons {
        display: flex;
        gap: var(--spacing-sm);
    }

    .ranking-icon {
        width: 50px;
        height: 50px;
        cursor: pointer;
        transition: transform 0.2s ease, filter 0.2s ease;
    }

    .ranking-icon:hover {
        transform: scale(1.1);
        filter: brightness(1.2);
    }

    .ranking-icon.selected {
        filter: brightness(1.5) sepia(1) saturate(8) hue-rotate(65deg);
        transform: scale(1.15);
    }
</style>

