# UPLOADING

- At the beginning of the session 
  - If you have been designated as an Uploader, ask the event organizer to set you up with
    - The S3 login credentials
    - The software needed to upload a file to S3 from your laptop through the command line
      - The basic commands needed for that are:
      ```
      pip install awscli	
      aws configure	
      aws s3 ls [eventS3Folder]
      ```
      - If you need more help to run these commands, please talk to the event organizer
  
- Claiming a bag for upload 
  - Baggers will bring you thumbdrives containing bags
  - Grab one of those thumbdrive to upload it to S3
  - Note that the Uploader(s) should make sure that all thumbdrives deposited by Baggers are carefully arranged into a small queue while waiting to be uploaded, and are clearly distinguished from the thumbdrives that have already been processed. This will avoid confusions. 

- Uploading the file
  - Plug the thumbdrive into your laptop and check its content
  - There should be a single Zip file on it: that's the bag
  - upload it using the command
  ```
  aws s3 cp [sourceFile] s3://[eventS3Folder]
  ```
  
- Recording that the upload took place  
  - In the "Uncrawlable Content" spreadsheet list, locate the bag you just uploaded and enter your slack name in the "Uploading to S3" cell

- Verification step 
 - In the "Uncrawlable Content" spreadsheet, click on S3 URL for the bag  
 - It should start downloading
 - When it is downloaded, unzip it 
 - Spot check some of the files (make sure they open and look normal, i.e., are not garbled)
     
- Finishing up
  - Once you are certain that the Zip file was uploaded successfully, delete the it from the thumbdrive 
  - Put the thumbdrive in the stack of available thumbdrives for Harvesters
