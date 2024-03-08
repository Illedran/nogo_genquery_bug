# Nogo genquery bug

```
$ bazel build //src:src_genquery

ERROR: /home/illedran/.cache/bazel/_bazel_illedran/a3b41e2226cf2286c26d4e18a5d6a010/external/io_bazel_rules_go/BUILD.bazel:71:16: in go_context_data rule @@io_bazel_rules_go//:go_context_data: cycle in dependency graph:
    //src:src-genquery (c996bfa92bcafc2798baf4dbf854da936ce6f49485d19b67b34b429667416404)
    //src:src-genquery (312a038fde71b14d7680a2d5856ddfa0ee2fb821b1f2d44cc703454abe09284c)
    //src:src
.-> @@io_bazel_rules_go//:go_context_data
|   @@io_bazel_rules_nogo//:nogo
|   @@io_bazel_rules_go//:tools_nogo
|   @@io_bazel_rules_go//:tools_nogo_actual
|   @@io_bazel_rules_go//go/tools/builders:nogo_srcs
|   @@org_golang_x_tools//internal/facts:facts
`-- @@io_bazel_rules_go//:go_context_data
```