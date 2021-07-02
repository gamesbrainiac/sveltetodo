<script>
    let inputValue = "";

    let items = ["Buy Bread", "Eat Cheese"];

    const addItem = () => {
        items.push(inputValue)
        items = items
    }
</script>

<div class="container">

    <h1 class="text-red-500">My Todos</h1>

    <input type="text" placeholder="add new item here..." bind:value="{inputValue}" />
    <button type="button" on:click={addItem} class="blue" >add item</button>

    <ol id="TodoList">
        {#each items as item}
            <li>{item}</li>
        {/each}
    </ol>

</div>

<style global lang="postcss">
    @tailwind base;
    @tailwind components;
    @tailwind utilities;
</style>