<script>
/* -------------------------
 *    IMPORTS COMPONENTS      
 * -------------------------
 */
import Button from '$lib/button.svelte';
import ApiButton from '$lib/apiButton.svelte';

/* -------------------------
 *   VARIABLE DEFINITIONS 
 * -------------------------
 */
let clicks = 0;
let resp = null ?? {message: "No Response"};

/* -------------------------
 *      HANDLES EVENTS
 * -------------------------
 */
const getClicks = (event) => {clicks = event.detail; }
const getResp = (event) => { resp = event.detail; }
</script>

<div class="heading">
    <h1>Dockerised Nginx, SvelteKit & PHP-FPM</h1>
</div>
<div class="sub-heading">
    <h2>This boilerplate facilitates the Dockerization of Nginx, SvelteKit, and PHP-FPM. Enclosed within are two illustrative examples designed to showcase the capabilities of SvelteKit's component system and its interaction with PHP-FPM, providing valuable insights for web development projects.</h2>
</div>

<div class="content">
    <div class="example-1 grid-item grid-left">
        <h2>Example 1</h2>
        <div class="demo-1">
            <Button on:increase={getClicks}/>
            <h2>This is the clicks * 3: <span>{clicks*3}</span></h2>
        </div>
    </div>
    <div class="example-2 grid-item grid-right">
        <h2>Example 2</h2>
        <div class="demo-2">
            <ApiButton on:getData={getResp}/>
            <h2>PHP Response: <span>{resp.message}</span> </h2>
        </div>
    </div>
</div>

<style>
@import url('https://fonts.googleapis.com/css2?family=Chivo:ital,wght@0,300;1,100&display=swap');
.heading{
    display: flex;
    justify-content: center;
    align-self: center;
    width: 100vw;
}

.sub-heading{
    display: flex;
    justify-content: center;
    width: 100vw;
}

.sub-heading h2{
    text-align: center;
    width: 50vw;
    color: white;
    font-weight: lighter;
}

.content{
    display: grid;
    grid-template-columns: 1fr 1fr;
    width: 70vw;
    margin-top: 5vh;
    margin-left:15vw;
    margin-right:15vw;
    border-top: 3px solid white;
}

.grid-item{
    padding: 1rem;
}
.grid-left{
    border-right: 1px solid white;
}

.grid-right{
    border-left: 1px solid white;
}

.example-1{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    color: white;
}
.demo-1{
    display: flex;
    flex-direction: row;
    align-items: center;
}
.demo-1 span{
    color: greenyellow;
}
.demo-1 h2{
    margin-left: 1rem;
    font-weight: lighter;
    margin-top:0;
    margin-bottom: 0;
}

.example-2{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    color: white;
}
.demo-2{
    display: flex;
    flex-direction: row;
    align-items: center;
}
.demo-2 span{
    color: greenyellow;
}
.demo-2 h2{
    margin-left: 1rem;
    font-weight: lighter;
    margin-top:0;
    margin-bottom: 0;
}

h1{
    color: orange;
}

:global(html){
    background: linear-gradient(to bottom right, #55566a, #282834);
    background-repeat: no-repeat;
    background-size: cover;
    border-radius: 10px;
    height: 100vh;
    font-family: 'Chivo', sans-serif;
}
</style>