# General Tips for designing prompts

## The Instruction
You have the ability to create prompts that are successful for different straightforward tasks by employing commands that direct the model towards your desired outcome. These commands can include instructions like "Compose," "Categorize," "Condense," "Convert," "Arrange," and so on.

```
### Instruction ###
Translate to Spanish:

Original Text: "Welcome to this Prompt Engineering Session"

Traduction:
```

## Specific Prompts

The key to obtaining optimal results from the model is to be clear, detailed, and specific in the instructions and prompts provided. By ensuring a well-structured and descriptive prompt, along with examples when applicable, one can achieve the desired outcomes and formats in the generated output.

```
Detect and extract the dates mentioned in the following text.
Desired format:
Dates: <comma_separated_list_of_dates>
Input: "Although these developments are encouraging to researchers, much is still a mystery. “We often have a black box between the brain and the effect we see in the periphery,” says Henrique Veiga-Fernandes, a neuroimmunologist at the Champalimaud Centre for the Unknown in Lisbon. This research was conducted between 2018 and 2020, and several significant breakthroughs occurred during this period. “If we want to use it in the therapeutic context, we actually need to understand the mechanism. The next experiment will take place on June 28th, 2023, and we anticipate exciting results.”
````

## Precise Prompts

To optimize prompt effectiveness, it's important to balance detail with directness. Avoid overly clever or imprecise descriptions. Clear and specific prompts enhance comprehension, analogous to effective communication. This approach improves the quality and accuracy of model-generated output.

For instance, if you have an interest in understanding the concept of prompt engineering, you can formulate a prompt like this:

```
Explain the concept prompt engineering. Keep the explanation short, only a few sentences, and don't be too descriptive.
```


The prompt above lacks clarity regarding the number of sentences and desired style. While you may still receive acceptable responses, a more effective prompt would be specific, concise, and straightforward. For instance, consider the following prompt: 

```
Provide a clear explanation of prompt engineering to a 5 year old, using 2-3 concise sentences.
```


# Advanced Prompt Engineering

## Zero-Shot


Zero-Shot refers to the ability to generate meaningful responses or outputs without explicit training examples. It involves leveraging a pre-trained language model's understanding of general knowledge and reasoning capabilities to respond intelligently to prompts that it has not been explicitly trained on.

```
Classify the text into neutral, negative or positive. 
Text: I think the vacation is okay.
Sentiment:
```

## Few-shot

Although large-language models showcase impressive zero-shot abilities, they face limitations when tackling intricate tasks under the zero-shot setting. To overcome this, few-shot prompting can be employed as a technique to facilitate in-context learning. By incorporating demonstrations within the prompt, we guide the model towards improved performance. These demonstrations act as conditioning for subsequent examples, where we desire the model to generate a response.

```
A "flibbergib" is a hypothetical concept in quantum data theory that represents the entangled state of multiple datasets. An example of a sentence that uses the word "flibbergib" is:
In this groundbreaking experiment, scientists successfully manipulated the flibbergib, demonstrating the potential for harnessing entangled data for quantum computations.

To "whizzleflop" is the process of generating synthetic data with random variations for testing and validation purposes. An example of a sentence that uses the word "whizzleflop" is:
```

## Chain of Thought (CoT)

Chain-of-thought (CoT) prompting allows for advanced reasoning abilities by employing intermediate reasoning steps. By integrating CoT prompting with few-shot prompting, one can achieve improved outcomes for intricate tasks that necessitate reasoning prior to providing a response.

```
The odd numbers in this group add up to an even number: 4, 8, 9, 15, 12, 2, 1.
A: Adding all the odd numbers (9, 15, 1) gives 25. The answer is False.
The odd numbers in this group add up to an even number: 15, 32, 5, 13, 82, 7, 1. 
A:
```

A newly emerged concept is the notion of zero-shot CoT which introduces the inclusion of **"Let's think step by step"** to the initial prompt. Let's attempt a straightforward problem to observe the model's performance.
