### HOSTING A STATIC WEBSITE ON AMAZON S3
## 1. Create a bucket
- Log in to the AWS management console.\
**Confirm the desired region is selected at the top right. The bucket will be hosted in the specified region.**
- Access Amazon S3 from the service menu on the top left of the console.
- Create a bucket and give it a globally unique name.
## 2. Upload website content to your bucket
- Upload html, css and other necessary files to the S3 bucket.\
![Uploaded html and CSS files.](screenshots/objects.png)
## 3. Configure a static website on Amazon S3
- Under **Properties** tab of the S3 bucket, navigate to **Static Website Hosting** and click **edit**. Note that the feature is *disabled*.\
![Static website hosting disabled.](screenshots/static-website-hosting-disabled.png)
- Enable and specify the home page of the website(this is compulsory).\
![Static website hosting editing](screenshots/edit-static-website-hosting.png)
- An endpoint URL now appears in the **Static Website Hosting** panel.
![Static website hosting enabled](screenshots/static-website-hosting-enabled.png)\
- Testing this URL on a browser, an error displays.\
![403 Error](screenshots/403-forbidden-error.png)
## 4. Allow public access to the website.
- Enable public access in the bucket settings: Under the **Permissions** tab of the S3 bucket, turn off the *block all public access* setting.![*Block public access* turned off](screenshots/block-public-access-off.png)\
Refresh the website. The error is still there.
- Attach a bucket policy that allows public read access.
The policy only allows users to view the website pages. ![Bucket policy](screenshots/bucket-policy.png)\
The website now displays successfully. ![Successfull webpage](screenshots/website-success.png)
