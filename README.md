# training-data
`Training Data` for the NLPContributionGraph Shared Task 11 at SemEval-2021

The repository is organized as follows:

    README.md                            
    [task-name-folder]/                                # natural_language_inference, paraphrase_generation, question_answering, relation_extraction, topic_models
        ├── [article-counter-folder]/                  # ranges between 0 to 100 since we annotated varying numbers of articles per task
        │   ├── [articlename].pdf                      # scholarly article pdf
        │   ├── [articlename]-Grobid-out.txt           # plaintext output from the [Grobid parser](https://github.com/kermitt2/grobid)
        │   ├── [articlename]-Stanza-out.txt           # plaintext preprocessed output from [Stanza](https://github.com/stanfordnlp/stanza)
        │   ├── sentences.txt                          # annotated Contribution sentences in the file
        │   ├── entities.txt                           # annotated entities in the Contribution sentences
        │   └── info-units/                            # the folder containing information units in JSON format
        │   │   └── research-problem.json              # `research problem` mandatory information unit in json format
        │   │   └── model.json                         # `model` information unit in json format; in some articles it is called `approach`
        │   │   └── ...                                # there are 12 information units in all and each article may be annotated by 3 or 6
        │   └── triples/                               # the folder containing information unit triples one per line
        │   │   └── research-problem.txt               # `research problem` triples (one research problem statement per line)
        │   │   └── model.txt                          # `model` triples (one statement per line)
        │   │   └── ...                                # there are 12 information units in all and each article may be annotated by 3 or 6
        │   └── ...                                    # there are between 1 to 100 articles annotated for each task, so this repeats for the remaining annotated articles
        └── ...                                        # there are 24 tasks selected overall, so this repeats 23 more times

### Data Element Counts

Total Papers Annotated: 237

|| Tasks | info-units | sentences | entities | total triples | total unique triples | subject | predicate | object |
| :---:  | :--- |:---:|  :---:   |   :---:  | :---: | :---: |  :---:  |   :---:   |  :---: |
|1 | natural_language_inference    |427 |2168 |12657|7969 | 7330 |3171 |1251 |5242 |
|2 | negation_scope_resolution     | 4  |28   |163  |94   |  94  | 50  | 42  | 80  |
|3 |   paraphrase_generation       |  9 |44   |293  |177  |  175 | 99  | 77  | 160 |
|4 |   part-of-speech_tagging      |36  |144  |804  |501  |  479 | 249 | 156 | 401 |
|5 |     passage_re-ranking        | 8  |32   |214  |126  |  123 | 63  | 66  | 103 |
|6 |      phrase_grounding         | 5  |29   |172  |102  |  102 | 58  | 53  | 94  |
|7 |     prosody_prediction        | 5  |31   |172  |105  |  103 | 58  | 43  | 97  |
|8 |    query_wellformedness       | 5  |11   |54   |35   |  35  | 22  | 25  | 33  |
|9 |     question_answering        |30  |194  |1059 |665  | 640  | 332 | 203 | 547 |
|10|    question_generation        | 7  |34   |133  |87   |  87  | 45  | 44  | 74  |
|11|    question_similarity        | 4  |16   |82   |51   |  51  | 30  | 26  | 49  |
|12|    relation_extraction        | 69 |346  |1923 |1154 | 1084 | 552 | 372 | 922 |
|13|     sarcasm_detection         | 10 |40   |225  |138  | 136  | 77  | 73  | 116 |
|14|     semantic_parsing          | 12 |60   |275  |183  | 180  | 91  | 74  | 157 |
|15| semantic_role_labeling        | 22 |100  |545  |338  | 318  | 163 | 137 | 288 |
|16| sentence_classification       | 15 |85   |513  |300  | 297  | 167 | 134 | 273 |
|17| sentence_compression          | 19 |77   |426  |260  | 248  | 138 | 104 | 223 |
|18|   sentiment_analysis          |240 |1275 |7452 |4517 | 4086 |1864 | 940 |2967 |
|19|   smile_recognition           | 3  |17   |85   |54   |  54  | 29  | 34  | 49  |
|20|temporal_information_extraction| 8  |26   |152  |94   |  93  | 58  | 62  | 85  |
|21|   text-to-speech_synthesis    |13  |69   |316  |197  | 192  | 103 | 98  | 174 |
|22|       text_generation         |24  |129  |704  |431  | 420  | 222 | 165 | 351 |
|23|     text_summarization        |70  |347  |1777 |1077 | 1010 | 513 | 346 | 825 |
|24|        topic_models           | 5  |18   |75   |48   |  48  | 30  | 28  | 48  |


### Note

For system training, participants are encouraged to merge the 50 files additionally from the [`trial-data`](https://github.com/ncg-task/trial-data) release.
