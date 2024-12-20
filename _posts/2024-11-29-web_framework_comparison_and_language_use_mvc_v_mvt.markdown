---
layout: post
title:      "Web Framework Comparison and Language Use: MVC v. MVT"
date:       2024-11-29 09:46:57 -0400
permalink: web_framework_comparison_and_language_use_mvc_v_mvt
---


One major source of confusion amongst developers is related to the ease at which people can talk past each other. One case of this is related to discussing the difference between API frameworks like Flask (python) and .NET (C#).

Flask is essentially derivative of Django. The main difference between the two is that Flask is a microframework that enables high customization, and Django is a more complete framework that offers opinionated implementations for API framework features. Ultimately, this makes Flask a less popular choice for quickly getting a fully-featured website up and running.

Where these two fundamentally differ from .NET is simply a matter of words.

C#'s .NET framework follows the model-view-controller (MVC) pattern. An API built in a MVC pattern receives a request via the controller and responds, still via the controller, with data. That data takes the form of json, a fully renderable page, or one of a bunch of other potential ways of packaging data. This data response makes up the view. The controller directly or indirectly calls some CRUD operation  to interact with the model. And then any relevant information from the model is integrated into the view.

Flask and Django call this control flow the model-view-template (MVT) pattern. Instead of a controller, the view is the receiver of the API request, and the view sends the packaged response data. "Template" is a confusing word to use, since it implies server-side rendering and jinja templates. But the template is the data response, however that is packaged. In this pattern, the model remains the same.

Here is a table demonstrating the difference (or lack thereof).


| Functionality           	| .NET Name  	| Flask Name 	|
|-------------------------	|------------	|------------	|
| CRUD/Database           	| Model      	| Model      	|
| Packaged Response Data  	| View       	| Template   	|
| Handle Request/Response 	| Controller 	| View       	|


Even though the difference is just a matter of words, it is crucial to use the matching pattern name when holding discussions about API frameworks. Flask view parent classes have the name "view" in them, so calling them "controllers" leaves developers at a loss of where to find them if they are too inexperienced to have encountered both MVC and MVT. Also, both pattern names include the words "view" and "model." "Model" ends up being acceptable as a universal term because it doesn't change meaning. "View" does change meaning, so its meaning won't be obvious in a conversation if there's no explicit statement concerning which pattern someone is referring to.

Code don't lie. And neither do patterns.
