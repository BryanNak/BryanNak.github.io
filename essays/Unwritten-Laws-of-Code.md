---
layout: essay
type: essay
title: "Unwritten Laws of Code"
# All dates must be YYYY-MM-DD format!
date: 2025-02-10
published: true
labels:
  - Software Engineering
  - Typescript
  - ESLint
---
<p align = "center">
<img width="700px" class="rounded pe-4" src="../img/unwritten-laws-of-code/xkcd-coding-standard.png">
</p>

## The Road to Better Code
If I were to look back at the very first program I wrote, I would probably wince at the sight of:
- improper indentation
- lack of proper documentation
- *very* useless variable names

That was only the beginning, however, and overtime I have gotten better (for the most part) at fixing these issues in my code by learning to code according to standards which are generally accepted as such. The beauty of coding is that there are so many ways to achieve a goal in programming, but there are most definitely "wrong" ways of writing code and everyone starting off has probably written unnecessary line of code in their program before.

## A Nightmare
Imagine you were told to review some code from a beginner programmer, and upon reviewing, they wrote an entire for loop which prints out elements in an array, all on **one** line:
```typescript
for(var i =0;i<array.length;i++) {console.log(i);};
```
A cursed nightmare no one should ever have to lay their eyes upon. No proper indentation, spacing, and to top it all of, it's all on one line.

To mitigate this problem, coding standards can easily be taught and passed on so that this situation does not happen again. Standards may range from just a few to hundreds depending on who you ask, but some examples could be:
- Commenting code
- proper indentation
- clean formatting (ambiguous but basically not spaghetti code)

There are many more out there, but those are some basic examples which can not only be helpful to yourself, but others in the future who may happen to stumble upon your code. Even when learning a new programming language, it is crucial to confine to the unwritten laws of code: coding standards.

The code above rewritten with coding standards in mind would look more like:
```typescript
//print out each element in the array
for (let i = 0; i < array.length; i++) {
  console.log(i);
}
```
## Applied Constraints
Recently I have been learning TypeScript to write simple programs, and due to its derivation from JavaScript, many things are still valid when using TypeScript, such as the use of `var` which is pretty much committing a sacrilege. Thankfully, **ESLint** exists and can help break this habit. It helps immensely with writing more clear-cut explicit code and because I have to take the time to fix my errors, I am also given an opportunity to see where I am doing things wrong such as forgetting to write return types for functions or variables and how I can avoid them in the future.

Tools such as ESLint make it easier to follow coding standards and help form much more readable, coherent code. Everyone in the world has their own way of writing code for a program but with just a few universally accepted "laws of code", each distinctly written code can have aspects similar to one another, allowing for not only easier cooperation and collaboration from others, but also an easier time for your current and future self.