
filegroup(
    name = "runtime_deps",
    srcs = [
        "%{site_bin}/bundle",
        "%{site_bin}/bundler",
    ] + glob([ "%{site_ruby}/**/*.rb" ]),
    visibility = [ "//visibility:public" ],
)

sh_binary(
    name = "bundle",
    data = [ ":runtime_deps" ],
    srcs = [ "bundle.sh" ],
    visibility = [ "//visibility:public" ],
)

sh_binary(
    name = "bundle-env",
    data = [
        ":runtime_deps",
        "@bazel_tools//tools/bash/runfiles",
    ],
    srcs = [ "bundle-env.sh" ],
    visibility = [ "//visibility:public" ],
)
