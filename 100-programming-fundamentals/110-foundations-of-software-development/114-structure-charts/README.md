---
description: >-
  Structure charts are decomposition tools that break the parts of a system into
  its modules and sub-modules until programmers begin writing functions
  represented at the bottom layer of the chart.
---

# 114 Structure charts

A structure chart is a representation of the hierarchy of functions within a program. It shows the functions, the data that flows between them (as parameters and return values) and gives a general indication of decisions and loops within the processing.&#x20;

<figure><img src="../../../.gitbook/assets/image (9).png" alt=""><figcaption><p>An outline of the key components of a structure chart</p></figcaption></figure>

The **Main** function is the function at the top. It is the first function that is called within the program and serves to direct the processing of the other functions. It doesn't have to be called "Main", but usually is.

The **Child** functions fall below this. They are listed in the order that they are called within the code. If they call other functions then they are listed below as sub-child functions (and you can keep going down as many levels as necessary). Child functions are joined to their parent function via a Call line.

If a child function is called from several parent functions, you don't have several lines, you instead list a copy of the function under every parent. A child function is also generally only listed once under each parent. If a parent calls that function several times (not in a loop) then only the first instance is listed. (The child function can be listed more than once however if one instance is inside either a loop or decision, and one is outside the loop or decision.)

A **loop** is indicated with a curved arrow and shows that the function, or functions, get called repeatedly. We don't list the criteria for the decision on the structure chart, only that is it repeated.

A **decision** is indicated with a diamond. Every child function coming from the same decision block is indicated under the same diamond.

**Parameters** are the data which gets passed down to and back from the functions. An open circle indicates plain data which is processed. A closed circle indicates a parameter which impacts the operation of a loop or decision in the diagram. This is referred to as a **flag** or **control variable**.

<figure><img src="../../../.gitbook/assets/image (11).png" alt=""><figcaption><p>A structure chart for a program that calculates are and volume.</p></figcaption></figure>

Structure charts benefit two people. The person creating the diagram gets a deeper understanding of the potential layout of the processing by thinking through the structure. The reader also understands the overall program and how it is intended to come together. Presentation is important to help both people get the most out of this diagram.
