<script>
    import Nested from './Nested.svelte';

    let inputValue = "";

    $: items = ["Buy Bread", "Eat Cheese"];

    const addItem = () => {
        items.push(inputValue)
        alert(items)
    }
</script>


<main>
    <div class="container">

        <h1>My Todos</h1>

        <form on:submit={addItem}>
            <input type="text" placeholder="add new item here..."
                   bind:value="{inputValue}" />
            <button type="submit">add item</button>
        </form>

        <ol id="TodoList">
            {#each items as item}
                <li>{item}</li>
            {/each}
        </ol>

    </div>

</main>

<style>


</style>