package(default_visibility = ["//visibility:public"])
cc_library(
    name = "bsoncpp",
    srcs=["src/bsonobj.cpp", "src/oid.cpp"],
    hdrs= glob(["src/*.h"]),
    includes = [".", "src"],
    deps = [":bsoncpp_lib", ":bsoncpp_util"]
)

cc_library(
    name = "bsoncpp_util",
    srcs = ["src/util/json.cpp"],
    hdrs = glob(["src/util/*.h", "src/*.h"]),
    deps = [":bsoncpp_lib"],
    includes = [".", "src"],
    visibility = ["//visibility:private"]
)

cc_library(
    name = "bsoncpp_lib",
    srcs = ["lib/base64.cpp", "lib/md5.c", "lib/nonce.cpp"],
    hdrs = ["lib/atomic_int.h", "lib/base64.h", "lib/md5.h", "lib/md5.hpp", "lib/nonce.h"],
    visibility = ["//visibility:private"]
)

cc_binary(
    name="bsondemo",
    srcs = ["bsondemo/bsondemo.cpp"],
    deps = [":bsoncpp"],
)
