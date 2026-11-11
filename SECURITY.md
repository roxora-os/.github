# Security policy

## Reporting a vulnerability

Please report security problems privately by email to
**oss@gahingwoo.com**. Do not open a public issue, pull request or
discussion for them.

Include what you can of the following:

- the affected board and image file name (for example
  `roxora-radxa-rock-4d-noble-edge-2026.11.0.img.xz`), or the repository and
  commit;
- what the problem is and what an attacker could do with it;
- steps to reproduce it.

We will confirm that we received your report, keep you informed while we
look into it, and agree with you on when the problem is made public.

## Where a problem belongs

Roxora combines software from other projects. Many problems are best fixed
where the code comes from:

- Kernel, device tree and U-Boot: these packages come from Armbian,
  which builds them from mainline Linux and U-Boot (or vendor trees) plus
  its own patches. Report them to us first. Report a problem to
  [Armbian](https://github.com/armbian/.github/blob/master/SECURITY.md)
  only if it also happens on an official Armbian image; problems in mainline
  code go to the
  [Linux kernel security team](https://docs.kernel.org/process/security-bugs.html)
  or the [U-Boot project](https://docs.u-boot.org/en/latest/develop/security.html).
- Ubuntu userspace: every other package comes unchanged from the Ubuntu
  archive. Report those to
  [Ubuntu security](https://ubuntu.com/security/disclosure-policy).
- Roxora itself: the build scripts, the apt pinning, the image
  configuration and the tools in the `roxora-os` repositories. Report those
  to us.

If you are not sure where a problem belongs, send it to us and we will help
pass it on.
