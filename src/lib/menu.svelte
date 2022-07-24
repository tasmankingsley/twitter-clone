<script>
    import { menu_width } from './stores';
    import { fly } from "svelte/transition";

    function toggle_menu() {
        if($menu_width === 300){
            $menu_width = 0;
        }
    }
</script>

<main>
    <div class="menu" style:width="{$menu_width}px">
        {#if $menu_width === 300 }
        <div class="menu_options" in:fly={{x: -400, duration: 500}}>
            <span on:click={toggle_menu}>x</span>
            <span>option</span>
            <span>option</span>
            <span>option</span>
            <span>option</span>
            <span>option</span>
            <span>option</span>
        </div>
        {/if}
    </div> 
</main>

<style>
.menu {
    font-size: 1.5rem;
    background-color: #0c0c12;
    color: #3658a6;
    position: fixed;
    width: 300px;
    height: 100vh;
    transition: width 0.3s;
    z-index: 3;
}

.menu_options {
    display: grid;
    grid-auto-flow: row;
    grid-template-rows: repeat(7, 100px);
    background-color: #0c0c12;
    /* gap: 20px 0; */
    /* text-align: left; */
}

span {
    line-height: 100px;
    cursor: pointer;
    width: 100%;
    height: 100%;
    /* border-bottom: #fff 1px solid; */
}

span:hover {
    background-color: #fff;
}

</style>