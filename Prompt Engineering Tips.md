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

## Ask for a strucured output

Many times LLMs are part or larger applications that requires specific formats for pipelining the process. The following prompt shows how to request a specific output in JSON format:


```
Generate a list of three made-up book titles along \ 
with their authors and genres. 
Provide them in JSON format with the following keys: 
book_id, title, author, genre.
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

```
I went to the market and bought 10 apples. I gave 2 apples to the neighbor and 2 to the repairman. I then went and bought 5 more apples and ate 1. How many apples did I remain with?
Let's think step by step.
```

## Generated Knowledge

LLMs are continually being enhanced, and a prominent approach involves integrating knowledge or information to enhance the model's predictive accuracy. Building upon this concept, can the model also be employed to generate knowledge prior to making a prediction?

```
Answer the question
Question: Who is the Machine Learning Teacher?
Answer: The Machine learning teacher is [name]
```

```
Answer the question
Question: Who is the Machine Learning Teacher?
Knowledge:  I (Angel Castellanos) am a Senior Data Scientist with over a decade of experience, I have honed my skills both in academia as a Researcher during my Ph.D. journey and in the industry, contributing to the success of some of Spain's premier data science departments.

With a perpetual curiosity, my mission is to fuse cutting-edge Machine Learning and Natural Language Processing research with tangible corporate challenges. I pride myself on transforming novel research concepts into game-changing products and services, such as modeling user interactions and constructing unsupervised dialog systems. 

Having devoted two years to developing AI-driven Unsupervised Language Models at Lang.ai, I enabled businesses to thrive in the AI era. Currently, I've taken on a new challenge at Japan Tobacco International (JTI). I am spearheading the execution of the data science strategy, shaping the company's future through data-driven insights.

In addition to my industry pursuits, I serve as a faculty member at one of Europe's elite business schools, IE University. Specializing in my two primary areas of interest - machine learning and natural language processing - I am honored to work alongside the most esteemed names and decision-makers in the Spanish Tech sector. By imparting my knowledge and experience to ambitious students, I am helping to 
empower future professionals in the fields of machine learning and natural language processing and shape the next generation of industry leaders, 

Answer: The Machine learning teacher is [name]
```

## Persona-driven Prompting

Persona-driven prompting is a feature that allows users to customize the behavior of the language model to match specific personas or characters. By providing instructions and details about the desired persona, users can shape the responses of the model to align with the persona's traits, speaking style, and knowledge base, enhancing the conversational experience.

```
Generate digital startup ideas based on the wish of the people. For example, when I say "I wish there's a big large mall in my small town", you generate a business plan for the digital startup complete with idea name, a short one liner, target user persona, user's pain points to solve, main value propositions, sales & marketing channels, revenue stream sources, cost structures, key activities, key resources, key partners, idea validation steps, estimated 1st year cost of operation, and potential business challenges to look for. Write the result in a markdown table.

Just acknowledge the task and I will start giving you ideas

```

```
I wish it was easier for me to keep track of my personal relationships with friends and family

```


