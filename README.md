# GPUProfiler-for-Linux


## Tested Linux distributions
CentOS 7.7, Ubuntu 18.04

## Limitations
Remoting protocol metric capture is not supported.

Console only, no UI support.

## Examples
Example output as viewed in GPUProfiler for Windows.
TODO

## Usage

```
$ ./gpuprofiler -h
Usage: gpuprofiler [OPTION]... [FILE]
 
A System and GPU resource collection tool.
Analyze results with GPUProfiler, http://gpuprofiler.com/
 
Options:
-i <number>    Sample interval. Default: 1 (second)
-d <number>    Collection duration. Default: 10 (minutes)
-r <number>    Repeat count. Default: 0 (times)
-t             Append timestamp to the output file
-h             Display usage
-v             Display version
```

Express method
 
```$ ./gpuprofiler yourfilename```
 
Results in sample interval 1 second, duration 10 minutes and the output file will be yourfilename.gpd
