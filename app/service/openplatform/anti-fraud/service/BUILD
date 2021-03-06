package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_test",
    "go_library",
)

go_test(
    name = "go_default_test",
    srcs = [
        "question_bank_bind_test.go",
        "question_bank_test.go",
        "question_test.go",
        "service_test.go",
    ],
    embed = [":go_default_library"],
    rundir = ".",
    tags = ["automanaged"],
    deps = [
        "//app/service/openplatform/anti-fraud/conf:go_default_library",
        "//app/service/openplatform/anti-fraud/model:go_default_library",
        "//library/ecode:go_default_library",
        "//vendor/github.com/smartystreets/goconvey/convey:go_default_library",
    ],
)

go_library(
    name = "go_default_library",
    srcs = [
        "graph.go",
        "question.go",
        "question_bank.go",
        "question_bank_bind.go",
        "risk.go",
        "service.go",
    ],
    importpath = "go-common/app/service/openplatform/anti-fraud/service",
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
    deps = [
        "//app/common/openplatform/geetest/model:go_default_library",
        "//app/common/openplatform/geetest/service:go_default_library",
        "//app/common/openplatform/random:go_default_library",
        "//app/service/openplatform/anti-fraud/api/grpc/v1:go_default_library",
        "//app/service/openplatform/anti-fraud/api/http/v1:go_default_library",
        "//app/service/openplatform/anti-fraud/conf:go_default_library",
        "//app/service/openplatform/anti-fraud/dao:go_default_library",
        "//app/service/openplatform/anti-fraud/model:go_default_library",
        "//library/cache/redis:go_default_library",
        "//library/database/sql:go_default_library",
        "//library/ecode:go_default_library",
        "//library/log:go_default_library",
        "//vendor/github.com/json-iterator/go:go_default_library",
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
