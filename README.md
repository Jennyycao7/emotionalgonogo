# Emotional Go-No Go Task

The following repository is a complete experimental task examining cognitive control, specifically the ability to withhold a prepotent behavioral response, and whether different emotional faces (happy or angry faces in our experiment) improve, decline, or have no effect on the ability to respond to and withhold from different stimuli. 

## The Emotional Go-No Go Task

The Emotional Go-No Go task has been commonly used to study how emotions impacts response inhibition and attention. For example, it has been used to study the developmental trajectory of people's ability to maintain cognitive control and consequently ability to emotionally regulate in the face of potentially interfering emotional stimuli. 

The basic idea is participants will respond to some stimuli (go faces) and withhold responses to others (no-go faces). Traditionally there is one go face and more than one no-go faces, with each facial emotion rotating as the go face. However for simplicity sake there are only 2 facial emotions present as stimulus in our experiment. 

## Emotions and Cognitive Control

Research on emotions and cognitive control suggests that negative faces (ie. angry) often slow responding as they engaged the amygdala and prefrontal regions differently. They also found that happy faces produce more commission errors when they are no-go conditions, as they have a positive valence and promote approach instead of inhibition. Some clinical groups also show less ability to inhibit than controls. 

## Project Overview

This experiment uses an emotional go-no go task to determine whether positive and negative valanced emotional faces (happy and angry respectively) affects i) commission errors - responding when you should have withheld, main measure of inhibitory control, ii) omission errors - failing to respond to a go stimulus, a measure of attention, and iii) reaction time - speed of correctly responded go trials, a measure of emotional bias. 

It is intended for use with a within-subject design, comparing performance for different facial expressions. Between-subjects analysis can also be used to explore a more general effect of facial expressions on cognitive control. The experiment can address differences in inhibitory control and attention in healthy controls, or, for future clinical relevance

## Experimental Designs

### Variables

#### Independent Variables
- Facial expression chosen for go and no-go (happy vs angry)
- Trial type (go vs no-go)

#### Dependent Variables
- Reaction time (for correct go trials)
- Go trials accuracy rate (%)
- No-Go trials accuracy rate (%)

## Experimental Blocks
- Participants will complete 2 practice blocks with 4 trials each (1 go, 3 no-go), with rotating facial expressions as go face
- They will then complete 2 counter-balanced main trial blocks with 20 trials each (16 go, 4 no-go)

## Parameters 
ITI_MIN = 0.5 # Shortest ITI between each trial
ITI_MAX = 1.0 # Longest ITI between each trial 
RESP_WINDOW = 1.5 # How long the participant has to respond for each face
FEEDBACK_DUR = 1.0 # How long 'Correct' and 'Incorrect' stays on when feedback is on
RESP_KEY = 'space' # The key corresponding to pressed
CONTINUE_KEY = 'return' # The key corresponding to advance
QUIT_KEY = 'escape' # The key corresponding to quit

## Parameters Customization 

### ITI_MIN and ITI_MAX
Affects how long the fixation cross stays on the window screen. ITI is a randomized float selected from a uniform distribution between ITI_MIN and ITI_MAX 

### RESP_WINDOW
Determines how long the participant has to press the response key for each trial for it to register. No response key pressed is also possible

### FEEDBACK_DUR
Determines how long the feedback screen is shown where applicable

### RESP_KEY, CONTINUE_KEY, QUIT_KEY
The various keys corresponding to recording a response to a trial, advancing across blocks, and quitting from the experiment respectively

## Running the Experiment
1. Open PsychoPy coder
2. Navigate to the project directory and open emotionalgonogo.py found in the emotionalgonogo/experiment file path
3. Run the code
4. Enter participant information (ID, Session number, Age, Gender) in the dialog box that appears
5. Follow the on-screen instructions

## During the Experiment
Spacebar: Press to indicate the facial expression in the trial matches the go face
No response: To indicate the facial expression in the trial matches the no-go face

## Analysis
The following can be analyzed from data within or across blocks and trials:

Accuracy: Hit rate, commission error, correct rejections, omission error
RT: Response time for hits and false alarms
Emotional effect: Compare all data between conditions (happy or angry as go condition)

Here is an example of the CSV for each participant:
<img width="640" height="749" alt="image" src="https://github.com/user-attachments/assets/512a61b2-d1a8-4f1e-ae7a-a106ac59a26f" />

For our experiment, we summarised go trials accuracy (%), no-go trials accuracy (%), and mean rt and standard deviation of rt of correct go trials. We also visualised 2 graphs: a bar chart showing accuracy (%) of go and no-go trials by condition (happy_go or angry_go), and a histogram showing the distribution of reaction times (s) of correct go trials by condition 

## Have fun with the experiment!
