# mhkt-mod

Moorhuhn Kart Thunder as a mod for Moorhuhn Kart: Open Source Edition, with 12 tracks and arenas, karts, powerups and pickups converted from the original game. The game ships it preinstalled and builds it from this repository. Every push to main also publishes a GitHub release with a zip per platform that you can put into the Mods folder of the game to install a newer build.

## Audio

Music (including menu/title/highscore cues) is normalized per song to -16 LUFS. Effects use one attenuation-only gain per source game, matching group medians to the quietest source while preserving intentional differences between cues; borrowed clips follow their source game's gain. Decoded peaks stay below 0 dBFS. Local cue gains and track music volumes are unchanged.

## Oil slick

The oil patch preserves its PNG's source alpha (`TextureImporterAlphaSource.FromInput`) and uses ordinary alpha blending without depth writes. Keep the texture's alpha channel and this import setting when replacing it; the road must remain visible around the spill instead of showing the rectangular quad.

## Racing paths

Racing paths are stored in the track scenes. Straight sections use fewer nodes; bends, road ramps, checkpoints and shortcut connections retain additional detail. Widths describe the driving corridor rather than adjacent plazas or side streets.

The main path follows the paved road, including Macao's island section. Alternate routes retain their intended off-road shortcuts and connect back to the main path through unobstructed entrances.

## License

MIT. Game assets belong to their respective owners. If there is a problem with any of them, message me and I will remove it.
