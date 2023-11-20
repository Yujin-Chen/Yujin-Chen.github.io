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
  <img src="./image/AI1.jpg" alt="AI Image" class="img-fluid" style="width:100%"/>
</p>


## Introduction
Artificial Intelligence (AI) exhibits immense power across diverse fields. It aids in task completion and can even execute tasks entirely on your behalf. Whenever you encounter something you don't understand, AI stands ready to provide explanations. Take ChatGPT, for instance, an interactive chat AI that responds dynamically to your input. Its capabilities are vast—you can accomplish numerous tasks with it. For instance, requesting code generation is as simple as entering the requirement or instruction, and it promptly produces the code, ready for immediate use.



## Personal Experience with AI
I've utilized ChatGPT within ICS 314 for various tasks such as brainstorming ideas, locating errors, writing code for me, explaining certain code that I don't understand, and more. 

### Experience WODs, In-class WODs, Practice WODs, and Writing Code.
I did use ChatGPT for In-class practice and Experience WODs. They are the same, they both does not have time limit. For instance, during a practice WOD named BK Menu, I asked ChatGPT to write the code for me.

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
This isn't what I want. I simply want to add a top border to my footer. It's frustrating that it keeps suggesting things that aren't what I'm looking for. So, never fully trust AI and always review everything yourself before using it.

I did not use ChatGPT during the in-class WODs for two reasons:
1. we would have to answer couple questions before submitting it. I feel that is too complicated so I did not use it. 
2. This test if I actually understand and the concept. Using ChatGPT in practice and experience WODs is mainly to help me understand the concept. 

### Essays
I also used to help me writing my essays. I would write the essay first then use ChatGPT to help me correct my grammar and spelling. It is very helpful. After using it I am satisfy. For example:

Prompt:
```
fix: Artificial Intelligence (AI) is powerful in all different 
fields. It can assist you to complete the task or even complete 
the task for you. When you do not understand something you can ask
 AI to explain it to you. For example, ChatGpt is an interactive 
 chat AI that responds based on your input. You can do many things
  with it. Like have it write code for. You would just need to 
  type in the requirement or instruction then it will generate the
   code. Then you can just use it right away.
```

Result:
```
Artificial Intelligence (AI) exhibits immense power across diverse 
fields. It aids in task completion and can even execute tasks 
entirely on your behalf. Whenever you encounter something you 
don't understand, AI stands ready to provide explanations. Take 
ChatGPT, for instance, an interactive chat AI that responds 
dynamically to your input. Its capabilities are vast—you can 
accomplish numerous tasks with it. For instance, requesting code 
generation is as simple as entering the requirement or 
instruction, and it promptly produces the code, ready for 
immediate use.
```
This is very helpful. It helps me correct my grammar and spelling for my introduction of this essay. The flow of this piece is better than my initial draft, and it aids in enhancing my writing. I plan to use it for future essay writing, if permitted, as it significantly improves my work.

### Answering a question in class or discord; Asking or Answering  smart questions
I haven't used ChatGPT to answer questions in class in class, on discord, or asking smart questions. It is because the instructor and TA are the one who are grading the assignment. So I do not trust AI to answer the question for me because it might not be correct. I would rather ask the instructor or TA for help.

### Final Project
For the final project, my group used ChatGPT to help us generate ideas. For instance, we asked ChatGPT to assist in creating a wireframe outlining the Uhnify landing page. Subsequently, we built upon that as a foundation. Here's what ChatGPT came up with:
```
Wireframe Description for UHnify Landing Page

Top Section:
* Brand Logo: Placed prominently at the top center or top left of 
the page, using a clear and high-resolution image that embodies 
the UHnify brand, consistent with the brand recognition strategy.

* Navigation Bar: Directly below or beside the brand logo, 
including links to other pages like "Home," "Browse Clubs," 
"Events," "Login," reflecting the typography and color palette 
from the mood board.

* Engaging Headline: "Your Campus Community Awaits: Engage with UH
 Manoa Clubs!" stands out against the Coconut White background, 
 set in bold Raleway font to grab attention immediately upon 
 landing on the page.

Introduction Section:
* Tagline: Below the headline, a brief and inviting introduction 
in Open Sans that says, "UHnify brings UH Manoa's clubs to your 
fingertips – Connect with peers, discover events, and join the 
conversation."

* Login/Sign Up: Positioned to the right of the tagline or as a 
standalone section, featuring contrasting buttons – one in Banana 
Leaf Green and another in Pale Yellow – drawing the eye and making
 it clear where to log in or sign up.

Main Content Area:
* Primary Call-to-Action (CTA): An "Explore Now" button in a 
strategic and central location on the screen, possibly with a 
subtle animation or hover effect to entice clicks. The button 
would be styled using the bold and inviting colors from the 
primary palette.

* Events Preview: A visually appealing carousel or grid displaying
 upcoming events, using thumbnails that incorporate the tropical 
 and green color scheme, with a quick hover animation or highlight
  to indicate new events. Each preview would link to the more 
  detailed Events Page.

Footer:
* Consistent Layout: At the bottom of the page, a footer that 
stretches across the screen, colored in a subtle shade from the 
color palette, perhaps the Light Tropical Green for a grounding 
effect.

* Information: Contains contact details, social media links, and 
quick links in a neatly organized manner, using the same fonts as 
the body text for consistency.

* Legal Information: Discreetly placed in a smaller font size but 
still legible and easy to find for those who need it.
```

### Learning a concept / tutorial, Code Examples and explaining Code
I did use ChatGpt to learn concept of something I don't understand. For example the arrow function, I was so confused. I never seen or used that before taking this course. So I ask ChatGPT to explain it to me. 

Prompt:
```
how do you use =>()?
```
Result:
```
The => syntax in programming languages, particularly in JavaScript
 and other languages adopting similar constructs, is used to 
create arrow functions, also known as fat arrow functions.

Here's a breakdown:

Arrow Functions: Arrow functions are a concise way to write 
function expressions in JavaScript.

Syntax: The basic syntax looks like this:

javascript
Copy code
const functionName = (parameters) => {
  // function body
};
Parameters: Arrow functions can take parameters inside the 
parentheses (). If there's only one parameter, the parentheses 
can be omitted. If there are no parameters, empty parentheses () 
or _ (underscore) can be used to denote that.

Function Body: If the function body is a single statement, you can
 omit the curly braces {} and the return keyword (if the single 
statement is a return statement). If there are multiple 
statements, you need to enclose them in {} and explicitly use 
return if you want to return something.

Usage: Arrow functions are often used for concise anonymous 
functions, especially in scenarios like array manipulation 
methods (e.g., map(), filter(), reduce()), where shorter, more 
readable code is preferred.

Example:

javascript
Copy code
// Regular function
function greet(name) {
  return `Hello, ${name}!`;
}

// Equivalent arrow function
const greetArrow = (name) => `Hello, ${name}!`;
Arrow functions have lexical scoping of this, which means they 
don't have their own this value. Instead, they inherit this from 
the surrounding code (lexical context). This can be advantageous 
in certain scenarios, especially when working with callbacks or 
handling context.

However, they might not be suitable in all situations, 
particularly when you need a function with its own this context or
 when defining object methods due to the way they handle this.

Overall, => or arrow functions provide a more concise syntax for 
writing functions, especially for shorter, more straightforward 
functions in JavaScript.
```
This is very helpful. It helps me understand the concept of arrow function. It explains to me what the code does, concept, and how to use it. 
### Quality Assurance and Documentation
I did not use AI for my documentation because my final project is not at that point yet. When I reach that step, I would give ChatGPT a try to see how it goes. I did use ChatGPT for Quality Assurance when when my code run into issues. For example the simple function below with some syntax errors.

Prompt:
```
Why is my code not running? Is there any syntax error?
function BertErnie(int){
if(int%4==0 & int%6==0){
console.log("BertErnie");
}
else if(int%4==0){
console.log("Bert");
}
else if(int%6=0){
console.log("Ernie");
}
else{
console.log(int);
}
}
for(let i=1;i<=100;i++){
BertErnie(i);
}
```

Result:
```

I see a syntax error in your code. In the else if statement for 
checking if a number is divisible by 6, you're using the 
assignment operator = instead of the equality operator == or ===.

Here's the corrected code:

javascript
Copy code
function BertErnie(int) {
  if (int % 4 == 0 && int % 6 == 0) {
    console.log("BertErnie");
  } else if (int % 4 == 0) {
    console.log("Bert");
  } else if (int % 6 == 0) {
    console.log("Ernie");
  } else {
    console.log(int);
  }
}

for (let i = 1; i <= 100; i++) {
  BertErnie(i);
}

Changes made:
Replaced the & operator with && for the logical AND operation.
Replaced int % 6 = 0 with int % 6 == 0 in the else if condition to
 check if int is divisible by 6.
This corrected code should now properly run and execute the 
BertErnie function for numbers from 1 to 100.
```
This is very helpful. It helps me find the syntax error and explain to me what is wrong with my code. It also help me fix the error. It saves a lot of time.
### Other uses in ICS 314 Not Listed
I did not use ChatGPT for other uses in ICS 314 not listed. I mainly use AI to write code and fix code errors. I did not use it for other uses because I do not know what other uses are there. 

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
