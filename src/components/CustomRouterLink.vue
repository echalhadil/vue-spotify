<template>
        <router-link 
        exact 
        active-class=' bg-gray-700 text-gray-100 ' 
        :to="to"
        class="flex items-center space-x-3 px-4 py-2 w-full rounded font-semibold text-sm hover:bg-gray-700 hover:text-gray-100"
        > 
                <slot></slot>
            <p>{{label}}</p>
        </router-link>

</template>

<script>
export default {
    name:'CustomrouterLink',
    props:{
        to:String,
        label:String
    }
}
</script>