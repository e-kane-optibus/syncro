# syncro-mods

## Purpose
This script performs the following operations that are required for feed compatibility with Syncromatic's Track: <br>
1. Removes all values in the trip_short_name column of trips.txt.<br>
2. Replaces all values in the run_number column with the corresponding values in the block_id column of runcut.txt.<br>
3. Reduces each value in the stop_sequence column of stop_times.txt by 1.

## Usage
Tested with Python 3.9.<br>
```python syncro.py trips.txt runcut.txt stop_times.txt``` <br>
Adjusted files are exported to the current directory as trips_syncro.txt, runcut_syncro.txt, and stop_times_syncro.txt after which the file names can be updated and added to the feed's .zip file to replace the original files. 
