workspace(
    name = "node-bazel-workshop",
    managed_directories = {
        "@npm": ["external/node_modules"],
    },
)

load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")

git_repository(
    name = "build_bazel_rules_nodejs",
    remote = "https://github.com/bazelbuild/rules_nodejs.git",
    tag = "3.8.0",
)

git_repository(
    name = "build_bazel_rules_typescript",
    remote = "https://github.com/bazelbuild/rules_nodejs.git",
    tag = "3.8.0",
    strip_prefix = '/third_party/github.com/bazelbuild/rules_typescript'
)

git_repository(
    name = "bazel_skylib",
    remote = "https://github.com/bazelbuild/bazel-skylib",
    tag = "1.0.3",
)

load("@build_bazel_rules_nodejs//:index.bzl", "yarn_install")

yarn_install(
    name = "npm",
    package_json = ":package.json",
    yarn_lock = ":yarn.lock",
)
