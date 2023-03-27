<script>
    export default {
        name:'AppSearch'
    }
</script>


<template>
<div class="select p-5 mx-5">
    <select class="form-select">
        <option selected></option>
        <option value="1">One</option>
        <option value="2">Two</option>
        <option value="3">Three</option>
    </select>
</div>
</template>

<style lang="scss" scoped>
.form-select{
    width: 20%;
}
.select{
    max-width: 1200px;
}
</style>