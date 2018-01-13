# AWS ASSOCIATED NOTES

## CloudFront

- A **_Content Delivery Network (CDN)_** is a system of distributed servers (network) that deliver webpages and other web content to a user based on the geographic locations of the user, the origin of the webpage and a content delivery server.

- **_Amazon CloudFront_** can be used to deliver your entire website, including dynamic, static, streaming, and interactive content using a global network of edge locations. Requests for your content are automatically routes to the nearest edge location, so content is delivered with the best possible performance.

### Main Features

- Optimized to work with other AWS, like S3, EC2, ELB, Route 53.
- CloudFront also works seamlessly with any **_non-AWS origin server_**, which stores the original, definitive versions of your files.


### Main concepts

- **Edge Location**: This is the location where content will be cached. This is separate to an AWS Region/AZ.

- **Origin**: This is the origin of all the files that the CDN will distribute. This can be either an S3 Bucket, an EC2 Instance, an Elastic Load Balancer or Route53.

- **Distribution**: This is the name given the CDN which consist of a collection of Edge locations:
  - **Web Distribution**: typically for Websites.
  - **RTMP**: Used for video streaming.

### Exam notes

- **Edge Locations are not just READ only**, you can write to them too (ie put an object on to them).
- **Objects** are **cached** for the life of the **TTL**.
- You can **clear cached object**, but you will be **charged**.
