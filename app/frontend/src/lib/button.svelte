<script>
import { createEventDispatcher } from 'svelte'
let dispatch = createEventDispatcher();

let count = 0;

const increase = () => {
    count += 1;
    dispatch('increase', count);
};
</script>

<div on:click={increase}>
    <span>clicked: {count}</span>
</div>

<style>
    div {
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: #a881af;
        width: 100px;
        height: 50px;
        padding: 3px;
        border-radius: 1rem;
    }
</style>