load("@org_tensorflow//tensorflow/core:platform/default/build_config.bzl", "tf_proto_library_cc")

tf_proto_library_cc(
    name = "sample0_proto",
    srcs = ["sample0.proto"],
    cc_api_version = 2,
    visibility = ["//visibility:public"],
)

proto_library(
    name = "sample1_proto",
    srcs = [],
    deps = ["@protobuf_archive//:descriptor_proto"],
)

proto_library(
    name = "sample2_proto",
    srcs = ["sample0.proto"],
)

cc_proto_library(
    name = "sample1_proto_cc",
    deps = [":sample1_proto"],
)

cc_proto_library(
    name = "sample2_proto_cc",
    deps = [":sample2_proto"],
)

cc_binary(
    name = "sample0.so",
    srcs = [],
    deps = [":sample0_proto_cc"],
    linkshared = 1,
    linkstatic = 1,
)

cc_binary(
    name = "sample1.so",
    srcs = [],
    deps = [":sample1_proto_cc"],
    linkshared = 1,
    linkstatic = 1,
)

cc_binary(
    name = "sample1",
    srcs = ["main.cc"],
    deps = [":sample1_proto_cc"],
)

cc_binary(
    name = "sample2.so",
    srcs = [],
    deps = [":sample2_proto_cc"],
    linkshared = 1,
    linkstatic = 1,
)

