## HealthCall
This is the repository for the healtcall corpus which consists with textual and audio data for the Arxiv preprint: https://arxiv.org/abs/2208.10249

[Arxiv 2022 Paper]

[Lackovic Nikola], [Montacié Claude], [Lalande Gauthier], [Caraty Marie-José]

<sup>1</sup>Malakoff Humanis.
<sup>2</sup>Sorbonne Université Paris, STIH<p>
<sup>*</sup> Both authors equally contributed to this work.

## Table of contents 

* [1. HealthCall Dataset](#1-HealthCall-Dataset)
    + [The dataset statistics](#the-dataset-statistics)
    + [The Json Structure](#the-dataset-structure)
* [2. Dataset sample and license](#2-dataset-sample-and-license)
    + [HealthCall](#healthcall)
    + [Licenses](#licenses)
* [3. Contact](#3-Contact)
* [4. Reference](#4-Reference)
* [5. How to cite](#5-how-to-cite)


## 1. HealthCall Dataset
  
The HealthCall (HC) corpus we provide is based on real audio interactions between call center agents and Malakoff Humanis customers who call to solve a problem or to request information. This corpus is designed to study natural spoken conversations and to predict CRM annotations made by human agents from various vocal interaction, audio and linguistic features. This corpus is composed of 2416 spoken conversations of varying duration (from a few minutes to several tens of minutes). Each conversation is anonymized respecting the General Data Protection Regulation (GDPR) recommendation and includes in addition to CRM annotations a transcription made by a Kaldi-based ASR system.
  
### The dataset statistics
	
#### General Description
	
| Corpus properties | Values |
| --------  | ------------------- |
| Number of conversations | 2416  | 
| Total Duration    | 251 hours 53 min |
| Max Duration    | 46 min 36 sec |
| Min Duration    | 1 min 18 sec |

#### Experimental Set


| Corpus properties | Values |
| ---------------- | ------ |
| Conversations Train | 	1214|
| Request (Process) | Train	650|
| Request (Member) | Train 	564|
| Complaint | Train 461|
| No Complaint | Train 753|
|Conversations Dev |	1202|
|Request (Process)  Dev |	584|
|Request (Member) Dev | 618|
|Complaint Dev | 455| 
|No Complaint Dev | 747|
	

### The dataset structure

We provide the json file for HealthCall with the following structure:
```
HealthCall_xx.json

"status": "qualified",
    "timestamp": "2021-01-25T10:26:11.279794Z",
    "tracking_info": {},
    "transcript_json": {
        "callData": [
            {  "content": "[pers.pre] bonjour",
                "datetime": 2.98,
                "duration": 0.88,
                "from": "out",
                "score": 0.86,
                "words": [
                    {"length": 0.36,
                        "score": 1.0,
                        "start": 2.98,
                        "value": [pers.pre]},
```



## 2. Dataset sample and license
```
  
To all the materials including speech data distributed here(hereinafter, “MATERIALS”), the following license(hereinafter, “LICENSE”) shall apply.

1. You are allowed to use the MATERIALS ONLY FOR NON-COMMERCIAL AI(Artificial Intelligence) RESEARCH AND DEVELOPMENT PURPOSES – ANY KIND OF COMMERCIAL USE IS STRICTLY PROHIBITED.
2. You should USE THE MATERIALS AS THEY WERE PROVIDED – ANY KIND OF MODIFICATION, EDITING AND REPRODUCTION TO DATA IS STRICTLY PROHIBITED.
3. You should use the MATERIALS only by/for yourself. You are NOT ALLOWED TO COPY, DISTRIBUTE, PROVIDE, TRANSPORT THE MATERIALS TO ANY 3RD PARTY OR TO THE PUBLIC including uploading the MATERIALS to internet.
4. You should clearly notify the source of the MATERIALS as “Malakoff Humanis” when your use the MATERIALS.
5. Malakoff Humanis DOES NOT GUARANTEE THE ACCURACY, COMPLETENESS, INTEGRITY, QUALITY OR ADEQUACY OF THE MATERIALS, THUS ARE NOT LIABLE OR RESPONSIBLE FOR THE MATERIALS PROVIDED HERE.

※ Please be noted that since the MATERIALS should be used within the confines of the voice right owner’s agreement (which was reflected in the LICENSE above), your non-compliance of the LICENSE (for example, using the MATERIAL for commercial use or modifying or distributing the MATERIAL) shall also constitute infringement on the voice right owner’s rights, thus may cause expose you to legal claims from the voice right owner.

```

`HealthCall` samples :

audio sample can be downloaded here : https://github.com/nikolalackovic/HealthCall/raw/main/Audio01_0fcd62FEa80454_2021-01-26_09h05_12Anonyme.wav
	
json sample can be downloaded here : https://github.com/nikolalackovic/HealthCall/raw/main/Transcription01_0fcd62FEa80454_2021-01-26_09h05.json


## 3. Contact

For any further information, contact : nikola.lackovic@malakoffhumanis.com or niko.lackovic@gmail.com

## 4. Reference
* Model
   * Camembert-base MODEL https://huggingface.co/camembert-base
   * Audio Model compare2016 https://audeering.github.io/opensmile-python/
   * Wave2Vec https://huggingface.co/facebook/wav2vec2-base

## 5. How to cite
```
@article{Lackovic, N., Montacié, C., Lalande, G., & Caraty, M. J. (2022). Prediction of User Request and Complaint in Spoken Customer-Agent Conversations. arXiv preprint arXiv:2208.10249.}
