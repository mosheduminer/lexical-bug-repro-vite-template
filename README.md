# Lexical-solid vite-plugin-solid bug repro

This repository contains a reproduction of [this issue](https://github.com/mosheduminer/lexical-solid/issues/20), complementing the solid-start based repro at https://github.com/mosheduminer/lexical-no-ssr-bug-repro.

## Reproducing

Expected behavior:
- the editor should automatically focus
- any change in the editor should result in an additional line shown below as a "log", with the current editor text as the content
- clicking on the button should result in another such log line

Actual behavior:
- focus does not occur
- changes do not result in log lines
- clicking the button results in an "empty" log

I believe the cause of this behavior is some issue which results in the lexical editor not being hooked up correctly (?). This may be caused by a bundling issue.

Note that this issue does not appear to have existed previously. The latest version in which this issue does not appear is lexical-solid v0.10.0 (which pins lexical v0.16.x), it begins to occur in v0.11.0 (which pins lexical v0.17.x) but does occur in later versions. I have no idea why this is (I don't see any changes that would have caused it), but I've mentioned the lexical versions in case it turns out they've made changes in those versions.
