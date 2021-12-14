load("@rules_python//python:pip.bzl", "compile_pip_requirements")
load("@third_party//:requirements.bzl", "requirement")
load("@rules_python//python:defs.bzl", "py_binary")

compile_pip_requirements(
    name = "third_party",
    requirements_in = "//third_party:requirements.in",
    requirements_txt = "//third_party:requirements.txt",
)

py_binary(
    name = "mr_validator",
    srcs = ["mr_validator.py"],
    deps = [
        requirement("python-gitlab"),
    ],
)
