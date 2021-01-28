# Part of the Carbon Language project, under the Apache License v2.0 with LLVM
# Exceptions. See /LICENSE for license information.
# SPDX-License-Identifier: Apache-2.0 WITH LLVM-exception

load("@rules_python//python:defs.bzl", "py_binary", "py_library", "py_test")

py_library(
    name = "github_helpers",
    srcs = ["github_helpers.py"],
)

py_test(
    name = "github_helpers_test",
    srcs = ["github_helpers_test.py"],
    python_version = "PY3",
    deps = [":github_helpers"],
)

py_binary(
    name = "pr_comments",
    srcs = ["pr_comments.py"],
    python_version = "PY3",
    deps = ["github_helpers"],
)

py_test(
    name = "pr_comments_test",
    srcs = ["pr_comments_test.py"],
    python_version = "PY3",
    deps = [":pr_comments"],
)

py_binary(
    name = "update_label_access",
    srcs = ["update_label_access.py"],
    python_version = "PY3",
    deps = ["github_helpers"],
)

py_test(
    name = "update_label_access_test",
    srcs = ["update_label_access_test.py"],
    python_version = "PY3",
    deps = [
        ":pr_comments",
        ":update_label_access",
    ],
)