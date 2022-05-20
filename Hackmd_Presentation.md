---

title: Final Presentation
tags: presentation
slideOptions:
  theme: dark
  transition: 'fade'
  
---

<style type="text/css">

.reveal .slides {
    min-height: 100%;
    width: 100%;
    height: 96mm;
}
    
.reveal img, .reveal video, .reveal iframe {
    width: 100%;
    min-width: 100%;
    max-height: 100%;
}
  
html, .reveal {
    color: #CFC7BF;
}
 
ol, ul {
    font-size: 3rem; 
}

.reveal pre code {
    display: block;
    width:100%;
    line-height: 1.5em;
    border-radius: 0.9rem;
    font-size: 2rem;
    padding: 3rem;
    overflow: auto;
}


</style>


---

# Career Accelerator in Data Science
## [Northeastern University](https://www.northeastern.edu/)
Data Analysis of ProjectFunction

by Jacob Tessers

---

## Who I Am

- Originally from Southern California, I have lived in Utah for the past 17 years. 
- I am married with no children.
- Currently working full-time while finishing this program.
- I am an avid gamer, though I also enjoy movies and learning.
- I hope to establish myself as a data analyst and further my learning to become a data scientist at some point down the line.

---

![](https://i.imgur.com/QZoI2yn.jpg)



---


## Technical Abilities

- Some experience with Python before this course, which helped tremendously.
- Completed courses with DataCamp and Coursera.
- Salesforce, particularly Tableau
- SQL
- Github

---


## The Client

-  Daryl Cecile (software developer at Capital One) is one of the founders of Project Function.
-  Rizwana Khan is the other founder, but I didn't meet her.
- [Project Function](https://projectfunction.io/) has since 2018 taught over 95 sessions in Web Development, Design with Unity and general coding.
- User friendly to beginner and experienced tech learners. 
- Sessions are free of charge.
- Large focus on helping minorities succeed in tech.

---

## Coming up with Project Function

![](https://i.imgur.com/0EP4Osh.png)

---

### Project Goals

- Explore the activites on Project Function’s online platform.
- See if students using the online platform perform better overall.
- Recommend improvements on the ways data is recorded.
- Identify patterns in student behavior using a small data sample.

---

## Project Challenges

- Data came from a data warehouse and was messy.
- There were many irrelevant tables.
- There was duplicated data.
- Some data was incomplete.
- There was a lot of overall missing data as we were given a small sample.

---

##### Small Snapshot of Activity Log

![](https://i.imgur.com/HUnK7Ky.png)


---

## The Data

The data provided includes 89 users with hundreds of individual records for these students.

---

### Tech Stack

- Google Sheets - Data came in Excel format
- [Pandas](https://pandas.pydata.org/pandas-docs/stable/)
- [Seaborn](https://seaborn.pydata.org/)
- [Plotly](https://plotly.com/)
- [Matplotlib](https://matplotlib.org/)

---

### Data Journey

- Which tables from the google sheet were relevant?
- Download as .csv.
- Push to Deepnote to query the data.

---


### Data Cleaning

- Repetivtive steps
- Had to use duplicated and drop_duplicates methods a lot

<iframe title="Embedded cell output" src="https://embed.deepnote.com/229baaf3-d665-413f-81cc-b5ca6160d049/6dee76f1-37d5-4e2e-95f0-b53463d43763/2ddf998538d746deb38192a05eda0a78?height=371" height="371" width="800"/>

---

#### Dropping Unnecessary Columns

<iframe title="Embedded cell output" src="https://embed.deepnote.com/8d15e87d-b710-4fff-80ef-ff0e4cb338ff/57808016-6f53-43ea-beb0-100cfe12df57/9add9f616e244b88a6886e337e404eeb?height=83" height="83" width="500"/>

---

### Data Exploration

---



```python=
activity_log['activity'].unique()
```

---

![](https://i.imgur.com/l3nhFcp.png)

---

### Renaming the Activity Column

As there were many unique activites, with several very similar, I added a column to group activites by an Overview, e.g., "Accessed a Session" for all entries that related to accessing different sessions. here is a small sample of how I used `.apply()` to do that.

```python=
activity_log['activity'].apply(
    lambda x: "Accessed a Session" if "Session" in x else x)
```

---

#### Interactive Visualization

---


<iframe title="Embedded cell output" src="https://embed.deepnote.com/229baaf3-d665-413f-81cc-b5ca6160d049/6dee76f1-37d5-4e2e-95f0-b53463d43763/c2517b0e15eb477495d9d13b9e80073a?height=601" height="600" width="700"/>

---

<iframe title="Embedded cell output" src="https://embed.deepnote.com/229baaf3-d665-413f-81cc-b5ca6160d049/6dee76f1-37d5-4e2e-95f0-b53463d43763/5cc9e11279094aa9aadcb3830671b060?height=601" height="601" width="700"/>

---

<iframe title="Embedded cell output" src="https://embed.deepnote.com/229baaf3-d665-413f-81cc-b5ca6160d049/6dee76f1-37d5-4e2e-95f0-b53463d43763/b49b12e0cf434f5db8c3130fef04ab36?height=601" height="601" width="800"/>

---


<iframe title="Embedded cell output" src="https://embed.deepnote.com/8d15e87d-b710-4fff-80ef-ff0e4cb338ff/6dee76f1-37d5-4e2e-95f0-b53463d43763/6b20f04b3a0f4908abcc13018d07836f?height=668" height="668" width="500"/>

---


### Personalizing the Data

By further analysis and incorporation of users on the platform, I was able to see how much involvement a particular user had, distinguishing between Online and In-Person participation.

---

<iframe title="Embedded cell output" src="https://embed.deepnote.com/8d15e87d-b710-4fff-80ef-ff0e4cb338ff/57808016-6f53-43ea-beb0-100cfe12df57/acb8442a3e284cc2a124a8b7305f6a72?height=676" height="676" width="700"/>


---

### Conclusion

- Data in a format makes it much easier to understand. 
- We can see that while more learners happened to be online and while they did participate, in-person learners happened to overall participate more.
- Factors could include:
    Work schedules, 
    Life or Sickness,
    Fluctuation of Interest

---

### Suggestions

- Log out data as timestamps in Activity log.
- Enforce uniqueness contraints on assignment submissions to overwrite duplicate submissions.
- Larger dataset to explore individual student behaviors.

