<template>
    <div>
        <h3>meu Home</h3>
        bem-vind{{ letraPorSexo }} {{ nome }}<br>
        sexo {{ sexo }}
    </div>
</template>


<script>
export default {
    name: 'MyHome',
    props: {
        nome: {type: String, required: true},
        sexo: {type: String, default: 'M'}
    },
    computed:{
        letraPorSexo() {
            if (this.sexo === 'F')
                return 'a'
            else
                return 'o'
        }
    }
}
</script>


<style>

</style>