<script>
    export let tagName
</script>

<div class="container-fluid p-0">
    <div class="d-flex flex-column">
        <div class="d-flex flex-row">
            <div id="entity">
                &lt;
            </div>
            <div id="tagName">
                {tagName}
            </div>
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
    #entity {
        color: #68707e;
    }
    #tagName {
        color: var(--tag-color);
    }
    div {
        color: whitesmoke;
    }
</style>
