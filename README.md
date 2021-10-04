# HackCMU2021

## Preamble

This project has been coded in the scope of the HackCMU 2021: http://hackcmu.org/. The HackCMU is a 1 day beginnerfriendly hackthon organized by the Carnegie Mellon University in Pittsburgh. Our team won the Sustainability Hack Challenge by Bloomberg. The code in this repository is functional, however as the model has been build in only one day, our model is not well tuned and has been trained. Our model is able to detect some litter in images similar to the trainings data, but especially for unseen data and unseen trash objects, the results are not very good. We might improve the model in the future, but no timeframe is set for this yet. 

## The Project

We trained a model to detect litter in images using Detectron2 https://github.com/facebookresearch/detectron2 and the TACO dataset https://github.com/pedropro/TACO. Our script can then read out the GPS location of the image. It reads out the location of all images in which litter has been detected and the number of litter in the image, and prints it out. The text can then be read in and presented on our heatmap, to visualize areas in which a lot of litter has been detected. 

## Team information
Team Name: Password1!
Philip Neugebauer, Hong Sng, Tyler Wilson, Allan Nguyen 
AndrewIDs: pneugeba, hongsng, tylerwil, allann

## Inspiration
We noticed that there was a lot of trash in our neighborhood and wondered if there was an efficient way to clean it all up.

## What it does
Our project uses existing bus camera footage to identify areas with a high density of litter. Once our AI identifies instances of litter in a location, we plot its coordinates and density in a Google Maps heatmap.

## How we built it
- We used TACO, an open image dataset of waste in the wild. It contains photos of litter taken under diverse environments, from tropical beaches to London streets. These images are manually labeled and segmented according to a hierarchical taxonomy to train and evaluate object detection algorithms. 
- We then used Detectron 2, an Open-Source PyTorch-based object detection library. We employed its  pretrained region-based convolutional neural network and retrained the model using TACO dataset to detect litter.
- Once the model was trained to identify litter in images, we fed it with street images to understand the density of litter in various areas in Pittsburgh. Then, we extracted GPS data from the images and visualized the density of litter on a heat map. The heat map was built using Google Maps' JavaScript API and hosted on Netlify. 

## Challenges we ran into
- It was difficult to install detectron2 on Windows (it was not officially supported for Windows)
- Issues uploading huge data sets to Google Drive and Collaboratory
- 3/4 members were having a hackathon for the first time
- Obtaining GPS data from photos

## Accomplishments that we're proud of
- We managed to successfully train our AI to detect litter in a short time frame
- We created a functional solution to our problem that can be used in other situations by other people
- Using a heatmap, we created an easily understandable visual representation of litter density
- We all started as strangers but we made a great team :)

## What we learned
- Our first time retraining a model on new data 
- Experience with Detectron2, Google Collaboratory, Google Maps API

## What's next for AI Trash Detection Heatmap
- We will publish our project as open-source on GitHub and add complete instructions on how to install and use it so that others can benefit from it
- We are interested in possible applications of our project with drones or robots, e.g. Drones or robots picking up trash with our AI.
