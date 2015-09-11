# readTrc
Little Python helper function to read .trc binary files from LeCroy Oscilloscopes.
Tested on Python3.

# Installation
Just copy the `readTrc.py` file in your python path.

# Usage
```python
import readTrc
fName = "./C1_00000.trc"
datX, datY, m = readTrc.readTrc( fName )
```

Note that in the above example `m` is a dictionary which contains the metadata. 
For example:
```
{'ACQ_DURATION': 0.0,
 'ACQ_VERT_OFFSET': 0.0,
 'BANDWIDTH_LIMIT': 'off',
 'FIRST_POINT': 0,
 'FIRST_VALID_PNT': 0,
 'FIXED_VERT_GAIN': '50_mV/div',
 'HORIZ_INTERVAL': 1.6666699270695418e-11,
 'HORIZ_OFFSET': -0.000100000004229008,
 'HORIZ_UNCERTAINTY': 9.999999960041972e-13,
 'HORUNIT': 'S',
 'INSTRUMENT_NAME': 'LECROYSDA18000',
 'INSTRUMENT_NUMBER': 15238,
 'LAST_VALID_PNT': 12000001,
 'MAX_VALUE': 22914.0,
 'MIN_VALUE': -23170.0,
 'NOMINAL_BITS': 8,
 'NOM_SUBARRAY_COUNT': 1,
 'PAIR_OFFSET': 0,
 'PIXEL_OFFSET': -0.0001,
 'PNTS_PER_SCREEN': 12000000,
 'POINTS_PER_PAIR': 0,
 'PROBE_ATT': 1.0,
 'PROCESSING_DONE': 'no_processing',
 'RECORD_TYPE': 'single_sweep',
 'RIS_SWEEPS': 1,
 'SEGMENT_INDEX': 0,
 'SPARSING_FACTOR': 1,
 'SUBARRAY_COUNT': 1,
 'SWEEPS_PER_ACQ': 1,
 'TIMEBASE': '20_us/div',
 'TRACE_LABEL': '',
 'TRIGGER_TIME': datetime.datetime(2015, 9, 10, 17, 5, 19, 127343),
 'USER_TEXT': '',
 'VERTICAL_GAIN': 8.631759556010365e-06,
 'VERTICAL_OFFSET': 0.0,
 'VERTICAL_VERNIER': 1.0,
 'VERTUNIT': 'V',
 'VERT_COUPLING': 'DC_50_Ohms',
 'WAVE_ARRAY_COUNT': 12000002,
 'WAVE_SOURCE': 0}
```

See [here](http://forums.ni.com/attachments/ni/60/4652/2/LeCroyWaveformTemplate_2_3.pdf) for more details.


	
