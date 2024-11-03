# Digitize Handwritten (pre-processing)

## Structure to access pre-processed data: 
- All data located in `dataForModel`
- Within each split of data there is the Betham data and the IAM data, and each folder further has the GT and OCR.

## Important to Note for Raw Data: 

### IAM Database
- Forms => images of whole pieces of paper, GT data is located on the forms
- used lines to extract the handwriting from files and concatenated to be one line in `.txt`
- GT was located in xml files, and extracted as one line in `.txt` file 

### Bentham Dataset 
- GT in XML files so extracted as one line in `.txt`
- Pages has whole handwritten no GT on top. There is `\n` throughout OCR

## Importing PyTesseract
- use `brew install tesseract`
- to find executable `which tesseract`