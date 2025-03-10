# 34669

## Current behavior

Renovate changes NuGet dependency versions whether specified with `Version` or `VersionOverride` metadata, without opportunity for discrimination.

## Expected behavior

Some `match*` property in `renovate.json` that allows a package rule to match on whether the version is specified by `Version` or `VersionOverride` metadata.

The point here is that while `Version` tends to set a typical or repo-wide version for a dependency, the `VersionOverride` metadata tends to represent a special case that requires a particular version for some reason.
Therefore it is not desirable to have a bot come and update it along with other (non-override) references to the same package.

## Link to the Renovate issue or Discussion

https://github.com/renovatebot/renovate/discussions/34669
