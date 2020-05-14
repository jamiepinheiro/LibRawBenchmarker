# LibRaw Benchmarker

A tool for benchmarking LibRaw's reading, unpacking and processing time for various RAW formats.

## Setup
1) Populate a samples folder with RAW files in the following structure: `samples/{make}/{camera_name}.{raw_format`}


## Usage
This builds the benchmarker and runs it against the RAW images in the `samples/` folder
1) Both [Google/Benchmark](https://github.com/google/benchmark), and [LibRaw](https://github.com/libraw/libraw) need to be installed to your local include path
2) Build with `bazel build //main:benchmarker`
3) Execute `bazel-bin/main/benchmarker` from the root directory

## Output
Produces output in the following format:

| Benchmark          	 | Time         	| CPU          	| Iterations 	|
|--------------------	 |--------------	|--------------	|------------	|
| a.cr2/min_time:1.000 	 | 733906650 ns 	| 734375000 ns 	| 2          	|
| b.cr2/min_time:1.000 	 | 65365626 ns  	| 64967105 ns  	| 19         	|
| c.nef/min_time:1.000 	 | 339142325 ns 	| 335937500 ns 	| 4          	|
| ...                	 | ...          	| ...          	| ...        	|

