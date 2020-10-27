# LOL Vs. Bots Assist

_Automation for Vs. Bots matches in League of Legends_

_© 2017–2020 T.D. Stoneheart. All rights reserved. Source code available under GPLv3 license._

-----

## Disclaimer

***Use this automation script responsibly and ethically.***

The author **does not** assume any responsibility when you use this automation script, as it is not related to, endorsed by, or affiliated with Riot Games by any way. Your account might get reported and banned.

Unlicensed derivatives, that is, forks of this project without publicizing source code and/or having the original copyright removed, have been around. The author **does not** assume any responsibility when you use those derivatives; **they might contain unwanted code if you are not able to see their source code**.

-----

## What this does

The script automatically creates a Vs. Bots game, accepts the match, attempts to select the user-configured champion, and plays the game. How it plays is simple: to move randomly or along a user-configured lane, and to use all available abilities, until the game is over.

A demonstration video can be found [here](https://www.youtube.com/watch?v=uWjDw5vED4k).

-----

## Important notes

The automation can be paused at any time by pressing <kbd>Shift</kbd>+<kbd>Pause</kbd>. You'll need to switch to another window during the game to be able to use this hotkey. When you pause, a dialog box is presented to ask if you want to resume the automation.

It is recommended that you have created a Vs. Bots game lobby beforehand, with the game client size being 1024×576.

The display scaling setting in your system must be set to 100% (or 96 DPI) for the automation script to work properly.

-----

## Options

|  Vietnamese  |  English  |  Description  |  Recommended selection  |
|-----|-----|-----|-----|
|Chỉ di chuyển |Moving only |Automates one (current) game only. Does not create a new game. |Unchecked |
|Tên tướng |Champion name |Searches for the champion you choose and picks the first champion found. Leave this field blank to select the first available champion in your champion pool. |`Ashe` |
|Phím kỹ năng |Ability keys |Uses the ability keys you configure. Abilities are leveled up and cast in the exact order entered, by using <kbd>Ctrl</kbd> key (for leveling up) and <kbd>Shift</kbd> key (for casting). Summoner spells and item hot keys can also be used. Note that with default key bindings, number keys from <kbd>1</kbd> to <kbd>5</kbd> cause the character to stop due to <kbd>Ctrl</kbd>+<kbd>1</kbd>–<kbd>5</kbd> character actions. |`rqwe` |
|Bản đồ nhỏ |Minimap |Check if your in-game minimap is on the left. Uncheck if it's on the right. |Right (unchecked) |
|Phép bổ trợ |Summoner spells |Uses both summoner spells during the game, by pressing <kbd>Shift</kbd>+<kbd>D</kbd> and <kbd>Shift</kbd>+<kbd>F</kbd>. In case of different key bindings, resort to the _Ability keys_ option. |Checked |
|Độ khó của máy |Bot difficulty |Self-explanatory. Only effective when you didn't create a game lobby before starting automation. |Trung bình _(Intermediate)_ |
|Giới hạn số ván |Game limit |Limits number of played games before stopping automation. Enter `0` _(zero)_ to disable the limit. |`0` |
|Khi hoàn thành |Completion action |Select an action to be done when the game limit is reached. Options include _do nothing_, _exit game_, _sleep_, _hibernate_, and _shut down_. |Không làm gì _(Do nothing)_ |
|Đẩy đường |Pushing lane |Select the lane that the character goes during the game. Options include _disabled_, _top lane_, _middle lane_, _bottom lane_, and _follow teammates_. Disabling this option makes your character move randomly; this helps decrease number of deaths but might incur an AFK warning. Choosing to follow teammates might put yourself in danger if some teammate is AFK. |Đường giữa _(Middle lane)_ |
|Mua vật phẩm |Purchasing item |Select the item you want to purchase in-game. The script can only buy the exact item but not component items in the recipe. It is recommended that you choose an item that is inexpensive but gives good boosts. Expensive items power up your character very slowly, whereas cheap items fill up your inventory quickly. |`BF` |

-----

## Known issues

* The script can't always pick the champion that the user selects. You might stumble upon a _"There was a problem selecting your champion. Please try again."_ message.
* Networking issues might soft-lock the automation, leaving the game stuck in _"Attempting to connect"_.
* The script requires most default key bindings and the in-game minimap scale setting being 100.
* Lane-based movement isn't really smooth and might temporarily stray to another lane.
* The user-configured item name might be occasionally sent as a chat message due to the use of the <kbd>Enter</kbd> key.
* If a web-based pop-up dialog spawn at any time during automation, the script might go haywire, endlessly opening web links, hogging system resources. This issue sometimes appear in Garena servers during events; Riot servers are not yet tested.
* The script can only operate on 100% (96 DPI) display scaling. If the system is in another scaling, `PixelGetColor()` won't find the correct pixel position since the actual pixel resolution has changed, and therefore, the script won't work properly.

-----
