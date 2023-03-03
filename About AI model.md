#### Model doesn't knew about newest event, company etc.
##### model trained by old data
Code for call model in python

``` shell 
pip install openai
```


```python
import os
import openai

openai.api_key = os.getenv("OPENAI_API_KEY")

response = openai.Completion.create(
  model="text-davinci-003"
  prompt="{calculate 2 + 2}",
  temperature=0.27,
  max_tokens=1553,
  top_p=1,
  frequency_penalty=0,
  presence_penalty=0
)
```

- **model** - openai have a several models for different task, this model oriented for response your question, also openai have models for generate code etc.
- **prompt** - your query for model
- **temperature** - value 0-1 raising the randomness.
- **max_tokens** -  Maximum length
- **top_p** - An alternative to sampling with temperature, called nucleus sampling, where the model considers the results of the tokens with top_p probability mass. So 0.1 means only the tokens comprising the top 10% probability mass are considered.
- **frequency_penalty** - Number between -2.0 and 2.0. Positive values penalize new tokens based on their existing frequency in the text so far, decreasing the model's likelihood to repeat the same line verbatim.
- **presence_penalty** - Number between -2.0 and 2.0. Positive values penalize new tokens based on whether they appear in the text so far, increasing the model's likelihood to talk about new topics.

***The model may return the answer in a slightly different structure, than you expected, and each answer offten different***
