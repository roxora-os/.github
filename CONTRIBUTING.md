# Contributing to Roxora

Thanks for helping. This page applies to every repository in the
`roxora-os` organization unless a repository has its own `CONTRIBUTING.md`.

## Questions

Ask questions in an issue on
[roxora-os/build](https://github.com/roxora-os/build/issues). Please search
the existing issues first.

Security problems are the exception: do not open a public issue for them.
See [SECURITY.md](SECURITY.md).

## Building an image

The build lives in [roxora-os/build](https://github.com/roxora-os/build). It
is an Armbian extension plus a wrapper script that drives a pinned
`armbian/build` checkout.

```sh
git clone https://github.com/roxora-os/build.git
cd build
./build.sh BOARD=radxa-rock-4d BRANCH=edge RELEASE=noble
```

- `BOARD`, `BRANCH` and `RELEASE` must match a line in `boards.conf`, which
  lists the supported combinations.
- Armbian's build needs root (it uses `sudo`) or Docker.
- The image is written to `output/` together with a `.sha256` file.
- `./build.sh --help` lists the options.

The official images are built by CI in `roxora-os/build`, not on anyone's
machine. You do not need to attach an image to a pull request.

## Pull requests

- One board or one change per pull request. A pull request that adds a board
  and also changes the package pinning is two pull requests.
- Say what you changed and why, and how you tested it: on real hardware
  (which board) or in CI only. The pull request template asks for this.
- Keep commits small and logical, with a clear message.

## Developer Certificate of Origin

Every commit must carry a `Signed-off-by:` line. Add it with `-s`:

```sh
git commit -s -m "Add support for Example Board"
```

This adds a line like the following, using the name and email from your git
configuration:

```
Signed-off-by: Your Name <you@example.com>
```

By signing off you state that you wrote the change, or otherwise have the
right to submit it under the project's open source license, as described in
the [Developer Certificate of Origin](https://developercertificate.org/).
Use your real name. Pull requests with commits that are not signed off
cannot be merged.

To sign off the last three commits you already made on your branch (change
the number to match):

```sh
git rebase --signoff HEAD~3
git push --force-with-lease
```

## Code of conduct

Everyone taking part in the project follows the
[Code of Conduct](CODE_OF_CONDUCT.md).
