https://huggingface.co/learn/agents-course
https://huggingface.co/learn/agents-course/unit0/onboarding#step-5-running-models-locally-with-ollama-in-case-you-run-into-credit-limits

The Agent Workflow:
Think → Act → Observe.

An Agent is a system that leverages an AI model to interact with its environment in order to achieve a user-defined objective.  
It combines reasoning, planning, and the execution of actions (often via external tools) to fulfill tasks.  
Think of the Agent as having two main parts:  
    The Brain (AI Model)  
    The Body (Capabilities and Tools)  


The most common AI model found in Agents is an LLM (Large Language Model), which takes Text as an input and outputs Text as well.  
developers of HuggingChat, ChatGPT and similar apps implemented additional functionality (called Tools), that the LLM can use to create images.  
An Agent can perform any task we implement via Tools to complete Actions.  

 an Agent is a system that uses an AI Model (typically an LLM) as its core reasoning engine, to:  
 Understand natural language:  
 Reason and plan:  
 Interact with its environment:  

 An LLM is a type of AI model that excels at understanding and generating human language. These models typically consist of many millions of parameters.  
 Most LLMs nowadays are built on the Transformer architecture—a deep learning architecture based on the “Attention” algorithm, that has gained significant interest since the release of BERT from Google in 2018.  

There are 3 types of transformers:  
Encoders  
Decoders  
Seq2Seq (Encoder–Decoder)  

Although Large Language Models come in various forms, LLMs are typically decoder-based models with billions of parameters.

The underlying principle of an LLM is simple yet highly effective: its objective is to predict the next token, given a sequence of previous tokens.  
You can think of a “token” as if it was a “word”  
Tokenization often works on sub-word units that can be combined.  

Each LLM has some special tokens specific to the model.  The most important of those is the End of sequence token (EOS).  
LLMs are said to be autoregressive, meaning that the output from one pass becomes the input for the next one. This loop continues until the model predicts the next token to be the EOS token, at which point the model can stop.

Messages: The Underlying System of LLMs  
System Messages  
 -  define how the model should behave.
 -  serve as persistent instructions  
system_message = {
    "role": "system",
    "content": "You are a professional customer service agent. Always be polite, clear, and helpful."
}  
Conversations: User and Assistant Messages
Chat templates help maintain context by preserving conversation history
ChatML - template format that structures conversations with clear role indicators (system, user, assistant).

Model Context Protocol (MCP): a unified tool interface  
(MCP) is an open protocol that standardizes how applications provide tools to LLMs  

