package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = [
        "admission_failure_handler_stub.go",
        "doc.go",
        "fake_handler_runner.go",
        "handlers.go",
        "interfaces.go",
        "predicate.go",
    ],
    tags = ["automanaged"],
    deps = [
        "//pkg/api/v1:go_default_library",
        "//pkg/kubelet/container:go_default_library",
        "//pkg/kubelet/types:go_default_library",
        "//pkg/kubelet/util/format:go_default_library",
        "//pkg/security/apparmor:go_default_library",
        "//plugin/pkg/scheduler/algorithm:go_default_library",
        "//plugin/pkg/scheduler/algorithm/predicates:go_default_library",
        "//plugin/pkg/scheduler/schedulercache:go_default_library",
        "//vendor:github.com/golang/glog",
        "//vendor:k8s.io/apimachinery/pkg/types",
        "//vendor:k8s.io/apimachinery/pkg/util/intstr",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["handlers_test.go"],
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = [
        "//pkg/api/v1:go_default_library",
        "//pkg/kubelet/container:go_default_library",
        "//vendor:k8s.io/apimachinery/pkg/util/intstr",
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
