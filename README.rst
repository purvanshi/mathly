iSolveMath
**********

**iSolveMath solves and visualizes Math Word Problems (MWPs).**


.. contents:: *Contents of this document*
   :depth: 2

Introduction
=============

iSolveMath is a platform where a student can enter a maths word problem, get an automatic answer and visual explanation generated of both the question and the answer.

Inspiration
===========
A student begins to solve Word Problems in the second grade, and these problems continue till the end of high school. Most students are unable to visualise such problems, and rely on rote learning instead.Finally developing a hatered towards the subject. 

Approach
========
The system at present solves starightforward simple interest problems like-

1.How much time will it take for an amount of $900 to yield $81 as interest at 4.5% per annum of simple interest?
2.If Manohar pays an interest of $750 for 2 years on a sum of $4,500, find the rate of interest.
3.Sahil took a loan for 6 years at the rate of 5% per annum on Simple Interest, If the total interest paid was $1230, Find the principal.

The process takes place as follows-
- Finding the question part and classifying into what is unknown.
- Finding the known quantities with the help of NER tagging and classification of money tag into simple interest, amount or    principal.
- Formula call and return of answer.
Each basic word problem can be classified into subcategories. For example, SI problems can be divided into:
  
  1. Finding a quantity when three others are given. 
  2. Investment of parts (example - splitting investment into two parts, and finding the cumulative interest after a year). This also includes profit sharing.

Current Work and research
=========================
The code at present is highly domain specific. To make it more generic, we have decided to solve word problems from basic. At present we are working on 4 basic operation problems(single and multistep). For better accuracies we will use deep neural networks to train our data.

Who can contribute
==================
-Researchers - People who want to challenge the current accuracies of present maths word problem solvers, or extend the research in this field to higher level and complex problems and who love to play with the language(natural language processing).
-Developers - We beleieve in building something which can be used by someone directly. Bridging the gap between research and develepment work, iSolveMath is a platform which involves both development and research work.
-ANYONE WHO LOVES MATHS AND BELIEVES EVERYONE ELSE SHOULD LOVE IT TOO.


Alternatives currently available in maths word problem solving
==============================================================

The following alternatives already exist, but they perform to a limited capacity:


- `WolframAlpha <http://wolframalpha.com>`_ (as detailed here - `[1] <https://www.wolframalpha.com/examples/MathematicalWordProblems.html>`_, and `[2] <http://blog.wolframalpha.com/2012/10/04/solving-word-problems-with-wolframalpha/>`_ ): WolframAlpha has been *the* computational engine ever since its inception in 2009. This means that it would return answers to factual answers directly, rather than linking to pages that *might* contain the content. WolframAlpha began offering solutions to single-step junior-school level problems in 2012, and has been refining it till now.

  The only problem with using WolframAlpha as a natural language parser (rather than a computational engine) is the maximum *complexity* of the word problems that the site can handle, which is depressingly low. 

- `Euclid <http://euclid.allenai.org/>`_: Euclid is one of the products of the Allen Institute of Artificial Intelligence (AI2), which was established by Microsoft co-founder Paul Allen in 2013 to further AI. It aims to solve SAT-style Math questions. (for example, "What is x, if x plus three is 10?"). 

  The thing that drags Euclid down is the sheer *perfection* expected from the user - sentences with small amounts of redundancy or ambiguity are instantly rejected. Sentences which have information that is not directly handed over to the user are also rejected.

  For example, consider the question "Each pencil costs $9.00. How much do 4 pencils cost?". Euclid is not able to parse such short questions, since it is cannot extract the unknown quantity (which is the cost) and a fact (which is the number of pencils) from the same sentence. Euclid expects the question to have been something like this "Each pencil costs $9. 4 pencils were brought. What is the total cost?"

- Online material - This is a double-edged sword. On one hand, you have seemingly *humongous* amounts of information, so large that you cannot even begin to comprehend it. On the other hand, the sheer information available at your fingertips is daunting - you don't know where to start or end, you don't know which site to trust (web security is a real concern), and the content is often hidden behind paywalls.
