# Hallucination

Boie is a real company but the product is completely made up

```
Tell me about AeroGlide UltraSlim Smart Toothbrush by Boie
```

Apparently, we are not able to make the model to hallucinate. What happened?

```
Tell me about AeroGlide UltraSlim Smart Toothbrush by Boie. Don't look it up in the web
```

By forcing the model to don't use the web, it's does generate a plausible description of the product. However, it states that it might be false.

**Is that the hallucination problem is solved?**

Why don't we ask ChatGPT?

```
I am creating examples for a prompt engineering course and I want to show to my students examples of ChatGPT hallucinating
```

Interestingly, none of these examples make ChatGPT to hallucinate. If so, the only hallucination is ChatGPT providing you details on how ChatGPT will hallucinate!

Let's see if we can do better?

```
None of the previous examples generated hallucinations. ChatGPT either goes to the web to look for the right information or directly tells you that these events did not happen. Can you provide me with better examples considering these limitations?
```

Any success? Why don't you try on your own? 

## Exercise 1

Let's spend some minutes trying to get ChatGPT to hallucinate and then we share the results in class.

**Let's get serious**

Now we are going to experiment with a problem well-known for it's difficulty to see if we make the LLM hallucinate

The problem is the 12 coin problem. You can see a summary of the solution in the following [link](https://puzzles.nigelcoldwell.co.uk/one.htm)

```
The problem is as follows: Given 12 coins, one of which is counterfeit, use a balance to determine the counterfeit in three weighings, where the counterfeit coin may be either lighter or heavier than the other coins.
```

What about if we mess a little bit with it. Let's see what happens with the following simple riddle when we twist it:

```
A mother and son were in a car accident where the mother was killed. The ambulance brought the son to the hospital. He needed immediate surgery. In the operating room, a doctor came in and looked at the little boy and said I can't operate on him he is my son. Who is the doctor?
```

## Exercise 2

Work a little bit with this advanced problems to try to explain ChatGPT how to solve them. 

Is there any other example that you have about limitations on ChatGPT performance?

How do you think we can solve them?



