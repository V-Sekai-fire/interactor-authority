# interactor-authority

The authority plane: one zone's single writer, which owns that zone's truth and ticks on the shared-memory ring.

## What it is for

A plane is a process with no networking. This one paces its tick with the harness's own wait, publishes entity state to the ring each tick, and leaves client transport and interest filtering to the fan-out edge that reads the ring. `gen/` holds vendored codegen output; regenerate it, never edit it.

## Build and run

```sh
cmake -S . -B build -DCMAKE_BUILD_TYPE=Release
cmake --build build
```

## Licence

The source files carry `Apache-2.0` SPDX headers; the repository has no licence file.
