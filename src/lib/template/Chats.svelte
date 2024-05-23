<script>
    import defaultImage from "$lib/assets/default_profile.jpg";

    export let name = "Sample person";
    export let lastMessage = "Sample last message";
    export let profilePictureURL = defaultImage;
</script>

<div class="chat-list">
    <!-- TODO: handle cases where display pictures are double, like in groups or multichats -->
    <img class="chat-list-profile-picture" src="{profilePictureURL}" alt="{name}'s chat name display">
    <div class="list-chat-texts">
        <h3 class="list-chat-name">{name}</h3>
        <span class="list-chat-content">
            {lastMessage}
        </span>
    </div>
</div>

<!-- TODO: convert to LESS -->
<style>
    @import "style.css";
</style>
