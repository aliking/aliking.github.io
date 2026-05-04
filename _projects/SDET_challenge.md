---
layout: project
title: "SDET Challenge"
description: "Take-home challenge for SDET role."
tech: [JSON Schema, AWS Lambda, JavaScript]
status: "🟢 Archived"
link: "https://github.com/aliking/sdet_challenge"
featured: false
---

A take-home coding challenge for a Software Development Engineer in Test role. I initially conceived this as an add-on to a job description, where the challenge was presented as a 'way to make your cover letter stand out' by submitting it as JSON document that met some specific criteria.

Later, it was just presented to candidates as a standard take-home test. The idea was that there was a URL that would return one of 100 JSON documents based on a query parameter and that some of those were invalid. The candidate's task was to find the invalid documents, use their ids to create a 'checkvalue' that would prove that they had found them all and then submit that as part of their own valid json document.

At the back of my mind I was always slightly worried that someone would just check all the documents manually, because that would have been terrible for them and immediately disqualifying.

JSON documents were served from S3 with an AWS Lambda function and AWS gateway, making it cheap and robust and giving me a notification when someone was doing the challenge.

This project also included a tool to automate validation of the submitted final document, deployed to Heroku. A technical recruiter could paste the submitted JSON document into the app, and it would report any problems and give some instructions about how I felt about different classes of errors.

{% picture "/assets/media/sdet_challenge/app.png" alt="Screenshot of the app, showing the results of validating a submitted JSON document" %}
