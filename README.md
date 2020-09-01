# IBM Datacap FAQ  
  
## 1. How is the licensing scheme for OCR in IBM Data Cap?  
OCR license is already part of datacap license. Datacap license can be in form of authorized user or PVU based license.  
  
## 2. What's the best practice to managing backlog document? FYI we have 60 Million pages that need to clasify in the 1st year, and around 6 Million in the 2nd year, and around 7 Million in 3rd year with growing rate about 10-15% YOY.  
To improve the performance you need to implement the rule-runner server so you will be able to run multi-thread process. 
Since you have big amount of documents, you may create a summary page that contains information that will need to be captured by datacap. 
  
## 3. What page identification technique that IBM think will be performance better for our internal document (Contract, National ID) ?  Can we implement multiple technique in 1 form? Is there any differentiation in the pricing scheme for all those available technique? or all those feature available in the default license scheme?  
Yes, we can combine multiple techniques like template and keyword for a single form. 

## 4. Can we reorder, split and merge page using Datacap?  

Yes we can configure Datacap to reorder, split and merge. This to be done manually by user using IBM Content Navigator  
  
## 5. - Can we detect object in document? whether the document is already signed by the branch user? We want to validate if the document is signed by the branch user, also we want to compare the sign in the document vs the one that recorded in the system for that particular user.  
With datacap we can setup a template to set the area for signature and then datacap can capture the signature and run the comparison against the signature database.  
  
## 6. What's the available licensing scheme for IBM Watson Natural Language Understanding (NLU)?  
We offer this as part of Datacap Insight authorized user license  

## What else besides OCR feature that Datacap can do?
- ICR (handwriting recognition), OMR (checklist recognition), signature verification
- Reformatting of data captured during OCR for example reformat date from dd/mm/yyyy to mmddyyyy

## How do you work with low quality images?  
OCR will not work on low quality images and dirty images. Pre-procesing is required to clean up the source documents and rescanning is required to have a high quality document.   
You will need to create fingerprint using various DPI values, 200, 300, etc.   

 If you decide to retain color for pages that are color, use a loss-less compression such as LZW. Do not use a lossy compression such as JPEG as this will reduce the quality of recognition, even if a high quality compression rate is chosen. Always use a loss-less compression for text that will be recognized.  
  
## Can we crop & save the face picture from the national ID / Driving License ?  
Yes we can configure Datacap to crop 

## Can we extract information from the bank statement? and what the best practice if there available multiple template for each bank? 
We need to develop the template from each bank  
  
## How can we improve the performance of Datacap?  
You need to implement enough rule-runner to enable multi-threading that will run the processes in parallel  




