# AkshitBaliyan-langsmith-MAT496



I began by downloading the initial notebook from the repository and setting up the LangSmith API key along with an OpenAI key
Installed all required dependencies including scikit-learn, pandas, BeautifulSoup, and others.

The setup worked smoothly with no errors, so I proceeded to Module 1.


MODULE 1

Video 1:
Each execution of the code generates a new trace. Traces record every function call, providing a detailed step-by-step breakdown of how the program runs. The LangSmith platform offers an intuitive UI to view these traces and the functions involved. Metadata about each run can also be stored and displayed in the trace—either added manually or during runtime. Both approaches were explored in the exercise.

Video 2:
There are four primary types of runs in LangSmith:

LLM – Directly invokes the language model.

Retriever – Fetches documents from a database.

Tool – Executes function calls (tools).

Chain – The default type, combining multiple runs into a workflow.

In this section, I practiced invoking an LLM, retrieving documents in the correct format, and calling tools. Additionally, I created a simple calculator tool (with ChatGPT’s help) for basic arithmetic operations and tested it through LangSmith.

Video 3:
Different ways to run traces include:

@traceable – The method used earlier; it automatically organizes sub-traces under parent traces.

LangGraph – Handles tracing automatically without manual setup.

trace() – Allows selective control over inputs/outputs.

wrap_openai – Directly integrates with the OpenAI SDK.

RunTree – Offers the most granular level of control; requires setting LANGSMITH_TRACING=0.

These options provide flexibility depending on whether simplicity or fine-grained control is preferred.

Video 4:
Conversation threads were introduced. By assigning a fixed thread ID, I could maintain a continuous dialogue with the model, enabling it to recall previous responses. I tested this by building my own conversation flow.

=>>>>  With this, Module 1 was successfully completed.


MODULE 2


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
