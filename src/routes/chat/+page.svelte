<!-- import Chats from "$lib/" -->
<script>
    import Chats from "$lib/template/Chats.svelte";
    import Acknowledgements from "$lib/template/Acknowledgements.svelte";

    import johnDoe from "$lib/assets/sample_users/john_doe.jpg";

    // Chats
    const chats = [
        {
            Name: "John Doe",
            LastMessage: "Sure, I'll hand in the tasks by EOD.",
            ProfilePictureURL: johnDoe,
        },
        {
            Name: "John Doe, Anita Max Wynn",
            LastMessage:
                "Twisted Tiger seems like a good name for a bar. Let's do it",
        },
        {
            Name: "Personal friend name",
            LastMessage: `Where are you? And I'm so sorry
I cannot sleep, I cannot dream tonight
I need somebody and always
This sick, strange darkness
Comes creeping on, so haunting every time`,
            ProfilePictureURL: "https://profile.line-scdn.net/0m010bf5fb72518ab84aa1c5b5be49aaa36eaf3d71d64d/preview"
        },
    ];
</script>

<h1>Chats</h1>

<div class="chat-lists" id="chat_lists">
    {#each chats as chat}
        <Chats
            name={chat.Name}
            lastMessage={chat.LastMessage}
            profilePictureURL={chat.ProfilePictureURL}
        />
    {/each}
</div>

<br>

<Acknowledgements />

<style>
    * {
        font-family: "Roboto", sans-serif;
    }
</style>
