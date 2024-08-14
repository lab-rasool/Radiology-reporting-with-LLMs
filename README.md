### Radiology-reporting-with-locally-run-LLMs

We utilize open-access LLMs to make radiology reports concise and well-structured and use [Ollama](https://github.com/ollama/ollama) platform to run LLMs locally behind a secure firewall.

We explore five different prompting approaches: 

- **Structure**: This approach focused solely on prompting the LLM to structure reports according to a predefined format.
  
- **Structure >> Conciseness**: The LLM was initially prompted to structure the reports according to a specified format. Subsequently, another prompt instructed the model to refine the structured output further for conciseness. Here, each report processing consisted of two calls to the LLM.
    
- **Conciseness >> Structure**: The LLM was first prompted to generate concise reports. Following this, the model was instructed to organize the concise information into a predefined structure.  Here, each report processing consisted of two calls to the LLM.

- **Structure + Conciseness**: The LLM was prompted to structure reports in a predefined format while also emphasizing the need for conciseness.

- **Structure + Conciseness (F, I)**: Given two prompts, the LLM was prompted to structure the Findings and Impressions sections in reports separately in a predefined format while also emphasizing the need for conciseness.  
