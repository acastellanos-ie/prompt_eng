# Hallucination

Boie is a real company but the product is completely made up

```
Tell me about AeroGlide UltraSlim Smart Toothbrush by Boie
```

Interestingly, the model does not generate a hallucinated response about the product. Instead, it either avoids responding or provides factual disclaimers. Why is that happening?

```
Tell me about AeroGlide UltraSlim Smart Toothbrush by Boie. Don't look it up in the web
```

When explicitly instructed not to use the web, the model generates a plausible but fabricated description of the product. However, it includes a disclaimer, indicating the possibility of inaccuracy.

**Is the hallucination problem solved?**

Why don’t we ask ChatGPT directly?

```
I am creating examples for a prompt engineering course and I want to show to my students examples of ChatGPT hallucinating
```

Surprisingly, none of these attempts cause the model to hallucinate. The only potential "hallucination" occurs when the model explains how it might hallucinate, which is meta in itself.

**Let’s see if we can do better.**

```
None of the previous examples generated hallucinations. ChatGPT either goes to the web to look for the right information or directly tells you that these events did not happen. Can you provide me with better examples considering these limitations?
```

Any success? Why don’t you try to generate hallucinations on your own?

## Exercise 1: Inducing Hallucination

Spend a few minutes attempting to get ChatGPT to hallucinate. Think about scenarios where you can provide ambiguous, partially true, or intentionally misleading prompts. Then, share your results with the class.

Reflect on the results:
- Did the model generate hallucinated content?
- Did it provide disclaimers or avoid hallucinating?

---

**Let’s get serious.**

Now, we’ll explore problems known for their complexity to see if we can prompt the model into hallucinating.

### Advanced Problem Example: The 12-Coin Problem
Here is the setup of the well-known 12-coin problem. You can see a summary of the solution in the following [link](https://puzzles.nigelcoldwell.co.uk/one.htm)

```
The problem is as follows: Given 12 coins, one of which is counterfeit, use a balance to determine the counterfeit in three weighings, where the counterfeit coin may be either lighter or heavier than the other coins.
```

Analyze the response for accuracy. Did the model hallucinate a solution that is logically incorrect?

---

### Twisting a Classic Riddle

Let’s see how the model handles a famous riddle with a subtle twist:

```
A mother and son were in a car accident where the mother was killed. The ambulance brought the son to the hospital. He needed immediate surgery. In the operating room, a doctor came in and looked at the little boy and said I can't operate on him he is my son. Who is the doctor?
```

Discuss the response. Did the model understand the riddle? What happens if you slightly rephrase it or add misleading details?


## Exercise 2: Exploring Limitations

Work with these advanced problems to see how well ChatGPT handles them:
1. Explain the 12-coin problem in detail, step by step. Test how effectively the model can follow logical reasoning.
2. Rephrase the classic riddle in different ways. Observe if the model struggles with subtle variations or cultural biases.

### Additional Exercises:
- **Fictitious Scenario Testing:** Ask the model about a completely fabricated scenario (e.g., "The Mars Treaty of 2085"). Analyze whether it generates plausible but false information.
- **Ambiguous Instructions:** Provide vague or contradictory instructions and observe how the model handles them.
- **Counterintuitive Questions:** Pose questions that challenge common sense or logical fallacies, such as, "If a train leaves New York traveling west at 200 mph, what color is its engine?"

**Discussion Questions:**
- What specific limitations did you observe in the model’s responses?
- Were there scenarios where the model provided fabricated or logically invalid information?
- How do you think we could improve the model to handle these challenges?

**Reflection:** What insights can you derive about the strengths and weaknesses of ChatGPT in addressing hallucination issues?


## Exercise 3: Solution Strategies

Propose strategies to address hallucination issues based on your experiments:
- How might prompt design reduce hallucinations?
- What role does user feedback play in refining model accuracy?
- Are there systemic improvements that could prevent hallucinations entirely?


