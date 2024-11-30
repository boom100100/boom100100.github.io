---
layout: post
title:      "The Big Picture: A Brief Curriculum Explainer"
permalink:  brief_curriculum_explainer
---


A very short description of the software development curriculum is that students learn how to write programs that can run locally. Then, students learn to set up a frontend and a backend for a website using common technologies related to Ruby and JavaScript. There is also a strong emphasis on web technologies like RESTful routing and API serving and requesting.

While the bootcamp only has to go so far to teach web development principles, there is more out there. Other ways to present programs include creating platform-specific applications. These are not web-based. An app that runs on a desktop will be different from one that runs on a phone at least because GUIs vary from one OS or platform to the next. Another cause for difference is that different platforms often are written in different programming languages, so apps that are widely available outside of on the web have been developed separately for each platform. (On a side note, even web development must account for variations from one browser, or even from one browser version, to the next.)

Developing for these platforms requires knowledge of not just the base language, but also GUI programming principles as related to where the app will run. Also, Atom isn't the only integrated development environment. It's even possible to find IDEs that are specific to a destination platform, instead of specific to a language.

And then, there is DevOps, a growing area in platform development. DevOps relies on a number of pipeline-building and logging technologies to create infrastructure that supports, monitors, tests, and deploys developed applications. Infrastracture as Code tools like Ansible, Chef, and Puppet define system setups, while Continuous Integration / Continuous Delivery tools like Jenkins allow organizing and automating the work of receiving updated code, testing it, and even deploying it to a live environment. And, companies like AWS and Google Cloud Platform offer a wide range of services that include file storage, database solutions, and other infrastructure. Learn Docker and Kubernetes to learn about containers and container orchestration, respectively.

Some good places to start learning about deploying an application are Heroku and Netlify. Heroku requires PostGreSQL, so be sure to conform your database setup before deploying if your app has a database. Using Heroku and Netlify offer a glimpse into how to use GitHub for CI/CD applications.
