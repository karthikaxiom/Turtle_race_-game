# Finish Check Timing

The race loop checks each turtle's current x-coordinate at the beginning of that turtle's turn, before calling `forward(...)`. A movement step that crosses the threshold is therefore observed on a later turn, not immediately after the movement call.

The maintained explanation is [Threshold Detection Timing](THRESHOLD_DETECTION.md). Update that page when the threshold or check order changes.
