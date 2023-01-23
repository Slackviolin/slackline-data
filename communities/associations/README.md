# ISA Associations

This is a list of Slackline Associations(that are ISA Members) for each country around the world. They are displayed on the [SlackMap](https://slackmap.com/communities). This data, is used to hand out editorship rights for lines & spots in SlackMap. All the members of the association become editors for the lines & spots in their country.

If you think the data is incorrect or missing please contact ISA.
**Email**: slackmap@slacklineinternational.org

## How to add/modify data

There are 2 files:

- `associations.json` - contains the detail data for each association in [JSON format](https://en.wikipedia.org/wiki/JSON)
- `associations.geojson` - contains the data only relevant for the map in [GeoJSON format](https://en.wikipedia.org/wiki/GeoJSON). The data has to be as small as possible to keep the map fast. Each feature is a country and contains the `id` of the association in the `properties` field.

Update the each file depending on your need **without** changing the structure of the file and create pull request. To validate the changes you can use:

- [JSONLint](https://jsonlint.com/) to validate the `communities.json` file
- [GeoJSON.io](http://geojson.io/) to validate the `communities.geojson` file

## Adding new country

 If you cannot find the country (adding a association from a new country) you need to add it tot eh geojson
 
 - Just copy paste a feature already in the geojson file and delete `geometry` field and adjust `properties` field accordingly (keep `ft: ca`)
 - You should get the `geometry` object for the country from [this list](https://github.com/AshKyd/geojson-regions/tree/master/countries/50m). Find your country and view the file in raw format (click `Raw` button on Github) and copy the url from browser. Then open [JSONHero](https://jsonhero.io/) and paste the url. This will format the JSON nicely and click on the `geometry` field on left and copy the entire value and paste it in your new feature in the geojson file.
 - Don't forget to add the association to the `associations.json` file as well.