# whosonfirst-globe

## Important

These is _not_ a finished project. It is mostly notes and a work in progress. A good place to start is the [Who's On First globes](https://www.aaronland.info/weblog/2019/02/21/internet/) blog post.

## example

```
$> wof-shapefile-index -timings -out test3.shp -shapetype POLYGON -mode meta /usr/local/data/whosonfirst-data/meta/wof-continent-latest.csv /usr/local/data/whosonfirst-data/meta/wof-country-latest.csv /usr/local/data/whosonfirst-data/meta/wof-region-latest.csv

$> nik2img.py map.xml test.png --bbox -180 -90 180 90 --dimensions 3600 1800

$> gdal_translate -of Gtiff -a_ullr -180 -90 180 90 -a_srs EPSG:4236 test.png test.tiff

$> ./bin/gdal2gores.py -ng 16 ./test.tiff ./gores.jpg
```

## gdal

_Please write me_

## mapnik

### installing mapnik

```
brew install mapnik
```

### installing nik2img

```
pip install mapnik nik2img
```

_I am not actually sure I understand where `nik2img` gets installed when you use `pip`..._

## See also

* https://github.com/springmeyer/nik2img
* https://github.com/whosonfirst/go-whosonfirst-shapefile
* https://github.com/whosonfirst-data/
