## Make all objects publicly accessible

**Description**: This bucket policy makes every object in the bucket publicly accessible by their URLs. By using this policy, it's no longer necessary to upload objects with the `public-read` ACL.

```
_policy = dumps({
    'Version': '2012-10-17',
    'Statement': [{
        'Action': ['s3:GetObject'],
        'Effect': 'Allow',
        'Principal': '*',
        'Resource': 'arn:aws:s3:::YOURBUCKETHERE/*',
        'Sid': 'YOURSIDHERE'
    }]
})
```
