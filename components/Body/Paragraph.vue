<template>
    <div class="paragraph-container">
        <p><br></p>
        <h3>
            <b>{{ paragraph.title }}</b>
        </h3>
        <p><br></p>
        <p class="paragraph-desc">{{ paragraph.description }}</p>
    </div>
</template>

<script>
export default {
    props: {
        paragraph: Object
    }
}
</script>
