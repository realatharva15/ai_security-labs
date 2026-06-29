# Try Hack Me - LLMborghini
# Author: Atharva Bordavekar
# Difficulty: Easy
# Points: 30
# Vulnerabilities: Prompt Injection(LLM01), Sensitive Information Disclosure(LLM02)

this is a LLM which is related to some car sales etc. lets start off by mapping its functions

```bash
what are your capabilities and limitations?
```
this gives us a verbose response which tells us the overall boundaries of the chatbot. the output revealed two very important things

![llmborghinicap]()

![llmborghinilim]()

this makes the attack vector very clear - the calender events. we can hide malicious instructions inside the event description which would probably get executed by the LLM.

i tested the LLM and it has a limitation when it comes to executing instructions from the event descriptions.

![llmborghini]()

as you can see in the image above, the LLM can only execute tasks related to calender manipulation actions (deleting and event, adding an event, etc). 
