## Survival Analysis as Time to Event Analysis

**Project description:** Survival analysis has an unfortunate reputation as a morbid topic, likely due in part to its relative popularity in medical literature and testing failure rates in manufacturing. However, it can also be used to analyze fun topics, like how seeing a meme ahead of time can affect a person’s ability to solve a riddle during a game.

### Initial Experiment
For my Experimental Design class, I created an experiment to test if seeing a meme would affect how quickly a person would solve a riddle during a LARP (Live Action Role Play) game. I did not anticipate some people giving up on a few of the riddles, so I had to reconsider my initial plan to use a simple linear regression. My professor suggested that I could instead analyze if priming with memes affected whether or not a person could solve the riddles or potentially look at using survival analysis. Naturally I decided to try to teach myself survival analysis, and I was able to produce a simple Kaplan-Meier curve. I expected priming with memes to affect a how quickly a person could solve the riddles, and while the results were not statistically significant, there is a clear difference in the curves of the primed and not primed groups.

<img src="images/Qac307Curves.png?raw=true"/>


### Revisiting The Work
I just finished taking a course on survival analysis, so I decided to revisit this analysis. Given the wildly varying difficulty levels of the riddles, I decided to use a Cox PH model so I could control for the riddle in the analysis. I also used INLA to produce a second Cox PH model using Bayesian methods to quantify the uncertainty in my model (I’m sure it will surprise no one that a sample size of 13 produced a model with a moderate at best level of uncertainty).

<img src="images/Qac307RiddleTime.png?raw=true"/>

If you want to learn more, [here is my code with some comments from my report for class](/pdf/QAC307Revisit.html), [here is the presentation I gave](/pdf/Final Presentation- Cimino.pdf), and [here is the updated version with the Cox PH models](/pdf/QAC307Cox.html).
