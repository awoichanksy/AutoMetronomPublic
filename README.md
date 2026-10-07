# Third-party notices

## BeatNet (model weights)

`AutoMetronom/Resources/BeatNet-model1.weights` contains the weights of BeatNet model 1
from <https://github.com/mjhydri/BeatNet>, converted to a flat Float32 file (LSTM biases summed).
The feature extraction (madmom `LOG_SPECT`) and the CRNN were re-implemented in Swift.

> M. Heydari, F. Cwitkowitz, Z. Duan: *BeatNet: CRNN and Particle Filtering for Online Joint
> Beat Downbeat and Meter Tracking*, ISMIR 2021.

License: Creative Commons Attribution 4.0 International (CC BY 4.0),
<https://creativecommons.org/licenses/by/4.0/>. Changes: format conversion, no retraining.
The attribution is shown in the app on the main screen.

## Test fixture

`AutoMetronomTests/Fixtures/beatnet-808-*.f32` are derived from `test_data/808kick120bpm.mp3`
of the same repository (CC BY 4.0), decoded to 22.05 kHz mono.

## Beat This! (model)

`AutoMetronom/Resources/beat_this_final0.onnx` is the "final0" checkpoint of
**Beat This!** (F. Foscarin, J. Schlüter, G. Widmer: *Beat This! Accurate Beat Tracking Without
DBN Postprocessing*, ISMIR 2024, <https://github.com/CPJKU/beat_this>), exported to ONNX by
<https://github.com/mosynthkey/beat_this_cpp>. Code and weights: MIT license,
Copyright (c) 2024 Institute of Computational Perception, JKU Linz.
SHA-256 of the file: `c5c1466e08abdb03fdeb50668a06f244b787d564c212490482231a9cfbe9ccbd`.

## ONNX Runtime

Linked via Swift Package Manager (<https://github.com/microsoft/onnxruntime-swift-package-manager>),
MIT license, Copyright (c) Microsoft Corporation.

## Test fixture (Beat This!)

`AutoMetronomTests/Fixtures/beatthis-vibeace-*.f32`: 8 s of "Vibe Ace" by Kevin MacLeod
(incompetech.com), licensed CC BY 3.0, taken from the librosa example data.

## Song recognition and tempo data

- Song recognition: Apple ShazamKit (Shazam catalog). An audio signature is sent to Apple.
- Tempo: Deezer API (`api.deezer.com`, track BPM by ISRC) and, optionally, GetSongBPM
  (`api.getsong.co`; free API key, a link to GetSongBPM.com is required and shown in the app).
