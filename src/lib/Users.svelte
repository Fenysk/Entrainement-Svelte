<script>
    import FilterUser from "./FilterUser.svelte";
    import User from "./User.svelte";


    let users = [
        {
            id:1,
            image: 'https://scontent-mrs2-1.xx.fbcdn.net/v/t39.30808-1/271712940_2061769743973521_7063223196201014351_n.jpg?stp=c577.197.833.833a_dst-jpg_s200x200&_nc_cat=109&ccb=1-7&_nc_sid=7f2442&_nc_ohc=ikvx2ZoAR-0AX-4yf8h&_nc_ht=scontent-mrs2-1.xx&oh=00_AfCYWf6yIklLeSPe9BCrYx_jE_qdcTe-ra7xSy86YSnG8Q&oe=637E0756',
            name: 'Alexis',
            email: 'alexisgailleton@icloud.com',
            active: true,
        },

        {
            id:2,
            image: 'https://pbs.twimg.com/profile_images/977496875887558661/L86xyLF4_400x400.jpg',
            name: 'Vitalik',
            email: 'vitalik@gmail.com',
            active: false,
        },
        
        {
            id:3,
            image: 'https://pbs.twimg.com/profile_images/1590968738358079488/IY9Gx6Ok_400x400.jpg',
            name: 'Elon',
            email: 'contact@tesla.com',
            active: false,
        },
        
        {
            id:4,
            image: 'https://pbs.twimg.com/profile_images/1433110531620151297/yryIod5I_400x400.jpg',
            name: 'Hasheur',
            email: 'contact@justmining.fr',
            active: false,
        },
        
        {
            id:5,
            image: 'https://pbs.twimg.com/profile_images/1544431732304363525/enTX8Ix9_400x400.jpg',
            name: 'Luck Fast',
            email: 'luckfastsama@gmail.com',
            active: true,
        },
        
        {
            id:6,
            image: 'https://pbs.twimg.com/profile_images/1530596275971936257/I5yowVDL_400x400.jpg',
            name: 'Jordan',
            email: 'j.bardella@rassemblementnational.fr',
            active: false,
        },

        {
            id:7,
            image: 'https://pbs.twimg.com/profile_images/1572157686396878854/3N6-9BPK_400x400.jpg',
            name: 'Antoine',
            email: 'antoine.daniel@20ty.gg',
            active: false,
        },

        {
            id:8,
            image: 'https://pbs.twimg.com/profile_images/1569877763246510080/MVB2k9wt_400x400.jpg',
            name: 'Adrien',
            email: 'dach@zerator.tv',
            active: false,
        },
    ]

    let filteredUsers = users

    const filter = ({detail}) => {

        if (detail === 'null') {
            filteredUsers = users
            return
        }

        const active = detail === 'true'
        filteredUsers = users.filter((user) => user.active === active)

    }

</script>

<h1 class='text-2xl text-center mt-10 underline'>Liste des utilisateurs</h1>

<div class='users_list'>

    <FilterUser on:filter={filter} />

    { #each filteredUsers as user }

    <User {user} />

    { :else }

    <p>Aucun utilisateur trouvé</p>
    
    { /each }

</div>