<script>
    export let tagName
    export let projectNameProp = ""
</script>

<div class="container-fluid p-0">
    <div class="d-flex flex-column">
    <!-- <div class="tag_line"></div> -->
        <div class="d-flex flex-row">
            <div id="entity">
                &lt;
            </div>
            <div id="tagName" class={projectNameProp !== "" ? "space": ""}>
                {tagName}
            </div>
            {#if projectNameProp !== ""}
                <div class="d-flex">
                    <div id="identifier">
                        projectName
                    </div>
                    <div>
                        =
                    </div>
                    <div id="string">
                        "{projectNameProp}"
                    </div>
                </div>
            {/if}
            <div id="entity">
                &gt;
            </div>
        </div>
        <div class="ms-5" id="custom-container">
            <slot></slot>
        </div>
        <div class="d-flex flex-row">
            <div id="entity">
                &lt;/
            </div>
            <div id="tagName">
                {tagName}
            </div>
            <div id="entity">
                &gt;
            </div>
        </div>
    </div>
</div>

<style>
    div {
        color: whitesmoke;
    }

    .tag_line {
        border-left: 1px solid grey;
        /* height: 270px; */
        height: 80%;
        transform: translate3d(3px, 35px, 0);
        position: absolute;
    }
</style>
