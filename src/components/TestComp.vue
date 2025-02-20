<script>
export default {
    data() {
        return {
            users: [
                {
                    id: 1,
                    name: 'name1',
                    salary: 100,
                    age: 30,
                    isEdit: false,
                },
                {
                    id: 2,
                    name: 'name2',
                    salary: 200,
                    age: 40,
                    isEdit: false,
                },
                {
                    id: 3,
                    name: 'name3',
                    salary: 300,
                    age: 50,
                    isEdit: false,
                },
            ],
        };
    },
    methods: {
        edit(user) {
            user.isEdit = true;
        },
        save(user) {
            user.isEdit = false;
        },
        remove(userId) {
            this.users = this.users.filter(user => user.id !== userId);
        },
    },
};
</script>

<template>
    <table>
        <thead>
            <tr>
                <th>ID</th>
                <th>Имя</th>
                <th>Зарплата</th>
                <th>Возраст</th>
                <th>Редактировать</th>
                <th>Удалить</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="user in users" :key="user.id">
                <td>{{ user.id }}</td>
                <td>
                    <template v-if="!user.isEdit">
                        {{ user.name }}
                    </template>
                    <template v-else>
                        <input v-model="user.name" />
                    </template>
                </td>
                <td>
                    <template v-if="!user.isEdit">
                        {{ user.salary }}
                    </template>
                    <template v-else>
                        <input v-model="user.salary" />
                    </template>
                </td>
                <td>
                    <template v-if="!user.isEdit">
                        {{ user.age }}
                    </template>
                    <template v-else>
                        <input v-model="user.age" />
                    </template>
                </td>
                <td>
                    <template v-if="!user.isEdit">
                        <button @click="edit(user)">Редактировать</button>
                    </template>
                    <template v-else>
                        <button @click="save(user)">Сохранить</button>
                    </template>
                </td>
                <td>
                    <button @click="remove(user.id)">Удалить</button>
                </td>
            </tr>
        </tbody>
    </table>
</template>	
  
  