<script>

    let users = [
        {
            image: 'https://scontent-mrs2-1.xx.fbcdn.net/v/t39.30808-1/271712940_2061769743973521_7063223196201014351_n.jpg?stp=c577.197.833.833a_dst-jpg_s200x200&_nc_cat=109&ccb=1-7&_nc_sid=7f2442&_nc_ohc=ikvx2ZoAR-0AX-4yf8h&_nc_ht=scontent-mrs2-1.xx&oh=00_AfCYWf6yIklLeSPe9BCrYx_jE_qdcTe-ra7xSy86YSnG8Q&oe=637E0756',
            name: 'Alexis',
            email: 'alexisgailleton@icloud.com',
        },

        {
            image: 'https://pbs.twimg.com/profile_images/977496875887558661/L86xyLF4_400x400.jpg',
            name: 'Vitalik',
            email: 'vitalik@gmail.com',
        },
        
        {
            image: 'https://pbs.twimg.com/profile_images/1590968738358079488/IY9Gx6Ok_400x400.jpg',
            name: 'Elon',
            email: 'contact@tesla.com',
        },
        
        {
            image: 'https://pbs.twimg.com/profile_images/1433110531620151297/yryIod5I_400x400.jpg',
            name: 'Hasheur',
            email: 'contact@justmining.fr',
        },
        
        {
            image: 'https://pbs.twimg.com/profile_images/1544431732304363525/enTX8Ix9_400x400.jpg',
            name: 'Luck Fast',
            email: 'luckfastsama@gmail.com',
        },
        
        {
            image: 'https://pbs.twimg.com/profile_images/1530596275971936257/I5yowVDL_400x400.jpg',
            name: 'Jordan',
            email: 'j.bardella@rassemblementnational.fr',
        },

        {
            image: 'https://pbs.twimg.com/profile_images/1572157686396878854/3N6-9BPK_400x400.jpg',
            name: 'Antoine',
            email: 'antoine.daniel@20ty.gg',
        },

        {
            image: 'https://pbs.twimg.com/profile_images/1569877763246510080/MVB2k9wt_400x400.jpg',
            name: 'Adrien',
            email: 'dach@zerator.tv',
        },
    ]

</script>

<div class='users_list'>

        {#each users as {image, name, email}, i}
        <div class='user'>

            <p class='text'>Numéro {i+1}</p>
            <img src='{image}' alt="{name}"/>
            <h3 class='user_name text'>{name}</h3>
            <p class='user_email text'>{email}</p>

        </div>
        {/each}

        <!-- Autre solution

            {#each users as user, i}
            <div class='user'>

                <p class='text'>Numéro {i+1}</p>
                <img src='{user.image}' alt="{user.name}"/>
                <h3 class='user_name text'>{user.name}</h3>
                <p class='user_email text'>{user.email}</p>

            </div>
            {/each}

        -->
  
</div>

<style lang="scss">
    * {
        margin: 0;
        padding: 0;
    }

    .users_list {
        display: flex;
        flex-flow: wrap;

        .user {
            margin: 16px;
            padding: 16px 12px;

            width: 150px;

            border-radius: 16px;

            display: flex;
            flex-flow: column;
            justify-content: center;
            align-items: center;

            img {
                height: 100px;
                border-radius: 8px;
            }

            .user_name {
                margin: 4px;
                font-weight: bold;
            }

            .user_email {
                font-size: 0.7rem;
                color: black !important;
                background-color: rgba(white, 0.75);
                padding: 6px;
                border-radius: 3px
            }
            
            .text {
                color: white;
                width: 100%;
                text-align: center;
                overflow: hidden;
            }

            background-color: rgba(230, 0, 0, 0.8);
        }
    }
</style>