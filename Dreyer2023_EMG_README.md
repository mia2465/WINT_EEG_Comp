# Dreyer2023 Data Exploration and EMG Analysis

This analysis covers all 87 participants returned by the MOABB
Dreyer2023 loader: 520 recordings and 20,792 labeled motor imagery trials.

## Methods

EMG mean and population standard deviation (ddof=0) were calculated
for whole recordings and fixed 0–5 second windows after left-hand
and right-hand cues. Values are reported in microvolts.

No additional filtering, rectification, normalization, baseline
correction, or artifact rejection was applied.

## Results

- Sampling frequency: 512 Hz
- Channels per recording: 27 EEG, 3 EOG, and 2 EMG
- EMG channels: EMGd and EMGg
- Left-hand cues: 10,394
- Right-hand cues: 10,398
- Trial × EMG channel rows: 41,584
- No skipped windows, missing EMG channels, invalid samples,
  or completely flat EMG signals were detected.

These basic checks do not establish that recordings are artifact-free.

## Exceptions and limitations

Participant 59 has four returned recordings rather than six.
Participant 40's run 2R3online has 14 left-hand and 18 right-hand cues.

Large EMG baseline offsets and amplitude variation remain under
investigation. NeuralBench's prepared inputs, preprocessing,
and competition splits have not yet been verified.

## Files

- recordings.csv: recording structure and cue counts
- channels.csv: channel names and types
- emg_run_stats.csv: whole-recording EMG statistics
- emg_trial_stats.csv: individual-trial EMG statistics
- emg_summary.csv: summaries by recording, hand label, and channel
- recording_count_exceptions.csv: recording-count exceptions
- cue_count_exceptions.csv: cue-count exceptions
- emg_overview.csv: dataset-wide whole-recording EMG overview

## Documentation

- [Data documentation](https://docs.google.com/document/d/1v89RUGt3t_NmL3Hvs00g2MNnULmNQeXIwxFA1PQ86Iw/edit?tab=t.0#heading=h.o4ozp9m1108u)
- [Shared results and notebook](https://drive.google.com/drive/u/1/folders/1U98Mc7kLUkbTmy6lrzm3hI2F9jN2ubcB)

Run the analysis notebook in Google Colab. It requires dataset setup
and Google Drive mounting; update the output path for your account.
