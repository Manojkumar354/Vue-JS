<template>
    
    <h1>HTML Binding</h1>

    <h3 v-html="htmlContent"> </h3>
    <h3 v-html="htmlContent2"></h3>
    
</template>

<script>

export default {
    name: 'HtmlBinding',
    data() {
        return {
            htmlContent: "<h2>This is HTML Binding</h2>",
            htmlContent2: "<h3>This is also HTML Binding</h3>"
        }
    }
}
</script>