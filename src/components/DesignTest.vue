<template>
    <div :class="$style.layout">
        <div :class="$style.content">
            <div :class="$style.section">
                <h1>Colors</h1>
                <div :class="$style.pallete">
                    <div :class="[$style.color, 'brand', 'card']">Brand color and text</div>
                    <div :class="[$style.color, 'accent', 'card']">Accent color and text</div>
                </div>
                <div :class="$style.pallete">
                    <div :class="[$style.color, 'surface-1', 'card']">Surface 1 color and text</div>
                    <div :class="[$style.color, 'surface-2', 'card']">Surface 2 color and text</div>
                    <div :class="[$style.color, 'surface-3', 'card']">Surface 3 color and text</div>
                    <div :class="[$style.color, 'surface-4', 'card']">Surface 4 color and text</div>
                </div>
            </div>
            <div :class="$style.section">
                <h1>Text scaling</h1>
                <p class="text-xs">Extra small text</p>
                <p class="text-sm">Small text</p>
                <p class="text-md">Medium text</p>
                <p class="text-lg">Large text</p>
                <p class="text-xl">Extra large text</p>
                <p class="text-xxl">2 extra large text</p>
                <p class="text-xxxl">3 extra large text</p>
            </div>
            <div :class="$style.section">
                <h1>Headings (this is an h1)</h1>
                <h2>Heading level 2</h2>
                <h3>Heading level 3</h3>
                <h4>Heading level 4</h4>
                <h5>Heading level 5</h5>
                <h6>Heading level 6</h6>
            </div>
            <div :class="$style.section">
                <h1>Buttons</h1>
                <button>Unmodified button</button>
                <button :class="['surface-2', 'hoverable']">Surface 2 button</button>
                <a :class="['button', 'surface-2', 'hoverable']" href="">Stylized link</a>
                <button :class="['brand', 'hoverable']">Branded button</button>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
</script>

<style module>
.layout {
    display: grid;
    grid-template-columns: 1fr 10fr 1fr;
    grid-template-areas: "left content right";
    padding: var(--space-lg);
}

.content {
    grid-area: content;
    margin: var(--space-md);
}

.section {
    border: 1px solid var(--color-black);
    border-radius: var(--border-radius);
    padding: var(--space-md);
    margin: var(--space-md);
}

.pallete {
    display: flex;
    gap: var(--space-md);
    padding: var(--space-md);
}

.color {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 200px;
    width: 200px;
}
</style>