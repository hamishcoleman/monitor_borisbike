I would like to be able to answer some useful questions about boris bike
usage.  Mostly, I would like to know "if I head to the dock, when is worst"

It is pretty trivial to fetch this data, so there are a couple of existing
projects to do so.  The one addition I wanted was to integrate it with munin.

resources:
- https://tfl.gov.uk/tfl/syndication/feeds/cycle-hire/livecyclehireupdates.xml
- https://api-tigris.tfl.gov.uk/BikePoint/BikePoints_448
- https://api-tigris.tfl.gov.uk/swagger/ui/index.html#!/BikePoint/BikePoint_Get
- https://data.london.gov.uk/dataset/number-bicycle-hires

projects:
- https://github.com/samanthacfu/boris-bike-analysis
- https://github.com/ChickenProp/boris-bikes
- https://github.com/SuzeShardlow/boris_bikes
- https://github.com/e-dard/boris
