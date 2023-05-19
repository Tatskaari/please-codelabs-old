go_library(
    name = "greetings",
    srcs = ["greetings.go"],
    visibility = ["//src/..."],
)

go_test(
    name = "greetings_test",
    srcs = ["greetings_test.go"],
    # Here we have used the shorthand `:greetings` label format. This format can be used to refer to a rule in the same
    # package and is shorthand for `//src/greetings:greetings`.
    deps = [
        ":greetings",
        # Could use a subrepo label i.e. ///third_party/go/github.com_stretchr_testify//assert instead if we want
        "//third_party/go:testify",
    ],
    external = True,
)

