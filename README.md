https://github.com/jphp-group/jphp-audio-extension   
https://github.com/SerafimArts/jphp-audio-extension


jphp-audio-extension
==================

Audio Extension for Jphp Language

Available classes:
- AudioDevice
- AudioSystem
- AudioTrack

или

- php\audio\AudioDevice
- php\audio\AudioSystem
- php\audio\AudioTrack
- php\audio\controls\PanControls
- php\audio\controls\VolumeControls
- php\audio\controls\BalanceControls
- php\audio\controls\AbstractAudioControls

Exmaple:

```php
<?php
use php\audio\AudioSystem;
use php\audio\AudioDevice;
use php\audio\AudioTrack;

$devices = AudioSystem::getDevices(AudioDevice::SPEAKER);
var_dump($devices);


$track = new AudioTrack(Stream::of('res://audio/1.mp3'));
$track->setVolume($track->getVolumeMaximum() / 2);
$track->setBalance($track->getBalanceMinimum());
$track->play();
```
