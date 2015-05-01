# collectd-bcache

This collectd python module collects [bcache](http://bcache.evilpiepirate.org/) SSD caching statistics.

## Usage

### Collectd

```
<LoadPlugin python>
    Globals true
</LoadPlugin>

<Plugin python>
    # bcache.py is at /opt/collectd-plugins/python
    ModulePath "/opt/collectd-plugins/python"

    Import "bcache"
</Plugin>

```

### Command-line (for testing)

```
# ./bcache.py
DEBUG: bcache-bcache0/bytes-dirty_data = 5261334937
DEBUG: bcache-bcache0/cache_ratio-five_minute = 92.0251997541
DEBUG: bcache-bcache0/cache_ratio-hour = 96.1182476602
DEBUG: bcache-bcache0/cache_ratio-day = 87.6099980315
DEBUG: bcache-bcache0/cache_ratio-total = 82.9416755058
DEBUG: bcache-bcache0/requests-bypass_hits = 2745
DEBUG: bcache-bcache0/requests-bypass_misses = 0
DEBUG: bcache-bcache0/requests-hits = 5989
DEBUG: bcache-bcache0/requests-miss_collisions = 0
DEBUG: bcache-bcache0/requests-misses = 519
DEBUG: bcache-bcache0/requests-readaheads = 0
DEBUG: bcache-bcache0/bytes-bypassed = 360710144

```
