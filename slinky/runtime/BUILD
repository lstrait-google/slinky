load("//third_party/bazel_rules/rules_cc/cc:cc_library.bzl", "cc_library")

package(
    default_applicable_licenses = ["//third_party/slinky:license"],
    default_visibility = ["//visibility:private"],
)

# This library contains the necessary functionality to evaluate pipelines.
cc_library(
    name = "runtime",
    srcs = [
        "buffer.cc",
        "depends_on.cc",
        "evaluate.cc",
        "expr_stmt.cc",
        "pipeline.cc",
        "print.cc",
    ],
    hdrs = [
        "buffer.h",
        "depends_on.h",
        "evaluate.h",
        "expr.h",
        "pipeline.h",
        "print.h",
        "stmt.h",
    ],
    compatible_with = ["//buildenv/target:non_prod"],
    visibility = ["//visibility:public"],
    deps = [
        "//third_party/slinky/base",
        "//third_party/slinky/base:chrome_trace",
        "//third_party/slinky/base:thread_pool",
    ],
)

cc_library(
    name = "visualize",
    srcs = ["visualize.cc"],
    hdrs = ["visualize.h"],
    compatible_with = ["//buildenv/target:non_prod"],
    visibility = ["//visibility:public"],
    deps = [
        ":runtime",
        "//third_party/slinky/base",
    ],
)
