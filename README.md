# GenAI for Software Development Assignment 1
Lynelle Chen, Ben Tremblay, Rowan Miller

* [1 Introduction](#1-introduction)  
* [2 Setup](#2-setup)
* [3 Run Model](#3-run-model)
* [4 Report](#4-report)

## **1. Introduction**  
We have developed a model to automatically complete a Java method given a starting set of code tokens. Our model uses the N-gram method to predict the next token in a sequence given (N - 1) preceding tokens. It is trained on a corpus of public GitHub repositories and stores the frequency of all sequences of N consecutive tokens. When predicting the next token in a sequence, it chooses the one with the highest probability in the training corpus. Our model was evaluated by being asked to automatically complete a method given only its first (N - 1) tokens.

## **2. Setup**  
This project is implemented in **Python 3** and is compatible with **macOS, Linux, and Windows**.  

Clone the repository to your workspace:  
```shell
~ $ git clone https://github.com/rvmiller0/n-grams.git

(2) Navigate into the repository:

~ $ cd n-grams
~/n-grams $

(3) Set up a virtual environment and activate it:

For macOS/Linux:

~/n-grams $ python -m venv ./venv/
~/n-grams $ source venv/bin/activate
(venv) ~/n-grams $ 
```

Install the required dependencies:
`(venv) ~/n-grams $ pip install -r requirements.txt`

When you're finished, to deactivate the virtual environment, use the command:
`(venv) $ deactivate`

## **3. Run Model**
The script takes a corpus of Java methods as input and automatically identifies the best-performing model based on a specific N-value. It then evaluates the selected model on the test set extracted according to the assignment specifications.
Since the training corpus differs from both the instructor-provided dataset and our own dataset, we store the results in a file named results_provided_model.[json/csv/txt] to distinguish them accordingly.

`(venv) ~/n-grams $ python ngram.py corpus.txt`

## 4. Report
The assignment report is available in the file Assignment_Report.pdf.
