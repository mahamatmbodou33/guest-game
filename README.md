# Documentation of Guest-Game Project

![Screenshot 2025-02-14 193223](https://github.com/user-attachments/assets/28fcbf79-6900-4a46-a1ab-a9cffb1303b2)

# 📌 Introduction

Memory Match is a simple yet engaging card-matching game where players test their memory skills by flipping over two cards at a time. Each card contains a hidden image, and the goal is to find matching pairs. If the selected cards match, they are removed from the board; if not, they remain until a correct match is found. The game continues until all pairs have been successfully matched. Perfect for players of all ages, Memory Match enhances concentration and recall while providing fun and entertainment!

# STEP BY STEP TO IMPLEMENT THE PROJECT

## Once you are in my project repository click to where it says #fork on the top corner. This will allow you to copy the entire package to your repository. 


![Screenshot 2025-02-11 195614](https://github.com/user-attachments/assets/47aa9b41-fdea-4cd3-bca6-0917fde30810)

## The next step is to create an s3 bucket. Choose any name of the bucket, but must be a globally unique name.

![Screenshot 2025-02-11 200334](https://github.com/user-attachments/assets/de6f2cc5-2327-4f28-b71d-74e042247855)

## While creating the bucket make sure to uncheck Block all public access. This will allow all user to access to your bucket where the game resides.


![Screenshot 2025-02-11 200543](https://github.com/user-attachments/assets/7d710aa7-fb61-4fa0-8152-d897fd35c524)


## Then, scroll down and click Create Bucket.

![Screenshot 2025-02-11 200714](https://github.com/user-attachments/assets/810113db-73cc-4674-b2ea-5c69979e12dc)

## Click on View detail

![Screenshot 2025-02-11 200838](https://github.com/user-attachments/assets/a15fd498-b712-495f-9300-a65694568f34)
## Click Properties to make some change
![Screenshot 2025-02-11 201009](https://github.com/user-attachments/assets/a83e1601-3398-4399-a037-f071c247ed1d)

## Scroll down to the bottom Where it says Static website hosting and click on edit.

![Screenshot 2025-02-11 201116](https://github.com/user-attachments/assets/e5576cf2-ca7c-471e-98a2-c59fe6f00556)

## enable static website hosting. This will allow us to host our single-page static website.

![Screenshot 2025-02-11 201212](https://github.com/user-attachments/assets/2738c113-2af7-4ecd-9671-47f9bdd98212)

## Next, make sure to name the default page to index.html

![Screenshot 2025-02-11 201447](https://github.com/user-attachments/assets/4cfcd196-56c6-47bb-b4c2-aea75e6c1aa5)

## Then, click on Permissions to create a bucket policy

![Screenshot 2025-02-11 201548](https://github.com/user-attachments/assets/2ff124d2-be88-4137-a833-8564c5843330)

## Click on edit.

![Screenshot 2025-02-11 201813](https://github.com/user-attachments/assets/d56c2053-4463-4532-9239-31d22148efb4)

## Use this code for your bucket policy.  This allows everyone to read/view everything in the bucket.  Be sure to update the Bucket-Name.

{
    "Version": "2012-10-17",
    "Statement": [
    	{
        	"Sid": "PublicReadGetObject",
        	"Effect": "Allow",
        	"Principal": "*",
        	"Action": [
            	"s3:GetObject"
        	],
        	"Resource": [
                "arn:aws:s3:::Bucket-Name/*"
        	]
    	}
    ]
}


![Screenshot 2025-02-11 202031](https://github.com/user-attachments/assets/6b1f1975-93d8-4458-8540-637d35a402b9)

## Click on Save change


![Screenshot 2025-02-11 202700](https://github.com/user-attachments/assets/239509d1-e25a-4224-b8b2-08eba8b48ed1)

## Click on edit public access

![Screenshot 2025-02-11 205335](https://github.com/user-attachments/assets/ba9cc69d-d8c1-4078-8abc-16815b472173)

## Make sure all those settings are unchecked.

![Screenshot 2025-02-11 205424](https://github.com/user-attachments/assets/1f27c964-8c3d-4bda-ab6a-fbb19d3c1e6b)

## Now it's time to create a cope-pipeline to automate the deployment process. Open a new window, search for AWS CodePipeline, and click on Create Pipeline.

![Screenshot 2025-02-11 205647](https://github.com/user-attachments/assets/5cff04f6-80ba-42f2-9d64-5ee594dba37b)


## Select the second option Build a custom pipeline

![Screenshot 2025-02-11 205827](https://github.com/user-attachments/assets/6c067ee2-8dc5-4903-96bd-c9e87b8e5d69)
## Enter the pipeline name and leave everything with the default option and click next.
![Screenshot 2025-02-11 210057](https://github.com/user-attachments/assets/0fa4137f-df04-44cf-b6fd-8229a3ad6be7)

## Select GithHub as a source provider and connect to GitHub.
![Screenshot 2025-02-11 210402](https://github.com/user-attachments/assets/43dfad70-9563-4f7f-a8f6-dfbbf5e7a949)
## After writing the connection name, click on install a new app and it will take you to your GitHub repository to install the app and continue with the connection and make sure to authorize the connector to connect to your GitHub
![Screenshot 2025-02-11 210554](https://github.com/user-attachments/assets/846625fc-8dce-4e72-995c-9de1bad6280f)

![Screenshot 2025-02-11 210923](https://github.com/user-attachments/assets/ef168390-250d-4b10-bf34-60dc5e564ea1)

![Screenshot 2025-02-11 210757](https://github.com/user-attachments/assets/6e600c2d-a72f-4fa5-8b62-85f78d7bd815)

## You can just select the repository where your project resides and save it.
![Screenshot 2025-02-11 211642](https://github.com/user-attachments/assets/99886876-8299-437a-b7f4-2dd53552e009)
## If you select the correct GitHub of the project, it will pop up, and choose main as a default branch.
![Screenshot 2025-02-11 211945](https://github.com/user-attachments/assets/acea05fb-44fe-4ed3-b9a8-0e5b965fb1e1)

## These sections are optional, skip them.
![Screenshot 2025-02-11 212046](https://github.com/user-attachments/assets/5ba1bc23-26ff-41a2-90e5-924749094389)

![Screenshot 2025-02-11 212203](https://github.com/user-attachments/assets/79632fb8-8822-4c5a-8916-855c63dd4879)
## Select Amazon s3 as the deploy provider and choose the bucket. 
![Screenshot 2025-02-11 212441](https://github.com/user-attachments/assets/741cf534-c2f2-4fe4-8f23-6bd0f0ae4310)
## Click Next
![Screenshot 2025-02-11 212528](https://github.com/user-attachments/assets/c2a9d19d-8e73-40e6-b27b-76c1723ba255)
## Click on Create a pipeline
![Screenshot 2025-02-11 212631](https://github.com/user-attachments/assets/ab13b0ad-5fb3-491d-9ad8-8c775d684c6b)
## Pipeline was successfully created
![Screenshot 2025-02-11 212801](https://github.com/user-attachments/assets/5e22d2ca-8862-4a24-8195-a8932d8ba43b)

## Go to your s3 bucket click on the properties and scroll down toward the end and you will find the URL
![Screenshot 2025-02-11 213015](https://github.com/user-attachments/assets/baffe3a0-65ec-4808-a505-2f5b5a1debda)
![Screenshot 2025-02-11 213108](https://github.com/user-attachments/assets/e047f614-779e-4ae7-ae3e-563b3efff843)
## If you follow all the above steps correctly, you will be able to run the app successfully. 
![Screenshot 2025-02-11 213320](https://github.com/user-attachments/assets/96303468-b187-4ced-ae31-c15e7624d7f9)
![Screenshot 2025-02-11 213536](https://github.com/user-attachments/assets/fde72a8c-90d1-463f-b6ea-72a8b6d0d9f9)
## Game is successfully working. 


All services used are eligible for the [AWS Free Tier](https://aws.amazon.com/free/).  However, charges will incur at some point so it's recommended that you shut down resources after completing this tutorial.
