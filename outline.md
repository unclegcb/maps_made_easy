The technique used in the presentation to create a map starts with a Standard Drupal installation, then installs and enables the following modules:

ctools
entity
views
views_ui
addressfield
ctools
geocoder
geofield
geophp
leaflet
libraries

Download the leaflet javascript library from http://leafletjs.com/download.html and unzip it. Rename the folder "leaflet" (removing the version number) and place it in:
sites/all/libraries/

Create your content type, and add a "Postal Address" field to it.
Add a "geolocation" field. Use "Well Known Text (WKT)", and use the "geocode from another field" widget. In the field settings, make sure to select the Postal Address field to be used as the "geocode from"

You can display the geolocation field as a map by configuring the content display, and selecting "Leaflet" as the display option for your field.

To create a map of all your locations, create a view that displays that content type and choose "Leaflet Map" for the display format.

Edit your view and add your geolocation field to the fields.

Under Format, click "Settings" and make sure that geolocation field is being used as the data source.
