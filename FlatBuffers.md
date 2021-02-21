## FlatBuffers

```
sudo pacman -S flatbuffers
```

### Building

Ref https://github.com/google/flatbuffers/blob/master/docs/source/Building.md#building-with-cmake

```
cd ~
git clone git@github.com:google/flatbuffers.git --depth 1
cd flatbuffers

sudo pacman -S cmake clang

CC=/usr/bin/clang CXX=/usr/bin/clang++ cmake -G "Unix Makefiles" -DCMAKE_BUILD_TYPE=Release
make -j $(nproc)

./flatc --rust samples/monster.fbs

sudo cp flatc /usr/local/bin/
```
