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

### Training Data Statistics

Total files: 238

|| Tasks | info-Units | sentences | entities | triples total | subject | predicate | object |
|| :---: |:---:|  :---:   |   :---:  | :---: |  :---:  |   :---:   |  :---: |
|1 | natural_language_inference    |    |     |     | 7330 |     |     |     |
|2 | negation_scope_resolution     |    |     |     |  94  |     |     |     |
|3 |   paraphrase_generation       |    |     |     |  175 |     |     |     |
|4 |   part-of-speech_tagging      |    |     |     |  479 |     |     |     |
|5 |     passage_re-ranking        |    |     |     |  123 |     |     |     |
|6 |      phrase_grounding         |    |     |     |  102 |     |     |     |
|7 |     prosody_prediction        |    |     |     |  103 |     |     |     |
|8 |    query_wellformedness       |    |     |     |  35  |     |     |     |
|9 |     question_answering        |    |     |     | 640  |     |     |     |
|10|    question_generation        |    |     |     |  87  |     |     |     |
|11|    question_similarity        |    |     |     |  51  |     |     |     |
|12|    relation_extraction        |    |     |     | 1084 |     |     |     |
|13|     sarcasm_detection         |    |     |     | 136  |     |     |     |
|14|     semantic_parsing          |    |     |     | 180  |     |     |     |
|15| semantic_role_labeling        |    |     |     | 318  |     |     |     |
|16| sentence_classification       |    |     |     | 297  |     |     |     |
|17| sentence_compression          |    |     |     | 248  |     |     |     |
|18|   sentiment_analysis          |    |     |     | 4086 |     |     |     |
|19|   smile_recognition           |    |     |     |  54  |     |     |     |
|20|temporal_information_extraction|    |     |     |  93  |     |     |     |
|21|   text-to-speech_synthesis    |    |     |     | 192  |     |     |     |
|22|       text_generation         |    |     |     | 420  |     |     |     |
|23|     text_summarization        |    |     |     | 1010 |     |     |     |
|24|        topic_models           |    |     |     |  48  |     |     |     |


### Note

For system training, participants are encouraged to merge the 50 files additionally from the [`trial-data`](https://github.com/ncg-task/trial-data) release.
