# ai_data_analysis
Program to analyze data, probably from sports but potentially also eSports and other similar topics. This project will also see how much code can be written via AI agents

## Ideas:
- Auto-clip generator
    - Use "key events" or something from match data & insert your own video
    - Auto-gif, etc

- Player & match ratings
    - Accumulated/averaged over time...easy to search...

## TOOLS:
### Drawing
- Excalidraw https://excalidraw.com
    - https://excalidraw.com/#room=1191f1c0fb92b71cdb4f,BdeWLHXw7aFYxsqwo2I7cg
### AI
- ChatGPT
    - 3.5 (Free)
    - 4 ($20/month)
- Llama 2

## Data Sources
- Whoscored (Free but manual?)
- Sofascore
- FBRef
- Wyscout
- Soccerment
- squawka
- https://statsbomb.com
- https://datasportsgroup.com/sports-coverage/
- https://rapidapi.com/blog/best-sports-apis-ranked/
- https://www.api-football.com/documentation-v3
- Talk with olivia.martin on Discord
    - Each data source calculates or plots event locations (passes, shot s, def actions) differently. MPL soccer has created a package that builds pitch visuals and allows you to pick your data source so you don’t have to manually interpret XY locations from the event
	- https://mplsoccer.readthedocs.io/en/latest/
        - That site is the perfect starting reference
    - Have a match on WhoScored up on Chrome. Then right click and Inspect, then click on Sources. It should default to the match file. It’ll be blank though, so reload the page. It should auto update but if not, click on the match file again. Then on I think line 1397 there is a json file named something like match. If you copy that entire line starting (and including) the {, you can paste that into a JSON to CSV converter online to download the data!
    - One note is that players will be entered as players IDs but I think on line 1394 or 1395 there is a player dictionary to reference—that’s the only tedious part
    - I would note that if you’re coding in Python the X, Y data is OPTA’s data. You can use the MPL Soccer Pitch function and put in pitch_type=‘Opta’ and that will auto calculate any adjustments for you
    - Each data source calculates or plots event locations  (passes, shot s, def actions) differently. MPL soccer has created a package that builds pitch visuals and allows you to pick your data source so you don’t have to manually interpret XY locations from the event


## References:

### Other Projects
- See this ETL pipeline for ideas: https://github.com/nyte-owl/nlstats
    - Uses SQL (Postgresql)
- Machlachbot tech: (https://twitter.com/ChicagoDmitry/status/1580141723631882242)
    — https://mplsoccer.readthedocs.io/en/latest/index.html
    — https://dagster.io/
    — https://fastapi.tiangolo.com/
    — https://www.thesportsdb.com/

