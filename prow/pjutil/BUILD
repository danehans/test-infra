package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = ["pjutil.go"],
    importpath = "k8s.io/test-infra/prow/pjutil",
    tags = ["automanaged"],
    deps = [
        "//prow/config:go_default_library",
        "//prow/kube:go_default_library",
        "//vendor/github.com/satori/go.uuid:go_default_library",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
)

go_test(
    name = "go_default_test",
    srcs = ["pjutil_test.go"],
    importpath = "k8s.io/test-infra/prow/pjutil",
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = ["//prow/kube:go_default_library"],
)
