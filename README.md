<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Host a Website on Amazon S3

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-host-a-website-on-s3)

**Author:** saqibh49@gmail.com  
**Email:** saqibh49@gmail.com

---

![Image](http://learn.nextwork.org/grateful_white_lucky_bat/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Introducing Today's Project!

### Project overview

In this project, I will demonstrate my ability to host a website on AWS S3. I'm doing this project to learn about some of the capabilities that come with AWS and how I can make use of them with just a bit of knowledge

### Tools and concepts

Services I used were AWS S3. Key concepts I learnt include how to create a bucket in S3, how to make it public, what goes into a bucket to create the actual site and how to set specific rules for who can edit what within my bucket.

### Time, challenges, and wins

This project took me approximately 1 hour to complete The most challenging part was finding little things, but just by exploring the platform, I was able to figure everything out. It was most rewarding to see the final product working like it should, from the actual website to the error when I tried deleting the index.html file.

---

## How I Set Up an S3 Bucket

### What I did in this step

In this step, I will open up S3 and create a bucket because this is where I will be storing all my website files

### How long it took to create the bucket

Creating an S3 bucket took me 2-3 minutes

### Region selection

The Region I picked for my S3 bucket was United States (Ohio) because thats the closest to me.

### Understanding bucket name uniqueness

S3 bucket names are globally unique! This means no other s3 bucket can be named the same as mine

![Image](http://learn.nextwork.org/grateful_white_lucky_bat/uploads/aws-host-a-website-on-s3_ba6d42ad)

---

## Upload Website Files to S3

### What I did in this step

In this step, I will add all my website files to my bucket because thats what my website is made of in the first place. 

### Files I uploaded

I uploaded two files to my S3 bucket - they were index.html and a folder called NextWork - Everyone should be in a job they love_files

### How the files work together

Both files are necessary for this project as index.html is the actual text and basic fomatting of the site and the folder contains all the creatives for the website including css and js instructions for making the website interactive. 

![Image](http://learn.nextwork.org/grateful_white_lucky_bat/uploads/aws-host-a-website-on-s3_a265af88)

---

## Static Website Hosting on S3

### What I did in this step

In this step, I will set up the website so it's visible publicly and get the link to view it because if we don't publish the website, what's the point in having it

### Understanding website hosting

Website hosting means essentially making a website public. By hosting it, it makes it visible to the internet.  

### How I enabled website hosting

To enable website hosting with my S3 bucket, I went to my bucket under S3, selected properties, scrolled down and hit Edit on the Hosting block. Then I selected Enable under the Static website hosting section.

### Access Control Lists (ACLs)

An ACL is a way of controlling who can control items within my bucket. I enabled it to allow me to be able to control every aspect of my bucket

![Image](http://learn.nextwork.org/grateful_white_lucky_bat/uploads/aws-host-a-website-on-s3_c22c54c0)

---

## Bucket Endpoints

### Understanding bucket endpoint URLs

Once static website is enabled, S3 produces a bucket endpoint URL, which is how the internet accesses my website.

### What I saw when I tested the endpoint

When I first visited the bucket endpoint URL, I saw a 403 Forbidden error message. The reason for this error was because the contents of my bucket are private, so even though I have a public bucket, none of the content in public.

![Image](http://learn.nextwork.org/grateful_white_lucky_bat/uploads/aws-host-a-website-on-s3_22ce4daf)

---

## Success!

### What I did in this step

In this step, I will make my website contents within my ucket publicly accessible because that is the only way my website will be visible publicly.

### How I resolved the 403 error

To resolve this 403 Forbidden error, I made both the index.html and the folder I uploaded publicly accessible using ACL. This was found under the actions tab when I clicked on each file.

![Image](http://learn.nextwork.org/grateful_white_lucky_bat/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Bucket Policies

### What I did in this extension

In this project extension I'm about to set up a bucket policy to prevent people from deleting my bucket. I'm doing this so that when I create an actual site in the future, my work isn't at risk of being deleted by anyone with a bit of AWS knowledge. 

### Understanding bucket policies

An alternative to ACLs are bucket policies, which are a more granular way of controlling who can edit, access, and delete items in my bucket. The benefit of using bucket policies is much more control over what I want edited and not, while ACLs are useful for overall settings regarding editing and deleting bucket objects. 

![Image](http://learn.nextwork.org/grateful_white_lucky_bat/uploads/aws-host-a-website-on-s3_sm2sm2sm)

### What my bucket policy does

My bucket policy puts specific permissions on items in my bucket allowing or blocking anyone I decide from deleting or editing the item. I tested this by trying to delete my website's index.html file and saw an error informing me that AWS failed to delete it. This error is caused by my policy from earlier.

---

---
