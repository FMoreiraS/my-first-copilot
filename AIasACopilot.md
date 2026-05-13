# How to use AI as a copilot like a software engineer
## AI in software development
Grosso modo, we yet need to know the basics, tools and techniques, but now we
must have AI as tool. Now, the main role of a developer is to be an
**orchestrator** rather than a code writer. Begginers need to study as always,
they can ask questions to AI, but do not should to ask code, neither can use
AI as a substitute, when starting to using a copilot.  
The developer can use AI to reinforce the learning and control the level of the
suggestions the AI give, to "think" just what the developer already knows. But
the most important point is: **a copilot must be the Dev's extension**. For
that, the new developer **must train his copilot**, to "**think and work as
himself**".

## Introduction to Prompt engineering
### Overview
**How AI models "understand" commands**: language models decompose the text to
identify **tokens**, the smallest information units for a specific model,
a character, word, phrase, etc, then **stabilish conections** between the
informations gathered.  
**How LMs "remember" what was said**: As someone chat with an AI, it group the
information provided by the user, creating a **context window**, something like
a short memory, because the models normally *do not persist data from chats*.
Althoug, there are ways to enable the model to save some informations (like
text files, "memory.md"). Context window is the **limit of tokens the model
can use simultaneously**. After surpassing the limit, the model starts to lose
understanding of the last used contextual elements.
**Essential elements in a prompt**:
1. Initial instruction
2. Context
3. Examples
4. Input data
5. Output format

### Application
**Precautions**:
- avoid biased prompts (that will direct the answer)
- models can hallucinate mentioning things that do not exist or roughly wrong,
    based in the prompt content.
- use anonymous data, to do not expose people.

**Tips to leverage prompts**: learn prompt engineering techniques and concepts
such as **inference parameters**

## Using AI and as copilot
**Integrated and outside copilots**: integrated copilots are *embedded* in the
IDE/editor, whereas outside copilots are *external, independent* AI tools, like
Chat GPT and Gemini. Integrated copilots have the advantage to know all the code
we are working on at the moment, while outside copilots need the developer give
context of the project.

### Copilot modes
To be a copilot, an AI must have at least **3 modes: agent, ask, and plan**.
There are others, according the specific editor or tool, such as *debug* and
edit, and even the user can create custom modes, like *study* and *refactor* modes.
What do each mode do?
- **Agent**: is a code generator, a more free mode to do tasks.
- **Ask**: is dedicated to answer questions, in a specific context.
- **Plan**: is an assistant in planning processes.
- **Study**: work as a more expert engineer suggesting how to study.

**What is a good copilot?** A good copilot is the most especialized, that is,
the copilot must be *focused* in a role (planner, agent...).  

### How to create copilot modes
Each mode can be declared in a *text file* (.txt, .md), with **all the need rules**
to limit what the copilot can and cannot do in each mode. These files can used
with any AI tool, like Chat GPT, or to customize existing modes in an integrated
copilot (for example, in VS Code).

#### File's structure
The text file for all the modes can have some common parts, adapted to each mode:
1. Identity paragraph, saying the model is a copilot in a specific mode, with
    its constraints (like prohibiting plan mode to generate code);
2. Stack, the most specific as possible (language, framework, versions, DBs, infra);
2. Personality (optional, to define how the copilot chat);
3. Rules of the mode, the "guardrails", such as output format, guidelines, what
    factors to consider before answer (like programming paradigm and libs).

It is very important, in the section of rules, to **define precisely how the
copilot must answer**. This makes *easier to understand* the answers and *stabilish
more control* over them, prevents messy or generic answers.