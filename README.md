# twitch_views
## Description
This repo is dedicated to analyzing the relationship between concurrent Twitch views, followers, and total views. The aim is to scrape Twitch for broadcasters streaming specific games, collect their data, and fit the small-dimension data to a regression variant.

## Data structure
A specific data entry will contain the following information:
* Streamer name
* Stream time (hour on interval [0,23])
* Stream category
* Follower count
* Total view count
* Concurrent view count for this stream at this time
Based on this, a streamer can have multiple entries. The goal in this design decision is to 1) gather more information for each game and 2) see the impact games have on concurrent viewer counts.
