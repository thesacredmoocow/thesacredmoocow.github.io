---
layout: single
title:  "Writing an Election Tallying program"
date:   2021-05-19 12:44:04 -0400
categories: projects
author_profile: true
share: false
tags: example
toc: true
---

## Summary
I wrote a quick CLI program which parses google forms responses, and outputs the winner of my school's student council elections

## Backstory
Due to a sudden influx of fake votes coming from emails not registered to my school, the student council approached me, looking for a solution. Normally votes would be held in-person, 
but due to Covid-19, they had to be done online using Google Forms. Unfortunately there was no way to restrict access to a certain group of people, only a certain domain.
This meant that students from other OCDSB schools could vote in our election, and had resulted in very skewed results in a previous election.

## The result
I only had a few days to write this program, so making it look nice was a (distant) second priority. 
My program needed to read in a list of all the students in my school as well as their email addresses and grades. Then it would check the votes for each grade's grade reps, 
and only add the votes to the total if the student was both a registered students. Lastly, it would output a file with human-readable text indicating which person won in each grade, as well as the number of votes for each person.

To make matters more difficult, I would not be allowed access to the database of student information due to privacy reasons. I had to perform my own testing using generated data and ensure everything worked prior to sending it off.

With all that done, I sent my program off to the teacher which would run the tally. Shortly afterwards, I heard back. My program had worked! Not only had it tallied all the votes correctly and printed out the winners of the election,
it had also printed out the invalid votes that it had caught! I had proof that my program had actually helped the election. Interestingly enough, one of these votes came from a teacher at my school...

[Source Code](https://github.com/thesacredmoocow/lisgar-studco-election-counter)
