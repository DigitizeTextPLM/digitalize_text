# Digitize Text (pre-processing)
> As society beecomes more reliant on technology there is an inccrease desire to transition materials that were once hard-copy (e.g., handwritten cursive, handwritten printed and type-writer documents) into electronically saved. The goal of this project is to explore how NLP techniques can assist in cleaning materials after extracting text from images using Optical Character Recognition (OCR) tool, Tesseract. The techniques explored include fine-tuning the pre-trained language model, GPT2. 

> NOTE: OCR is primarily developed for extracting printed material from images of text.

# Code to Run: 

## Pre-Training Model: 
- File Name:   `gpt-train.ipynb`
- Change paths to where data is located on local machine
- Run code blocks in order
> Warning: May run into memory issues, so we advise to use Koa's NV-H100 GPU 

## Evaluating Data
> Our primary evaluation metric is cosine similarity 
- File Name: `gpt-evaluation-save.ipynb`
- Change paths to where processed data is located on local machine
- Run code blocks in order

## Tesseract 
- File Name: `OCR_tesseract_digitize.ipynb`
- Use function `run_tesseract_on_images` and provide the relative input and output directories 
> Warning: Second `run_tesseract_on_images` function concatenates the OCR from multiple images

# Data

## Structure to access pre-processed data: 
- All data is split and located in `dataForModel`
- Within each split of data there is the Betham data and the IAM data, and each folder further has the GT and OCR.
- Train: Val: Test == 70:20:10

## Important to Note for Raw Data Pre-Processing: 

### IAM Database
- Forms => images of whole pieces of paper, GT data is located on the forms
- used lines to extract the handwriting from files and concatenated to be one line in `.txt`
- GT was located in xml files based on position, and extracted as one line in `.txt` file 

### Bentham Dataset 
- GT in XML files so extracted as one line in `.txt`
- Pages has whole handwritten no GT on top. There is `\n` throughout OCR

# Uncommon Imports
## Importing [Google's PyTesseract](https://github.com/tesseract-ocr/tesseract) 
- use `brew install tesseract`
- to find executable `which tesseract`

# Authors 
- Joel Nicolow
- Amanda Nitta
- Jan (Mark) Schittenhelm
