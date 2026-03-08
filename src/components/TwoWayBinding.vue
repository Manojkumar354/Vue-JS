<template>
    <div class="two-way-binding">
        <h2>Two-Way Binding</h2>
        
        <div class="input-group">
            <label for="text-input">Text Input:</label>
            <input id="text-input" v-model="message" type="text" placeholder="Type something...">
            <p>You typed: {{ message }}</p>
        </div>

        <div class="input-group">
            <label for="number-input">Number Input:</label>
            <input id="number-input" v-model.number="count" type="number">
            <p>Number: {{ count }}</p>
        </div>

        <div class="input-group">
            <label for="checkbox">
                <input id="checkbox" v-model="isChecked" type="checkbox">
                Checkbox: {{ isChecked }}
            </label>
        </div>

        <div class="input-group">
            <label for="select">Select:</label>
            <select id="select" v-model="selectedOption">
                <option value="">-- Choose --</option>
                <option value="vue">Vue</option>
                <option value="react">React</option>
                <option value="angular">Angular</option>
            </select>
            <p>Selected: {{ selectedOption }}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'TwoWayBinding',
    data() {
        return {
            message: '',
            count: 0,
            isChecked: false,
            selectedOption: ''
        };
    }
};
</script>

<style scoped>
.two-way-binding {
    /* max-width: 500px; */
    margin: 20px;
    text-align: center;
}

.input-group {
    margin: 15px 0;
}

label {
    display: block;
    margin-bottom: 5px;
    font-weight: bold;
}

input[type="text"],
input[type="number"],
select {
    padding: 8px;
    border: 1px solid #ccc;
    border-radius: 4px;
    font-size: 14px;
}

p {
    margin: 5px 0 0 0;
    color: #666;
}
</style>