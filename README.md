# Use to extract details from a aadhaar card

 Trained using YOLOv8

Check out the Github [Repo](https://github.com/Akash-k-p/Aadhaar_Extractor/) for more info

> Note : Requires external installation of tesseract , and setting the environment variable of the same


## How to use :

```
from Aadhaar_extractor.Extractor import AadhaarExtractor

#create a object of the AadhaarExtractor class by passing the image of the aadhaar card as argument`


obj = AadhaarExtractor("aadhaar.jpg")

#use obj.extract() for extracting the data 

extractedData = obj.extract()

```


The extract() method will return , a list of all the fields detected .

This module currently detects five fields:

1. Aadhaar Number (aadhaar_no)
2. Date of Birth (dob)
3. Gender (gender)
4. Name (name)
5. Address (address)

Each field is member of the list(detected field), has four fields in the following order

1. The coordinates of the detected field in x1,y1,x2,y2 format (type=list)

2. The name of the field

3. Confidence of detection 

4. Extracted text from the detected field



