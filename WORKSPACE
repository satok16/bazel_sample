load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "io_bazel_rules_closure",
    sha256 = "a38539c5b5c358548e75b44141b4ab637bba7c4dc02b46b1f62a96d6433f56ae",
    strip_prefix = "rules_closure-dbb96841cc0a5fb2664c37822803b06dab20c7d1",
    urls = [
        "https://mirror.bazel.build/github.com/bazelbuild/rules_closure/archive/dbb96841cc0a5fb2664c37822803b06dab20c7d1.tar.gz",
        "https://github.com/bazelbuild/rules_closure/archive/dbb96841cc0a5fb2664c37822803b06dab20c7d1.tar.gz",  # 2018-04-13
    ],
)

http_archive(
    name = "org_tensorflow",
    urls = [
        "https://storage.googleapis.com/fluxworks-storage/public/tensorflow_r1.11_configured.tar.bz2",
  ],
  type = "tar.bz2",
  strip_prefix = "tensorflow",
)

load('@org_tensorflow//tensorflow:workspace.bzl', 'tf_workspace')

tf_workspace(path_prefix = "", tf_repo_name = "org_tensorflow")
