# hax actions
This repository provides [GitHub
actions](https://github.com/features/actions) for installing and
configuring [the hax toolchain](https://github.com/hacspec/hax) and
its dependencies.

This GitHub action:
 - Installs the hax toolchain (plus `cargo` and `rustc`);
 - Installs [F*](https://github.com/fstarlang/fstar) (the version of F\*
   is frozen and pinned in hax);
 - Provides the environment variable `HAX_PROOF_LIBS`, `HAX_LIB` and
   `HACL_HOME`, which are commonly expected by our makefiles that
   verify hax-extracted code with F*.

By default, the action uses the latest hax on `main` on the repository
`github:hacspec/hax`. The inputs `hax_repository` and `hax_reference`
can be set to change this behavior.

Running this action is fast: it takes about a minute and a half (we
use [cachix](https://app.cachix.org/cache/hax): so commits on the main
branch of `hax` are pre-built).
