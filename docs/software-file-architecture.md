# Application File Architecture

```
├── spectra/
|    ├── __init__.py
|    ├── preprocessing/
|    |    ├── __init__.py
|    |    ├── smoothing/  
|    |    |    ├── __init__.py
|    |    |    ├── kaiser.py
|    |    |    └── savgol.py
|    |    ├── baseline_correction/  
|    |    |    ├── __init__.py
|    |    |    └── airpls.py
|    |    └── README.md
|    ├── cli/
|    |    ├── __init__.py
|    |    └── README.md
|    ├── io/
|    |    ├── __init__.py
|    |    └── README.md
|    ├── util/
|    └── README.md
├── web/
├── tests/
├── scripts/
├── docs/
|    ├── images/
|    ├── pdfs/
|    ├── notebooks/
|    └── README.md
├── .gitignore
├── .travis.yml
├── setup.py
├── requirements.txt
├── DOCKERFILE
└── README.md
```
