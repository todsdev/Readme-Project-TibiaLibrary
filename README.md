<!-- # Title -->
# Tibia Library
  ![Demo](https://media.discordapp.net/attachments/655489748885831713/1082405458930843648/logo.png?width=712&height=620)


---

 <!-- # Short Description -->

>- The app uses all the data available from [Tibia Data API](https://tibiadata.com), such as *Characters*, *Creatures*, *Guilds*, *Houses* and more
>- Access to functionalities using [Google Firebase](https://firebase.google.com) to interact with other users
>- Uses [ROOM](https://developer.android.com/jetpack/androidx/releases/room?hl=pt-br) in order to store in the device local database, information such as 
*Creatures* and *Characters*

It was developed in order to supply the need of a official game mobile app with those functions. It is a game that I play over than 15 years,
so I was really excited when I discovered the [Tibia Data API](https://tibiadata.com). After a few months of hard work, this is the result and will be
soon be available on [Google Play](https://play.google.com/store/games?hl=pt_BR&gl=US) for all the Tibian players, as I am! \
<small>*Link available soon*</small>


<!-- # Badges -->
<div style="display: inline_block"><br>
    <img height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/androidstudio/androidstudio-original.svg">
    <img height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/kotlin/kotlin-original.svg">
    <img height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/firebase/firebase-plain.svg">
    <img height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg">
    <img height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg">

</div>

---

# Tags

`Android Studio` `Kotlin` `Coroutines` `MVVM` `Room` `Hilt` `Clean Architecture` `Paging 3` `Firebase Analytics` `AdMob` `Firebase Authentication` `Firebase Realtime Database` `Remote Config`

---


# Demo

## Extra Functions

### Data Error Handling
![](https://media.discordapp.net/attachments/655489748885831713/1082444493103571025/data_error_handling.gif?width=400&height=900)
>- All fragments covered by the *Data Error Handling*, which is a button that refresh the data in case of any problems with the process of data management

***
### Remote Config
![](https://media.discordapp.net/attachments/655489748885831713/1082449294176550983/remote_config.gif?width=900&height=900)
>- *First of all, sorry for the bad gif*
>- All the menus from the *Drawer Navigation* are controlled by the [Google Firebase Remote Config](https://firebase.google.com/docs/remote-config?hl=pt-br), besides the **News Fragment** and **Settings Fragment**.
I opted to wrap the view of those menus to access fragment in order to control any problems that may happen with the app during the time that it's available. It creates a space
to disable features in order to fix and release new versions with the bug fixes and/or improvements. 
>- Most of the fragments contains [Google AdMob](https://admob.google.com/home/) banners in the bottom of the fragment, and the visibility is also controlled by [Google Firebase](https://firebase.google.com) Remote Config
in order to prioritize the *Ads* in the most used fragments. The application also use [Google Firebase Analytics](https://firebase.google.com/docs/analytics?hl=pt-br), a
tool that allows me to access the data in order to know which feature is being more used
>- The [Google Firebase Remote Config](https://firebase.google.com/docs/remote-config?hl=pt-br) allows the developer to send notifications at any time by enabling the boolean key for notifications and a string key, which if is different from empty, sends a notification, creating a very powerful tool

***
### Authentication
![](https://media.discordapp.net/attachments/655489748885831713/1082412483945443348/login_and_register.gif?width=400&height=900)
>- Authentication options, all mediated by [Google Firebase](https://firebase.google.com)
>- Google Authentication
>- Email & Password Authentication
>- Lost Password Recovery

***
### Settings
![](https://media.discordapp.net/attachments/655489748885831713/1082471679374131340/settings.gif?width=400&height=900)
>- Allows the user to enable and disable the **Dark Mode** and the change persists if the app is restarted
>- Check the number of *Characters* and *Creatures* saved in the **Watch List** and the **Bestiary Tracker** respectively
>- Register and unregister the main *Character* of the user in order to be able to interact with the **Community Fragment**, **Find Party Fragment** and **Market Fragment**
>- The registration of a *Character* depends on paramethers that are checked by the [Tibia Data API](https://tibiadata.com) in order to specify which member is using the functions above and, if not used correctly, can be applied restrictions
>- Logout of the app, which causes the inability to use the device, since it's needed to be registered in order to use all the functions provided by the app

***
## Fragments ([Tibia Data API](https://tibiadata.com))

### News
![](https://media.discordapp.net/attachments/655489748885831713/1082415816315777134/news.gif?width=400&height=900)
>- App funcionalities that starts from the **News Fragment**
>- **News Fragment** displaying the list of the last news provided by the game, travelling to the **News Details Fragment**
>- **News Fragment** -> **News Details Fragment**

***
### Characters
![](https://media.discordapp.net/attachments/655489748885831713/1082417246372118609/characters.gif?width=400&height=900)
>- App funcionalities that starts from the **Characters Fragment**
>- **Character Fragment** display a few funcionalities, such as: \
    - Displaying previously the *Watch List* to easy access to the *Characters* into the database \
    - Displaying the information about the user registered *Character* \
    - Allow the user to **search** thought all the *Characters* available into the database 
>- **Characters Fragment** -> **Character Details Fragment**
>- **Character Details Fragment** display the specific data for a *Character*

***
### Creatures
![](https://media.discordapp.net/attachments/655489748885831713/1082425870062456924/creatures_and_bestiary_tracker.gif?width=400&height=900)
>- App functionalities that starts from the **Creatures Fragment**
>- **Creatures Fragment** displaying all the *Creatures* available in the API
>- Displaying specific game content related to the day, such as the *Boosted Creature*
>- Adding *Creatures* into the *Bestiary Tracker* list with a long click
>- **Search** thought the *Creature* list by name, using **Text Watcher** to respond to each new insert or deletion of characters
>- **Creatures Fragment** -> **Creature Details Fragment**
>- **Creature Details Fragment** display the specific data for a **Creature** and also allows adding the it to the *Bestiary Tracker*

***
### Boostable Bosses
![](https://media.discordapp.net/attachments/655489748885831713/1082426925005426839/boostable_bosses.gif?width=400&height=900)
>- App functionalities that starts from the **Boostable Bosses Fragment**
>- **Boostable Bosses Fragment** displaying all the *Boostable Bosses* available in the API
>- Displaying specific game content related to the day, such as the *Boosted Boss*
>- **Search** thought the *Boostable Boss* list by name, using **Text Watcher** to respond to each new insert or deletion of characters

***
### Guilds
![](https://media.discordapp.net/attachments/655489748885831713/1082428345368711198/guilds.gif?width=400&height=900)
>- App functionalities that starts from the **Guilds Fragment**
>- **Guilds Fragment** displays all the *Guilds* related to a specific server (known as **world** in the game)
>- *World* list received thought the API
>- **Guilds Fragment** -> **Guild Details Fragment** -> **Character Details Fragment**
>- **Guild Details Fragment** displays the specific data for a *Guild*, with information such as the members
>- Easily check the content of any *Characters* of the guild with a simple click
>- **Search** thought the *Guild* list by name, using **Text Watcher** to respond to each new insert or deletion of characters

***
### Houses
![](https://media.discordapp.net/attachments/655489748885831713/1082429495958581369/houses.gif?width=400&height=900)
>- App functionalities that starts from the **Houses Fragment**
>- **Houses Fragment** displays all the *Houses* and *Guild Halls* related to a specific server and also a in-game city
>- *World* list received thought the API
>- **Houses Fragment** -> **House Details Fragment** -> **Character Details Fragment**
>- **House Details Fragment** displays the specific data for a *House* or a *Guild Hall*, which information such as: \
    - If it have a owner, who is it \
    - If it's under auction \
    - Values and location 
>- Easily check the *Character* content of owner of the house or of the bid with a simple click

***
### Spells
![](https://media.discordapp.net/attachments/655489748885831713/1082431233830682624/spells.gif?width=400&height=900)
>- App functionalities that starts from the **Spells Fragment**
>- **Spells Fragment** displays all the *Spells* of the game
>- **Spells Fragment** -> **Spell Details Fragment**
>- **Spell Details Fragment** displaying the specific data for a *Spell*
>- **Search** thought the *Spell* list by name, using **Text Watcher** to respond to each new insert or deletion of characters

***
### Highscores
![](https://media.discordapp.net/attachments/655489748885831713/1082434002973102150/highscores.gif?width=400&height=900)
>- App functionalities that starts from the **Highscores Fragment**
>- **Highscores Fragment** displays all the **Highscores** related to a specific server and other paramethers
>- *World* list received thought the API
>- **Highscores Fragment** -> **Character Details Fragment**
>- Easily check the *Character* content of the high ranked players

***
### Kill Statistics
![](https://media.discordapp.net/attachments/655489748885831713/1082436190596243586/kill_statistics.gif?width=400&height=900)
>- App funcionalities that starts from the **Kill Statistics Fragment**
>- *World* list received thought the API
>- **Kill Statistics Fragment** displays all the content related to a specific server about *Creature* kill/death statistics
>- **Search** thought the *Kill Statistics* list by name, using **Text Watcher** to respond to each new insert or deletion of characters

***
### Fansites
![](https://media.discordapp.net/attachments/655489748885831713/1082443643740246157/fansites.gif?width=400&height=900)
>- App functionalities that starts from the **Fansites Fragment**
>- **Fansites Fragment** travels to all the official *Fansites* and *Supporters* websites of the game, but also the *Supporters* of the app

***

## Fragments ([Firebase Realtime Database](https://firebase.google.com/docs/database?hl=pt-br))

### Find Party
![](https://media.discordapp.net/attachments/655489748885831713/1082465883223498822/find_party.gif?width=400&height=900)
>- App functionalities that starts from the **Find Party Fragment**
>- **Find Party Fragment** allows the user to search *Find Party* requests for specific servers
>- **Find Party Fragment** -> **My Find Party Fragment**
>- **My Find Party Fragment** controls the user posts in order to be able to delete whenever they want
>- Interaction in-game only

***
### Market
![](https://media.discordapp.net/attachments/655489748885831713/1082467085558501416/market.gif?width=400&height=900)
>- App functionalities that starts from the **Market Fragment**
>- **Market Fragment** allows the user to search *Market* announcements for specific servers
>- **Market Fragment** -> **My Market Fragment**
>- **My Market Fragment** controls the user announcements in order to be able to delete whenever they want
>- Interaction in-game only

***
### Community
![](https://media.discordapp.net/attachments/655489748885831713/1082467712879575081/community.gif?width=400&height=900)
>- App functionalities that starts from the **Community Fragment**
>- **Community Fragment** allows the user to search *Community* posts for all the game
>- **Community Fragment** -> **My Community Fragment**
>- **My Community Fragment** controls the user posts in order to be able to delete whenever they want
>- **Community Fragment** -> **Community Interaction Fragment**
>- **Community Interaction Fragment** allows the users to communicate between them in a forum example, where there is a main post and comments for the users
>- Interaction in-app only

***

## Fragments ([ROOM](https://developer.android.com/jetpack/androidx/releases/room?hl=pt-br))

### Watch List & Bestiary Tracker
![](https://media.discordapp.net/attachments/655489748885831713/1082469928231252068/watch_list_and_bestiary_tracker.gif?width=400&height=900)
>- Both **Bestiary Tracker Fragment** and **Watch List Fragment** uses [ROOM](https://developer.android.com/jetpack/androidx/releases/room?hl=pt-br)
to store *Creatures* and *Characters*
>- They allow the user to swipe the items and delete them, but also recover if needed
>- They navigate to their specific locations
>- **Watch List Fragment** -> **Character Details Fragment**
>- **Bestiary Tracker Fragment** -> **Creature Details Fragment**

---

# Code Example
```kotlin
class BoostableBossesPagingSource(private val tibiaApi: TibiaApi, private val query: String?) : PagingSource<Int, BoostableBossesModel>() {
    private var firstLoad = true

    override suspend fun load(params: LoadParams<Int>): LoadResult<Int, BoostableBossesModel> {
        if (!firstLoad) return LoadResult.Page(data = listOf(), prevKey = null, nextKey = null)
        firstLoad = false
        val page = params.key ?: Constants.STARTING_PAGE_INDEX
        return try {
            withContext(Dispatchers.IO) {
                val response = tibiaApi.getBoostableBosses(page)
                if (response.isSuccessful) {
                    val boostableBosses = response.body()?.boostableBosses?.boostableBossList
                    val filteredCreatures = boostableBosses?.filter { boostableBoss ->
                        query?.let {
                            boostableBoss.name.contains(query, ignoreCase = true)
                        } ?: true
                    }
                    LoadResult.Page(
                        data = filteredCreatures!!,
                        prevKey = null,
                        nextKey = if (filteredCreatures.isEmpty()) null else page + 1
                    )
                } else {
                    LoadResult.Error(Exception(ERROR))
                }
            }
        } catch (e: Exception) {
            LoadResult.Error(e)
        }
    }

    override fun getRefreshKey(state: PagingState<Int, BoostableBossesModel>): Int? {
        return state.anchorPosition?.let { position ->
            val anchorPage = state.closestPageToPosition(position)
            anchorPage?.prevKey?.plus(1)?: anchorPage?.nextKey?.minus(1)
        }
    }
}
```

This code above shows one of the **Paging Sources** used to page the data received from the API and display for the user in a recycler view. This snippet
allows the application to receive the page with 20 items each, but also allows searchs by text, which I'm using a **Text Watcher** in order to display real-time
results to the user when searching. It also allows the application to handle any data error from the content, and the application handle to display a message to the user
and tells why the data is not being displayed. It's a very helpful and powerful library, the [Paging Library](https://developer.android.com/topic/libraries/architecture/paging/v3-overview?hl=pt-br)
, that gives many methods to deal with all the adversities of network requests.

---

# Libraries

>- [Timber](https://github.com/JakeWharton/timber)
>- [Lifecycle](https://developer.android.com/jetpack/androidx/releases/lifecycle)
>- [Coroutines](https://developer.android.com/kotlin/coroutines?hl=pt-br)
>- [KTX](https://developer.android.com/kotlin/ktx)
>- [Navigation Components](https://developer.android.com/guide/navigation)
>- [Hilt](https://dagger.dev/hilt/)
>- [ROOM](https://developer.android.com/jetpack/androidx/releases/room?hl=pt-br)
>- [Picasso](https://square.github.io/picasso/)
>- [Picasso Palette](https://github.com/florent37/PicassoPalette)
>- [Google Firebase](https://firebase.google.com): \
    -**AdMob** \
    -**Firebase Authentication for 'Email and Password' & 'Google Authentication'** \
    -**Firebase Realtime Database** \
    -**Firebase Analytics** && **Remote Config**
>- [Tibia Data API](https://tibiadata.com)
---

# Contributors

- [Thiago Rodrigues](https://www.linkedin.com/in/tods/)
