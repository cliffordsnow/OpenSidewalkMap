# OpenSidewalkMap

_[opensidewalkmap.us](https://opensidewalkmap.us)_

This is a prototype web map application for viewing [OpenStreetMap](https://openstreetmap.org/about) (OSM) 
sidewalk data. The tool is being developed in support of our 
[Pedestrian Working Group](https://openstreetmap.us/news/2024/02/pedestrian-working-group/), a community project to improve the quality of 
sidewalk data in OSM. 

⚠️ This tool is still in early development and serves as a proof-of-concept. OpenStreetMap US is seeking funding partners to build out the tool as the primary app for visualizing, updating, validating, and maintaining OpenStreetMap trail data in the United States. The app will close the feedback loop between trail users, trail managers, and trail mappers. If you or your organization are interested in supporting this tool, please [contact us](https://openstreetmap.us/contact/) or consider [donating](https://openstreetmap.app.neoncrm.com/forms/trails-stewardship-initiative).

## Prototype functionality

### UI features

- View OpenStreetMap sidewalk data using various map styles.
- Click a feature to view its current tags, relations, and metadata.
- Use quick links to open the feature on [openstreetmap.org](https://openstreetmap.org), iD, JOSM, and other viewers.

### Map styles

OpenSidewalkMap aims to display all crossings, curbs, tactile pads, sidewalks, steps, and footpaths present in OpenStreetMap.

#### Pedestrian Ways

The following style show footways.
- Footpaths


The following styles highlight the presence and values of trail attribute tags. 
Purple lines mean an attribute is missing, incomplete, or needs review, 
while teal lines indicate the attribute is good to go.

- [`crossing`](https://wiki.openstreetmap.org/wiki/Key:crossing)
- [`kerb`](https://wiki.openstreetmap.org/wiki/Key:kerb)
- [`tactile_paving`](https://wiki.openstreetmap.org/wiki/Key:tactile_paving)
- [`surface`](https://wiki.openstreetmap.org/wiki/Key:surface)
- [`steps`](https://wiki.openstreetmap.org/wiki/Tag:highway%3Dsteps)
- [`smoothness`](https://wiki.openstreetmap.org/wiki/Key:smoothness)
- [`width`](https://wiki.openstreetmap.org/wiki/Key:width)
- [`incline`](https://wiki.openstreetmap.org/wiki/Key:incline)
- [`fixme`](https://wiki.openstreetmap.org/wiki/Key:fixme)/[`todo`](https://wiki.openstreetmap.org/wiki/Key:todo)
- [`check_date`](https://wiki.openstreetmap.org/wiki/Key:check_date)/[`survey:date`](https://wiki.openstreetmap.org/wiki/Key:survey:date)
- Last Edited Date: the timestamp of the latest version of the feature

#### Other features that are of interest to pedestrians

- [`buildings`](https://wiki.openstreetmap.org/wiki/Key:building)
- `businesses` Including shops, healthcare, grocery stores, mini-marts, etc.
- [`leisure`](https://wiki.openstreetmap.org/wiki/Key:leisure)
- 


### Map tiles
Trail vector tiles are rendered and hosted by OpenStreetMap US using the schema files [here](https://github.com/osmus/tileservice/blob/main/renderer/layers). Thank you to [@zelonewolf](https://github.com/zelonewolf) for setting up the vector tile pipeline. Render time is currently about 4 hours, so any changes you make will take 4 to 8 hours to appear on the map. Map tiles are not available for public use at this time.

### Static stylesheets
<<<<<<< HEAD
OpenSidewalkMap has complex, parameter-driven styling. For performance, styles are generated at runtime. However, static stylesheets are also generated at build time for ease-of-use by other apps. You can browse the full list of available styles once they are available.<!-- [here](https://opensidewalkmap.us/dist/styles/).--> Generated styles are subject to the same license as the rest of OpenSidewalkMap (see below).
=======
OpenSidewalkMap has complex, parameter-driven styling. For performance, styles are generated at runtime. However, static stylesheets are also generated at build time for ease-of-use by other apps. You can browse the full list of available styles [here](https://opensidewalkmap.us/dist/styles/). Generated styles are subject to the same license as the rest of OpenSidewalkMap (see below).
>>>>>>> b99bd7263d00fbb3b436cb993453ced30e4f497b

## Get involved

### Code of Conduct
Participation in OpenSidewalkMap is subject to the [OpenStreetMap US Code of Conduct](https://wiki.openstreetmap.org/wiki/Foundation/Local_Chapters/United_States/Code_of_Conduct_Committee/OSM_US_Code_of_Conduct). Please take a moment to review the CoC prior to contributing, and remember to be nice :)

### Contributing

You can open an [issue](https://github.com/osmus/OpenSidewalkMap/issues) in this repository if you have a question or comment. Please search existing issues first in case someone else had the same thought. [Pull request](https://github.com/osmus/OpenSidewalkMap/pulls) are public, but we recommend opening or commenting on an issue before writing any code so that we can make sure your work is aligned with the goals of the project.

We also collaborate via the [#sidewalks](https://osmus.slack.com/archives/sidewalks) channel
on [OpenStreetMap US Slack](https://openstreetmap.us/slack). Anyone is free to join.

### Development setup
1. [Clone the repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository)
2. Open your terminal and `cd` into the repo's directory
3. Run `npm install` and `npm run build` (first-time setup only)
4. Run `node serve.js` to start the development server
5. Visit [http://localhost:4001](http://localhost:4001) in your browser
6. That's it!

#### Building sprites

Source vector images for use in the map are located at [/style/sprites/svg/](/style/sprites/svg/). If you add or change any of these, you'll need to rebuild the spritesheets.

1. Install the [spreet](https://github.com/flother/spreet) command line tool
2. Run `npm run sprites`

## License

The OpenSidewalkMap source code is distributed under the [MIT license](https://github.com/osmus/OpenSidewalkMap/blob/main/LICENSE). Dependencies are subject to their respective licenses.
