# AWS S3 Buckets

:wave: :wave: :wave: :wave: :wave:

# Documentation

My Personal Documentation 

## AWS S3 Buckets

Steps Involved:

- ✅ Log into AWS Management console
- ✅ Choose region
- ✅ Navigate to the Amazon S3 console 
- (Amazon S3 buckets form a global namespace, even though each bucket is created in a specific region)

- ✅ Start the create bucket process
- ✅ Name your bucket
- ✅ Choose your region

# Upload object

- ✅ Load your new bucket in the Amazon S3 console
- ✅ Select Upload, then Add Files
- ✅ Start Upload. You will see the status of your file in the Transfers section

## Open the Amazon S3 URL

- ✅ Now open the properties for the object
- ✅ Copy the Amazon S3 URL for the object
- ✅ Paste the URL in the address bar of a new browser window or tab
- ✅ When you get an XML error code AccessDenied

## Make the Object Public

- ✅ Go back to the Amazon S3 Console and select Make Public

## Rename Object

- ✅ Rename the object, but keep the same file extension.

## Delete the Object

- ✅ Select Delete and Select OK when prompted if you want to delete the object
- ✅ To verify, try to reload the deleted object’s Amazon S3 URL (You should once again get the XML AccessDenied error message)

## Enable Version Control

- ✅ load the properties of your bucket. Don’t open the bucket.
- ✅ Enable versioning in the properties and select OK to verify
- (Note that versioning can be suspended, but not turned off.)

## Create Multiple Versions of an Object

- ✅ Create a text file with .txt extension on your computer and write what you want in the text file 
- ✅ Save the text file to a location of your choosing
- ✅ Upload the text file to your bucket. This will be version 1
- ✅ After you have uploaded the text file to your bucket, open the copy on your local computer and change the words
- Save the text file with the original filename

- ✅ Upload the modified file to your bucket
- ✅ Select Show Versions on the uploaded object
- You will now see two different versions of the object with different Version IDs and possibly different sizes

## Delete an Object and Then Restore It

- ✅ Open the bucket containing the text file with the two versions
- ✅ Select Hide Versions
- ✅ Select Delete, and then select OK to verify
- ✅ Your object will now be deleted, and you can no longer see the object
- ✅ Select Show Versions
- Both versions of the object now show their version IDs

## Restore an Object

- ✅ Open your bucket
- ✅ Select Show Versions
- ✅ Select the oldest version and download the object
- ✅ Upload to the same bucket
- ✅ Select Hide Versions, and the file should re-appear
- 
To restore a version, you copy the desired version into the same bucket. In the
Amazon S3 console, this requires a download then re-upload of the object. Using APIs, SDKs, or AWS CLI, you can copy a version directly without downloading and re- uploading.

## Lifecycle Management

- ✅ Select your bucket
- ✅ Under Properties, add a Lifecycle Rule
- ✅ Explore the various options to add lifecycle rules to objects in this bucket
- do not implement any of these options, as you may incur additional costs
- Most lifecycle rules require some number of days to expire before the transition
takes effect. For example, it takes a minimum of 30 days to transition from Amazon S3 Standard to Amazon S3 Standard-IA. This makes it impractical to create a lifecycle rule and see the actual result in an exercise

## Enable Static Hosting on Your Bucket

- ✅ Select your bucket
- ✅ In the Properties section, select Enable Website Hosting
- ✅ For the index document name, enter index.txt, and for the error document name, enter error.txt
- Use a text editor to create two text files and save them as index.txt and error.txt. In the index.txt file, write the phrase “Hello World,” and in the error.txt file, write thephrase“Error Page.”Save both text files and upload them to your bucket.

- ✅ Make the two objects public
- ✅ Copy the Endpoint: link under Static Website Hosting and paste it in a browser window or tab
- In the address bar in your browser, try adding a forward slash followed by a made- up filename 
- You should now see the phrase "Error Page" displayed.

- ✅ To clean up, delete all of the objects in your bucket and then delete the bucket itself 