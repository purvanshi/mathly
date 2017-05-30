iSolveMath
**********

**iSolveMath is a project which aims to solve and visualize Math Word Problems (MWPs).**


.. contents:: *Contents of this document*
   :depth: 2

Introduction
=============

A student begins to solve Math Word Problems in the second grade, and these problems continue till the end of high school. Most students are unable to solve such problems, and rely on rote learning instead. We decided to tackle this common problem of word problems. 

A lot of research has been done in this field, but most research is concentrated on the simpler problems of 2nd grade (junior school level), such as addition. 

iSolveMath aims to solve problems up to 6th grade (middle school level), which include:

- Simple Interest (S.I.)
- Profit & Loss
- Work
- Speed, Distance & Time
- Unitary Method
- Single and Multi-step Addition, Subtraction, Multiplication and Division

We also aim to encourage further research in this area.

Approach
===========

We decided on the following approach, which is used instinctively by students, and is also detailed in numerous research papers:

- Classification: In this step, we will classify the problem and assign to it its category. This is performed by a classifier, which uses `SVM <https://en.wikipedia.org/wiki/Support_vector_machine>`_.
- Extraction of unknown quantities: In this step, we will find the unknown quantity (the values to be found). Suppose a person enters a question as "John invested $500 in a bank at the rate of 5 p.a. Find the simple interest incurred in one year." Then, the unknown quantity / question to be extracted is "Find the S.I. …" This task is accomplished by POS Tagging and Wh-word (or question words, such as who, what etc.) recognition.
- Extraction of known quantities: In this step, we will find the known quantities (the quantities which are surreptitiously mentioned in the question). For the same example above, the known quantities extracted are "Principal = $500", "Rate = 5", and "Time = 1". This task is accomplished by NER Tagging.
- Generation of answer: Each basic word problem can be classified into subcategories. For example, SI problems can be divided into:
  
  1. Finding a quantity when three others are given. 
  2. Finding amount.
  3. Investment of parts (example - splitting investment into two parts, and finding the cumulative interest after a year). This also includes profit sharing.

  This task will call the function according to the subcategory found using previous steps.

Alternatives
============

The following alternatives already exist, but they perform to a limited capacity:


- `WolframAlpha <http://wolframalpha.com>`_ (as detailed here - `[1] <https://www.wolframalpha.com/examples/MathematicalWordProblems.html>`_, and `[2] <http://blog.wolframalpha.com/2012/10/04/solving-word-problems-with-wolframalpha/>`_ ): WolframAlpha has been *the* computational engine ever since its inception in 2009. This means that it would return answers to factual answers directly, rather than linking to pages that *might* contain the content. WolframAlpha began offering solutions to single-step junior-school level problems in 2012, and has been refining it till now.

  The only problem with using WolframAlpha as a natural language parser (rather than a computational engine) is the maximum *complexity* of the word problems that the site can handle, which is depressingly low. 

- `Euclid <http://euclid.allenai.org/>`_: Euclid is one of the products of the Allen Institute of Artificial Intelligence (AI2), which was established by Microsoft co-founder Paul Allen in 2013 to further AI. It aims to solve SAT-style Math questions. (for example, "What is x, if x plus three is 10?"). 

  The thing that drags Euclid down is the sheer *perfection* expected from the user - sentences with small amounts of redundancy or ambiguity are instantly rejected. Sentences which have information that is not directly handed over to the user are also rejected.

  For example, consider the question "Each pencil costs $9.00. How much do 4 pencils cost?". Euclid is not able to parse such short questions, since it is cannot extract the unknown quantity (which is the cost) and a fact (which is the number of pencils) from the same sentence. Euclid expects the question to have been something like this "Each pencil costs $9. 4 pencils were brought. What is the total cost?"

- Online material - This is a double-edged sword. On one hand, you have seemingly *humongous* amounts of information, so large that you cannot even begin to comprehend it. On the other hand, the sheer information available at your fingertips is daunting - you don't know where to start or end, you don't know which site to trust (web security is a real concern), and the content is often hidden behind paywalls.

Conclusion
==========

We hope that this project will help reduce the hardships and angst that students face because of Math. We also hope that researchers and programmers will take our project (and the subcategory of Math Word Problems) and advance it even further.
