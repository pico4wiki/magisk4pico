# magisk4pico

a fork of [Magisk](https://github.com/topjohnwu/Magisk) that works on PICO 4 headsets by changing the bundled-in busybox to something that is compatible with PICO's `phoenix` kernel and architecture.

## changes

- replace `libbusybox` with a prebuilt one known to work with PICO headsets
- go back to the old way of doing bootctl (without a patch)
- downgrade AGP for easier development in Intellij IDEA

## building

you need to have python3, GCC, the Android SDK, and rust/rustup installed
```sh
python3 build.py ndk # downloads the Android NDK necessary
python3 build.py -vr all # builds it all! (verbose and in release mode, native libraries and app)
```

after, you should have your app in `out/app-release.apk`!