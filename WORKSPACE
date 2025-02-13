workspace(name = "rtorrent")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "libtorrent",
    sha256 = "52252ec56fcf8f8e2cf3024f18ac42059512a49d693127c5c822425213bb4c6f",
    strip_prefix = "libtorrent-46b32949f35c32c518a1b634d6ec9cab0fe2580d",
    url = "https://github.com/jesec/libtorrent/archive/46b32949f35c32c518a1b634d6ec9cab0fe2580d.zip",
)

load("@libtorrent//:libtorrent_repos.bzl", "libtorrent_repos")

libtorrent_repos()

load("@libtorrent//:libtorrent_deps.bzl", "libtorrent_deps")

libtorrent_deps()

http_archive(
    name = "bazel_skylib",
    sha256 = "1c531376ac7e5a180e0237938a2536de0c54d93f5c278634818e0efc952dd56c",
    urls = [
        "https://github.com/bazelbuild/bazel-skylib/releases/download/1.0.3/bazel-skylib-1.0.3.tar.gz",
        "https://mirror.bazel.build/github.com/bazelbuild/bazel-skylib/releases/download/1.0.3/bazel-skylib-1.0.3.tar.gz",
    ],
)

load("@bazel_skylib//:workspace.bzl", "bazel_skylib_workspace")

bazel_skylib_workspace()

http_archive(
    name = "rules_pkg",
    sha256 = "038f1caa773a7e35b3663865ffb003169c6a71dc995e39bf4815792f385d837d",
    urls = [
        "https://mirror.bazel.build/github.com/bazelbuild/rules_pkg/releases/download/0.4.0/rules_pkg-0.4.0.tar.gz",
        "https://github.com/bazelbuild/rules_pkg/releases/download/0.4.0/rules_pkg-0.4.0.tar.gz",
    ],
)

load("@rules_pkg//:deps.bzl", "rules_pkg_dependencies")

rules_pkg_dependencies()

http_archive(
    name = "cares",
    build_file = "@rtorrent//:third_party/cares.BUILD",
    sha256 = "d73dd0f6de824afd407ce10750ea081af47eba52b8a6cb307d220131ad93fc40",
    strip_prefix = "c-ares-1.17.1",
    urls = [
        "https://github.com/c-ares/c-ares/releases/download/cares-1_17_1/c-ares-1.17.1.tar.gz",
        "https://c-ares.haxx.se/download/c-ares-1.17.1.tar.gz",
    ],
)

http_archive(
    name = "curl",
    build_file = "@rtorrent//:third_party/curl.BUILD",
    sha256 = "b0a3428acb60fa59044c4d0baae4e4fc09ae9af1d8a3aa84b2e3fbcd99841f77",
    strip_prefix = "curl-7.77.0",
    urls = [
        "https://github.com/curl/curl/releases/download/curl-7_77_0/curl-7.77.0.tar.gz",
        "https://curl.haxx.se/download/curl-7.77.0.tar.gz",
    ],
)

http_archive(
    name = "json",
    build_file = "@rtorrent//:third_party/json.BUILD",
    sha256 = "61e605be15e88deeac4582aaf01c09d616f8302edde7adcaba9261ddc3b4ceca",
    urls = ["https://github.com/nlohmann/json/releases/download/v3.10.2/include.zip"],
)

http_archive(
    name = "ncurses",
    build_file = "@rtorrent//:third_party/ncurses.BUILD",
    sha256 = "30306e0c76e0f9f1f0de987cf1c82a5c21e1ce6568b9227f7da5b71cbea86c9d",
    strip_prefix = "ncurses-6.2",
    urls = ["https://ftp.gnu.org/gnu/ncurses/ncurses-6.2.tar.gz"],
)

http_archive(
    name = "com_google_absl",
    sha256 = "59b862f50e710277f8ede96f083a5bb8d7c9595376146838b9580be90374ee1f",
    strip_prefix = "abseil-cpp-20210324.2",
    urls = ["https://github.com/abseil/abseil-cpp/archive/refs/tags/20210324.2.tar.gz"],
)

http_archive(
    name = "com_google_googletest",
    sha256 = "b4870bf121ff7795ba20d20bcdd8627b8e088f2d1dab299a031c1034eddc93d5",
    strip_prefix = "googletest-release-1.11.0",
    urls = ["https://github.com/google/googletest/archive/refs/tags/release-1.11.0.tar.gz"],
)

# Foreign CC dependencies
http_archive(
    name = "xmlrpc",
    build_file = "@rtorrent//:third_party/xmlrpc.BUILD",
    patches = ["@rtorrent//:third_party/xmlrpc.patch"],
    sha256 = "92f8945d7748c48ddaf2a9eb60fb366c642f32136ce68abedc75244f9a0ea492",
    strip_prefix = "xmlrpc-c-90978dfa964a57e6a31d76b128d0fa4ee9db574b/trunk",
    urls = ["https://github.com/mirror/xmlrpc-c/archive/90978dfa964a57e6a31d76b128d0fa4ee9db574b.zip"],
)
