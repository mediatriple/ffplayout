# mediatriple/ffplayout (live-reji fork)

Fork of [ffplayout/ffplayout](https://github.com/ffplayout/ffplayout) v1.1.0 (upstream is archived).
Used by [mediatriple/live-reji](https://github.com/mediatriple/live-reji) as its embedded playout engine.

Work happens on the `live-reji` branch; every release is a tag `v1.1.0-live-reji.N` that the
live-reji Dockerfile pins. Each change is its own commit, see `git log v1.1.0..live-reji`.

Changes on top of v1.1.0:

- `build.rs`: skip the npm frontend build without `embed_frontend`.
- filter: pad height from width for sources wider than the target aspect.
- playlist: remote sources are not resolved as storage paths.
- control: `jump` command (`{"control": "jump", "index": N}`) to start any clip of the list.
