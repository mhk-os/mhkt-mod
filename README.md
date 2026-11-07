# mhkt-mod

Moorhuhn Kart Thunder as a mod for Moorhuhn Kart: Open Source Edition, with 12 tracks and arenas, karts, powerups and pickups converted from the original game. The game ships it preinstalled and builds it from this repository. Every push to main also publishes a GitHub release with a zip per platform that you can put into the Mods folder of the game to install a newer build.

## Audio

Music (including menu/title/highscore cues) is normalized per song to -16 LUFS. Effects use one attenuation-only gain per source game, matching group medians to the quietest source while preserving intentional differences between cues; borrowed clips follow their source game's gain. Decoded peaks stay below 0 dBFS. Local cue gains and track music volumes are unchanged.

## Oil slick

The oil patch preserves its PNG's source alpha (`TextureImporterAlphaSource.FromInput`) and uses ordinary alpha blending without depth writes. Keep the texture's alpha channel and this import setting when replacing it; the road must remain visible around the spill instead of showing the rectangular quad.

## Racing paths

Racing paths are stored in the track scenes. Straight sections use fewer nodes; bends, road ramps, checkpoints and shortcut connections retain additional detail. Widths describe the driving corridor rather than adjacent plazas or side streets.

The main path follows the paved road, including Macao's island section. Alternate routes retain their intended off-road shortcuts and connect back to the main path through unobstructed entrances.

## Track variants

Every track except Beijing can be driven in reverse. Every track has a time of day option. St. Petersburg has snow, Dubai a sandstorm and every other track rain. The overlay definitions are in each track's `Variants` folder, the overlay scenes (`<track>.night.unity`, `<track>.day.unity`, `<track>.rain.unity`, `<track>.snow.unity`, `<track>.sandstorm.unity`, `<track>.reverse.unity`) next to the track scene, the cover map for rain (`<track>.cover.asset`) beside them and the generated night, day, rain, snow and sandstorm skies in `Textures/Sky`. Night overlays darken the sun and ambient light and turn the karts' headlights on; rain adds rain with thunder, wet uncovered ground and less grip outdoors; snow adds snowfall and a little less grip outdoors; a sandstorm adds thick dusty fog and blowing sand. Reverse overlays turn the speed pad arrows round.

## License

MIT. Game assets belong to their respective owners. If there is a problem with any of them, message me and I will remove it.
