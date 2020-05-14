cc_binary(
    name = "benchmarker",
    srcs = ["benchmarker.cpp"],
    copts = ["-I/usr/local/include"],
    linkopts = ["-L/usr/local/lib", "-Lbenchmark/build/src", "-lbenchmark", "-lpthread", "-lraw"]
)