# Post compile cleanup buildpack

This is a Heroku buildpack to remove files before they become part of a "slug"

### Usage

Create a file in the project root named `.post-compile-cleanup` and populate it
with paths that should be removed after the compile phase.  It should have one
path per line.

This buildpack should be ordered after the buildpacks that produce the files
and directories that need to be cleaned up.

Example

```
> cat .post-compile-cleanup

node_modules
tmp/path/to/thing
```

