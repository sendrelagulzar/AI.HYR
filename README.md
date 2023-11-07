# AI.HYR take-home test

## Thought process

The overall goal of the AIResume project is to develop a system that can automatically extract key information from resumes, such as candidate name, email address, phone number, and work experience. This information can then be used to screen candidates more efficiently and to build a more comprehensive database of candidates.

To achieve this goal, I decided to use a large language model (LLM) called OpenAI. LLMs are trained on massive datasets of text and code, and they can be used to perform a variety of tasks, including text generation, translation, and code writing.

I also decided to use a library called LangChain. LangChain is a library that makes it easy to chain together different LLMs and other NLP tools. This allows me to build complex NLP workflows without having to write a lot of code myself.

## Challenges faced

One of the biggest challenges I faced was extracting the text from the PDF resumes. I used the PyPDF2 library to do this, but it was tricky to get it to work correctly. I also had to deal with the fact that the resumes were in different formats, which made it difficult to extract the information consistently.

Another challenge was training the LLM to extract the key information from the resumes. I used a variety of techniques, such as fine-tuning the LLM on a dataset of labeled resumes and using prompt templates. However, it was still difficult to get the LLM to extract the information accurately and consistently.

## Approach taken

To extract the key information from the resumes, I used the following approach:

Read the PDF resume using PyPDF2.
Extract the text from the PDF resume.
Prompt the LLM to extract the key information from the text.
Post-process the output of the LLM to correct any errors.
I used the following prompt template for the LLM:

Find Candidate’s {question} in given text {text}
For example, to extract the candidate's name, I would use the following prompt:

Find Candidate’s name in given text {text}
where {text} is the text of the resume.

I also used the following post-processing steps to correct any errors in the output of the LLM:

Remove any punctuation marks or special characters.
Convert the output to lowercase.
Strip any leading or trailing whitespace.

## Results

The AIResume system is able to extract the key information from resumes with a high degree of accuracy. The system is also able to handle resumes in different formats.
