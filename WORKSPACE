workspace(name = "rules_proto_demo")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "build_stack_rules_proto",
    sha256 = "ad2bd886ed2ca0f5891ee58415bf875839787ae44414e178f468685a8b5d0bb1",
    strip_prefix = "rules_proto-2f4e4f62a3d7a43654d69533faa0652e1c4f5082",
    urls = ["https://github.com/stackb/rules_proto/archive/2f4e4f62a3d7a43654d69533faa0652e1c4f5082.tar.gz"],
)

load("@build_stack_rules_proto//python:deps.bzl", "python_grpc_library", "python_proto_library")
python_grpc_library()
python_proto_library()

load("@io_bazel_rules_python//python:pip.bzl", "pip_import", "pip_repositories")

pip_repositories()

pip_import(
    name = "protobuf_py_deps",
    requirements = "@build_stack_rules_proto//python/requirements:protobuf.txt",
)

load("@protobuf_py_deps//:requirements.bzl", protobuf_pip_install = "pip_install")

protobuf_pip_install()
