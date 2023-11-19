---
layout: essay
type: essay
title: "Powerful AI"
# All dates must be YYYY-MM-DD format!
date: 2023-11-15
published: true
labels:
  - Artificial Intelligence
  - Reflect
---

<p style="text-align:center; ">
  <img src="./image/AI.jpg" alt="AI Image" class="img-fluid" />
</p>


## Introduction
Artificial Intelligence (AI) exhibits immense power across diverse fields. It aids in task completion and can even execute tasks entirely on your behalf. Whenever you encounter something you don't understand, AI stands ready to provide explanations. Take ChatGPT, for instance, an interactive chat AI that responds dynamically to your input. Its capabilities are vast—you can accomplish numerous tasks with it. For instance, requesting code generation is as simple as entering the requirement or instruction, and it promptly produces the code, ready for immediate use.



## Personal Experience with AI
I've utilized ChatGPT within ICS 314 for various tasks such as brainstorming ideas, locating errors, writing code for me, explaining certain code that I don't understand, and more. For instance, during a practice WOD named BK Menu, I asked ChatGPT to write the code for me.

Prompt:
```
The goal of this WOD is to implement a class that keeps track of the total calories, fat, 
and sodium in a Burger King order and notifies you when your order has exceeded the recommended 
daily maximum for a sedentary college student (i.e. 2,000 calories, 70 grams fat, 2300 mg sodium).

Here is some code to define objects containing reference values for various BK items:

const bkItems = {
  cokeLarge:     {calories: 380, fat: 0, sodium: 10},
  cokeMedium:    {calories: 290, fat: 0, sodium: 5},
  cokeSmall:     {calories: 140, fat: 0, sodium: 0},
  frappeLarge:   {calories: 600, fat: 25, sodium: 360},
  frappeSmall:   {calories: 410, fat: 19, sodium: 230},
  whopper:        {calories: 650, fat: 37, sodium: 910},
  doubleWhopper: {calories: 900, fat: 56, sodium: 980},
  tripleWhopper: {calories: 1160, fat: 75, sodium: 1050},
  chickenSandwich: {calories: 660, fat: 40, sodium: 1220},
  friesLarge:    {calories: 500, fat: 22, sodium: 900},
  friesMedium:   {calories: 410, fat: 18, sodium: 570},
  friesSmall:    {calories: 240, fat: 10, sodium: 330}
};
Now create a class called BKMenu whose constructor accepts the bkItems data 
structure and saves it. The BKMenu class should also store the recommended daily 
maximum for calories, fat, and sodium.

BKMenu implements an add() function that accepts a string indicating the item 
ordered, which will be one of the fields in the bkItems data structure. For 
example, “cokeLarge”, “whopper”.

Whenever the add() function is called, if the recommended daily maximum for 
calories, fat, or sodium is now exceeded for that order, the function should print
 out the total along with a message to the console for that value.

For example:

const myMenu = new BKMenu(bkItems);
myMenu.add("cokeLarge");
myMenu.add("frappeLarge");
myMenu.add("tripleWhopper");
// console prints:
//   Calories exceeds allowance of 2000: 2140
//   Fat exceeds allowance of 70: 100
myMenu.add("friesLarge");
// console prints:
//   Calories exceeds allowance of 2000: 2640
//   Fat exceeds allowance of 70: 122
//   Sodium exceeds allowance of 2300: 2320
```
Result:
```
class BKMenu {
  constructor(bkItems) {
    this.bkItems = bkItems;
    this.recommendedDailyMax = {
      calories: 2000,
      fat: 70,
      sodium: 2300
    };
    this.order = {
      calories: 0,
      fat: 0,
      sodium: 0
    };
  }

  add(item) {
    const menuItem = this.bkItems[item];
    if (!menuItem) {
      console.log(`Item '${item}' not found in the BK menu.`);
      return;
    }

    this.order.calories += menuItem.calories;
    this.order.fat += menuItem.fat;
    this.order.sodium += menuItem.sodium;

    if (this.order.calories > this.recommendedDailyMax.calories) {
      console.log(`Calories exceeds allowance of ${this.recommendedDailyMax.calories}: ${this.order.calories}`);
    }

    if (this.order.fat > this.recommendedDailyMax.fat) {
      console.log(`Fat exceeds allowance of ${this.recommendedDailyMax.fat}: ${this.order.fat}`);
    }

    if (this.order.sodium > this.recommendedDailyMax.sodium) {
      console.log(`Sodium exceeds allowance of ${this.recommendedDailyMax.sodium}: ${this.order.sodium}`);
    }
  }
}

const bkItems = {
  // ... (your item definitions here)
};

const myMenu = new BKMenu(bkItems);
myMenu.add("cokeLarge");
myMenu.add("frappeLarge");
myMenu.add("tripleWhopper");
myMenu.add("friesLarge");

```
The ChatGPT has already completed most of the task for me. I just need to add in the item definition that is provided in the instructions. I tested it and got the expected result. This assistance is helpful, but it's important not to place 100% trust in AI. Sometimes, AI makes mistakes too. It doesn't comprehend our exact thoughts, so the result might not precisely meet your needs. For instance, when I use co-pilot in IntelliJ and typed
```
footer {
 border-top: #0A5421;
 border-top-width: 3px;
 border-top-style: solid;
 ```
in the style sheet, it gives me random suggestions.

Then this is what Co-pilot suggested:
```
background-color: #4F7942;
color: #ffffff;
padding: 50px;
text-align: center;
font-size: 1.5rem;
font-weight: 500;
font-family: 'Open Sans', sans-serif;
```
This isn't what I want. I simply want to add a top border to my footer. It's frustrating that it keeps suggesting things that aren't what I'm looking for. So, never fully trust AI and always review everything yourself before using it

## Impact on Learning and Understanding
Although one can't fully trust AI responses, I always test them to ensure accuracy by checking the results or ask instructor for verification. If there's something I don't understand, I copy and paste that line into the chat box for ChatGPT to explain how it works in detail. Even if I still don't understand, I can ask follow-up questions or request a simpler example. This process helps me grasp the concept and problem-solving methods, enabling me to solve similar issues independently in the future. This significant influence of AI enhances my learning experience.

## Practical Applications
AI's widespread use in today’s world is undeniable, particularly in real-world projects, saving considerable time. With vast data in its database, ChatGPT eliminates the need for extensive searches. If code fails to run properly, pasting it and describing the issue prompts ChatGPT to identify errors and suggest fixes. While its suggestions might not always resolve the problem, they provide insights into the problematic code section.

## Challenges and Opportunities
The primary limitation in using AI within the course is its accuracy, given that AI tools like ChatGPT are still in development and not flawless in discerning correctness. Nevertheless, AI serves as valuable support in teaching. For instance, in my ICS 314 course this Spring 2023 semester, the us of AI tools are allowed, easing the instructor’s workload and saving students time by using AI first before seeking direct help.

## Comparative Analysis
Traditional teaching methods persist as the primary mode of instruction compared to AI-enhanced approaches. Classroom interactions between instructors and students, and peer-to-peer discussions, offer unique learning opportunities that AI cannot replicate. Consequently, I believe discussions with peers and instructors remain the most effective way to learn. Each person has their individual way of thinking and understanding, contributing to an expansion of perspectives. AI, being programmed, maintains a fixed approach, lacking the diverse and nuanced thinking inherent in human interactions.

## Future considerations
ChatGPT's ongoing development indicates its continuous learning and improvement, signaling the potential for increased accuracy and stability in the future. AI, despite its current state, remains a growing trend, indicating a future where reliance on AI will likely increase. I believe it will make both instructor and student lives easier, saving time and effort. 

## Conclusion
From the experience I had with AI, it definitely helped me throughout the course and enhanced my understanding. This has shown that AI is an important tool in software engineering education. However, I believe that AI will never replace human interactions, which are essential to learning and understanding. AI will continue to serve as a valuable tool, but it will never replace the human element. So I recommend that we continue to use AI as a tool to enhance our learning experience but don't rely on it entirely.
