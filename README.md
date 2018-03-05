# twitch_views
## Description
This repo is dedicated to analyzing the relationship between Twitch current viewers, followers, and total views. The aim is to scrape Twitch for broadcasters streaming specific games, collect their data, and fit the small-dimension data to a regression variant.

## Data structure
A specific data entry will contain the following information:
* Streamer name
* Stream time (hour on interval [0,23])
* Stream category
* Follower count
* Total view count
* Concurrent view count for this stream at this time

Based on this, individual streamers and categories can have multiple entries. The current implementation ignores the variance variables like stream time and category could have on current viewership.

## Scraping Process
A scraper navigates to the Twitch browse page for a predefined popular Twitch category. From this page, the scraper collects the username for each current streamer streaming under the category. After collecting each stream for the current category, the scraper then goes to each stream and collects the current viewer, follower, and total view counts. This data represents a single database entry. This data is then stored in the database, after which the process continues for each remaining stream. After all streams have been recorded, the scraper moves on to redo this process for each remaining category.
