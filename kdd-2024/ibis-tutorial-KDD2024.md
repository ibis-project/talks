# Descriptive Title 

We need a title here, in the past we had this options

- Scipy and PyCon 2024: Intro to Ibis: blazing fast analytics with DuckDB, Polars, Snowflake, and more,
from the comfort of your Python repl.
- PyData NYC 2023: Ibis - Expressive analytics in Python at any scale

I think we needs something more DS/ML/AI kind of thing. Here are some options I 
brainstormed with gpt and modified, but Im not convinced by anyone: 

- "Ibis: The Data Scientist's Powerhouse for Blazing-Fast Analytics and Machine Learning"
- "Mastering Data Analytics and ML with Ibis: Speed, Simplicity, and Scale"
- "Elevate Your Data Science Game with Ibis: Fast, Flexible, and Future-Proof"
- "Ibis: Your Gateway to Expressive Analytics and Streamlined ML"

# Abstract (300 words)

I tried to adapt what we had for SciPy and PyCon, and include something on Streaming 
and ML. Keep in mind that streaming and ML will be a small part of this tutorial, per 
Ian's suggestion 20%, please make suggestions with this in mind. 

**(I believe we are at 270 words now)**

Tabular data analysis, a staple in data science, often encounters scalability 
challenges with pandas. In response, modern analytical databases (like DuckDB) 
offer significant performance boosts but typically demand SQL expertise. Many of 
these systems only provide a SQL interface though; something far different from 
pandas’ dataframe interface, requiring a rewrite of your analysis code.

This is where Ibis comes in. Ibis is a pure-Python open-source library, originally 
created by Wes McKinney (creator of pandas), that provides a dataframe interface to
many popular databases and analytics tools (DuckDB, Polars, Snowflake, Spark, etc). This 
lets users analyze data using the same consistent API, regardless of which backend 
they’re using, and without ever having to learn SQL. This tutorial introduces 
Ibis, emphasizing its role in simplifying data manipulation across diverse platforms.

Additionally, attendees will explore Ibis' advancements in stream-batch unification. The 
Ibis-flink backend combines stream and batch into a single 
framework, addressing common barriers faced by data scientists venturing into 
streaming analytics. By leveraging Ibis unified Python dataframe API, we facilitate 
seamless transitions between batch and streaming workflows, reducing operational
complexities and enabling real-time machine learning applications.

Last but not least, this tutorial will also introduce IbisML, an evolving library 
for building machine learning pipelines using Ibis. IbisML brings the portability
of Ibis to ML pipelines -- preprocess your data on any of the 20+ backends that 
Ibis supports, then efficiently handoff to popular training libraries like
scikit-learn, XGBoost, or PyTorch

Attendees will learn that using Ibis for preprocessing, data transformation, and 
feature engineering allows seamless compilation of pipelines to SQL, enabling 
execution on diverse performant backends without the need for code rewriting 
during production deployment.

# Target audience and prerequisites for the tutorial (e.g. audience expertise)

The target audience for this hands-on tutorial is data scientists, data and machine
learning engineers, researchers, practitioners, and industry professionals who are 
already familiar with data analysis and data manipulation tools in Python. 

They may have encountered scalability challenges with some libraries like pandas 
and are interested in exploring alternative solutions to improve performance and
efficiency.

Additionally, individuals interested in data streaming technology and machine 
learning applications will find value in learning about Ibis' advancements in 
these areas. 

This is a hands-on tutorial, with numerous examples. Participants should ideally
have some experience using Python and dataframe libraries like pandas or polars,
but no SQL experience is necessary.

# Tutors (name, affiliation, email, address, phone)

Notes: 
- I'll collect the extra info separately given that this is a public repo. 
- For the in person tutorial I was thinking in Gil and I, at the moment. Not sure 
  what the budget will be, or the situation. We need at least 2 people to run a 3h 
  tutorial.
 
Naty Clementi
Gil Forsyth 

# Tutors’ short bio and expertise related to the tutorial (up to 200 words per tutor)

1. List of in-person presenters, i.e., tutors who will attend KDD and present 
   part of the tutorial

- Naty Clementi
- Gil Forsyth 
  

### Naty Clementi

**Bio**
Naty Clementi is a senior software engineer at Voltron Data, contributing to Ibis full time. She is a former academic with a Masters in Physics and PhD in Mechanical and Aerospace Engineering. She is also an active member of Pyladies and volunteers as one of the directors of Women Who Code in the Washington DC network. She is originally from Argentina, and speaks both Spanish and English fluently. 

**Expertise:** 
Naty Clementi is an experienced instructor and educator. She has presented tutorials at meetups and conferences such as SciPy, PyData NYC, PyData Seattle, PyCon US. She has also taught multiple Python courses to graduate and undergraduate engineering students at George Washington University. 

The most recent Ibis tutorial is the accepted Ibis tutorial at PyCon US 2024: 
[Tutorials: Introduction to Ibis: blazing fast analytics with DuckDB, Polars, Snowflake, and more, from the comfort of your Python repl.](https://us.pycon.org/2024/schedule/presentation/55/)


### Gil Forsyth

**Bio**
Gil Forsyth is a staff software engineer at Voltron Data. He followed the common career path of Japanese language specialist -> administrative assistant -> mechanical engineer -> computational fluid dynamicist -> data scientist -> software engineer -> machine learning engineer -> software engineer. Gil contributes to several projects in the PyData ecosystem and is a core maintainer of xonsh and Ibis.

**Expertise:** 
Gil Forsyth is an experienced instructor, having led tutorials at several PyData conferences, PyCon, and SciPy. He also ran internal training on Python and distributed data analysis at Capital One for several years. Gil is one of the core maintainers of Ibis.

The most recent Ibis tutorial is the accepted Ibis tutorial at PyCon US 2024: 
[Tutorials: Introduction to Ibis: blazing fast analytics with DuckDB, Polars, Snowflake, and more, from the comfort of your Python repl.](https://us.pycon.org/2024/schedule/presentation/55/)


2. List of contributors, i.e., tutors who will only help prepare the tutorial material

- I'm not sure who to put here, I will need designated responsible people for some 
  Ibis ML showcase and Ibis streaming (Chloe?)


# Corresponding tutor with her/his email address

- Naty Clementi (I'll add my email upon submission)

# Tutorial outline. Please provide as much detail as possible.

Here is where I need some help. I modify parts of the Scipy outline to include more about 
why Ibis, what is Ibis and for Who, I think this will let us introduce Ibis as part 
of a "composable data ecosystem" (also requested by Ian).  We need to include 
some streaming content and some ML content, again keep in mind that the ask is 
to introduce this as a 20% of total content.

## 0:00 - Intro and Setup “Going beyond pandas”

Get attendees up and running in a GitHub Codespace or on their laptops. A bit of
motivation about the kinds of problems where Ibis can help, and a general survey 
of attendees to find out what their existing pain points and experiences are.

## 0:15 - Introduction to Ibis basics

**Slides**
- What is Ibis?: Ibis as part of a composable data ecosystem.
- Why Ibis?: present the problems that Ibis tackles and the benefits of adopting it.
- Who Is Ibis for?: show how data engineers, data analysts, data scientists, and any data practitioner can benefit from Ibis

**Get familiarized with basics: **

A hands-on, follow-along notebook introducing the basic verbs of Ibis data 
analysis (select, filter, group_by, order_by, and aggregate), demonstrating a 
simple example on a few local query engines with hands-on exercises throughout.

## 1:00 - Coffee Break (5 minutes that definitely takes 10 minutes)

## 1:10 - In-memory tables, joins, and data analysis (need to adapt this for audience)

Building on the previous notebook, we'll explore how to join in-memory data (from 
a pandas DataFrame, Python dictionary, or PyArrow Table) with existing tables in 
a local database and continue analysis on the join result.

We'll explore chained joins, and demonstrate read_parquet and other read_* methods for loading local data into
existing databases. Then we'll continue with a series of hands-on exercises, 
building up an analysis pipeline for some IMDB ratings data, but only operating 
on a 5% sample of the original dataset. After, we show how the same expression 
can be computed on the full dataset without any code changes, both for local 
execution, or with bursting to a cloud database (or other hosted database).

## 1:50 - Coffee Break (5 minutes) + Q&A in the room

HERE IS WHERE WE NEED TO THINK HOW TO TIE THE PREVIOUS CONTENT WITH STREAMING AND ML 
WHAT WE HAVE IN THE SCIPY TUTORIAL IS 

## 2:10 - Selectors 
Continuing on from joins, we'll introduce selectors as a means of quickly 
renaming and cleaning datasets, a powerful feature ~stolen from~ inspired by dplyr.

# 3:00 - Coffee Break (5 minutes) + Q&A in the room

## HELP HERE MAYBE AN EXAMPLE THAT CAN SHOW STREAMING AND ML, OR TWO? IT'LL HAVE TO BE SMALL
I'M WORRIED ABOUT THINGS BEING DISCONNECTED

# 3:10 - PyPI data exploration and integration with the broader Python ecosystem 

Demonstate projection pushdown and column pruning when operating on remote datasets. Explore questions about PyPI maintainers, search for typo-squatters, and try to find explanations for outliers using data from https://py-code.org/datasets.

Feed Ibis expressions into common plotting tools to look for outliers and demonstrate interoperability.

(Note: depending on conference wifi, even with column pruning and parquet files this may be untenable. We have backup exercises that perform the same analysis but make use of either the Clickhouse Playground or a sponsored SnowFlake account, so only basic internet connectivity will be required. Bonus: using Ibis means shifting to these backup options is a one-line operation!)
3:30- Intro to geospatial workflows

Introduction to using Ibis geospatial with supported backends. Short hands-on exercises using NYC subway and bike-share data to try to find the fastest way to get a pizza from one borough to another.


# If the tutorial or a similar/highly related tutorial has been presented before (either by the same author(s) or by others): A list of forums, their event dates and locations, the number of participants, and the similarities/differences of prior tutorials to the one proposed for prior KDDs (up to 100 words for each entry)


**PyData NYC (short tutorial):**  

This was a short form of an Ibis hands on tutorial, that concentrates on the basics. It was a 90 min tutorial that covered an introduction and hands on example, but did not cover ibis streaming, or Ibis ML. 

- youtube recording link: [Ibis - Expressive analytics in Python at any scale | PyData NYC	2022](https://www.youtube.com/watch?v=XdZklxTbCEA)
- Number attendees: ~25-50
  
**PyCon US - Pittsburgh USA -coming May 2024:**

This is a 3h hands on tutorial that is targeted to a broader Python audience, that will go over Ibis capabilities, covering an introduction and extensive use of the Ibis API through hands-on examples. This tutorial will not showcase streaming and ML capabilities. 

- Link: [Tutorials: Introduction to Ibis: blazing fast analytics with DuckDB, Polars,	Snowflake, and more, from the comfort of your Python repl.](https://us.pycon.org/2024/schedule/presentation/55/)  
- Number attendees: Expected ~50-100 

# A list of up to 30 most important references that will be covered in the tutorial

- Ibis docs: https://ibis-project.org/
- Ibis repository: https://github.com/ibis-project/ibis
- Ibis blogs: https://ibis-project.org/posts
- Ibis tutorial PyData NYC 2023: https://github.com/ibis-project/ibis-tutorial
- The composable codex: https://voltrondata.com/codex
- Maybe other crucial libraries docs? 
- Any relevant papers? 

# Strategies that you plan to employ to encourage audience participation and interactivity throughout the tutorial presentation

Note: I adapted this based on my experience (and probably Gil's too) from Software
Carpentry, we used some of these in the past. 

To encourage audience participation and interactivity throughout the tutorial 
presentation, we will employ several strategies following the general practices 
use by [Software Carpentry](https://software-carpentry.org/), as well as other 
practices that the instructors have found useful. These strategies include:

- **Sticky Notes for Status Flags:** Each learner will be provided with two 
sticky notes of different colors, such as red and green. Learners can use these 
to discreetly indicate their status: green for completion or assistance needed, 
and red for encountering problems. This method allows learners to continue 
working while signaling for help, facilitating a smoother learning process for 
everyone.

- **Minute Cards for Feedback:** Before each break, learners will take a minute 
to write one positive aspect on a green sticky note and one area for improvement 
or question on a red sticky note. This anonymous feedback allows instructors to 
adjust the pace and content of the tutorial based on learners' needs and interests.

- **Pair Programming:** Pairing learners encourages collaborative problem-solving, 
clarification of concepts, and discussion of shared interests. Seating arrangements 
will facilitate pairing, with learners switching partners periodically to maximize
interaction and prevent anyone from feeling isolated.

- **Collaborative space to ask questions:** We will use the conference slack, or 
provide a channel for the students to ask questions in a written format while the 
tutorial is being performed. This lets us capture more questions, given that 
sometimes not everyone feels comfortable asking it out loud.

- **Peak Rule for Lesson Endings:** We will aim to end each lesson/section on a 
high note, leaving learners with a positive impression of the session. By focusing
on the most intense and final moments, we enhance the overall learning experience
and leave participants feeling motivated and satisfied.

- **One Up, One Down Feedback:** At the end of the day, learners will provide
alternating positive and negative feedback points about the day's session. This 
structured feedback encourages participants to express their honest opinions, 
helping instructors to address concerns effectively.




