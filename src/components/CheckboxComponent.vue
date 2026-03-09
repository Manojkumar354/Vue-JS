<template>
    <div class="checkbox-component">
        <h1>Checkbox Data</h1><br/><br/>

        <h2>Technology</h2>
        <label>
            <input type="checkbox" v-model="technology" value="Vue.js">
            Vue.js
        </label>

        <label>
            <input type="checkbox" v-model="technology" value="React">
            React  
        </label>

        <label>
            <input type="checkbox" v-model="technology" value="Angular">
            Angular
        </label>

        <h2>Professions</h2>
        <label>
            <input type="radio" v-model="professions" value="Developer">
            Developer
        </label>
        <label>
            <input type="radio" v-model="professions" value="Designer">
            Designer      
        </label>

        <br/><br/>
        <h3>Selected Technologies: {{ technology }}</h3>    
        <h3>Selected Profession: {{ professions }}</h3>
    </div>
</template>

<script>
export default {
    name: 'CheckboxComponent',
    data() {
        return {
            technology: [],
            professions: ''
        }
    }
}
</script>

<style scoped>
.checkbox-component label {
    display: flex;
    align-items: center;
    cursor: pointer;
    gap: 8px;
}

input[type="checkbox"] {
    cursor: pointer;
}

</style>