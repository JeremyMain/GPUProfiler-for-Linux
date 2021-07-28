# GPUProfiler-for-Linux

This is a basic, no fluf version of GPUProfiler for Linux that will allow you to capture and analyse the resource utilization of various workloads on Linux systems.

The console based application will collect and save a .GPD file that can be viewed in GPUProfiler for Windows or exported to CSV as input to your favorite data cruncher.


## Tested Linux distributions
CentOS 7.7, Ubuntu 18.04


## Tested Hypervisors
RedHat KVM, Citrix XenServer, Citrix Hypervisor, Nutanix AHV

As much as I would like to add support for VMware vSphere, the system details and metrics that I can collect without expert insider knowledge would be insufficient to make it useful so I have not been able to add support for vSphere. 

If you have said expert knowledge and wish to help get vSphere support please contact me.

## Limitations
Remoting protocol metrics capture is not supported.

Console only, no UI support.

Currently does not capture data for hardware configurations without an NVIDIA GPU


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
