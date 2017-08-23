<template>
    <div>
        <!--
            Variable 'row' holding slot prop references showing unresolved
        -->
        <b-component :data="someData">
            <template scope="row">
                {{ row }}
            </template>
        </b-component>

        <!--
            Destructured component defined prop 'propName' showing unresolved
        -->
        <b-component :data="someMoreData">
            <template scope="{ propName }">
                {{ propName }}
            </template>
        </b-component>

        <!--
            Destructured and reassigned component defined prop 'propName'
            to 'newPropName' showing unresolved
        -->
        <b-component :data="evenMoreData">
            <template scope="{ propName: newPropName }">
                {{ newPropName }}
            </template>
        </b-component>

    </div>
</template>

<script>
    import BComponent from './BComponent.vue'

    export default {
        name: 'aComponent',

        components: { BComponent },

        data(){
            return {
                someData: {foo: 'baz'},
                someMoreData: {bar: 'foo'},
                evenMoreData: {baz: 'bar'}
            }
        }
    }
</script>