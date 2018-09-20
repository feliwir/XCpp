load("//app:version.bzl", "PRODUCT", "ANDROIDPATH", "PACKAGENAME")

licenses(["notice"])

cc_library(
    name = "native_glue",
    srcs = glob(["*.cpp"]),
    deps = ["//shared/core:core"],
)

android_binary(
    name = "app",
    deps = [
        "native_glue",
        "@androidsdk//com.android.support:appcompat-v7-25.3.1"
        ],
    srcs = ["MainActivity.java"],
    custom_package = PACKAGENAME,
    manifest = "AndroidManifest.xml",
    resource_files = glob(["res/**"]),
)