FROM ubuntu:20.04
# BUNDLE LAYERS
RUN apt-get update -y && apt install -y --no-install-recommends \
  curl \
  osmium-tool \
 && rm -rf /var/lib/apt/lists/* 
# Creating 2 dir
RUN mkdir /osmfiles \
 && mkdir /merged \
# Fetching data from 2 locations
 && curl https://download.geofabrik.de/europe/monaco-latest.osm.pbf -o /osmfiles/monaco.osm.pbf \
 && curl https://download.geofabrik.de/europe/andorra-latest.osm.pbf -o /osmfiles/andorra.osm.pbf \
# Merging two into one
 && osmium merge /osmfiles/monaco.osm.pbf /osmfiles/andorra.osm.pbf -o /merged/merged.osm.pbf
