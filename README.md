# Olli Simple Bus Movement Simulator

## Prerequisites

* [Node.js](https://nodejs.org/en/download/)

## Quick Start

1. Clone this [repo](https://github.com/ibm-watson-data-lab/olli-simple-sim)
1. From terminal, go to the root directory of the cloned repo
1. From terminal, Run command

    `npm install`

1. Edit `.env` (in root directory) accordingly
1. From terminal,  run command

    `npm start`

Simulator should start and you should see events in the console.log. If a client app is configured with same Cloudant database, you should see a bus move on the map

## Configuration

The following settings can be configured in the `.env` file:

* `simulator_target_cloudant` -  Cloudant/CouchDB database url (fully qualified) to send events to (e.g, `http://username:password@127.0.0.1:5984/ollilocation`)
* `simulator_number_of_runs` - number of times the simulator runs through the complete route (default: `-1` which mean infinite)
* `simulator_stop_duration` - how long (in milliseconds) to wait at each stop (default: `25`)
* `simulator_event_interval` - how long (in milliseconds) to wait before sending the next coordinate to the database (default: `5`)


		  map.on('click', function(e) {
		    var coordinates = e.lngLat;

		    new mapboxgl.Popup()
		      .setLngLat(coordinates)
		      .setHTML('you clicked here: <br/>' + coordinates)
		      .addTo(map);
		  });




            map.addSource('route2', {
    'type': 'geojson',
    'data': './route2.json' 
});
map.addLayer({
    'id': 'route2',
    'type': 'line',
    'source': 'route2',
    'layout': {
        'line-join': 'round',
        'line-cap': 'round'
    },
    'paint': {
        'line-color': '#007cbf',
        'line-width': 2
    }

});

  map.addSource('route3', {
    'type': 'geojson',
    'data': './route2.json' 
});
map.addLayer({
    'id': 'route3',
    'type': 'line',
    'source': 'route3',
    'layout': {
        'line-join': 'round',
        'line-cap': 'round'
    },
    'paint': {
        'line-color': '#007cbf',
        'line-width': 2
    }

});

# Technical detils

1. `couchdb` - use docker-compose to spin up
2.  
# What can you do with this Repo?
# How to run this demo?
