# Feature binding task
Last edit: 11/22/2024

## Edit history
- 11/22/2024 by Alex He - removed summary csv saving since no trialList used
- 11/21/2024 by Alex He - added voice over instruction to encourage questions on the schematic diagram
- 10/24/2024 by Alex He - added a print message of task ID at the onset of task
- 10/12/2024 by Alex He - increased logging granularity from warning to debug (maximal level)
- 10/10/2024 by Alex He - added MilliKey response box and finalized voice-over audio
- 09/27/2024 by Alex He - fixed a bug of skipping one image stimulus for main trials
- 09/25/2024 by Alex He - added winHandle.activate() to make sure window is on foreground
- 09/23/2024 by Alex He - upgraded to run on PsychoPy 2024.2.2
- 09/18/2024 by Alex He - updated image stimuli sets to allow five repeated test sessions
- 09/07/2024 by Alex He - finalized the task design and experiment setup
- 08/02/2024 by Alex He - created initial draft of the task

## Description
This is a short-delay memory paradigm using a two-alternative forced choice (2AFC) test on old/new recognition of visual picture stimuli. This behavioral paradigm is adapted from the object-location short-term memory task:

Das, S. R., Mancuso, L., Olson, I. R., Arnold, S. E., & Wolk, D. A. (2016). Short-term memory depends on dissociable medial temporal lobe regions in amnestic mild cognitive impairment. Cerebral Cortex, 26(5), 2006-2017.

In each trial, three visual objects are presented one at a time for 1 second, and followed by an 8-second delay. Instead of the three conditions with cues of 'Remember Object', 'Remember Location', or 'Remember Object and Location' in the original object-location short-term memory task (Das et al. 2016), all trials in the current version will test the successful encoding and recognition of conjunctive features (i.e., all trials are the "Remember Object and Location" type, and no cue will be displayed). A total of 80 trials (all conjunction) will be presented, with 40 trials being intact that should be responded as Old, and the remaining 40 trials being rearranged that should be responded as New.

Compared to the original design, this version no longer extracts the delta in behavioral performance between single versus conjunction feature conditions. We are more interested in analyzing neural signals during successful versus failed conjunctive feature binding in encoding and recognition after a short delay, as well as the neural signatures of feature binding during the delay period. We also have many more trials by dropping single feature trials and only administering conjunction feature trials to better estimate behavioral performance.

## Outcome measures
- Behavioral performance across all trials (d')
- Alpha activity during the 8-s delay period
- A sharp alpha-beta power reduction at the onset of stimulus
- Potential parietal ERP old/new effect during testing
- Potential subsequent memory effects during encoding
