
## Purpose
Better understand the benefits of using a content delivery network like AWS Cloudfront when a web application is experiency latency due to a spike in end users trying to access the application.

## Issues
There was a sudden influx of users trying to access our URL Shortner web application in a short amount of time and they were experiencing issues with load times. The latency users were experiencing was at 40 ms.

## System Design
![AWS](screenshots/Screenshot%202023-09-29%20at%203.49.15%20PM.png)

## Optimization
The web application did not have a content delivery network initially, using one will help significantly with remediating our latency issues. Adding a CDN like Cloudfront will deliver a faster website to our users due to its ability to access the static content that is stored in our s3 bucket. Cloudfront will route requests through the closest edge location of the end user. After adding a CDN the load time of the web application went down to 10ms.