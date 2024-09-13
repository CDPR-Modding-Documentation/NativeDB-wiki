# gameGameAudioSystem

## Description

Responsible for managing all audio-related functionality within the game. This system controls everything from background music and sound effects to character dialogue and environmental sounds.

Game sounds can be browsed on [SoundDB](https://sounddb.redmodding.org/).

## Functions

#### Play(eventName: CName, opt entityID: entEntityID, opt emitterName: CName) -> Void

Play a sound by its event name, optionally specifying an entity as emitter with its name.

Emitter name is used with chatters and subtitles.

#### Stop(eventName: CName, opt entityID: entEntityID, opt emitterName: CName) -> Void

Stop a previously played sound, optionally defined on an entity with specific name.

#### Switch(switchName: CName, switchValue: CName, opt entityID: entEntityID, opt emitterName: CName) -> Void

Switch from one sound to another, optionally specifying an entity as emitter with its name.

