SVG Exhaustive Attribute Order Optimizer
========================================

[SVGO](https://github.com/svg/svgo) already takes care of transformations
that can reduce the byte size of the .svg file.

This repository, however, focuses on the relationship between the already-optimized SVG
and the compression layer. In our case, [Brotli](https://github.com/google/brotli)
because it has a large pre-shared dictionary that helps compress SVGs.

Rather than having a clever algorithm, this repository exhaustively checks all possible
parameter order combinations and checks the compressed size of each one, which makes
it a bad fit for SVGs with many attributes.

This program is slow, and runtime grows exponentially with SVG complexity.
It saves only a handful of bytes per file.

But I've already built it, so you can partake in the madness without building it yourself.
