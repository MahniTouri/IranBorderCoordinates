# IranBorderCoordinates
Contains all coordinates of the border of Iran
Data Sources:
https://overpass-turbo.eu/
via this query:
```
[out:json][timeout:60];
rel["boundary"="administrative"]["admin_level"="2"]["ISO3166-1"="IR"]->.country;
way(r.country:"outer")->.border;
node(w.border);
out skel qt;
```
