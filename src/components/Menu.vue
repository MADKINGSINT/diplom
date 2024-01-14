<template>
    <div id="app">
        <Slide>
            <a id="home" href="#">
                <span>Home</span>
            </a>
        </Slide>
    </div>
</template>

<script>
import { Slide } from "vue-burger-menu";

export default {
    name: "App",
    components: {
        Slide
    }
};
</script>