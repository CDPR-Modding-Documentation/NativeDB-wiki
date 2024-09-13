---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# gameGameAudioSystem

## Description

Responsible for managing all audio-related functionality within the game. This system controls everything from background music and sound effects to character dialogue and environmental sounds.

Game sounds can be browsed and listened to on [SoundDB](https://sounddb.redmodding.org/).

Sounds can be replaced with [REDmod](https://wiki.redmodding.org/cyberpunk-2077-modding/for-mod-creators-theory/modding-tools/redmod/audio-modding), with predefined [audio parameters](https://wiki.redmodding.org/cyberpunk-2077-modding/for-mod-creators-theory/modding-tools/redmod/audio-modding#parameters).

If you need more control over how sounds can be played in-game, you might want to consider [Audioware](https://cyb3rpsych0s1s.github.io/audioware/).

## Functions

#### Play(eventName: CName, opt entityID: entEntityID, opt emitterName: CName) -> Void

Play a sound by its event name, optionally specifying an entity as emitter with its name.

Emitter name is used with chatters and subtitles.

#### Stop(eventName: CName, opt entityID: entEntityID, opt emitterName: CName) -> Void

Stop a previously played sound, optionally defined on an entity with specific name.

#### Switch(switchName: CName, switchValue: CName, opt entityID: entEntityID, opt emitterName: CName) -> Void

Switch from one sound to another, optionally specifying an entity as emitter with its name.

#### VoIsPerceptible(entityId: entEntityID) -> Bool

Whether entity's voice (a.k.a voiceover) can be heard from where player stands.
