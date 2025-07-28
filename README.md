Welcome back code monkeys! In today's project we will be using AWS QuickSight and viewing large Date sets into a nice and easy to understand graph. Very simple lab for newcomers

What will we need?

[QuickSight](https://aws.amazon.com/quicksight/?nc2=type_a&amazon-quicksight-whats-new.sort-by=item.additionalFields.postDateTime&amazon-quicksight-whats-new.sort-order=desc)

[S3](https://aws.amazon.com/s3/?nc2=type_a)

[Any Large Dataset](https://aws.amazon.com/marketplace/solutions/data-analytics/data-sets)

[manifest.json](https://github.com/user-attachments/files/17592026/manifest.json)



How much will it Cost?

Most of this will use AWS free tier and should only invoke little to no cost. Feel free to use [AWS pricing calculator ](https://calculator.aws/#/)for more in-depth information.

S3 bucket cost 
![S3 bucket cost](https://github.com/user-attachments/assets/f55519f4-024b-4344-9bcc-a4f150adadbf)

![brave_screenshot_aws amazon com](https://github.com/user-attachments/assets/9575423d-a37d-4fd9-b759-9817b279a5a1)


What's the Architecture Design?

![diagram-export-9-13-2024-11_50_39-AM](https://github.com/user-attachments/assets/97acac7d-0369-481c-b79c-6dd1b64c9037)


Step 1- S3 Bucket
-Navigate to Amazon S3 
-Create a Bucket, keep all default settings
-Upload dateset to the newly created bucket
-Open the 'Manifest JSON" file from
-Replace bucket name with the newly created on

Example:
 {
  "fileLocations": [
    {
      "URIs": [
        **"s3://curykidprojects/Amazon-Bestseller-Dataset.csv**"
      ]
    }
  ],
  "globalUploadSettings": {
    "format": "CSV",
    "delimiter": ",",
    "textqualifier": "\"",
    "containsHeader": "true"
  }
}

-Upload the edit Json file to the bucket



Step 2- QuickSight
-Navigate to Amazon QuickSight and create an accout
- You will be able to start a free trial; be sure to cancel before 30 days to avoid overcharges
- Enter your information and email address
- Link your S3 bucket and hit finish; it will take a few minutes for account to be created
![Screenshot (40)](https://github.com/user-attachments/assets/38213bd9-1e28-4586-aacc-878cdbc5b63a)
![Screenshot (41)](https://github.com/user-attachments/assets/7d3586c8-af0d-465e-a228-e22b0540de37)

-Click "Go to Amazon QuickSight" to access the interface
-Click on dataset 
-Click on S3
-Return back to S3 bucket and click the "Copy S3 URL"
![Screenshot (42)](https://github.com/user-attachments/assets/31f8b8a0-a3da-4725-89b0-fbf31d6c879c)

-Return to QuickSight and paste the URL
![Screenshot (43)](https://github.com/user-attachments/assets/10c50023-a55a-480b-8a8a-a255756fc0b8)

-Click Visualize
-Click create for interactive sheet
-Drag filters from the Field List in order to create visualizations
![Screenshot (44)](https://github.com/user-attachments/assets/c44094f1-059b-4d4b-8641-4b4285d8d833)

-Try a variation of filters till your heart is content

![Screenshot (45)](https://github.com/user-attachments/assets/2dc9260e-5683-4212-8a97-1144239e98bb)


And we are done! Congrats on completing this short lab
