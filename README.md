SVG Exhaustive Attribute Order Optimizer
========================================

[SVGO](https://github.com/svg/svgo) already takes care of transformations
that can reduce the byte size of the .svg file.

This repository however, focuses on the relationship between the already-optimized SVG
and the compression layer. In our case, [Brotli](https://github.com/google/brotli)
because it has a large pre-shared dictionary that helps compress SVGs.

Rather than having a clever algorithm, this repository exclausively checks all possible
parameter order combinations and checks the compressed size of each of them. Which makes
it a bad fit for SVGs with tons of attributes.

This program is slow to run, and worsens exponentially the more attributes exist in a SVG.
It saves only a handful of bytes per file and makes an imperceptible difference.

But I already built it, so you can partake in the madness without building it yourself.
