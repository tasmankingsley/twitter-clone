<script>
    import { menu_width } from './stores';

    function toggle_menu() {
        if($menu_width === 0){
            $menu_width = 300;
        }
    }
</script>

<main>
    <div class="top">
        <span class="menu" on:click={toggle_menu}>menu</span>
        <span>feed</span>
    </div>

    <div class="bottom">
        <span>bottom tabs</span>
    </div>
</main>

<style>
    div {
        font-size: 1.5rem;
        background-color: #0c0c12;
        color: #f9f9f9;
        position: fixed;
        width: 100%;
        height: 50px;
        line-height: 50px;
    }

    .top {
        top: 0px;
    }

    .bottom {
        bottom: 0px;
    }

    .menu {
        left: 10px;
        position: absolute;
    }

    span {
        cursor: pointer;
    }

</style>