## rPUBG
An R wrapper for the pubgtracker.com public API

## Synopsis

https://pubgtracker.com/ hosts a public API for requesting PUBG player statistics. This wrapper allows R users to easily make API calls and receive player data back in R friendly data types. Use of the package and API requires an API key (Free). To request your API key and for more information about the public API, visit https://pubgtracker.com/site-api.

## Installation

The package can be installed directly from GitHub by using the devtools package:

install.packages("devtools")
library(devtools)

install_github("lazyjustin/rPUBG")

## Getting Started

Before making API calls, use the set_api_key function to store your API key:
set_api_key("00000000-0000-0000-0000-000000000000")

Next, you can request specific player data with a PUBG player nickname:
fetch_pubg_player_stats("lazyjustin")

Or, you can search for a particular player by searching for a 64-bit Steam ID:
find_pubg_player_by_steam_id_64("10101010101010101")

## Code examples

Filtered results can also be requested by using the fetch_filtered_pubg_player_stats function:

fetch_filtered_pubg_player_stats("lazyjustin", region = "na")  - Request player stats for "lazyjustin", North American region only

fetch_filtered_pubg_player_stats("lazyjustin", region = "agg", match = "duo") - Request player stats for "lazyjustin", (All regions, aggregated, duo match type only)

fetch_filtered_pubg_player_stats("lazyjustin", region = "na", match = "duo", season = "2017-pre2")  - Request player stats for "lazyjustin", (North America, duo games, 2017-pre2 season)

## Contributors

Special thanks to https://pubgtracker.com/ for all server functionality and public API.

## License

MIT - Justin B Moore, 2017