package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_test(
    name = "go_default_test",
    srcs = [
        "event_test.go",
        "finder_test.go",
    ],
    importpath = "k8s.io/test-infra/mungegithub/mungers/matchers/event",
    library = ":go_default_library",
    deps = ["//vendor/github.com/google/go-github/github:go_default_library"],
)

go_library(
    name = "go_default_library",
    srcs = [
        "event.go",
        "finder.go",
        "operators.go",
    ],
    importpath = "k8s.io/test-infra/mungegithub/mungers/matchers/event",
    deps = ["//vendor/github.com/google/go-github/github:go_default_library"],
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
