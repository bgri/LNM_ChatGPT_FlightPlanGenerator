# LNM_ChatGPT_FlightPlanGenerator
A prompt for ChatGPT to create flight plans compatible with [Little Navmap](https://albar965.github.io/littlenavmap.html) for use with Flight Simulators

![image](https://user-images.githubusercontent.com/14062627/230480871-06bfac36-0089-42a7-a615-c75be223b695.png)

## Overview
This prompt should generate a reasonably sane flight plan. Maybe. I'm not a pilot and I just wanted something to throw up navigation aids when I'm tooling around in Flight Simulator 2020. This does the trick.

My workflow is:
- run this prompt
- answer the questions
- copy the output to a TEXT file
- save the text file with a name and extension .lnmpln
- load that .lnmpln file into Little Navmap
- review it in Little Navmap
- save it out in MSFS 2020 flightplan format
-   ![image](https://user-images.githubusercontent.com/14062627/230484903-f0e4a87d-48c2-4ab0-b0ad-9f5ffc8b1640.png)
- Then load up MSFS 2020 and load the flight plan. Seems to work fine. Haven't tested it in other flight sims.

## Syntax
Using this prompt, ChatGPT will attempt to generate a reasonable flight plan from an ORIGIN to a DESTINATION.
There are options, and ChatGPT also prompts you for various detail. 

## Input
When ChatGPT says it's ready, enter your idea of a flight plan. I've had success with things like:
- ``` Toronto Montreal ```
- ``` Edmonton to Victoria SCENIC ```
- ``` Ottawa Winnepeg VERY DIRECT ```
- ``` vfr scenic around Maui ```

You may be asked for additional information. Or not. It's kinda random.

There are three keywords it watches for:
- SCENIC - tries to generate a flight plan with waypoints around scenic areas. Not necessairly ones built in the MSFS 2020 world, real world ones.
- DIRECT - tries to find the shortest route with nav beacons or airports between Origin and Destination.
- VERY DIRECT - tries to draw a flight plan directly between Origin and Destination with no other waypoints.

## Observations
- sometimes will pick a random nav point and insist it's valid. Simply re-run the query and you'll get better results.
- if asked for cruising altitude, you can use answers like ``` above the mountains ```. It'll figure it out.
- will generate random en-route waypoints occasionally. Keep 'em or nuke 'em, your choice.

## Great Circle Route and other IFR stuff
- I mostly fly VFR so really can't say if this is working well or not. I've not tested it with airway routes etc. I've written stuff in there, but who knows if it's legit or not :)

## Limitations
- in the free version of Chat_GPT, if there's more than about seven waypoints it'll just stop. It looks like that's a limitation of the output window?
-   I've added a rule to limit the number of SCENIC waypoints. This seems to help but doesn't always get applied. 

## Disclaimer
NOT TO BE USED FOR GENERATION OF REAL WORLD FLIGHT PLANS. Kinda goes without saying, but sometimes ya just gotta say.
