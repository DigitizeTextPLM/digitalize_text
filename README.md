# Digitize Text (pre-processing)
> As society beecomes more reliant on technology there is an inccrease desire to transition materials that were once hard-copy (e.g., handwritten cursive, handwritten printed and type-writer documents) into electronically saved. The goal of this project is to explore how NLP techniques can assist in cleaning materials after extracting text from images using Optical Character Recognition (OCR) tools. The techniques explored include fine-tuning the pre-trained language model, GPT2. 

> NOTE: OCR is primarily developed for extracting printed material from images of text.


## Structure to access pre-processed data: 
- All data is split and located in `dataForModel`
- Within each split of data there is the Betham data and the IAM data, and each folder further has the GT and OCR.
- Train: Val: Test == 70:20:10

## Important to Note for Raw Data: 

### IAM Database
- Forms => images of whole pieces of paper, GT data is located on the forms
- used lines to extract the handwriting from files and concatenated to be one line in `.txt`
- GT was located in xml files based on position, and extracted as one line in `.txt` file 

### Bentham Dataset 
- GT in XML files so extracted as one line in `.txt`
- Pages has whole handwritten no GT on top. There is `\n` throughout OCR

## Importing PyTesseract
- use `brew install tesseract`
- to find executable `which tesseract`

# Authors 
- Joel Nicolow
- Amanda Nitta
- Jan (Mark) Schittenhelm