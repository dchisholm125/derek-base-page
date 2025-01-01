<script setup lang="ts">

</script>

<template>
    <div class="d-flex" style="background-color: #efefef;">
        <CalloutDown class="mt-3" text="Below is the site in an <iframe> element, you can navigate to it directly to the site via new tab " /> 
        <span class="mt-3 pt-1" > 
            <a 
                href="https://www.thistledownrecoveryhome.com/" 
                class="ms-2 fw-medium fs-5" 
                target="_blank" 
                style="font-family: 'Courier New', Courier, monospace"
                  >
                here</a>.
        </span>
    </div>    
    
    <!-- Could do a less manual calc here, but hey ---  it's just my portfolio =P -->
    <iframe class="border border-solid border-secondary" src="https://www.thistledownrecoveryhome.com/" style="height: calc(100vh - 142px); width: 99vw"></iframe>
</template>