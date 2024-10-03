# example-unrunnable-expand-template

This repo is cut to demonstrate an non-executable is_executable template

# Wut?

This succeeds:

```
$ bazel build //:hydrate && bazel-bin/hydrate.sh 
```

This fails:

```
$ bazel run //:hydrate
ERROR: Cannot run target //:hydrate: Not executable
```
.. despite:
```
expand_template_rule(
    name = "hydrate",
    ...
    is_executable = True,  # <-- inorite?  executable!
```
