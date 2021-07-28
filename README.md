# GPUProfiler-for-Linux


## Tested Linux distributions
CentOS 7.7, Ubuntu 18.04

## Limitations
Remoting protocol metric capture is not supported.

Console only, no UI support.

## Examples
Example output as viewed in GPUProfiler for Windows.

Training a Neural Network on a DGX-1 with 8x V100 GPUs (Showing one hour)
![image](https://user-images.githubusercontent.com/19617537/127305628-c707d949-d06d-4b2b-bd16-b4f7ae20f6d5.png)

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
