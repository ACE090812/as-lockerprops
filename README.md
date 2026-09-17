# as-lockerprops

Streamed assets only - no scripts. Ships the `aslocker` locker wall model, its texture
dictionary, and its door-open/close animations (`aslocker_animation`), registered via
`data_file 'DLC_ITYP_REQUEST'` in `fxmanifest.lua` so the archetype is loadable by name from any
other resource.

Used by `sd_postalprime` (listed as a `dependencies` entry there) to spawn the physical locker
wall at each of its `Config.lockers` points and play that wall's per-door animations. Start this
resource before `sd_postalprime` in `server.cfg`.

Nothing in here needs editing - just keep it started. If you have the matching `asparcel_*` box
props (the small parcel object that sits in an open door), drop them into `stream/` here too and
let `sd_postalprime` know so it can spawn one instead of just an interaction point.
