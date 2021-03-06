package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_test(
    name = "go_default_test",
    srcs = [
        "chain_test.go",
        "config_test.go",
        "errors_test.go",
        "handler_test.go",
    ],
    embed = [":go_default_library"],
    importpath = "k8s.io/apiserver/pkg/admission",
    deps = [
        "//vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime/schema:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/json:go_default_library",
        "//vendor/k8s.io/apiserver/pkg/apis/apiserver:go_default_library",
        "//vendor/k8s.io/apiserver/pkg/apis/apiserver/v1alpha1:go_default_library",
    ],
)

go_library(
    name = "go_default_library",
    srcs = [
        "attributes.go",
        "chain.go",
        "config.go",
        "errors.go",
        "handler.go",
        "interfaces.go",
        "plugins.go",
    ],
    importpath = "k8s.io/apiserver/pkg/admission",
    deps = [
        "//vendor/github.com/ghodss/yaml:go_default_library",
        "//vendor/github.com/golang/glog:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/api/errors:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/api/meta:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime/schema:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime/serializer:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/errors:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/sets:go_default_library",
        "//vendor/k8s.io/apiserver/pkg/apis/apiserver:go_default_library",
        "//vendor/k8s.io/apiserver/pkg/apis/apiserver/v1alpha1:go_default_library",
        "//vendor/k8s.io/apiserver/pkg/authentication/user:go_default_library",
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
    srcs = [
        ":package-srcs",
        "//staging/src/k8s.io/apiserver/pkg/admission/configuration:all-srcs",
        "//staging/src/k8s.io/apiserver/pkg/admission/initializer:all-srcs",
        "//staging/src/k8s.io/apiserver/pkg/admission/metrics:all-srcs",
        "//staging/src/k8s.io/apiserver/pkg/admission/plugin/initialization:all-srcs",
        "//staging/src/k8s.io/apiserver/pkg/admission/plugin/namespace/lifecycle:all-srcs",
        "//staging/src/k8s.io/apiserver/pkg/admission/plugin/webhook/config:all-srcs",
        "//staging/src/k8s.io/apiserver/pkg/admission/plugin/webhook/errors:all-srcs",
        "//staging/src/k8s.io/apiserver/pkg/admission/plugin/webhook/initializer:all-srcs",
        "//staging/src/k8s.io/apiserver/pkg/admission/plugin/webhook/mutating:all-srcs",
        "//staging/src/k8s.io/apiserver/pkg/admission/plugin/webhook/namespace:all-srcs",
        "//staging/src/k8s.io/apiserver/pkg/admission/plugin/webhook/request:all-srcs",
        "//staging/src/k8s.io/apiserver/pkg/admission/plugin/webhook/rules:all-srcs",
        "//staging/src/k8s.io/apiserver/pkg/admission/plugin/webhook/testcerts:all-srcs",
        "//staging/src/k8s.io/apiserver/pkg/admission/plugin/webhook/validating:all-srcs",
        "//staging/src/k8s.io/apiserver/pkg/admission/plugin/webhook/versioned:all-srcs",
    ],
    tags = ["automanaged"],
)
