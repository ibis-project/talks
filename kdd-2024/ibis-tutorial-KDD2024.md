# Notes about submission process for hands on tutorial. 

- The proposal has to be submitted in the two column format paper
- The overleaf template to use is `sample-sigconf.tex` and can be found here in 
  this [link]( https://www.overleaf.com/latex/templates/acm-conference-proceedings-primary-article-template/wbvnghjbzwpc.) and for the
  bibliography you can modify the `.bib` file that is used at the end of the `.tex` 
  file in the bibliography section. 
- For this particular case, I modified the template name to `ibis-hands-on-tutorial-KDD.tex`
  and change sections to cover the 11 points required in Proposal section in 
  this [link](https://kdd2024.kdd.org/call-for-hands-on-tutorials/) for 2024 
  submissions, as well as created `ibis-tutorial.bib`.  
- The `.tex` template has two sections that are mainly for proceedings and right 
  according to the email exchange with the tutorial committee "The convention is 
  to leave them as is for submission time.  Indeed, the DOI is not defined until 
  camera-ready phase (post acceptance)". You can do your best at feeling in some
  blanks about the conference if you want. 


# Descriptive Title 

- "Ibis: The Data Scientist's Powerhouse for Blazing-Fast Analytics and Machine Learning"


# Abstract (300 words)

Tabular data analysis, a staple in data science, often encounters scalability 
challenges with pandas. In response, modern analytical databases (like DuckDB) 
offer significant performance boosts but typically demand SQL preference and
expertise. Many of these systems only provide a SQL interface though; something
far different from pandas’ dataframe interface, requiring a rewrite of your
analysis code.

This is where Ibis comes in. Ibis is a pure-Python open-source library,
originally created by Wes McKinney (creator of pandas), that provides a
dataframe interface to many popular databases and analytics tools (DuckDB,
Polars, Snowflake, Spark, etc). This lets users analyze data using the same
consistent API, regardless of which backend they’re using, and without ever
having to learn SQL. This tutorial introduces Ibis, emphasizing its role in
simplifying data manipulation across diverse platforms.

Additionally, attendees will explore Ibis' advancements in stream-batch unification. The 
Ibis-flink backend combines stream and batch into a single 
framework, addressing common barriers faced by data scientists venturing into 
streaming analytics. By leveraging Ibis' unified Python dataframe API, we facilitate 
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
 
- Naty Clementi
- Gil Forsyth
- Chloe He 

# Tutors’ short bio and expertise related to the tutorial (up to 200 words per tutor)

1. List of in-person presenters, i.e., tutors who will attend KDD and present 
   part of the tutorial

- Naty Clementi
- Gil Forsyth
- Chloe He  
  

### Naty Clementi

**Bio**
Naty Clementi is a senior software engineer at Voltron Data, contributing to
Ibis full time. She is a former academic with a Masters in Physics and PhD in
Mechanical and Aerospace Engineering. She is also an active member of Pyladies
and volunteers as one of the directors of Women Who Code in the Washington DC
network. She is originally from Argentina, and speaks both Spanish and English
fluently. 

**Expertise:** 
Naty Clementi is an experienced instructor and educator. She has presented
tutorials at meetups and conferences such as SciPy, PyData NYC, PyData Seattle,
PyCon US. She has also taught multiple Python courses to graduate and
undergraduate engineering students at George Washington University. 

The most recent Ibis tutorial is the accepted Ibis tutorial at PyCon US 2024: 
[Tutorials: Introduction to Ibis: blazing fast analytics with DuckDB, Polars, Snowflake, and more, from the comfort of your Python repl.](https://us.pycon.org/2024/schedule/presentation/55/)


### Gil Forsyth

**Bio**
Gil Forsyth is a staff software engineer at Voltron Data. He followed the common
career path of Japanese language specialist -> administrative assistant ->
mechanical engineer -> computational fluid dynamicist -> data scientist ->
software engineer -> machine learning engineer -> software engineer. Gil
contributes to several projects in the PyData ecosystem and is a core maintainer
of xonsh and Ibis.

**Expertise:** Gil Forsyth is an experienced instructor, having led tutorials at
several PyData conferences, PyCon, and SciPy. He also ran internal training on
Python and distributed data analysis at Capital One for several years. Gil is
one of the core maintainers of Ibis.

The most recent Ibis tutorial is the accepted Ibis tutorial at PyCon US 2024: 
[Tutorials: Introduction to Ibis: blazing fast analytics with DuckDB, Polars, Snowflake, and more, from the comfort of your Python repl.](https://us.pycon.org/2024/schedule/presentation/55/)


### Chloe He

**Bio**
Chloe has a background in data science and started working on streaming systems
when she was a Founding Engineer at Claypot AI, a startup tackling challenges in
real-time machine learning. She led the infrastructure development of an
open-source real-time feature engineering platform and worked on the translating
and optimizing streaming workloads that served low-latency use cases. Later, she
brought her streaming expertise to Voltron Data, where she now leads the
development of Ibis streaming.

**Expertise:**
Chloe has presented talks and workshops across a number of conferences, such as
DataConnect, NVIDIA GTC, and Google DevFest. She also taught lectures for the
Machine Learning System Design course at Stanford and a crash course on
recommendation systems.


2. List of contributors, i.e., tutors who will only help prepare the tutorial material

- Cody Peterson
- Deepyaman Datta


# Corresponding tutor with her/his email address

- Naty Clementi 

# Tutorial outline. Please provide as much detail as possible.

## Intro and Setup “Going beyond pandas”

Get attendees up and running in a GitHub Codespace or on their laptops. A bit of
motivation about the kinds of problems where Ibis can help, and a general survey 
of attendees to find out what their existing pain points and experiences are.

## Introduction to Ibis basics

**Slides**
- What is Ibis?: Ibis as part of a composable data ecosystem.
- Why Ibis?: present the problems that Ibis tackles and the benefits of adopting it.
- Who Is Ibis for?: show how data engineers, data analysts, data scientists, and
  any data practitioner can benefit from Ibis

**Get familiarized with basics:**

A hands-on, follow-along notebook introducing the basic verbs of Ibis data 
analysis (select, filter, group_by, order_by, and aggregate), demonstrating a 
simple example on a few local query engines with hands-on exercises throughout.

## In-memory tables, joins, and data analysis

Building on the previous notebook, we'll explore how to join in-memory data (from 
a pandas DataFrame, polars DataFrame, Python dictionary, or PyArrow Table) with
existing tables in  a local database and continue analysis on the join result.

We'll explore chained joins, and demonstrate `read_parquet` and other `read_*` methods
for loading local data into existing databases. Then we'll continue with a series 
of hands-on exercises, building up an analysis pipeline for some IMDB ratings data,
but only operating on a 5% sample of the original dataset. After, we show how the 
same expression can be computed on the full dataset without any code changes, both 
for local execution, or with bursting to a cloud database (or other hosted database).

## Streaming 

We'll build on our previous batch analysis example and turn what we've learned
towards a similar problem, but now with a real-time and constantly updating data
source. 

With hands-on exercises, we'll explore how to set up rudimentary anomaly
detection, and demonstrate how to window and group streaming data-sources before
redirecting them to downstream sinks.

## IbisML

We will demonstrate how to define machine learning features, create data
transformation pipelines, and execute them across backends using IbisML. We will
then use these features to train an ML model

## Closing remarks. 


# If the tutorial or a similar/highly related tutorial has been presented before (either by the same author(s) or by others): A list of forums, their event dates and locations, the number of participants, and the similarities/differences of prior tutorials to the one proposed for prior KDDs (up to 100 words for each entry)


**PyData NYC (short tutorial):**  

This was a short form of an Ibis hands on tutorial, that concentrates on the
basics. It was a 90 min tutorial that covered an introduction and hands on
example, but did not cover ibis streaming, or Ibis ML. 

- Content in Github repository: [Ibis Tutorial PyData NYC 2023](https://github.com/ibis-project/ibis-tutorial)
- youtube recording link: [ Ibis: A fast, flexible, and portable tool for data analytics](https://www.youtube.com/watch?v=TyopbrmlZx8)
- Number attendees: ~25-50
  
**PyCon US - Pittsburgh USA -coming May 2024:**

This is a 3h hands on tutorial that is targeted to a broader Python audience,
that will go over Ibis capabilities, covering an introduction and extensive use
of the Ibis API through hands-on examples. This tutorial will not showcase
streaming and ML capabilities. 

- Link: [Tutorials: Introduction to Ibis: blazing fast analytics with DuckDB, Polars,	Snowflake, and more, from the comfort of your Python repl.](https://us.pycon.org/2024/schedule/presentation/55/)  
- Number attendees: Expected ~50-100 

# A list of up to 30 most important references that will be covered in the tutorial

- Ibis docs: https://ibis-project.org/
- Ibis repository: https://github.com/ibis-project/ibis
- Ibis blogs: https://ibis-project.org/posts
- Ibis tutorial PyData NYC 2023: https://github.com/ibis-project/ibis-tutorial
- The composable codex: https://voltrondata.com/codex
- Welcome to the Tidyverse: https://joss.theoj.org/papers/10.21105/joss.01686
- The Composable Data Management System Manifesto: https://www.vldb.org/pvldb/vol16/p2679-pedreira.pdf


# Strategies that you plan to employ to encourage audience participation and interactivity throughout the tutorial presentation


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


# A brief discussion of the potential societal impacts of your tutorial

Ibis and therefore this tutorial encapsulate several significant societal impacts, 
particularly in enhancing developer efficiency and optimizing resources.

**Saving Developer Time:** Ibis reduces time spent on database and code migrations 
by providing a consistent API across various backends, allowing developers to 
focus on innovation and product quality.

**Promoting Standardization:** With a unified Python dataframe API, Ibis fosters 
interoperability and collaboration, leading to more efficient workflows and knowledge
sharing.

**Facilitating Access to Advanced Analytics:** By simplifying backend complexities
and offering a familiar Python interface, Ibis lowers barriers for data scientists 
and researchers to leverage advanced analytics techniques and foster innovation. 
