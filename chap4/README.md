# Roberta-sequence-classification in a Docker container served by a Flask application
Requires to download the model from here: 
https://github.com/onnx/models/tree/main/text/machine_comprehension/roberta

Then put it in the chap4 directory: 
```
chap4$ tree
.
├── Dockerfile
├── Makefile
├── README.md
├── requirements.txt
├── roberta-sequence-classification-9.onnx
└── webapp
    └── app.py
```