# libmdbx-rs


Rust bindings for [libmdbx](https://libmdbx.dqdkfa.ru).

Forked from the Apache licenced version of the `reth` [repo with specific commit](https://github.com/paradigmxyz/reth/commit/1e0d72459b60327acd23598b33fb275112762c13).
NOTE: Most of the repo came from [lmdb-rs bindings](https://github.com/mozilla/lmdb-rs).

## Updating the libmdbx Version

To update the libmdbx version you must clone it and copy the `dist/` folder in `mdbx-sys/`.
Make sure to follow the [building steps](https://libmdbx.dqdkfa.ru/usage.html#getting).

```bash
# clone libmmdbx to a repository outside at specific tag
git clone https://gitflic.ru/project/erthink/libmdbx.git ../libmdbx --branch v0.7.0
make -C ../libmdbx dist

# copy the `libmdbx/dist/` folder just created into `mdbx-sys/libmdbx`
rm -rf mdbx-sys/libmdbx
cp -R ../libmdbx/dist mdbx-sys/libmdbx

# add the changes to the next commit you will make
git add mdbx-sys/libmdbx
```
