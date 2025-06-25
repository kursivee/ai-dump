# WORK IN PROGRESS
Paper in question: https://arxiv.org/pdf/2506.08872 Your Brain on ChatGPT: Accumulation
of Cognitive Debt when Using an AI
Assistant for Essay Writing Task
## Brain dump

Reading research papers is insanely hard because I have no background in writing any of this stuff. So I wanted AI to process this research paper and translate it to something more readable by gen pop. So first I read the abstract myself to get a better understanding of what it was about. I took some notes on what the abstract was trying to say at a high level. Then I tried uploading the PDF and asking it to translate the abstract. It gave something more like a summary cause it left out some important details. I tried asking it to translate again but this time I copy/pasted the abstract into the prompt. The copy/paste method seem to retain more detail around the study. I think it more or less did an acceptable job but something feels off to me. 

Ok I figured out what it was. So I have this idea that one key component of learning is the ability to take an idea and root it into something else. If I take the paper and translate it through chatgpt to a point to where I can understand it, sure I'll learn the gist of the paper but I won't learn about the more complicated topics that the paper brings up.

Take this excerpt from the abstract

```
We used electroencephalography (EEG) to record participants' brain 
activity in order to assess their cognitive engagement and 
cognitive load, and to gain a deeper understanding of neural
activations during the essay writing task. 
```

The chatGPT translation (more or less)
```
To see what was going on in their brains during writing,
the team used a device called EEG (electroencephalography).
This tool measures brain activity and helps understand 
how much mental effort someone is putting in—called cognitive
load—and how connected different brain regions are.
```

I think it's a good rephrase. The translation is definetly easier to digest than the original. But here's why this approach felt off to me. If I were to see the original excerpt in another paper, I would still probably be confused on what it was saying because I'm not used to it being said that way. I didn't learn how to map the more complex excerpt to something digestiable. I'd argue that I've essentially created a dependency on chatGPT to make that translation for me. I haven't read the paper yet but my guess is that this is what it's hinting towards. We're trading the process of obtaining information for information. We're trading how to obtain knowledge for knowledge. This is not something AI has to do. I think it's something we're inadvertantly letting AI do. 

 The goal shouldn't be to make complex things simple through distillation, it should be through improvement of self. Distillation is a technique for improvement, not a means to an end. 


 ## Better approach
 This is a prompt I gave ChatGPT to explain what my new approach is. I'll just put in raw cause I don't have a good way of forumlating it yet. I'm still piecing it together.

 ```
Use the paper for context if it applies too.
The idea here is for me to start at the beginning. Even though the paper has its own ordering,
chances are it's not going to make sense to me if I follow it.
So if I'm asking about EEG because of abstract, then bring up where EEG is used in
future parts of the paper if it will help me understand. 

Think of it like this, learning requires input from multiple sources. 
The paper provides the reason why I need to learn but the paper itself is
not set up to teach. So we need to deconstruct the paper in such a way that I 
can both learn and understand what the paper is saying. This involves having 
to learn from different sources like neuroscience articles or wikis. 
Or another way to put it, this paper is ordered by time. 
I need it ordered by function. Then I will learn each function in as much
isolation as possible. Then when I go back and read the paper in timeline order,
I will have enough information to see the interweaving of each function. 
I'll still probably be confused but I won't be lost.
```

To me this sounds right. I feel like I'm not doing anything novel here. This is basically how education works, America just does a shit job of tying things back together. I'm just leveraging AI to super charge the process.

After a bit of finagling, I got a response from chatGPT that looks to be close to what I'm looking for

### AI Response 1
```
⚡️What Are Alpha and Beta Waves?
🧠 EEG measures electrical activity—specifically, brain waves. These come in “bands” based on frequency:
Wave Type	Frequency (Hz)	Common Meaning
Alpha	8–12 Hz	Calm focus, alert but relaxed
Beta	13–30 Hz	Active thinking, problem-solving, engagement

    Think of it like tuning into a radio station.
    Alpha is the "steady focus" channel.
    Beta is the "engaged thinking" channel.

🔬 Why These Matter in Cognitive Tasks

    Alpha waves show up when your brain is:

        Internally focused (thinking, but not overwhelmed)

        Engaged in attention, visual processing, or semantic retrieval

        Found in regions like the parietal and occipital lobes during learning tasks

    Beta waves are linked to:

        Task engagement

        Working memory

        Executive function (e.g., planning, reasoning)

    So in learning scenarios, high alpha and beta activation = “I’m thinking hard and managing this info.”
    Low levels = “I’m not engaging deeply with the task.”

📍Back to the Paper

The authors say:

    “LLM-to-Brain participants showed weaker neural connectivity and under-engagement of alpha and beta networks.”

Translation:
Even after people stopped using ChatGPT, their brains were still showing less focused thought and effort, compared to people who never used it at all.

They also say:

    “Brain-to-LLM participants demonstrated... re-engagement of widespread occipito-parietal and prefrontal nodes... similar to the Search Engine group.”

So when Brain-only users switched to using ChatGPT, their visual and reasoning regions got less active—just like people who used ChatGPT all along.
```

It's got the description to help me digest what alpha/beta waves are. It explains why their relevant and then it relates it back to the paper. Not bad.