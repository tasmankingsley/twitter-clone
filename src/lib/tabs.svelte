<script>
    import { menu_width } from './stores';

    function toggle_menu() {
        if($menu_width = 0){
            $menu_width = 300;
        } else if($menu_width = 300) {
            $menu_width = 0;
        }
    }
</script>

<main>
    <div class="top" on:click={toggle_menu}>top</div>

    <div class="bottom">bottom</div>
</main>

<style>
    div {
        font-size: 1.5rem;
        background-color: #1a1b27;
        color: #f9f9f9;
        position: fixed;
        width: 100%;
        height: 40px;
        line-height: 40px;
    }

    .top {
        top: 0px;
    }

    .bottom {
        bottom: 0px;
    }

</style>