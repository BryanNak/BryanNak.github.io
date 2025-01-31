---
layout: essay
type: essay
title: "Think First Then Speak"
# All dates must be YYYY-MM-DD format!
date: 2025-01-30
published: false
labels:
  - Questions
  - Answers
  - StackOverflow
---

<img width="300px" class="rounded float-start pe-4" src="../img/rtfm.png">

## Answers to those who search
Questions are constants in our lives and are used in all sorts of ways. You may hear the phrase quite often as a child or student that there are no such things as "dumb questions." However, that is not always the case. There are times when questions, contrary to the popular saying, are definitely through skin and bone dumb. Knowing how to ask questions is unbeknownst to some people, a skill that, like any other, must be practiced in order to get better at. A good example would be of this person asking about the [processing time of a sorted vs. unsorted array](https://stackoverflow.com/questions/11227809/why-is-processing-a-sorted-array-faster-than-processing-an-unsorted-array). They wrote their observations with the code provided about how sorting some data took 1.93 seconds and without the code that sorts the data, it took 11.54 seconds. The whole code snippet is provided:

```cpp
#include <algorithm>
#include <ctime>
#include <iostream>

int main()
{
    // Generate data
    const unsigned arraySize = 32768;
    int data[arraySize];

    for (unsigned c = 0; c < arraySize; ++c)
        data[c] = std::rand() % 256;

    // !!! With this, the next loop runs faster.
    std::sort(data, data + arraySize);

    // Test
    clock_t start = clock();
    long long sum = 0;
    for (unsigned i = 0; i < 100000; ++i)
    {
        for (unsigned c = 0; c < arraySize; ++c)
        {   // Primary loop.
            if (data[c] >= 128)
                sum += data[c];
        }
    }

    double elapsedTime = static_cast<double>(clock()-start) / CLOCKS_PER_SEC;

    std::cout << elapsedTime << '\n';
    std::cout << "sum = " << sum << '\n';
}
```
They not only conducted their test in C++ but also Java and provided the code for that as well. They wrote their pondering thoughts relevant and provided answers to those, and even linked and summarized other questions asked on stack overflow that were similar to the problem that they were having! This person provided the question plain and simple, provided what they had and what they knew, and showed that they tried to find an answer and analyzed thoroughly why their answers couldn't answer the original problem. They knew how to ask a smart question, and through that, they received very thorough answers to the problem.

## Answers in the palm of your hand
It is quite common to see people search for a solution on the internet and, after one link and no answer, turn to communities and ask for a solution. This mindset births a somewhat helpless image for the original poster.
A good example of this would be this user on stack overflow asking the [difference between structural vs. behavioral patterns](https://stackoverflow.com/questions/79402043/structural-vs-behavioral-patterns-need-absolute-clarity). First off, the title of the post includes "Need absolute clarity," which already quickly violates Eric Raymond's [How To Ask Questions The Smart Way](http://www.catb.org/esr/faqs/smart-questions.html) criteria. Titles like this make people *less* inclined to look at your post and deter them from answering it. They provided no information other than the literal description of the two patterns and asked what the difference is, which is quite ironic. This person has also asked this question in the wrong forum; They asked it in stack overflow, which is for questions about programming, while their question would be more relevant to the super user forum. Even one of the comments in the post tells the user that there are many examples of [structural patterns](https://refactoring.guru/design-patterns/structural-patterns) and [behavioral patterns](https://refactoring.guru/design-patterns/behavioral-patterns) that, when I took a look at them, had tons of graphics and text explaining each one in a pretty clear and straightforward explanation. 

## Conclusion
Learning to ask smart questions is not a hard thing to do, and it will help everyone *immensely*. Sure, there may be people who have high tolerance who are kind enough to answer dumb questions, but there are way more people who are driven enough to point out how stupid you are for asking that question. It is important to ask a question that is fully communicated to the audience rather than a half-effort question that is looking for an immediate answer. If you are asking a question, then the people answering shouldn't have to ask follow-up questions just to answer your question; that would be a telltale sign that your question is not smart. It is a skill that smart software engineers **need** in order to succeed because in this field, anything could contribute to a problem occurring. There are so many aspects that could affect a program, from the tiniest fault in hardware to just one missing semicolon in code, and that is why it is important to state as much information relative to the problem as possible so that people can help you swiftly and thoroughly.
