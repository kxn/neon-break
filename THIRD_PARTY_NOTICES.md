# Asset and runtime notices

- V9 presentation poses and boundary masonry texture: generated with built-in imagegen for this project. Original sources and specifications are preserved in art_source/presentation_v9/ and tools/author_v9.py. Current ACE-Step music provenance: assets/source/music_v9/. Short electronic defeat accent is synthesized by tools/death_audio_v9.py, without external voice/sample material.

- Godot Engine 4.7.2, official Windows runtime. Copyright Godot Engine contributors. MIT license: https://godotengine.org/license/
- Noto Sans SC, Google / Noto contributors. SIL Open Font License 1.1. Full license is included at `assets/fonts/OFL.txt` in the source project and packaged data.
- Character, vehicle and environment illustrations were generated for this project using the built-in image generation tool. Character motion clips were generated using the user's local MiniMax H3 Q5 service, then uniformly extracted and chroma-keyed into sprite atlases. Original inputs and request provenance are in `art_source/` in the source project.
- Current street and boss music were generated for this project through the user's local ACE-Step 1.5 service. Requests, seeds, raw results and processing records are retained in `assets/source/music_v7/` (previous version in `music_v6/`); generated music is cropped and loop-processed by `tools/loop_music_v6.py --version v7`. No third-party song was supplied as a reference.
- Sound effects and earlier fallback scores are synthesized by `tools/make_audio.py` and `tools/make_arcade_audio.py`; they use no external recordings or samples.
- The game is an original cyberpunk demo. Its title, characters, setting and assets are not taken from the reference arcade games.

- V8 weapon art: built-in image generation; three held-weapon walks: user H3 protected Q5 first/last-frame service. Sources under art_source/weapons_v8 and art_source/h3/weapon_*_walk_v8. Boost sound synthesized by tools/make_boost_v8.py without external samples.
