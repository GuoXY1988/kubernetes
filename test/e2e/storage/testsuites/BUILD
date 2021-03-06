load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "base.go",
        "disruptive.go",
        "driveroperations.go",
        "ephemeral.go",
        "multivolume.go",
        "provisioning.go",
        "snapshottable.go",
        "subpath.go",
        "testdriver.go",
        "topology.go",
        "volume_expand.go",
        "volume_io.go",
        "volumelimits.go",
        "volumemode.go",
        "volumes.go",
    ],
    importpath = "k8s.io/kubernetes/test/e2e/storage/testsuites",
    visibility = ["//visibility:public"],
    deps = [
        "//pkg/controller/volume/events:go_default_library",
        "//pkg/kubelet/events:go_default_library",
        "//pkg/volume/util:go_default_library",
        "//staging/src/k8s.io/api/core/v1:go_default_library",
        "//staging/src/k8s.io/api/storage/v1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/api/errors:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/api/resource:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/apis/meta/v1/unstructured:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/fields:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/labels:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/runtime/schema:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/util/errors:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/util/rand:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/util/sets:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/util/wait:go_default_library",
        "//staging/src/k8s.io/apiserver/pkg/storage/names:go_default_library",
        "//staging/src/k8s.io/client-go/dynamic:go_default_library",
        "//staging/src/k8s.io/client-go/kubernetes:go_default_library",
        "//staging/src/k8s.io/component-base/metrics/testutil:go_default_library",
        "//staging/src/k8s.io/csi-translation-lib:go_default_library",
        "//staging/src/k8s.io/csi-translation-lib/plugins:go_default_library",
        "//test/e2e/framework:go_default_library",
        "//test/e2e/framework/metrics:go_default_library",
        "//test/e2e/framework/node:go_default_library",
        "//test/e2e/framework/pod:go_default_library",
        "//test/e2e/framework/podlogs:go_default_library",
        "//test/e2e/framework/pv:go_default_library",
        "//test/e2e/framework/volume:go_default_library",
        "//test/e2e/storage/testpatterns:go_default_library",
        "//test/e2e/storage/utils:go_default_library",
        "//test/utils/image:go_default_library",
        "//vendor/github.com/onsi/ginkgo:go_default_library",
        "//vendor/github.com/onsi/gomega:go_default_library",
        "//vendor/github.com/pkg/errors:go_default_library",
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
    visibility = ["//visibility:public"],
)

go_test(
    name = "go_default_test",
    srcs = ["base_test.go"],
    embed = [":go_default_library"],
    deps = ["//test/e2e/framework/volume:go_default_library"],
)
