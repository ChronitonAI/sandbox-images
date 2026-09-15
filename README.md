# sandbox-images

Release assets for webmux's sandboxed sessions: a Debian root filesystem, BinaryBuilder2
toolchains and tool prefixes, packed as `.tar.zst`. They are built by
`sandbox/build/images.jl` in [ChronitonAI/tech](https://github.com/ChronitonAI/tech), which
also holds the manifest (`sandbox/manifest/<triplet>.toml`) that pins each file by sha256.
`webmux run` downloads them on first use. Each release is tagged `images-<hash of the file
set>`; a file's name embeds its content hash, so a release never changes once published.
