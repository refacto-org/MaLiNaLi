> ai format : 

__tf lite vs onnx__

# tf lite
- tf lite could work on flutter even though ops/flex are not handled 
    - https://github.com/tensorflow/flutter-tflite/issues/41#issuecomment-1891012867
  - but seems far-fetched/already obsolete
- android native is possible but limits much, vocal message in a module would be cumbersome
- except for icefall sherpa if going for this solution for speech

## android repos if stick to tf lite
- https://github.com/somyakantdash/EngToHiTranslatorApp
- https://github.com/apaar97/translate - 6 years ago
- https://github.com/viniciusmo/android-text-to-speech - 10 years ago

# onnx
- speech is almost there -> whisper already supported in fonnx & model available
- translation IS handled, but no existing dart demo -> 1st milestone
- all in Flutter ++ for crowdsourcing features
