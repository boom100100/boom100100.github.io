---
layout: post
title:      "When has_many Elements Need to Be in Order"
date:       2020-07-31 19:31:22 +0000
permalink:  when_has_many_elements_need_to_be_in_order
---


**Problem**

Imagine if a developer were working on a container model that requires the elements it holds to have a changeable order. For example, a Chapter model that has many Paragraphs. A creator of paragraphs would likely need to do a revision that puts one paragraph before or after another.

In a typical array, the solution would be to insert a paragraph at any spot, instead of just at the end. But that's not possible in ActiveRecord's native functionality. ActiveRecord only has a #create function that would put a paragraph at the end of the array.

**Solution**

There are many solutions, some of which are better than others. Assuming one has already created a SQL database using ActiveRecord, a gem would be a quick addition to allow ordering the paragraphs. After installing the [acts_as_list](https://www.ruby-toolbox.com/categories/Active_Record_Sortables) gem for an existing database, a developer must modify the migration by adding a position field as an index. After migrating the database, there are a bunch of functions that can reorder the has_many elements. Note that the acts_as_list link above offers similar gem-based solutions. Note that this solution works even if one hasn't made the database yet.


**Non-Solution**

There are two bad solutions.

The first bad solution is creating an order field and writing code that accounts for all conditions in which the order must be updated. Once a new order is clear for one element, the backend must iterate through all other elements in the has_many relationship to update them as well. Iterating over all elements at every change leaves much room for error.

The second bad solution forces the user to copy and paste all paragraph content so it's in the right order while leaving the paragraph objects in their original order. Having a user manually reorder is especially cumbersome when the shift is more than a few spaces or when it requires uploading files.
