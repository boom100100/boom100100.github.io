---
layout: post
title:      "React Redux Final Project: The Research Helper Form Builder"
permalink:  research_helper_form_builder
---


Writing teachers are required to convince students to use reliable sources. But different teachers have different views on what is reliable. And, it is at the student's discretion to follow the advice of their instructors.

My Research Helper app brings these issues together to offer a solution that allows students to create research from a limited pool of sources. Search terms feed into two third-party APIs to deliver research from Wikipedia and a variety of sources that are more reliable. The user can then name a data point and write some paragraphs that explain how the research fits into the overall project. In other words, it's a way of constructing research papers around their data.

In addition to relying on APIs, the Chart.js library allows a user to add data they collected (presumably from their own experiment) and present it in a bar graph. The same space for naming and interpreting the data is available.

While many research papers are long enough to merit section titles, naming a section can be hard. Another third-party API allows searching for topic words that can contribute to a section title. Inputting a paragraph of text can return topic words, and the user can choose the most relevant topics and compose them into a section title. Just as the research paper, as a whole, is built around the data it contains, the section title is built around the content it will contain.

An uninspired student can find interesting topics by using another third-party API that is connected to the app. This API is a random data collector. In the context of the app, it helps a student find ideas about what to research. This is especially useful for a user that doesn't know where to begin.

The backend of the app is Ruby on Rails. Since the frontend is in HTML/CSS/JavaScript, CORS connects the backend to the frontend by allowing the headers to go through. Also, the frontend is built in React, so Redux and Thunk are necessary to separate the data from the app and allow persistence.

Next steps include allowing teachers to choose from a pool of research sources, instead of the developer choosing the sources. Also, the app only supports creating bar graphs, but it can utilize Chart.js more thoroughly by allowing plot charts, pie charts, and other diagrams.
