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

Direct download :

- https://energyexplorer.s3.fr-par.scw.cloud/communes.a43ce8f71f2969542f258d3b6174084472a254c3e15f1368970a4bdd1c58cbdb.gpkg
- https://energyexplorer.s3.fr-par.scw.cloud/departements.6ab2fe63c9b50427ddef32f6c5384c113ff8ba31d1e30d7a68d88ad8b7f651f1.gpkg
- https://energyexplorer.s3.fr-par.scw.cloud/epci.11a54a2d7a13a243cf887b6db92660f2b0fdcf1bae269d9d87ac971fac2da8ed.gpkg
- https://energyexplorer.s3.fr-par.scw.cloud/regions.674cd4b698eb7af02ee29d81c3cafe4070684f1b6e60d1e852245ef1be892698.gpkg

(Lambert-93)

Source : [ADMIN-EXPRESS (nov 22)](https://geoservices.ign.fr/adminexpress) / IGN / Licence Ouverte

### IRIS contours
 
- iris.gpkg (Lambert-93)

Direct download : https://energyexplorer.s3.fr-par.scw.cloud/iris.b4a1d9dbfbf951840aaeec9cf7612096454d95ef74756e585c1f2c293f91d9ca.gpkg

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
