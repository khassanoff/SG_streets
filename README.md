# SG_streets
An evaluation set for speech recognition experiments used in [1]. This set contains 6 interview sessions (close talk microphone) of Singaporean students reading passages about Singapore streets. Each interview sessions consists of 2 recordings corresponding to interviewer and interviewee. 

No.	| Recording id                  | Street names	                | Speaker gender  | Duration	| # Words
----|-------------------------------|-------------------------------|-----------------|-------------|---------
1	| mml-14-feb-2018-a-session4    | Balestier, Ang Mo Kio	        | Female          |	00:09:57	| 1,479
2	| mml-15-dec-2017-session4	    | Kreta ayer, Aljunied	        | Male	          | 00:10:25	| 1,207
3	| mml-19-dec-2017-b-session4    | Marsiling, Bedok	            | Male	          | 00:07:24	| 862
4	| mml-19-jan-2018-b-session4	| Boon Lay	                    | Female	      | 00:09:30	| 1,695
5	| mml-24-jan-2018-a-session4	| Bukit Batok	                | Male	          | 00:07:41	| 1,081
6	| mml-24-jan-2018-b-session4	| Sembawang	                    | Female	      | 00:09:03	| 1,018

## Other notes:
- Compound street names are combined using underscore symbol, i.e. 'boon lay' -> 'boon_lay'.
- To simulate the scenario where these street names are rare words, ensure that they are absent or appear 1-3 times in the train set.
- The main application of the evaluation set is to correctly recognize these street names while preserving the WER.
- List of Singapore street names can be found in: https://geographic.org/streetview/singapore/
- The pronunciation lexicon can be obtained from G2P models such as http://www.speech.cs.cmu.edu/tools/lextool.html . E.g. for word "boon_lay", first generate pronunciation lexicon of "boon" and "lay" separately, and then combine all pronunciation variations.
- The readers are Singaporeans (accent is different from English speakers in other contries), and thus train set containing Singapore English is recommended, e.g. https://www2.imda.gov.sg/NationalSpeechCorpus.

# References
[1] Khassanov, Y., Zeng, Z., Pham, V. T., Xu, H., & Chng, E. S. (2019). Enriching Rare Word Representations in Neural Language Models by Embedding Matrix Augmentation. arXiv preprint arXiv:1904.03799.
