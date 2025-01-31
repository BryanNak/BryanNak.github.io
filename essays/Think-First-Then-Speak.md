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

<img width="300px" class="rounded float-start pe-4" src="../img/smart-questions/rtfm.png">

## Answers to those who search
Questions are constants in our lives and are used in all sorts of ways. You may hear the phrase quite often as a child or student that there are no such things as "dumb questions", however that is not always the case. There are times where questions, on the contrary to the popular saying, are definitely through skin and bone dumb. Knowing how to ask questions is unbeknownst to some people, a skill that like any other, must be practiced in order to get better at. A good example would be of this person asking about [processing time of a sorted vs unsorted array](https://stackoverflow.com/questions/11227809/why-is-processing-a-sorted-array-faster-than-processing-an-unsorted-array). They wrote their observations with code provided about how sorting some data took 1.93 seconds and without the code that sorts the data, it took 11.54 seconds. The whole code snippet is provided:
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
They not only conducted their test in c++ but also Java and provided the code for that as well. They wrote their pondering thoughts relevant and provided answers to those, and even linked and summarized other questions asked on stack overflow that were similar to the problem that they were having! This person provided the question plain and simple, provided what they had and what they knew, and showed that they tried to find an answer and analyzed thoroughly why their answers couldn't answer the original problem. They knew how to ask a smart question and thru that, they received very thorough answers to the problem.

## Answers in the palm of your hand
It is quite common to see people search for a solution on the internet and after one link and no answer, turn to communities and ask for a solution. This mindset births a somewhat helpless image for the original poster.


## Conclusion


