# Location Entity Type for Foundry VTT

Ideas for a Location Entity in general.  Not everything necessarily belongs in the same class.  I may have
gone overboard with some of the details, but implement the easy stuff first, chip away at the harder stuff later.

Location *could* be implemented as a number of other Entity types, but I think it's different enough from them to
warrant it's own Entity type.

## Properties
List of properties a Location Entity should probably have:
- name: of the location
- type: e.g. city, town, temple, ruin, island, plane, cavern, underground metropolis, continent, shop
- size: physical area of the location
- population: general population size
- residents: Who lives there?
- description:
  - first impression: flavour text describing what the PCs first notice/see/feel/smell about the location
  - details: more information about the location
  - player notes: special section that's always available for players to add details they think may be of use
- coordinates: generally how to find the location
  - absolute: (longitude, latitude, altitude)
    - high altitude could be atop a mountain, floating in the sky, or in space
    - low altitude could mean in a valley, underground, or underwater
  - relative: (e.g. 35 km NE from Neverwinter, or 1 day's walk from the Burrow)
  - special: e.g. on a different plane
- can move: default false, but some locations may move (floating city, Howl's Moving Castle)
- parent location: e.g. if it's a city, what country is it in?  If it's a shop, what town is it in?
- sub locations: (reverse of parent location)
- scene: reference to game scene, if any (future: many scenes? (e.g. pre-encounter, encounter, post-encounter))
- token: e.g. to put on a scene (map) of parent location
  - revealed: has location been revealed on the map?
- notable NPCs: list of important characters (residents, allies, villains) in this location
- known to PCs: do the player characters know about this location yet?


## Features
- Locations should have their own sheets that lays out all this information.
- Token HUD should give the option to open the sheet, or to open the scene
- Token could have a halo of light

