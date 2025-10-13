# AkshitBaliyan-langsmith-MAT496
Langsmith Academy Course - Module 1 & 2

Roll Number: 2310110029

I began by downloading the initial notebook from the repository and setting up the LangSmith API key along with an OpenAI key
Installed all required dependencies including scikit-learn, pandas, BeautifulSoup, and others.

The setup worked smoothly with no errors, so I proceeded to Module 1.


# MODULE 1

Video 1:
Each execution of the code generates a new trace. Traces record every function call, providing a detailed step-by-step breakdown of how the program runs. The LangSmith platform offers an intuitive UI to view these traces and the functions involved. Metadata about each run can also be stored and displayed in the trace either added manually or during runtime. Both approaches were explored in the exercise.


Video 2:
There are four primary types of runs in LangSmith:

LLM : Directly invokes the language model.
Retriever : Fetches documents from a database.
Tool : Executes function calls (tools).
Chain : The default type, combining multiple runs into a workflow.

In this section, I practiced invoking an LLM, retrieving documents in the correct format, and calling tools. Additionally, I created a simple calculator tool (with ChatGPT’s help) for basic arithmetic operations and tested it through LangSmith.


Video 3:
Different ways to run traces include:

@traceable : The method used earlier; it automatically organizes sub-traces under parent traces.
LangGraph : Handles tracing automatically without manual setup.
trace() : Allows selective control over inputs/outputs.
wrap_openai : Directly integrates with the OpenAI SDK.
RunTree : Offers the most granular level of control; requires setting LANGSMITH_TRACING=0.

These options provide flexibility depending on whether simplicity or fine-grained control is preferred.


Video 4:
Conversation threads were introduced. By assigning a fixed thread ID, I could maintain a continuous dialogue with the model, enabling it to recall previous responses. I tested this by building my own conversation flow.



# MODULE 2

Video 1: Creating a Dataset
This task was simple—followed the tutorial to create a dataset using my OpenAI key. I generated five AI-based fields, experimented with the schema, and built a flexible dataset structure. I also demonstrated filtering and splitting the dataset in the notebook.
Datasets act as predefined examples (with inputs and optional outputs) to help LLMs perform better.


Video 2: Evaluators
Evaluators assess the LLM’s outputs by comparing them against reference Q&A. Different scoring techniques can be applied. I implemented:

A similarity score evaluator (from the course),
A correctness evaluator,
A hallucination evaluator, and
A composite evaluator that aggregates results from all three.


Video 3: Experiments
Running a model on a dataset and evaluating its performance is termed an experiment. I experimented with:

Entire datasets,
Dataset splits and filtered subsets,
Different OpenAI models to analyze runtime,
Multiple concurrent runs.

The experiments required adapting code depending on the dataset and carefully checking outputs.


Video 4: Analyzing Experiments
Reviewed and documented experiment results with observations included in the notebook.


(Optional Part) : 

Video 5: Pairwise Experiments
This feature enables comparison between two experiments, making it easier to determine which approach is more effective for a given use case.


Video 6: Summary Evaluators
Summary evaluators combine results from multiple evaluations. I had already come across something similar earlier when experimenting with evaluators—creating a composite score by assigning weights to individual evaluators.




# Module 3  (Assignment 2nd starts here) : 

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/1305ba49-b671-41f1-bd33-d7773251b968" />

Downloaded above resources and pushed in the repository.

Video 1 : 

I got the playground running and successfully tested the provided example. After that, I decided to experiment by using my own dataset and tweaking the system messages to see how the output would change. I've attached a few images to show what I observed.

Learning for me : I spent some time getting familiar with the LangSmith playground, a space designed for testing and refining prompts. It's cool because you can bring in your own data, so I used the dataset I created for the last assignment to see the model's different reactions.
To push it further, I edited the system message to ask for replies in a different language, and it worked perfectly.
I learned how to use its core features like referencing my own datasets, swapping models, and iterating to get better results. All in all, it was a relatively simple but very practical introduction to this feature.


Video 2 :                                                                                                                                                                        
I created a prompt directly on the LangSmith site. I went a step beyond the lesson by making a more dynamic prompt with extra variables like profession, location, and language. Once I saw that working, I also tried pushing a prompt from my notebook up to the website to test it there. I did notice one small difference from the video: the import code snippet uses client now, not hub. It didn't affect the outcome, though, so I just kept going.

Video 3 :                                                                                                                                                                                                 
I just finished the video on the prompt engineering lifecycle. I created my own prompt that responds to emotions and tested it with a dataset I'd already made. I had to tweak the prompt's syntax to get it to work with my data's format, but it ran successfully in the end. I've saved the results in the notebook.

Video 4:                                                                                                                                                                                    

<img width="1917" height="925" alt="image" src="https://github.com/user-attachments/assets/677fa6e3-efa0-4e17-93e5-84e3ffdf1ad6" />


<img width="1920" height="926" alt="image" src="https://github.com/user-attachments/assets/a8502906-489c-47ee-a278-9fd62c4f94a2" />


I learned about the prompt canvas and its tooling. The 'diff' button is a really useful feature for seeing exactly what's changed between my prompt versions. I learned about the actions that adjust the reading level and length, and I even used the chatbot itself to get suggestions on how to make my prompt better.


I changed the persona of the bot to a cricketer instead of a pirate like shown in the video.                                                                                                                       
I asked the question "Where did you learn to play the cover drive?" instead of how did you lose your leg.
