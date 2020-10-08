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
        └── ...                                        # there are 25 tasks selected overall, so this repeats 24 more times

### Data Elements Counts

Total files: 238

|| Tasks | info-units | sentences | entities | triples total | subject | predicate | object |
| :---:  | :--- |:---:|  :---:   |   :---:  | :---: |  :---:  |   :---:   |  :---: |
|1 | natural_language_inference    |    |     |     | 7330 |3171 |1251 |5242 |
|2 | negation_scope_resolution     |    |     |     |  94  | 50  | 42  | 80  |
|3 |   paraphrase_generation       |    |     |     |  175 | 99  | 77  | 160 |
|4 |   part-of-speech_tagging      |    |     |     |  479 | 249 | 156 | 401 |
|5 |     passage_re-ranking        |    |     |     |  123 | 63  | 66  | 103 |
|6 |      phrase_grounding         |    |     |     |  102 | 58  | 53  | 94  |
|7 |     prosody_prediction        |    |     |     |  103 | 58  | 43  | 97  |
|8 |    query_wellformedness       |    |     |     |  35  | 22  | 25  | 33  |
|9 |     question_answering        |    |     |     | 640  | 332 | 203 | 547 |
|10|    question_generation        |    |     |     |  87  | 45  | 44  | 74  |
|11|    question_similarity        |    |     |     |  51  | 30  | 26  | 49  |
|12|    relation_extraction        |    |     |     | 1084 | 552 | 372 | 922 |
|13|     sarcasm_detection         |    |     |     | 136  | 77  | 73  | 116 |
|14|     semantic_parsing          |    |     |     | 180  | 91  | 74  | 157 |
|15| semantic_role_labeling        |    |     |     | 318  | 163 | 137 | 288 |
|16| sentence_classification       |    |     |     | 297  | 167 | 134 | 273 |
|17| sentence_compression          |    |     |     | 248  | 138 | 104 | 223 |
|18|   sentiment_analysis          |    |     |     | 4086 |1864 | 940 |2967 |
|19|   smile_recognition           |    |     |     |  54  | 29  | 34  | 49  |
|20|temporal_information_extraction|    |     |     |  93  | 58  | 62  | 85  |
|21|   text-to-speech_synthesis    |    |     |     | 192  | 103 | 98  | 174 |
|22|       text_generation         |    |     |     | 420  | 222 | 165 | 351 |
|23|     text_summarization        |    |     |     | 1010 | 513 | 346 | 825 |
|24|        topic_models           |    |     |     |  48  | 30  | 28  | 48  |


### Note

For system training, participants are encouraged to merge the 50 files additionally from the [`trial-data`](https://github.com/ncg-task/trial-data) release.
