# Structural Ray Tracing in Slang — Extended Abstract


A 1–2 page SIGGRAPH-style extended abstract (ACM `acmart`, `sigconf`) introducing
Slang's structural ray-tracing work: a shader-declared *trace program schema* that
makes one pipeline ray-tracing codebase compile to D3D12, Vulkan, OptiX, and Metal,
while giving the compiler enough visibility to check each trace call against its
reachable programs.

This is work in progress. Related artifacts:

- Design proposal: <https://github.com/shader-slang/spec/pull/59>
- Implementation (WIP): <https://github.com/shader-slang/slang/pull/12691>
- Cross-platform Cornell-box demo: <https://github.com/kaizhangNV/structural-rt-cornell-demo>
- Falcor 2 port: <https://github.com/kaizhangNV/falcor2/pull/1>

## Files

| File | Purpose |
| --- | --- |
| `structural-rt-abstract.tex` | LaTeX source (acmart `sigconf`, `nonacm` draft mode) |
| `structural-rt-abstract.pdf` | Built PDF |
| `references.bib` | BibTeX references (project links, MSL specification) |
| `figures/cornell-demo.png` | Cornell-box render from the cross-platform demo (Figure 1) |

## Building

Any TeX distribution that ships `acmart` works. The simplest is
[Tectonic](https://tectonic-typesetting.github.io/), which fetches packages
automatically:

```bash
tectonic structural-rt-abstract.tex
```

## TODO before submission

- Confirm co-authors and affiliation city/country (placeholders/TODOs in the tex).
- Add performance measurements (runtime parity, compile-time cost) once the
  implementation is final; they are deliberately omitted for now.
- Reclaim the two lines currently spilling onto page 3.
