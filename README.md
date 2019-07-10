# Immersion Day Website Template

### To use this template:
1. Modify 'index.html' to add the Immersion Day Name and Agenda content 

2. Download this repo to an Amazon S3 bucket

3. If you're adding in links to file downloads, you must update the S3 bucket CORS configuration using the following code:
```
<?xml version="1.0" encoding="UTF-8"?>
<CORSConfiguration xmlns="http://s3.amazonaws.com/doc/2006-03-01/">
<CORSRule>
    <AllowedOrigin>*</AllowedOrigin>
    <AllowedMethod>GET</AllowedMethod>
    <MaxAgeSeconds>3000</MaxAgeSeconds>
    <AllowedHeader>Content-Type</AllowedHeader>
</CORSRule>
</CORSConfiguration>
```

4. Set up an Amazon Cloudfront Distribution to connect to the S3 bucket and serve it in a secure manner. Remember to select *Restrict Bucket Access* and *Create New Origin Access Identity*
