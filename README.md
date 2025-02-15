# Documentation of Guest-Game Project

![Screenshot 2025-02-14 193223](https://github.com/user-attachments/assets/28fcbf79-6900-4a46-a1ab-a9cffb1303b2)

# 📌 Introduction

Memory Match is a simple yet engaging card-matching game where players test their memory skills by flipping over two cards at a time. Each card contains a hidden image, and the goal is to find matching pairs. If the selected cards match, they are removed from the board; if not, they remain until a correct match is found. The game continues until all pairs have been successfully matched. Perfect for players of all ages, Memory Match enhances concentration and recall while providing fun and entertainment!

This repo contains the code files used in this [YouTube video](https://youtu.be/biYVW1TMYAU).

## TL;DR
Code for a game is hosted in GitHub.  We create an S3 bucket for static website hosting, then create a continuous deployment pipeline (using AWS Code Pipeline) to automatically deploy the code whenever changes are made.

## The Game
A simple memory matching game.  The user clicks two cards (images of memes) to try to match them.  If there's a match, the cards disappear from the board.  If there's no match, the cards are flipped back to their blank side so the user can try again.

The game consists of HTML, CSS and JavaScript.

Ideas for additional features:
- A scoring mechanism
- A timer
- Add additional cards
- Multi-player capabilities so you can compare scores 

## The Deployment Environment
The code will be deployed and hosted in S3.

## The Deployment Pipeline
The pipeline is created using AWS Code Pipeline.  The pipeline pulls the code from GitHub, and deploys it to S3 whenever a change is detected in the code.

## Cost
All services used are eligible for the [AWS Free Tier](https://aws.amazon.com/free/).  However, charges will incur at some point so it's recommended that you shut down resources after completing this tutorial.
