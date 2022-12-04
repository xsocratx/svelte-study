<script>
    import EventDispatcher from "./EventDispatcher.svelte";
    function handleMessage(event){
        alert(event.detail.text);
    }
</script>

<EventDispatcher on:message={handleMessage} />