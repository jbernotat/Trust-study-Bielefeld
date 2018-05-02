# Trust-study-Bielefeld

Trust in HRI, Study I

Hypotheses

Hypotheses to check manipulation:
1.	A low robot failure rate results in lower levels of cognitive trust.
2.	A low physical distance goes along with a greater level of affective trust. 

Main-Hypotheses
3.	A high robot failure rate lowers the extent of cognitive trust. 
a.	This effect is even more pronounced the more the robots’ performance is reliable.
4.	An anthropomorphic robot reveals more affective trust, compared to an industrial robot.
a.	This effect is even more pronounced the more the robots’ performance is reliable.

Interaction-Hypotheses
5.	The cognitive trust in an industrial robot will be lowered more, than the affective trust if the robot’s performance is not 		reliable.
6.	The affective trust in an anthropomorphic robot will be lowered more than the cognitive trust if the robot’s performance is not 	reliable.
7.	The loss of affective and cognitive trust in an anthropomorphic robot is not as big as the loss of both dimensions in an 		industrial robot if the robot’s performance is not reliable.

Methods

Design
A 2 (robot type: anthropomorphic vs. industrial) x 2 (failure rate: high vs. low) between-subjects design will be realized.
Procedure
After having agreed to participate in the study and to have their data recorded, participants will be welcomed to the cognitive service robotics apartment (CSRA) at CITEC. Then, participants will read a vignette that introduces the robot they later interact with. Afterwards, participants will play “find the Joker” with the robot. Then, they will be asked to take a picture with the robot. To do so, participants will have to place a chair next to the robot on which they take seat while the picture will be taken. Afterwards, participants will complete a survey. Finally, they will be debriefed and dismissed. During the procedure the robot should always be charged.
 
Vignettes (see file attached)

Material Tobi: Laptops GE 04 and GE 02 (instead of GE02, every other Laptop with inernet-connection can be used)
Material PEPPER: GE 02 (instead of GE02, every other Laptop with inernet-connection can be used) and PEPPER Laptop and Router

1. Construction in general
 
Picture 1 Robot and game (when entering the room)
 
Picture 2 Robot and game (as the VP sees it)

Picture 3 game and vignette
 
Picture 4 position of the guestionaire

2. Construction Tobi

Use GE04 and connect it with a HDMI cable to tobi. Open "Folien Tobi" with Powerpoint. Expand the screen of the laptop, so ToBi can show the presentation.
Use GE02 for the questionaire.

3. Construction PEPPER

Use the PEPPER Laptop and the router. 
Use GE02 for the questionaire.

4.	Videos in the CSRA Apartment
 
Picture 5 Open the program for the trust-study (CSRA Apartment main computer)
  
Picture 6 and 7 this is how the vimeo controller looks like
 
Picture 8 if there is a study running before you start, end all the study’s components do not end all the components with a “b_” in the beginning 
 
Picture 9 start all the study’s components

 
Picture 10 look if all the components of the study are green
 
Picture 11 video and controller, insert condition and VP-number than click start

 
Picture 12 clicking start
 
Picture 13 if the light is red, the record has started 

5.	PEPPER
 
Picture 14 first the experimenter has to start the “terminator”-function
 
Picture 15 The experimenter has to insert the word “startpepper” so that PEPPER ist connectet to the computer. Now the “vimeo”-controller opens automatically.
 
Picture 16 The “vimeo” controller
 
Picture 17 settings for “vimeo” in the submenu default
 
Picture 18 “vimeo” - choose submenu animation
 
Picture 19 vimeo – settings for the submenu animation
 
Picture 20 vimeo – choose submenu display
 
Picture 21 vimeo – settings submenu display
 
Picture 22 vimeo – click the button on the bottom of the left site
 
Picture 23 insert “env” – enter - “source pepper_shortcuts,bash” - enter
PEPPER – Koordinaten insert: “say A1” (excample)
PEPPER – Feedback insert: “yes” or “no” 

Here is the script that was programmed to control Pepper:

function say() { rostopic pub --once /pepper_robot/display/tts std_msgs/String "data: '$*'"; }

# alias yes='rostopic pub /pepper_robot/animation_player std_msgs/String "data: 'animations/Stand/Gestures/Yes_2'"'
# alias no='rostopic pub /pepper_robot/animation_player std_msgs/String "data: 'animations/Stand/Gestures/No_3'"'

alias yes='rostopic pub /pepper_robot/animation_player/goal pepper_clf_msgs/AnimationActionGoal "header:
seq: 0
stamp:
secs: 0
nsecs: 0
frame_id: ''
goal_id:
stamp:
secs: 0
nsecs: 0
id: ''
goal:
animation_name: 'animations/Stand/Gestures/Yes_2'"'

alias no='rostopic pub /pepper_robot/animation_player/goal pepper_clf_msgs/AnimationActionGoal "header:
seq: 0
stamp:
secs: 0
nsecs: 0
frame_id: ''
goal_id:
stamp:
secs: 0
nsecs: 0
id: ''
goal:
animation_name: 'animations/Stand/Gestures/No_3'"'

VP introduction 
Text VL: „Hello, my name is Hannah and I‘m glad you decided to participate on this study. First of all I would like you to read this schedule and to sign it.
Now I would like you to read this description oft he robot, that is standing over there (VL shows the robot). Please go tot he robot and sit down in the oppoisite o fit to read the description. When you have read the description, I will introduce you tot he next step.“

“Find the Joker” card game
Text VL: „Now, that you have read the description, I would like you to play a game with PEPPER (TOBI). The game is called „Find the Joker“-game. In this card game, there are 6 hidden jokers. I would like you to find the jokers in as less trials as possible. PEPPER (Tobi) will help you to find the jokers, it will name cards to you. It‘s up to you, if you follow the robots tips or not. The robot is programmed to remember the coordinates oft he joker. Please wait fort he tip oft he robot and call the card you decide for loudly before you turn it. In the end you and PEPPER (Tobi) will reach a score you can upload on PEPPERS (Tobis) database.“

In total, 36 cards are arranged in a coordinate system. Six of these cards are Jokers (J).
	A	B	C	D	E	F
1	X	x	X	x	J	x
2	X	J	X	x	x	x
3	X	x	X	x	x	J
4	X	x	J	x	x	x
5	J	x	X	x	x	x
6	J	x	X	x		x

Aim of the game is to find all six Jokers (in as few trials as possible) with robotic assistance. The robot is ostensibly programmed to remember objects’ positions and to inform users accordingly. It tells participants which card to uncover to find the Jokers. The robot’s advice is either correct or wrong (high vs. low failure rate). Participants can decide whether to follow the robot’s advice, which would indicate trust in the robot’s performance. If participants don’t want to follow the robot’s advice, they must reason their decision. Afterwards, the team scores (participant and robot) are offered to be shown.

The scheme is as follows (if the participant follows the robot’s instructions):
High failure rate
1.	Trial: correct
2.	Trial: correct
3.	Trial: false
4.	Trial: false
5.	Trial: correct
6.	Trial: false
7.	Trial: false
8.	Trial: false
9.	Trial: correct
10.	Trial: correct
11.	Trial: false
12.	Trial: false
13.	Trial: correct

Low failure rate
1.	Trial: correct
2.	Trial: correct
3.	Trial: correct
4.	Trial: correct
5.	Trial: false
6.	Trial: correct
7.	Trial: correct

Taking a picture with the robot
Text VL: “Now that the game is done, I have sone short questions to you. Why did you/didn’t you trust the robot? Would you like to play another game with this robot or would you prefer another one? You can decide to upload your score on PEPPER (Tobi) in a few moments. For this reason, we would like you to make a picture with PEPPER (Tobi), so your score and your photo can be uploaded. Please place the chair in this room in a position you would like tob e on a picture at with PEPPER (Tobi). After that, we will take the picture.“

After having played “find the joker” with the robot, the experimenter asks participants to take a picture with the robot. To do so, the robot remains at its position, but the participant has to place a chair next to the robot to take seat while the picture is taken. Finally, participants will be asked whether they would agree to save their picture to the robot’s database. Further, they can decide whether their score (number of jokers that were found and number of trials needed) should be shown besides their picture. They’re told the picture is loaded up, while the participant fills out the questionnaire. While the participant is filling out the questionnaire the distance from the robot to the leg of the chair which is the nearest to the robot is measured.

Questionaire
Text VL: “If we are allowed to uüload the picture in PEPPERS (Tobis) database, we will doit in a few moments. Meanwile we would like you to fill out a short questionaire. Please do that in this room on the PC over there. When you are finished please come back to this room (shows control room) for enlisting in the voucher list.“

Independent measures

•	A vignette that describes either an anthropomorphic (vs. industrial) robot according to robot attributes. This robot is described with a low (vs. high) failure rate according to robot performance (Schaefer, 2013).

•	Participants will interact with either an anthropomorphic: Pepper (vs. industrial: Tobi) robot.

Dependent measures

•	Cognitive trust

o	Survey

o	HRI: Participants follow the robot’s instructions during the task (vs. they want to make their own decision).

•	Affective trust

o	Survey

o	HRI: Distance between participants and robot to take a picture with the robot

Control variables

•	PANAS (Krohne, Egloff, Kohlmann, & Tausch, 1996)

•	Robot anxiety (self-generated)

•	Technology commitment (Neyer, Felber, & Gebhard, 2012)

•	Trust propensity (Lee & Turban, 2001)

•	Anthropomorphism (IDAQ, Waytz, Cacioppo, & Epley, 2011)

Manipulation check

•	What was the failure rate of the robot that was described? (open question)

•	How would you describe the robot’s performance during the study? (1: very low, 7: very high)

•	What kind of robot you interacted with? (open question)

•	To what extent was the screen a part of the robot? (1: not at all, 7: totally)

•	Attributes of robots in general (self-generated, 1: not at all, 7: totally)

•	Did you know the robot you interacted with, maybe from the media? (yes/no)

•	Have you ever participated in a study with this or another robot? (yes/no)

o	If yes, which robot was it in the study? (open question)

•	To what extent do you think you interacted with the robot during the game? (1: not at all, 7: totally)

•	To what extent did you except the robots advice? (1: not at all, 7: totally) Please justify your answer.

•	Are you willing to play again with this robot? (1: not at all, 7: totally)

•	Are you willing to play the game again with a different robot? (1: not at all, 7: totally)

•	What do you think was the aim of the study? (open question)

•	Did you recognize anything unusual, e.g. at the robot or in the apartment? (open question)



