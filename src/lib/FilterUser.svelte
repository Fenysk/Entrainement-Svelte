<script>
    
    import { createEventDispatcher } from "svelte";

    const dispatch = createEventDispatcher();
    const filter = (e) => {
        dispatch('filter', e.target.value)
    }

</script>

<div class='ml-4 mt-6'>
    <label for='users_list' class='font-bold'>Filtres d'utilisateur :</label>
    <select
        on:change={filter}
        name='user_filtrer'
        id='user_filtrer'
        class='border rounded-lg px-4 py-2 ml-4'>

        <option default value={null}>All</option>
        <option value={true}>Active</option>
        <option value={false}>Inactive</option>
    </select>
</div>