# gameFxSystem

## Description

This system allows you to spawn (particle) effects in the world. It should be able to spawn any \[FxResource]. You can find a list of effects with WolvenKit in the AssetBrowser by filtering files with `.effect` extension.

## Functions

#### SpawnEffect(resource: gameFxResource, transform: WorldTransform, opt ignoreTimeDilation: Bool) -> handle:gameFxInstance

Create a new effect at `transform` position in the world, based on a `resource` (your effect). You need to keep a reference of the returned \[FxInstance] to later control and stop your effect.

See these snippets of code for [redscript](https://discord.com/channels/717692382849663036/804399334246187038/1399020692212547755) and for [CET](https://discord.com/channels/717692382849663036/795037494106128434/1371778368902533172) to create a \[FxResource].
