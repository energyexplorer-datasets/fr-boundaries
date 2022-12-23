# fr-boundaries

Administrative boundaries used in the EnergyExplorer.org project

## Content

### France

- france-geojson-metropole-lambert.geojson (Lambert-93)
- france-geojson-metropole.geojson (WGS84)

Source : https://github.com/gregoiredavid/france-geojson / Licence Ouverte

### Administrative boundaries

- communes.gpkg
- epci.gpkg
- departements.gpkg
- regions.gpkg

(Lambert-93)

Source : [ADMIN-EXPRESS (nov 22)](https://geoservices.ign.fr/adminexpress) / IGN / Licence Ouverte

### IRIS contours
 
- iris.gpkg (Lambert-93)

Source : [Contours IRIS](https://geoservices.ign.fr/contoursiris) / IGN & INSEE / Licence Ouverte

## .DOWNLOAD_ME files

The large files are stored outside this repository. They are replaced by a ".DOWNLOAD_ME" file containing their URL.

To easily retrieve all files at once, you can use the `./download.sh` utility from the [energyexplorer-datasets/common](https://github.com/energyexplorer-datasets/common) repository.

```
git clone https://github.com/energyexplorer-datasets/common.git
git clone https://github.com/energyexplorer-datasets/fr-solar-installed-capacity.git
cd fr-solar-installed-capacity
../common/download.sh
```

You can have the new or updated files automatically downloaded when you do a `git pull`. For that, add a hook to your git repository:
```
cd fr-solar-installed-capacity # if not already here
echo -e '#!/bin/sh\nexec ../common/download.sh' >> .git/hooks/post-merge
chmod +x .git/hooks/post-merge
```
