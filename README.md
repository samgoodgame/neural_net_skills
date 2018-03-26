# neural_net_skills
_A neural network language model to show relationships between skills_

![What skills are the most closely related?](./assets/data.png "Which skills should I pick up?")

### Overview
This project trains a skip-gram Word2vec model in order to make accurate inferences about technical skills. The primary source of training data is a corpus of 40,000 job descriptions scraped from the Internet. I'm working on secondary sources. The practical use case of this model is to be able to generate a canonical list of technical skills and elucidate the relationships between them. The model is assessed using the same analogy tasks that the original Word2vec paper proposed. The baseline accuracy of this model on a set of 1,954 general language model analogy tasks is 18.17% -- but those tasks aren't really tailored for a job-related dataset, so the tasks themselves need some editing.

#### Data:
- Job description data (~40,000 JDs), scraped from the Internet
- Stackoverflow data, via their API.
  - Status: POC compete; just need to figure out what query I want.
- Possible: Department of Labor [O*NET Database](https://www.onetonline.org/) and [My Next Move](https://www.mynextmove.org/) site
  - Status: database uploaded locally; I just need to extract the text and format it for ingestion

#### Possible additional methods
- Cross-train the Google Word2vec model. Start with it, then add all of my current data as additional training. This should help it perform generally, as well as with job-specific tasks.
