## HealthCall
This is the repository for the healtcall corpus which consists with textual and audio data for the Arxiv preprint: https://arxiv.org/abs/2208.10249

[Arxiv 2022 Paper]

[Lackovic Nikola], [Montacié Claude], [Lalande Gauthier], [Caraty Marie-José]

<sup>1</sup>Malakoff Humanis.
<sup>2</sup>Sorbonne Université Paris, STIH<p>
<sup>*</sup> Both authors equally contributed to this work.

Automatic prediction of user requests and complaints from spoken conversations between customers and human agents are two important tasks in customer relationship management. 
For this purpose, we have investigated vocal interaction, audio and linguistic features related to these tasks. The experiments were conducted on 2,416 spoken conversations from the Malakoff Humanis (health mutual) call center. Each conversation was recorded on two separate audio channels, the first one for the user and the second one for the agent. The text transcription of each channel was obtained by the Nuance speech recognition system. Vocal interaction features were computed from a statistical model of talk spurts and silences. Each word of the text transcript was encoded by a Bidirectional Encoder Representation from Transformers (BERT). The sequence of encoded words is then fed into a feature compression block: a single linguistic feature vector for the entire ? channel. 
Audio features were extracted using openSMILE and ComPaRe audio feature set. The results show that linguistic features predict the type of user request better than other features. On the other hand, the vocal interaction and audio features are more discriminating in detecting user complaints. The combination of all these features allows a significant improvement of the results in terms of Unweighted Average Recall (UAR).




## Table of contents 

* [1. HealthCall Dataset](#1-HealthCall-Dataset)
    + [The dataset statistics](#the-dataset-statistics)
    + [The Json Structure](#the-dataset-structure)
* [2. Dataset downloading and license](#2-dataset-downloading-and-license)
    + [HealthCall](#clovacall)
    + [Licenses](#licenses)
* [3. Reference](#7-reference)
* [4. How to cite](#8-how-to-cite)


## 1. HealthCall Dataset
  
The HealthCall (HC) corpus we provide is based on real audio interactions between call center agents and Malakoff Humanis customers who call to solve a problem or to request information. This corpus is designed to study natural spoken conversations and to predict CRM annotations made by human agents from various vocal interaction, audio and linguistic features. This corpus is composed of 2416 spoken conversations of varying duration (from a few minutes to several tens of minutes). Each conversation is anonymized respecting the General Data Protection Regulation (GDPR) recommendation and includes in addition to CRM annotations a transcription made by a Kaldi-based ASR system.
  
### The dataset statistics

####Corpus Properties	Values

#####General Description
	
Number of conversations	2416
Total Duration 251 hours 53 min
Max Duration 46 min 36 sec
Min Duration 1 min 18 sec

#####Experimental Set
	
TRAIN
  
Conversations Train 	1214
Request (Process) Train	650
Request (Member) Train 	564
Complaint Train 461
No Complaint Train 753

 DEV

Conversations Dev	1202
Request (Process)  Dev	584
Request (Member) Dev 618
Complaint Dev 455
No Complaint Dev 747


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



## 2. Dataset downloading and license
```
  
JE NE SAIS PAS QUOI METTRE COMME LICENSE

```

`HealthCall` dataset can be download for researchers involved in Acdaemic Organizations by applying via [here]
 (insert form)
## 3. Contact

For any further information, contact : nikola.lackovic@malakoffhumanis.com or niko.lackovic@gmail.com

## 4. Reference
* Model
   * Camembert-base MODEL https://huggingface.co/camembert-base
   * Audio Model compare2016 (link)
   * Other Audio Model Link

## 5. How to cite
```
@article{N. Lackovic, C. Montacié, G. Lalande, and M.-J. Caraty, “Prediction of User Request and Complaint in Spoken Customer-Agent Conversations”, in Proceedings INTERSPEECH 2022, 23rd Annual Conference of the International Speech Communication Association, Incheon, Korea, pp. 100–104, 2022.
