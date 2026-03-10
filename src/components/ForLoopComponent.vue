<template>
<h1>For Loop Component</h1>
<ul>
    <li v-for="item in items" :key="item">
        {{ item }}
    </li>
</ul>
<br/>
<br/>

<ul>
    <li v-for="user in users" :key="user">
        {{ user.name }} - {{ user.age }}
    </li>
</ul>


</template>

<script>
export default {
    data() {
        return {
            items: ['Item 1', 'Item 2', 'Item 3'],
            users: [
                { name: 'John', age: 30 },
                { name: 'Jane', age: 25 },
                { name: 'Doe', age: 35 }
             ]
        }
    }
}
</script>