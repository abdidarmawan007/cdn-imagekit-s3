## Real-time image optimization, resizing and Image CDN with Imagekit + S3
![alt text](https://i.imgur.com/KOS3WYv.jpg)

### Create user iam and roles, for roles make sure just get object only to spesific bucket (our asset static bucket)
![alt text](https://i.imgur.com/ReqoPVp.png)

### Add origin S3 bucket in Imagekit (bucketname,S3 key id and secret)
![alt text](https://i.imgur.com/KTYGrnt.png)

### Config for automated images optimize for format images and quelity and Chrome Mobile and Opera Mobile allow users to activate a data-saver mode
![alt text](https://i.imgur.com/GKY0a9w.png)

### Restrict images size based on users device
![alt text](https://i.imgur.com/WNL71Xw.png)

### auto remove images metadata and png compression
![alt text](https://i.imgur.com/XODOaQi.png)

### Test curl your images for check cache hit from pop
##### x-cache: Hit from cloudfront (hit from pop cloudfront)
##### x-amz-cf-pop: SIN52-C3 (hit cache from pop singapore)
```
curl -I https://ik.imagekit.io/3421i31n/catalog/a578c9ff0b6ec424853da33e73aef22d.png
```
```
HTTP/2 200 
content-type: image/png
x-server: ImageKit.io
cache-control: public, s-maxage=15552000, max-age=15552000, must-revalidate
x-cache: Hit from cloudfront
via: 1.1 4e3c79d06b4e17a0f3bc8206.cloudfront.net (CloudFront)
x-amz-cf-pop: SIN52-C3
x-amz-cf-id: EEPA9b2amQBM0mVJUoTCFCdHptDvfxRagEx6bzidiQ==
age: 11959
```
