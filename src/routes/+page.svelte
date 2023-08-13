<script>
    import CodeTag from "../components/CodeTag.svelte";
    import About from "../components/About.svelte";
</script>

<div class="container-fluid">
    <p class="">
        src > routes > index.js
    </p>
    
    <p class="">
        Thomas Taulo, 1 second ago | 1 author (Thomas Taulo)
    </p>
    <div class="d-flex">
        
        <div class="d-inline-flex flex-column align-items-end ms-3" id="code-line-container">
            {#each Array(100).fill() as _, index}
                <div>
                    {index + 1} 
                </div>
            {/each}
        </div>    
        <div class="d-flex flex-column ms-4">
            <div id="comment">
                // about me
            </div>
            <CodeTag tagName="script" --tag-color=#5296cb>
                <slot>
                    <About/>
                </slot>
            </CodeTag>

            <div class="empty_line">
                placeholder
            </div>

            <div id="comment">
                // school projects
            </div>
            <CodeTag tagName="Project" --tag-color=#49c0aa>
            </CodeTag>
            
            <div class="empty_line">
                placeholder
            </div>

            <div id="comment">
                // work projects
            </div>
            <CodeTag tagName="Project" --tag-color=#49c0aa>
            </CodeTag>

            <div class="empty_line">
                placeholder
            </div>
            
            <div id="comment">
                // hobby / personal projects
            </div>
            
            <CodeTag tagName="Project" --tag-color=#49c0aa>

            </CodeTag>
        </div>
    </div>
</div>

<style>
    #code-line-container {
        color: #68707e;
        height: 100%;
    }
    p {
        color: #68707e;
    }
    #comment {
        color: #679451;
    }

    /* set color same as background to create emtpy line. Bad but temporary solution */
    .empty_line {
        display: flex;
        color: #1f1f1f;;
    }
</style>