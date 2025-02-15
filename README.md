# Documentation of Guest-Game Project

![Screenshot 2025-02-14 193223](https://github.com/user-attachments/assets/28fcbf79-6900-4a46-a1ab-a9cffb1303b2)

# 📌 Introduction

Memory Match is a simple yet engaging card-matching game where players test their memory skills by flipping over two cards at a time. Each card contains a hidden image, and the goal is to find matching pairs. If the selected cards match, they are removed from the board; if not, they remain until a correct match is found. The game continues until all pairs have been successfully matched. Perfect for players of all ages, Memory Match enhances concentration and recall while providing fun and entertainment!

# STEP BY STEP TO IMPLEMENT THE PROJECT

Once you are in my project repository click to where it says #fork on the top corner. This will allow you to copy the entire package to your repository. 


![Screenshot 2025-02-11 195614](https://github.com/user-attachments/assets/47aa9b41-fdea-4cd3-bca6-0917fde30810)

The next step is to create an s3 bucket. Choose any name of the bucket, but must be a globally unique name.

![Screenshot 2025-02-11 200334](https://github.com/user-attachments/assets/de6f2cc5-2327-4f28-b71d-74e042247855)

While creating the bucket make sure to uncheck Block all public access. This will allow all user to access to your bucket where the game resides.


![Screenshot 2025-02-11 200543](https://github.com/user-attachments/assets/7d710aa7-fb61-4fa0-8152-d897fd35c524)


Then, scroll down and click Create Bucket.

![Screenshot 2025-02-11 200714](https://github.com/user-attachments/assets/810113db-73cc-4674-b2ea-5c69979e12dc)

Click on View detail

![Screenshot 2025-02-11 200838](https://github.com/user-attachments/assets/a15fd498-b712-495f-9300-a65694568f34)

click Properties to make some change

![Screenshot 2025-02-11 201009](https://github.com/user-attachments/assets/a83e1601-3398-4399-a037-f071c247ed1d)

Scroll down to the bottom Where it says Static website hosting and click on edit.

![Screenshot 2025-02-11 201116](https://github.com/user-attachments/assets/e5576cf2-ca7c-471e-98a2-c59fe6f00556)

Enable static website hosting. This will allow us to host our single-page static website.

![Screenshot 2025-02-11 201212](https://github.com/user-attachments/assets/2738c113-2af7-4ecd-9671-47f9bdd98212)

Next, make sure to name the default page to index.html

![Screenshot 2025-02-11 201447](https://github.com/user-attachments/assets/4cfcd196-56c6-47bb-b4c2-aea75e6c1aa5)

Then, click on Permissions to create a bucket policy

![Screenshot 2025-02-11 201548](https://github.com/user-attachments/assets/2ff124d2-be88-4137-a833-8564c5843330)

Click on edit.

![Screenshot 2025-02-11 201813](https://github.com/user-attachments/assets/d56c2053-4463-4532-9239-31d22148efb4)


All services used are eligible for the [AWS Free Tier](https://aws.amazon.com/free/).  However, charges will incur at some point so it's recommended that you shut down resources after completing this tutorial.
