This is the challenge `oob-v8` from `*CTF-2019`.

Vulnerability: OOB-Read/Write

V8 Commit: `6dc88c191f5ecc5389dc26efa3ca0907faef3598`

Building release and debug versions of d8:
```
fetch v8
cd v8
git checkout 6dc88c191f5ecc5389dc26efa3ca0907faef3598
gclient sync -D
git apply /path/to/oob.diff
./tools/dev/v8gen.py x64.release
ninja -C ./out.gn/x64.release
./tools/dev/v8gen.py x64.debug
ninja -C ./out.gn/x64.debug
```

References:

https://faraz.faith/2019-12-13-starctf-oob-v8-indepth/

https://jhalon.github.io/chrome-browser-exploitation-1/