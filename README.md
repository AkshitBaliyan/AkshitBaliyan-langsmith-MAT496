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

