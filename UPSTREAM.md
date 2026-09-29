# Upstream and maintenance review

This package maintains `unist-util-inspect@7.0.2` under the independent `@stackline/unist-util-inspect` name.

- Source: https://github.com/syntax-tree/unist-util-inspect/tree/04775f5f5af91c1ba3dc81cadf957b4abd49642e
- Public npm artifact integrity: `sha512-Op0XnmHUl6C2zo/yJCwhXQSm/SmW22eDZdWP2qdf4WpGrgO1ZxFodq+5zFyeRGasFjJotAnLgfuD1jkcKqiH1Q==`.
- Upstream issue evidence checked: 2026-09-29T00:22:11.437550+00:00.
- Original license and author notices are retained.
- The upstream published runtime files and declarations are hash-checked in `.stackline/upstream.json`. Any runtime fix is explicitly listed there.
- Functional upstream suites run against the source and extracted final package. Development tools were reduced to those used by validation; full source and runtime audits must pass.
- Only direct dependencies of the original Stackline portfolio are in this migration. This is not a claim that all transitive projects are maintained by Stackline.

## Issue triage

The queried open-issue list contained no issue entries. This does not establish that the upstream is abandoned or bug-free. No runtime bug fix is claimed for this initial maintenance release.

The evidence query fetched the latest 100 open and 30 closed issue/PR entries and removed PRs. Closed entries were collected for context; this report does not claim an exhaustive historic review.

## Release discipline

The source commit, passing CI and CodeQL, reviewed CI tarball hash, npm provenance, normal and aliased installs, and immutable GitHub release are checked before a release is complete. Published versions and tags are never replaced.
