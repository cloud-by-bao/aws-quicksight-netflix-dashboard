<<<<<<< HEAD
<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Visualize data with QuickSight

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-analytics-quicksight)

**Author:** Bao Luong  
**Email:** baodevops21@gmail.com

---

![Image](http://learn.nextwork.org/stimulated_brown_festive_kaffir_lime/uploads/aws-analytics-quicksight_6c7f7ef0)

---

## Introducing Today's Project!

In this project, I will demonstrate how to use amazon QuickSight to analayze huge dataset of Netflix and generate visualizations and insights. I'm doing this project to learn how to use cloud data sertices for data analysis.

### Tools and concepts

Services I used were S3 and QuickSight... Key concepts I learnt include maifest.json files, data visualization techniques (e.g. charts, filters) and how to perform a data refresh in QuickSight. 

### Project reflection

This project took me approximately about 1-1.5 hours. The most challenging part was understanding how a manifest.json works. It was most rewarding to create and generate Netflix raw data into a dashboard that gives better insights and visualization of the data. 

After this project, I plan to work on Cloud Security with IAM on AWS. I will start this project on very soon.

---

## Upload project files into S3

S3 is used in this project to store two files, which are manifest.json (which is a text file that uses a specific format for storing and transmitting data for QuickSight) and netflix_files.csv (which is the raw data that are being analyzed today). 

I edited the manifest.json file by updating the S3 URI that corresponds to our dataset's file location. It’s important to edit this file because it is how QuickSight will find and analyze the data. If I didn't update the file then QuickSight will not be able to find the location of our  dataset and will cause erorrs.  

![Image](http://learn.nextwork.org/stimulated_brown_festive_kaffir_lime/uploads/aws-analytics-quicksight_3c3cd85a)

---

## Create QuickSight account

Creating a QuickSight account cost $0 as it comes with a free trial of 30 days. Important step to do is to uncheck the add-on in the sign up called Pixel-Perfect Reports, so you do not get charged. 

Creating an account took me about 4-5 mins, including setting up the S3 permission. 

![Image](http://learn.nextwork.org/stimulated_brown_festive_kaffir_lime/uploads/aws-analytics-quicksight_f4ab4214)

---

## Download the Dataset

I connected the S3 bucket to QuickSight by visiting the Datasets page. There were many options for data sources available, but for this project I chose S3. 

The manifest.json file was important in this step because it provides QuickSight how to read the data - in this project, it tells QuickSight that we're uploading .CSV file (spreadsheet) and the delimiter (i.e. commas) so that QuickSight knows how to break up the data for analysis. 

![Image](http://learn.nextwork.org/stimulated_brown_festive_kaffir_lime/uploads/aws-analytics-quicksight_6f874996)

---

## My first visualization

To create visualizations on QuickSight, I clicked on data field/labels e.g. Release_year and QuickSight will automatically a graph that best visualize the data. I can drag the data labels into sections like "Group By" or "Y-Axis" to determine how our graphic should display our data. 

The chart/graph shown here is a breakdown of the release years of the content inside Netflix - i.e. how many TV shows/movies were released on xyz year? You can see that there is a total of 8800+ content pieces, and 2019 with the most content released, 

I created this graph by dragging and dropping the release_year lable into the Y-Axis and changing the bar chart to donut chart. 

![Image](http://learn.nextwork.org/stimulated_brown_festive_kaffir_lime/uploads/aws-analytics-quicksight_aff3aad7)

---

## Using filters

Filters are useful for narrowing down our data to the subset that we want to focus on, and in this case I used the filters to narrow down content with a release date of 2015 and beyond. 

This visualization is a breakdown of tv shows/movies that belong in one of the three categories -action and adventure, tv comedies, and thrillers. Here, I added a filter by "listed on" data label i.e. only these three categories could pass the filter. 

![Image](http://learn.nextwork.org/stimulated_brown_festive_kaffir_lime/uploads/aws-analytics-quicksight_c32248c5)

---

## Setting up a dashboard

As a finishing touch, I updated titles of the charts in our dashboard for better readibility and communicate the purpose of the chart clearer than the default titles. 

Did you know you could export your dashboard as PDFs too? I did this by selecting Publish and then "Generate PDF" on the top right of QuickSight analysis. 

![Image](http://learn.nextwork.org/stimulated_brown_festive_kaffir_lime/uploads/aws-analytics-quicksight_6c7f7ef0)

---

## Refreshing source data

In this project's extension, I downloaded fresh data that's different from my original dataset because it has missing country data. Analyzing incomplete data brings the risk of generating inaccurate insights, which leads to the wrong business decisions that can cause the company time and money. 

Once I downloaded new data, I had to update my S3 bucket because it is still storing the previous version of the data. I also uploaded a new manifest.json file that points to the new updated dataset/csv file. This ensures that QuickSight will pull in the new version of the data and not the previous data with the missing country data. 

I initally couldn't see my updated data in QuickSight, so I had to visit the dataset page and peform a full refresh of our data

![Image](http://learn.nextwork.org/stimulated_brown_festive_kaffir_lime/uploads/aws-analytics-quicksight_86415f4e3)

---

---
=======
<p align="center">
  <img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />
</p>

# 📊 Visualizing Netflix Data with AWS QuickSight

**🔗 Project Link:** [View on NextWork](http://learn.nextwork.org/projects/aws-analytics-quicksight)  
**👤 Author:** Bao Luong  
**📧 Email:** baodevops21@gmail.com

---

## 📝 Project Overview

In this project, I demonstrate how to analyze a large Netflix dataset using **Amazon QuickSight**. This end-to-end walkthrough covers using **Amazon S3 to store data**, configuring a `manifest.json`, and generating powerful **interactive dashboards** with QuickSight.

---

## 🧰 Tools & Concepts

- **AWS Services:** S3, QuickSight
- **Key Concepts:** `manifest.json`, data filters, data visualizations (charts, graphs), dataset refresh, S3 permissions

---

## ⏱ Time Spent

- Approx. 1–1.5 hours
- Biggest challenge: Understanding how `manifest.json` connects to S3
- Most rewarding: Seeing Netflix raw CSV data turned into interactive charts

---

## 🪣 Upload Project Files to S3

- Uploaded:
  - `netflix_files.csv` – raw dataset
  - `manifest.json` – specifies file format, structure, and location
- Edited the `S3Uri` inside the manifest to ensure QuickSight could locate the dataset

---

## 🧾 Creating a QuickSight Account

- Free 30-day trial — make sure to **uncheck "Pixel-Perfect Reports"** to avoid charges.
- Took 4–5 minutes including permissions setup.

---

## 🔗 Connecting QuickSight to S3

- From the **Datasets** page in QuickSight, chose **S3** as the source.
- Used the `manifest.json` to configure:
  - Data format (`.csv`)
  - Delimiters (`commas`)
  - File structure

---

## 📈 First Visualization

- Used `release_year` to create a chart showing how many shows/movies were released by year.
- Changed the chart type to **donut** for better readability.

---

## 🎛 Using Filters

- Applied a filter to show data from **2015 and beyond**.
- Limited results to 3 categories: *Action & Adventure*, *TV Comedies*, and *Thrillers*.

---

## 📊 Setting Up a Dashboard

- Customized chart titles for clarity
- Published dashboard and exported it as a PDF using **Generate PDF**

---

## 🔁 Refreshing Source Data

- Replaced original CSV with one that included country data
- Updated both the S3 file and `manifest.json`
- Performed a full refresh in QuickSight to reflect updated data

---

## 🗂 Project Structure

```
aws-quicksight-netflix-dashboard/
├── manifest.json
├── netflix_files.csv
├── README.md
└── screenshots/ (optional if self-hosting images)
```

---

## ✅ Final Thoughts

> “This project helped me understand how AWS data tools work in real time. Visualizing insights from a raw dataset gave me confidence in using cloud-native tools like QuickSight.”

---

## 📌 Related Links

- [Amazon QuickSight](https://aws.amazon.com/quicksight/)
- [AWS S3 Docs](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html)

---

## ⭐️ Like This Project?

If you found this helpful, give this repo a ⭐ and connect with me on [LinkedIn](https://www.linkedin.com/in/bluong21/)!
>>>>>>> e3e95c6 (Initial commit: QuickSight Netflix dashboard project)
