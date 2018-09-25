load("//app:version.bzl", "PRODUCT", "ANDROIDPATH", "PACKAGENAME")

licenses(["notice"])

cc_library(
    name = "android_glue",
    srcs = glob(["cpp/*.cpp","cpp/*.hpp"]),
    deps = ["//shared/core:core"],
    #linkopts = ["-llog", "-landroid", "-lEGL", "-lGLESv1_CM"]
)

android_binary(
    name = "app",
    deps = [
        ":android_glue",
        "@androidsdk//com.android.support:appcompat-v7-25.3.1"
        ],
    srcs = ["MainActivity.java"],
    custom_package = PACKAGENAME,
    manifest = "AndroidManifest.xml",
    resource_files = glob(["res/**"]),
)