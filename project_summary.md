# Project Title
Global Playground

## Authors
- Elite Sher, https://github.com/elitesher

## Description
'Global Playground' is an interactive sandBox, where local and distant users can play and interact.

Imagine a sandbox with hills and valleys, mountains and lakes.

Virtual beings inhabit the different environments. Like in real life, each of them can only live in certain environments: some under the water, others on the hill top. 
Global Playground is a real sandBox. But this time, the players are from all around the world!. Local and Distant users will be able to watch the installation simultaneously by sharing a live video channel (ChromeWebLab / YouTube channel event). They will also be able to change and affect the environment. By doing so - they control the living populations in the sandbox.

On the sand, different terrains are projected, following the sand shape. The world map (by GOOGLE maps) is projected as well, and resembles the location of the local and distant players. The virtual entities are projected on the sand and react and interact with the map, the terrains the players and with each other. 

Together, they all form the Global Playground - an environment that offers Symbiotic relationships between the physical and the virtual, the near and the far.

## Link to Prototype
NOTE: If your project lives online you can add one or more links here. Make sure you have a stable version of your project running before linking it.

[Google maps interactivity test](https://vimeo.com/90173086?utm_source=email&utm_medium=clip-transcode_complete-finished-20120100&utm_campaign=7701&email_id=Y2xpcF90cmFuc2NvZGVkfGJjODY0MTc3MzI4NDQ2MTYxMDlhZGQ1MmRiNmQ2ZTQzMzM5fDI1Mzg4OTM5fDEzOTU4NzczNjZ8NzcwMQ%3D%3D "Google maps interactivity test")

[Prototype testing](http://vimeo.com/88198341?utm_source=email&utm_medium=clip-transcode_complete-finished-20120100&utm_campaign=7701&email_id=Y2xpcF90cmFuc2NvZGVkfDY2ZTA3YjIwZTU3MGU3MTQxYmE3MzI5MDk0NDllMWMyOTF8MjUzODg5Mzl8MTM5Mzk3MjE4N3w3NzAx "Prototype testing")

## Example Code

```
void setup () {
map = new UnfoldingMap (this, new Google.GoogleMapProvider());
MapUtils.createDefaultEventDispatcher(this, map);
List countries = GeoJSONReader.loadData(this, "countries.geo.json");
List countryMarkers = MapUtils.createSimpleMarkers(countries);
map.addMarkers(countryMarkers);

setupKinect ();
createTerrain ();
createCrestures ();
}

void draw () {
  context.update();
  updateTerrain();
  runCreatures (creature1);
  runCreatures (creature2);
  runCreatures (creature3);
}

function runCreatures(ArrayList <creature> creatures) {
checkCollisionTerrain (); //checks the location of the creature on the terrain
checkMap (); //check if you are in the ocean or a country
behaviour = decideCreatureBehaviour (); //according to the location on the terrain, the creature will behave
runCreature (behaviour);
}
```


## Links to External Libraries
 NOTE: You can also use this space to link to external libraries or Github repositories you used on your project.
 
 These links will be updated continually
 
[Unfolding library Link](http://unfoldingmaps.org/ "Unfolding library Link")

## Images & Videos
NOTE: For additional images you can either use a relative link to an image on this repo or an absolute link to an externally hosted image.

![Example Image](project_images/cover.jpg?raw=true "Example Image")

![Example Image1](project_images/Cover example.jpg?raw=true "Example Image1")

http://vimeo.com/88235744?utm_source=email&utm_medium=clip-transcode_complete-finished-20120100&utm_campaign=7701&email_id=Y2xpcF90cmFuc2NvZGVkfGIxZjI0MWVlYWI4ZTk5M2NiZmVhZjYwMDNiODhjYTIwMTAwMHwyNTM4ODkzOXwxMzk0MDE1MTE3fDc3MDE%3D
