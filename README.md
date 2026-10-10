# interactor-authority

The authority plane: one zone's single writer, which owns that zone's truth and ticks on the shared-memory ring.

## What it is for

A plane is a process with no networking. This one paces its tick with the harness's own wait, integrates the zone's entities each tick through a state handle, publishes nothing to the ring yet, and leaves client transport and interest filtering to the fan-out edge that reads the ring. `gen/` holds vendored codegen output; regenerate it, never edit it.

## Build and run

```sh
cmake -S . -B build -DCMAKE_BUILD_TYPE=Release
cmake --build build
```

## Licence

Apache-2.0. See [LICENSE](LICENSE).
