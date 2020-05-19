I would like to be able to answer some useful questions about boris bike
usage.  Mostly, I would like to know "if I head to the dock, when is worst"

It is pretty trivial to fetch this data, so there are a couple of existing
projects to do so.  The one addition I wanted was to integrate it with munin.

## Quick usage:

    ./monitor_borisbike show $id [$id ...]

Where ID is the internal BikePoint ID number of the dock that you are
interested in - eg, "130" for "Tower Gardens"

    ./monitor_borisbike config $id [$id ...]

Outputs details that can be used with munin, but also shows the location
name of for each ID, which can be used to confirm the correct dock has been
selected.

## With Munin:

Create a config file /etc/munin/plugin-conf.d/borisbike to define the docks
you are interested in monitoring.

    [borisbike]
    end.BORIS_IDS 130 732

copy or symlink the monitor_borisbike file as /etc/munin/plugins/borisbike
and restart munin-node.

## Resources

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
