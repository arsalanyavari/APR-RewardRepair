# RewardRepair
Neural Program Repair using Execution-based Backpropagation (Paper under review)

## Folder Structure
 ```bash
 ├── data: csv data used for training
 │ 
 ├── model: the trained model of RewardRepair
 │
 ├──syntactic_training.py: script to syntactically train RewardRepair
 │
 ├──semantic_training.py: script to semantically train RewardRepair
 │
 ├──ResultForRQ1: raw experiment data for RQ1
 │
 ├──ResultForRQ2: raw experiment data for RQ2
 │
 ├──ResultForRQ3: raw experiment data for RQ3
 │
 ├──ComparisonData.csv: the file to compare with the state-of-the-art
 
```

## Prerequisites

* JDK 1.8
* Pytorch==1.7.1
* transformers>=4.10.0
* OS: Linux and Mac
* Add submodule Bears and copy the folder myscript to Bears


```
git submodule add https://github.com/bears-bugs/bears-benchmark.git
cp -rf myscript ./bears-benchmar/
pip install transformers
```
Extract the training data
```
tar -xzvf MegaDiff-CodRep.tar.gz
tar -xzvf pretrain.csv.tgz
```
To run our script
```
python3 syntactic_training.py
python3 semantic_training.py
```


## RQ2: Details reults are available in RewardRepair/ResultForRQ2/
| Benchmarks | Top30 | Top100 | Top200 |
| :---: | :---: | :---: |:---: |
| QuixBugs | 44.1% | 35.7% | 31.5%|
| Defects4J | 45.7% | 38.0% |33.6%|

