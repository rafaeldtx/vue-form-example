<template>
    <div class="form">
        <form class="card-grid" v-if="!submitted">
            <h1 class="title" v-if="title">{{ title }}</h1>
            <hr v-if="title">

            <input-group label="Name">
                <input
                    type="text"
                    name="name"
                    id="name"
                    v-model.lazy="attributes.name"
                />
            </input-group>

            <input-group label="Surname">
                <input
                    type="text"
                    name="surname"
                    id="surname"
                    v-model.lazy="attributes.surname"
                />
            </input-group>

             <input-group label="Email">
                <input
                    type="email"
                    name="email"
                    id="email"
                    v-model.lazy="attributes.email"
                />
            </input-group>

            <input-group label="Password">
                <input
                    type="password"
                    name="password"
                    id="password"
                    v-model.lazy="attributes.password"
                />
            </input-group>

            <input-group label="Save Data?">
                <input
                    type="checkbox"
                    name="saveData"
                    id="saveData"
                    v-model.lazy="attributes.saveData"
                />
            </input-group>

            <hr>
            <button @click.prevent="submit">Submit</button>
        </form>

        <div class="card-grid" v-else>
            <result :attributes="attributes" />
        </div>
    </div>
</template>

<script>
import InputGroup from './InputGroup'
import Result from './Result'

export default {
    components: { InputGroup, Result },
    props: {
        title: {
            type: String,
            default: null
        }
    },
    data() {
        return {
            submitted: false,
            attributes: {
                name: null,
                surname: null,
                email: null,
                password: null,
                saveData: false
            }
        }
    },
    methods: {
        submit() {
            this.submitted = true
        }
    }
}
</script>

<style>
.title {
    text-align: center;
}

.form .card-grid {
    background-color: #F2F2F2;
    border-radius: 8px;
    padding: 1rem;
    margin: 1.3rem 15px;
}
</style>
