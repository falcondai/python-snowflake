snowflake.py
============

Utility functions for creating and melting [Twitter snowflake][1] ID's.

[1]: https://github.com/twitter/snowflake

Examples
--------
```python
import time
from snowflake import *

# using tweet id from https://twitter.com/falcondai/status/345063379196600321
snowflake_id = 345063379196600321
timestamp, data_center, worker, sequence = melt(snowflake_id)
print 'the tweet was created at %s' % local_datetime(timestamp)

# create a snowflake id for the current millisecond
print snowflake(time.time()*1000, 1, 0, 0)
```

License
-------
MIT License

Author
------
Falcon Dai