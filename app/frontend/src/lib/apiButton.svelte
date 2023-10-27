<script>
import { createEventDispatcher } from 'svelte'
let dispatch = createEventDispatcher();
let data;
const fetchData = async () => {
    //execute php in static folder labeled router.php
    const response = await fetch('/router.php');
    data = await response.json();
    dispatch('getData', data);
}
</script>

<div on:click={fetchData}>
    <span>Make Request</span>
</div>

<style>
    div {
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: #a881af;
        width: fit-content; 
        height: 50px;
        padding: 3px;
        padding-left: 5px;
        padding-right: 5px;
        border-radius: 1rem;
    }
</style>