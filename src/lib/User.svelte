<script>
    export let user
</script>

<div class='user
            flex
            m-5
            bg-white
            border
            p-2
            rounded-lg
            shadow-md
            max-w-lg
            
            hover:shadow-lg
            cursor-pointer
            items-center'>

    <p class='w-20'>{user.id}</p>
    <img class='rounded-full w-24 h-24 mx-4' src='{user.image}' alt="{user.name}"/>
    <h3 class='mx-4 w-20 font-bold'>{user.name}</h3>
    <p class='mx-4 w-20 whitespace-pre-wrap'>{user.email}</p>

</div>