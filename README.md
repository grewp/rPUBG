## rPUBG
An R wrapper for the pubgtracker.com public API

## Synopsis

https://pubgtracker.com/ hosts a public API for requesting PUBG player statistics. This wrapper allows R users to easily make API calls and receive player data back in R friendly data types. Use of the package and API requires an API key (Free). To request your API key and for more information about the public API, visit https://pubgtracker.com/site-api.

## Installation

The package can be installed directly from GitHub by using the devtools package:
```R
install.packages("devtools")

library(devtools)

install_github("lazyjustin/rPUBG")

library(rPUBG)
```
## Getting Started

Before making API calls, use the set_api_key function to store your API key:
```R
set_api_key("00000000-0000-0000-0000-000000000000")
```
Next, you can request specific player data with a PUBG player nickname:
```R
fetch_pubg_player_stats("lazyjustin")
```
Or, you can search for a particular player by searching for a 64-bit Steam ID:
```R
find_pubg_player_by_steam_id_64("10101010101010101")
```
## Code examples

Filtered results can also be requested by using the fetch_filtered_pubg_player_stats function:

*Request player stats for "lazyjustin", North American region only*
```R
fetch_filtered_pubg_player_stats("lazyjustin", region = "na")
```
*Request player stats for "lazyjustin", (All regions, aggregated, duo match type only)*
```R
fetch_filtered_pubg_player_stats("lazyjustin", region = "agg", match = "duo")
```
*Request player stats for "lazyjustin", (North America, duo games, 2017-pre2 season)*
```R
fetch_filtered_pubg_player_stats("lazyjustin", region = "na", match = "duo", season = "2017-pre2")
```

## Contributors

Special thanks to https://pubgtracker.com/ for all server functionality and public API.

Thanks to Jeroen Ooms and the jsonlite package:

Jeroen Ooms (2014). The jsonlite Package: A Practical and Consistent Mapping Between JSON Data and R Objects. arXiv:1403.2805 [stat.CO] URL https://arxiv.org/abs/1403.2805.

## License

MIT - Justin B Moore, 2017