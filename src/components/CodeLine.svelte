<div class="d-inline-flex flex-column align-items-end" id="code-line-container">
    {#each Array(100).fill() as _, index}
        <div>
            {index + 1} 
        </div>
    {/each}
</div>  


<style>
    #code-line-container {
        color: #68707e;
    }
</style>