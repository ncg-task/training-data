# train-data
Training data for the NLPContributionGraph Shared Task 11 at SemEval-2021

For Codalab evaluations in the Practice phase, participants systems will be evaluated against the [Trial Data](https://github.com/ncg-task/trial-data)

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

### Dataset Statistics
