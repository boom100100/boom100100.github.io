---
layout: post
title:      "Rails Final Project: The Online Learning Platform"
permalink:  online_learning_platform
published: false
---

Online learning has a lot to offer. Teachers need a way of organizing and delivering their content, and students need to access their teachers' resources and track their progress. Organizing and tracking progress for content via a website is a simple way to centralize learning.

As a final project, creating a digital learning management system was a choice with many preexisting examples like Flatiron School, Lynda, Udemy, and Coursera to imitate. Ultimately, the task became choosing the essential features from the many.

The overall structure of the site has two main components: courses and users. Teachers create and control courses. Courses are containers for lessons, so those are also under the control of teachers. Categories, however, are tags that belong to lessons. Teachers can create them, but can't delete them.

Students can associate themselves with courses and mark their progress in each course and lesson.

The user models also include admins. Other than having full control, the admins are different in that they aren't allowed to access the site as other user models are allowed to. An admin that already exists must create another admin, so there is no sign up flow for admins. Similarly, admins are not allowed to use the GitHub sign in flow, since that doubles as a way of signing up.

Next steps include creating a ticket flow for technical issues and a comments flow for academic issues so that there can be clear documentation.

