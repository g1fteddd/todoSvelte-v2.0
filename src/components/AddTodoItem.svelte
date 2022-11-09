<script>
    export let title = "Введите задачу которую хотите сделать!";
    export let buttonTitle = "Add Todo";

    let items = [];

    function handleAddClick() {
        items = [...items, "item"];
    }

    $: console.log(items);
</script>

<div class="main-container">
    <label for="todo-text">{title}</label>
    <input class="todo-input" id="todo-text" />
    <button on:click={handleAddClick}>{buttonTitle}</button>
</div>

<style>
    label {
        color: cornsilk;
    }
    .main-container {
        background-color: lightseagreen;
        background-repeat: 5px;
        padding: 10px;
    }
    .todo-input {
        width: 100%;
    }
</style>
