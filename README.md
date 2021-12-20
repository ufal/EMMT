# About EMMT

We present EMMT, a dataset containing monocular eye movement recordings, audio data and 4-electrode wearable electroencephalogram (EEG) data of 43 participants while engaged in sight translation task supported by an image.

The full description of the experiment design is in the paper accompanying the EMMT dataset:

>  EMMT (Eyetracked Multi-Modal Translation), a simultaneous eye-tracking, 4-electrode EEG and audio corpus for multi-modal reading and translation scenarios<br>
>  Sunit Bhattacharya, Věra Kloudová, Vilém Zouhar, Ondřej Bojar<br>
>  2021


### Description of the data collected

The participants processed inputs in four stages: (1) reading an English sentence aloud, (2) translating it to Czech, (3) observing an image, related or unrelated to the sentence, (4) producing the same or a new translation.

Three kinds of data were recorded during the course of the experiment: eye-tracking (gaze), EEG and audio.

For the experiment, each participant was presented with a set of 32 text and image stimuli. Each such set of 32 stimuli s referred to as a ``probe``. 20 such probes were used for the purpose of the experiment. EMMT contains the gaze and audio recordings of 43 participants (P01-P43). EEG data of 28 (out of 43) participants was collected and accordingly included in EMMT. 

### Description of the folder structure

This is the overall folder structure used here: 

```
EMMT/
    -Probes/
        -Probe<xy>
            -P<participant_id>-<order_of_presentation>-S<sentence_id>-<cond>-<cong>-i<cond><image_id>.eeg
            -P<participant_id>-<order_of_presentation>-S<sentence_id>-<cond>-<cong>-i<cond><image_id>.et
            -P<participant_id>-<order_of_presentation>-S<sentence_id>-<cond>-<cong>-i<cond><image_id>.events
            -P<participant_id>-<order_of_presentation>-S<sentence_id>-<cond>-<cong>-i<cond><image_id>.mp3
            -...
            -probe
        -...
        -Participants.csv
        -Sentences.csv

    -experiment_pics/
        -a<image_id>.jpg
        -a...   
        -u<image_id>.jpg
        -u...
        -100.jpg

```

The folder ``Probes`` contain the recordings corresponding to the probes presented to the participants. The probes are numbered in the format:``Probe<xy>`` with ``<xy>`` ranging from 01 to 20. 
The details about the probe can be found in the file ``probe`` inside each ``Probe<xy>``. Also inside each ``Probe<xy>`` reside four types of files corresponding to each sentence stimuli presented to the participants. They can be found in the following format:
``P<participant_id>-<order_of_presentation>-S<sentence_id>-<cond>-i<cond><image_id>``


<participant_id> corresponds to the unique participant ID accorded to each participant. The anonymized participant names and the <participant_id> corresponding to them can be found in the file ``Probes\Participants.csv``. 
<order_of_presentation> refers to the actual order in which the sentence was presented to a participant. The stimuli listed in the ``probe`` were presented in a random order to each participant during the experiment. <order_of_presentation> contains the information about that ordering.
<sentence_id> refers to the unique sentence ID that has been bestowed upon each sentence used as a textual stimuli in the experiment. Information about the sentence IDs correponding to the actual sentences can be found in ``Probes\Sentences.csv``. 
<cond> refers to the condition captured by the textual stimulus. <cond> has the values of A or U corresponding to an ambiguous or unambiguous sentence respectively. 
<cong> refers to the congruency between the textual stimulus and the visual stimulus. <cong> has the values of C,I,M or K corresponding to Congruent (text and image are related), Incongruent (text and image are unrelated), M (image has no clues), K (images used for the contrastive case). 
<image_id> refers to the id of the actual image presented to a participant for that particular sentenceID. The images can be found at ``experiment_pics/<image_id>``.

For some sentence ``P<participant_id>-<order_of_presentation>-S<sentence_id>-<cond>-i<cond><image_id>``, the ``.eeg`` file contains the raw EEG data corresponding to that particular sentence. Similarly, the corresponding ``.eeg`` and ``.mp3`` files contain the gaze data and audio data respectively. Finally, the 



## Authors

* Sunit Bhattacharya
* Věra Kloudová 
* Vilém Zouhar
* Ondřej Bojar

## License

This project is licensed under a Creative Commons Attribution 4.0 International License. - see the [LICENSE.md](LICENSE.md) file for details
