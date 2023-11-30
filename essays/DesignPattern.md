---
layout: essay
type: essay
title: "Design Pattern?"
# All dates must be YYYY-MM-DD format!
date: 2023-11-29
published: true
labels:
  - Design pattern
---

My perspective on design patterns likens them to tools, each with its distinct purpose. Just as a Phillips screwdriver serves its specific function with Phillips screws and isn't suitable for flat head screws, design patterns function similarly. You can't apply them universally; understanding the pattern's purpose and its appropriate application is crucial. Misapplying a design pattern might result in malfunction, potentially causing the entire application to break down. Hence, a design pattern is a tool that requires knowing when and how to use it effectively to solve a problem.

In my ICS 314 Software Engineering course, I'm currently engaged in a final project titled UHnify. Our aim is to facilitate easier access to club information for students at the University of Hawaii at Manoa. Within this project, my team and I have implemented several design patterns. One such pattern is the publish-subscribe pattern, utilized to establish communication between the Mongo database and various components. For instance, upon a user submitting all required information, data insertion occurs in the database, followed by publishing the club collection. Subsequently, the club component subscribes to this collection to exhibit the club information.

Another design pattern we employed is the reactive data pattern. This pattern is instrumental in displaying user-added or updated information within a collection in real-time. As an illustration, our project includes a club creation page enabling users to add clubs. Upon submitting the information, the new club card instantly appears on the 'find club' page, facilitated by the application of the reactive data pattern.

Additionally, we utilized the Singleton pattern by creating a singular instance of a class for data access. For example, our 'Events' class serves as an instance to access the events collection, presenting event information on the dedicated event page. 


In conclusion, design patterns are versatile tools utilized for problem-solving in software development. Yet, comprehending the specific purpose and appropriate context for each pattern is crucial. Misapplying a design pattern can lead to malfunctions, risking the breakdown of an entire application. If my team had employed a different design pattern for the purposes I've outlined, it might not have functioned as intended. Therefore, utilizing a design pattern necessitates a clear understanding of when and how to effectively apply it to address specific problems within the software architecture.
