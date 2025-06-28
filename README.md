［disclaimers: (1)this is a custom procedure compare to official pmos guide. please go through official guide and make sure it works for you first. (2)since pmbootstrap and pmaport is changing rapidly and this repo cant follow with official too closely so the action build might breaks.]

# Nightly SM7125 PostmarketOS Builds

This repository contains workflows and configurations to automatically build PostmarketOS edge images for SM7125 devices supported by our mainline kernel fork. These images are intended for testing purposes only and should make testing more accessible to people without the capabilities to compile the kernel from source.

## Image Information

The CI builds images once per week on fridays at midnight UTC. When completed, it will upload artifacts for miatoll device that was built. These artifacts contain `boot.img` and an xz-compressed rootfs. Artifacts are kept for one week (i.e. until the next rebuild).

The default user is called `user`, the password is `147147`, just like on official PostmarketOS stable images.

## Downloading

Head to the [Actions tab](https://github.com/redbluexe1/postmarketos-nightly-builds/actions), select the most recent successful run and download the artifact. Extract the Zip, de-compress the rootfs and you're ready to experiment!

## Mini wiki
Here is a mini wiki for install and boot pmOS on Joyeuse (tianma panel)
https://github.com/99degree/postmarket-nightly-builds/wiki/Boot-image-manipulation

## Prebuild kernel and modules
[HERE](https://github.com/99degree/linux/actions) is a github action build for linux kernel arm64 binary that is replaceable to pmos kernel also working fine with fastboot boot cmd. Feel free to download the weekly build of linux repo/next branch and use it with pmos initramfs to boot pmos rootfs.
