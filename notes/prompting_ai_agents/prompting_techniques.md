# Prompting Engineering

## Elements of a Prompt

Instruction - a specific task or instruction you want the model to perform

Context - external information or additional context that can steer the model to better responses

Input Data - the input or question that we are interested to find a response for

Output Indicator - the type or format of the output.

## Techniques

* Zero-shot Prompting: . The zero-shot prompt directly instructs the model to perform a task without any additional examples to steer it.


* Few-Shot Prompting:  Few-shot prompting can be used as a technique to enable in-context learning where we provide demonstrations in the prompt to steer the model to better performance. The demonstrations serve as conditioning for subsequent examples where we would like the model to generate a response.


* Chain-of-Thought (CoT), +z-shot: "Let's think step by step",  enables complex reasoning capabilities through intermediate reasoning steps. You can combine it with few-shot prompting to get better results on more complex tasks that require reasoning before responding.


* Meta Prompting or 0-shot: focuses on the structural and syntactical aspects of tasks and problems rather than their specific content details. This goal with meta prompting is to construct a more abstract, structured way of interacting with large language models (LLMs), emphasizing the form and pattern of information over traditional content-centric methods.


* Self-consistency: The idea is to sample multiple, diverse reasoning paths through few-shot CoT, and use the generations to select the most consistent answer. This helps to boost the performance of CoT prompting on tasks involving arithmetic and commonsense reasoning.


* Generate Knowledge: the ability to incorporate knowledge or information to help the model make more accurate predictions.


* Compose or Chaining: break tasks into its subtasks. Once those subtasks have been identified, the LLM is prompted with a subtask and then its response is used as input to another prompt. This is what's referred to as prompt chaining, where a task is split into subtasks with the idea to create a chain of prompt operations.


* Tree of Thought (ToT): generalizes over chain-of-thought prompting and encourages exploration over thoughts that serve as intermediate steps for general problem solving with language models.
"Imagine three different experts are answering this question.
All experts will write down 1 step of their thinking,
then share it with the group.
Then all experts will go on to the next step, etc.
If any expert realises they're wrong at any point then they leave.
The question is..."


* Directional Stimulus Prompting: Use Hint or Stimmulus to orient the LLM.


* Reflexion: converts feedback (either free-form language or scalar) from the environment into linguistic feedback, also referred to as self-reflection, which is provided as context for an LLM agent in the next episode. This helps the agent rapidly and effectively learn from prior mistakes leading to performance improvements on many advanced tasks.
"Providing a pointing of the answer response, in order the LLM learn and provide accurate information".


*