package(default_visibility = ["//visibility:private"])

load("@build_stack_rules_proto//python:python_proto_library.bzl", "python_proto_library")

proto_library(
    name = "proto_lib_a",
    srcs = ["demo.proto"],
)

proto_library(
    name = "proto_lib_b",
    srcs = ["demo.proto"],
)

python_proto_library(
    name = "py_lib_a",
    deps = ["proto_lib_a"],
)

python_proto_library(
    name = "py_lib_b",
    deps = ["proto_lib_b"],
)
