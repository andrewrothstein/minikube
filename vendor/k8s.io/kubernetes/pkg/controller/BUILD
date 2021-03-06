package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_test(
    name = "go_default_test",
    srcs = [
        "controller_ref_manager_test.go",
        "controller_utils_test.go",
    ],
    library = ":go_default_library",
    deps = [
        "//pkg/api:go_default_library",
        "//pkg/api/install:go_default_library",
        "//pkg/api/testapi:go_default_library",
        "//pkg/controller/testutil:go_default_library",
        "//pkg/securitycontext:go_default_library",
        "//vendor/k8s.io/api/core/v1:go_default_library",
        "//vendor/k8s.io/api/extensions/v1beta1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/api/equality:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/labels:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime/schema:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/types:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/clock:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/sets:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/uuid:go_default_library",
        "//vendor/k8s.io/client-go/kubernetes:go_default_library",
        "//vendor/k8s.io/client-go/kubernetes/fake:go_default_library",
        "//vendor/k8s.io/client-go/rest:go_default_library",
        "//vendor/k8s.io/client-go/tools/cache:go_default_library",
        "//vendor/k8s.io/client-go/tools/record:go_default_library",
        "//vendor/k8s.io/client-go/util/testing:go_default_library",
    ],
)

go_library(
    name = "go_default_library",
    srcs = [
        "client_builder.go",
        "controller_ref_manager.go",
        "controller_utils.go",
        "doc.go",
        "lookup_cache.go",
    ],
    deps = [
        "//pkg/api:go_default_library",
        "//pkg/api/install:go_default_library",
        "//pkg/api/v1/pod:go_default_library",
        "//pkg/api/validation:go_default_library",
        "//pkg/serviceaccount:go_default_library",
        "//pkg/util/hash:go_default_library",
        "//pkg/util/taints:go_default_library",
        "//vendor/github.com/golang/glog:go_default_library",
        "//vendor/github.com/golang/groupcache/lru:go_default_library",
        "//vendor/k8s.io/api/apps/v1beta1:go_default_library",
        "//vendor/k8s.io/api/authentication/v1:go_default_library",
        "//vendor/k8s.io/api/core/v1:go_default_library",
        "//vendor/k8s.io/api/extensions/v1beta1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/api/errors:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/api/meta:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/fields:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/labels:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime/schema:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/types:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/clock:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/errors:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/runtime:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/sets:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/strategicpatch:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/wait:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/watch:go_default_library",
        "//vendor/k8s.io/apiserver/pkg/authentication/serviceaccount:go_default_library",
        "//vendor/k8s.io/client-go/kubernetes:go_default_library",
        "//vendor/k8s.io/client-go/kubernetes/scheme:go_default_library",
        "//vendor/k8s.io/client-go/kubernetes/typed/authentication/v1:go_default_library",
        "//vendor/k8s.io/client-go/kubernetes/typed/core/v1:go_default_library",
        "//vendor/k8s.io/client-go/rest:go_default_library",
        "//vendor/k8s.io/client-go/tools/cache:go_default_library",
        "//vendor/k8s.io/client-go/tools/record:go_default_library",
        "//vendor/k8s.io/client-go/tools/reference:go_default_library",
        "//vendor/k8s.io/client-go/util/integer:go_default_library",
        "//vendor/k8s.io/client-go/util/retry:go_default_library",
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
        "//pkg/controller/bootstrap:all-srcs",
        "//pkg/controller/certificates:all-srcs",
        "//pkg/controller/cloud:all-srcs",
        "//pkg/controller/cronjob:all-srcs",
        "//pkg/controller/daemon:all-srcs",
        "//pkg/controller/deployment:all-srcs",
        "//pkg/controller/disruption:all-srcs",
        "//pkg/controller/endpoint:all-srcs",
        "//pkg/controller/garbagecollector:all-srcs",
        "//pkg/controller/history:all-srcs",
        "//pkg/controller/job:all-srcs",
        "//pkg/controller/namespace:all-srcs",
        "//pkg/controller/node:all-srcs",
        "//pkg/controller/podautoscaler:all-srcs",
        "//pkg/controller/podgc:all-srcs",
        "//pkg/controller/replicaset:all-srcs",
        "//pkg/controller/replication:all-srcs",
        "//pkg/controller/resourcequota:all-srcs",
        "//pkg/controller/route:all-srcs",
        "//pkg/controller/service:all-srcs",
        "//pkg/controller/serviceaccount:all-srcs",
        "//pkg/controller/statefulset:all-srcs",
        "//pkg/controller/testutil:all-srcs",
        "//pkg/controller/ttl:all-srcs",
        "//pkg/controller/volume/attachdetach:all-srcs",
        "//pkg/controller/volume/events:all-srcs",
        "//pkg/controller/volume/expand:all-srcs",
        "//pkg/controller/volume/persistentvolume:all-srcs",
    ],
    tags = ["automanaged"],
)
