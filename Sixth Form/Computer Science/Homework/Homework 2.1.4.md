---
date: 2026-10-02
tags:
  - computer-science
  - a-level
spec code: H446
---
# Homework 4: Thinking Logically

1. **(a)** How many lines of output will the following pseudocode algorithm produce? Show your calculation. **[3]**

```pseudocode
for a = 8 to 19 step 4
    for b = 1 to 3
        if a mod b >= b/3 then
            if a/4 <= b+1 then
                print ("Homer")
            else
                print ("Marge")
            endif
        else
            print ("Bart")
        endif
    next b
next a
```

There a 3 iterations for the two print loops
$$
3*3=9
$$
*9*

---
**(b)** Trace through the pseudocode and write down what is output. **[4]**

```
Bart
Bart
Homer
Bart
Bart
Bart
Bart
Bart
Homer
```
---

## Question 2

You need to make $n$ pancakes for a number of people as quickly as possible. Your only frying pan is big enough to make two pancakes at a time. A pancake needs one minute’s cooking on each side, regardless of whether there are one or two pancakes in the pan.

* **(a)** What is the minimum time to fry 3 pancakes? **[1]**
  4
* **(b)** Explain how you arrived at your answer. **[2]**
Because 2<sup>2</sup> is greater than 3 that means 2 is the minimum number of pans needed and each pancake needs to cook for two mins so$$2*2=4$$
* **(c)** What is the minimum time to fry $n$ pancakes?
*n minutes if n is greater than one* 

---

## Question 3

**(a)** A firm of caterers has been hired to cater for a fundraising dinner at a village hall. Here is a list of tasks:

> **Tasks:** Prepare vegetables, Serve wine, Heat main course, Whip cream, Prepare fruit salad, Lay tables, Set out tables, Set out chairs, Serve coffee

* **(i)** List five of the tasks which can be done concurrently. **[2]**
	- *Prepare vegetables*
	- *Whip cream*
	- *prepare fruit salad*
	- *set out tables*
	- *set out chairs*
* **(ii)** List five tasks which must be done sequentially, specifying the order in which they must be done. **[2]**
	1. *Set out tables*
	2. *Lay tables*
	3. *Heat main course*
	4. *Serve wine*
	5. *Serve coffee*
---

**(b)** An airline reservation system is an example of concurrent processing. Describe briefly another example of concurrent processing in a computer system. **[2]**
	*Operating system, playing music in the background while the user is typing on a document*

---

**(c)** List two benefits and two drawbacks that may result from concurrent processing. **[4]**

* **Benefits:**
  1. Increased efficiency
  2. Improved system responsiveness
* **Drawbacks:**
  1. Increased complexity
  2. Competition for processing power

---

> [!info] **Total: 20 marks**

