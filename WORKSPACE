load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "rules_python",
    url = "https://github.com/bazelbuild/rules_python/releases/download/0.5.0/rules_python-0.5.0.tar.gz",
    sha256 = "cd6730ed53a002c56ce4e2f396ba3b3be262fd7cb68339f0377a45e8227fe332",
)

# Load third-party python dependencies
load("@rules_python//python:pip.bzl", "pip_parse")

pip_parse(
    name = "third_party",
    requirements_lock = "//third_party:requirements.txt",
)

# Install all third-party python dependencies
load("@third_party//:requirements.bzl", "install_deps")

install_deps()
