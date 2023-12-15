# Kat's Weekly Reports

## Week 14[11/30-12/7]
This week Kanchan and I worked together to refine the visuals and add more visual and audio elements in the interactions. We trained the gesture recognition algorithm in Edge Impulse.
See our project video: https://www.youtube.com/watch?v=w3z2xJe8K5Y&ab_channel=KatherineLiu


## Week 13[11/23-11/30]
This week I worked on the game design. 

<img width="900" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/803517a9-3e17-499a-b383-59c8f01e9870">



## Week 12[11/16-11/23]
This week I configured the accelerometer to and successfully connected it to p5.js.
Connection and library reference: https://github.com/rickkas7/ADXL362DMA

<img width="400" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/72431456-97b8-44af-ae3a-feec1ddaa9b6">


Connecting photon to p5.js using API call: https://github.com/alblaine/particle-photon-P5-example/blob/master/README.md
I tested with the accelerometer and used it to rotate a box in p5.js: https://editor.p5js.org/katherine_liu/full/FgXO-HtwP



## Week 11[11/09-11/16]
This week I did more research on my final project proposal and started experimenting with the sensors. 

### Sensors
**Accelerometers:** measure linear motion in X, Y, or Z. They can be used to detect when they are being moved around, detect motion, shock or vibration. They can also be used to detect gravitational pull in order to detect orientation or tilt.

**Gyroscopes:** measure rotational motion in X, Y or Z. 

**Magnetometers:** sense where the strongest magnetic force is coming from, generally used to detect magnetic north, but can also be used for measuring magnetic fields. When combined with accelerometers and gyroscopes you can stabilize orientation calculations and also determine orientation with respect to the Earth.

**IR sensors:** distance

**Force sensor resistor:** pressure 

**Ultrasonic sensors:** distance


#### most prominent: ADXL362 (GY362) accelerometer breakout
    
    https://docs.particle.io/reference/datasheets/accessories/edge-ml-kit/#adxl362-gy362-accelerometer-breakout 
    Motion detection library https://github.com/rickkas7/ADXL362DMA 

### Communication between the photon and the console
    
    Make an API call in P5.js and store the reading as a variable: 
    https://github.com/alblaine/particle-photon-P5-example/blob/master/README.md 

I also looked into the history of the development of motion game controllers. This video has been super helpful: https://www.youtube.com/watch?v=fGjlhNzZSYQ&ab_channel=nimk
Some prominent figures are:

<img width="400" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/8f6dea17-fecc-47f6-99f5-22d003625733">

Some popular games that involve motion control:

<img width="400" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/b1fa640a-e04b-486c-b929-e71b252a85d3">




## Week 10[11/02-11/09]
It was great to see a cohort of MiniMe projects from last week's presentation. Now it's time to synthesize all the technology we have been playing with and make something fun and useful!

For the final project, I want to create a motion-controlled game that allows players to interact with the game through physical movements. Sensors and microcontrollers will capture physical input from the user and translate it into in-game actions. This project will also involve the design and fabrication of the physical interface of the controller/ accessory. The game will be programmed in P5.js and web-based. 

## Week 9[10/26-11/02]

**Insights from 10/16 Peter's talk:**
🟡What's the best practice to break the knowledge sets into different chunks to optimize the response performance?
- 3-500 tokens
- considering the use case
🟡Use the welcome message to recognize who the bot is talking to and use instructions to ask the bot to talk in different ways based on the answer 

I decided to build a personal cover letter generator that can parse a job listing and extract relevant aspects from my experience, projects, and school courses,

Some problems with the existing cover letter generator: 
- Generic Content 
- Outdated templates
- Lack of personalization
- Limited consideration (on work experiences, overlooking skills gained from design projects and courses)

A good cover letter generator should: 
- Identify both technical and soft skills needed for the job
- Understand nuances between varied positions in different industries
- Extract relevant pieces from my professional experiences, projects, and course
- Gracefully address potential gaps if my experience doesn't align closely with the job description
- Research on company values and express my personal alignment with the company

I used those as the basis for the general instruction for the bot.

<img width="900" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/640e5fce-b8f3-492f-ac76-3f351ed25938">

I also added a separate instruction that specifically addresses how the bot should write.

<img width="900" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/da5912b0-0c27-48a8-b7dc-233821212863">

For the knowledge set, I curated my professional experiences, education backgrounds, skills, course content, and design projects. 

<img width="900" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/88f2ddb4-7194-4500-adbe-0e43ffe676c0">

Here are some detailed adjustments to tune the model:

<img width="600" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/9aebd5c2-aecf-441b-a6ca-b4132f312f63">

- I wrote additional detailed instructions to make sure the bot provides the right info and speaks as preferred
- I allowed the bot to pull as much information as it needs to make the accurate pair between my skills and the job listing
- I set the temperature, the "creativity" dial, to 0.7. So that it produces coherent, professional, and relevant content while taking a bit more randomness, which can be helpful for roles in creative industries.

**Variations: Compatibility Checker**
Normally people regard a cover letter as just an extra work to do during the job application and believe resume and portfolio (for designers) are more important. I don't disagree with that. But I do think cover letter is a good space to reflect on yourself.


## Week 8[10/19-10/26]
This week we started working on Project 3 to design a mini ME using Large Language Models. 

Our guest speaker had a very informative presentation on how LLM functions and a detailed walk-through to demonstrate how we can play with it using Zero Width. 

Some insights from Peter's talk:
- LLMs know how words relate statistically, but not what they mean. In essence, the only thing LLM does is to fill in the blank.
- A token is a unit or chunk into which text is divided for analysis.
- Retrieval-augmented generation is an AI framework for retrieving facts from an external knowledge base.
- In this project, we will be largely working on **fine-tuning** the LLM, which is to give specialized instructions based on the given dataset to train the model to be a little more "intelligent."
  <img width="700" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/13299148-31f8-4648-a788-fa8e12ed4e19">
- LLM understands the prompt based on semantic space:
  <img width="700" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/a4da50f2-a239-49ed-9a53-4a7ebab6840e">

Zero Width has a straightforward interface to start with:
<img width="900" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/c2e49fde-6ea3-4fd4-b445-2a0e5460f409">


Following Peter's instructions, I created a new knowledge set with information on our course projects from the class wiki and linked it to the instructions.

<img width="400" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/5a411036-c032-4e30-aec7-666096431468">

<img width="400" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/e73f9b3f-fa34-48d3-9740-5194ff14cd3c">


Then I went to the demo page and tested if the database had been incorporated:

<img width="500" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/4780c255-e89a-438a-822e-f0ed24e76576">

It turned out the bot was able to pull the knowledge perfectly. However, it took nearly a whole minute to generate the answer, and the answer was very chunky and cumbersome which was difficult to get a clear grasp of the idea. So I asked the follow-up question:


<img width="500" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/5e5b5920-29c7-4a30-827e-ab11eceb63fd">

So the bot is able to relate to the context of the speaking (i.e. connecting to previous questions) and re-pull the relevant dataset:

<img width="500" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/38e854c3-5a5f-4f3a-856b-eb6890f11a2a">

There are two questions that come out of  playing with Zero Width:
1. How can we optimize the response time of the bot? Do we manually break down the knowledge sets into smaller chunks?
2. How can we adjust the length and richness of the response content? Is there a parameter that we can use?





## Week 7[10/12-10/19]
This week we have been on the final stage of designing our magical Photon gear!

I started looking at OLED and trying to make it display positive messages. This part has been one of the biggest challenges of the project. Before I soldered the OLED pins, I was not aware of the option of using the Stemma QT connector which would make the connecting and debugging part much easier. While I had the code to flash and run smoothly, I struggled a lot with no content showing on the display screen. Thanks to Jeff who had multiple debugging sessions with us,  we eventually recognized that there was a problem with the port and device name and made the OLED to function.

I brainstormed with Emily on our new physical interface. On the top is the sketch done by Emily. Then I went to Adobe Illustrator to draw out our shapes for laser-cutting the box. 

After Stephanie finished laser-cutting the box, we gather together to test the photoresistor placement and assembled the complete functional piece.


<img width="300" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/f38b56e6-ccd7-4c37-8df3-b3f5d2df46ab">
<img width="300" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/9f03ee58-3311-45ff-8152-b281ea4d50cb">
<img width="300" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/33524be1-5966-4405-aaaf-3f89eb442f28">
<img width="300" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/18a3eac4-0538-438b-a87c-7169ad351510">

## Week 6[10/05-10/12]
This week we worked on more details on the electronics and re-scale our project.

As we looked more into the shredding part of the project, we realized that we needed a more powerful torque servo and needed to re-design the gears to fit the manual shredder. To build a more creative output rather than basically reverse engineering an auto-shredder, I proposed to use a vibration servo to simulate the shredding experience. For the printing part, we decided to use an OLED display for the first prototype to show the positive messages. 

Emily synthesized our updated idea into a therapy cat, which will swallow negative thoughts, show reactions of digesting (vibration,) and display a positive message on its belly (OLED.) Based on the updated proposal, I organized and drew the flow chart of computation.

<img width="700" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/ca7a42b7-f4e5-440c-8e5d-603666e3a946">



## Week 5[09/28-10/05]
This week I worked with my team members to specify our vision on Project 2. 

Based on our theme of "Exploring Mental Health Needs of Graduate Students," we decided to design an “emotional vending machine,” which is a unique combination of a shredder and a printer. Users will jot down their negative feelings on provided index cards, put them into the shredder, and in return, receive cheerful and uplifting messages printed out to lift their spirits. We will collect the cheering messages from the cohort community to form a database and feed it to the printing system.

Here is the flow chart of the basic mechanism. 

<img width="300" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/508434c0-65bd-49a3-adc5-0fe1ecfdf526">

We went to the makerspace and talked to the design specialists for advice. Here are some sketches of the whole structure from brainstorming. (Sketch 1 done by Shayne, Sketch 2 done by Cody, Sketch 3 done by Chris)

<img width="200" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/e90a9fa5-7bad-4dd7-ba1a-e14d9dbcf0ac">
<img width="200" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/2c5f9abc-902a-4b4d-8685-bf8409958a6e">
<img width="200" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/84278983-4043-4145-965d-42203aaf4512">


#### Testing the sensors
In order to turn on the manual shredder, we need a sensor that detects the approaching of the paper near the entrance. Me and Emily tested both the photoresistor and the ultrasonic sensor with code. 

<img width="200" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/65a6edaf-45f0-4028-9c19-fd60c2f9cfce">
<img width="200" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/e0d5eadb-a53f-4320-a464-c8e0393bed1f">
<img width="200" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/fef4adbb-3711-4059-a89b-63c5edd92533">



## Week 5[09/21-09/28]
This week I explored more of the Photon Kit, and connected it to the developing space.

This is the first class exercise where we set the breadcrumb and wrote the code to flash the LED bulb.
A video of the working kit can be seen https://youtube.com/shorts/-VTYeR_i7Kg?feature=share

This is the second class exercise where we defined variables and added more dynamics to the flashing. 
Here is my code, where it only flashes the LED when the analog value is greater than 1000. I used the monitor console to determine the threshold value.

<img width="300" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/99380194-c4a2-473b-857b-6a91f4108826">
<img width="300" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/5183276c-69f6-4cba-b71c-ce12cd5f7250">


https://youtube.com/shorts/Yz4j4J56VDo?feature=share

## Week 4[09/14-09/21]

This week we started to look at physical computing!

I successfully set up my Photon 2, connected it to the campus IoT network, and tested some starter code!

<img width="300" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/14ee03bd-d2fe-45c1-bfc2-7cb51461583e">

<img width="300" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/1c73d563-e815-4a54-a507-38b52fee0e95">


## Week 3 [09/07-09/14]

This week I personalized my phone stand design and went for print!

Here are my final rendered models.

<img width="300" alt="image-of-stands" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/2abf9f27-53f3-475f-8ac7-43ab2ec1de3a">


Since I was using Form3 printers, for which I had to pay for the material, I tried to simplify the shape and minimize the volume. I used the "shell" commands in Rhino to remove the bottom of my initial design to make it hollow inside. I also created a streamlined version that gets rid of the outer sphere and only keeps the key center structure. 

<img width="300" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/a3bcc721-c590-4053-b6a2-f2e968dd72f2">

For the circular phone stand, I used Grey tough 1500 v1 resin, and for the streamlined, I used Clear v4 resin, which was very lightweight and took much less time to print and cure. Thanks to Charon and Reina who assisted me in removing the tough support material! It took a joint efforts of us three. 

<img width="300" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/eee8d3eb-7e0a-4311-b320-4f81f78cd4bb">

Here are the final products.

<img width="300" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/a659b619-bc7e-475d-9bb7-7ff4901f1ad6">
<img width="300" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/14ba256b-38f9-40d4-9ba0-f67b58b063f1">

Here is my brief video about the process. https://youtu.be/HrWu8Tms1RY 

## Week 2 [08/31-09/07]

This week I learned more about Rhino and Grasshopper through online tutorials. 

TJ's walkthrough of the simple phone stand design is especially helpful. 

<img width="300" alt="grasshopper2" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/3878733c-e3dd-4129-903e-9d2818bdff7a">


As I become more familiar with Grasshopper, I feel more confident to play with the parameters and start to how I can incorporate my own aesthetic and design into the given sample. 

<img width="300" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/3ee693df-38ea-4970-8cb7-963ef5fd573e">

<img width="300" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/2d3c14a8-e02a-4de8-9a80-1a7a1660fbcd">

I'm also exploring the use of python and c# in grasshopper to create more intricate geometries. 



## Week 1 [08/24-08/31]

### Reflections

This week I used laser cutting to make a phone stand.

<img width="300" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/143938d9-3b3b-4c09-99e8-834e25a4a160">



#### Rhino and Grasshopper

The computational design is completed via Rhino and Grasshopper. I've never used Rhino or any 3D-modeling design tools before. The interface was a bit intimidating when I first opened it. 

<img width="300" alt="grasshopper2" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/ccbea282-debc-4aa9-b2cf-ce5077de3186">

I got more comfortable with navigating the files after the tutorials in class and online. During my laser-cutting session, I had a clearer vision of Grasshopper files as Cody provided more industrial practices and tips, such as grouping and organizing modules and disabling unnecessary functions.  

<img width="300" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/f11ba455-46b6-44f6-a551-ebe56ac2659f">


<img width="300" alt="image" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/94c74757-32a6-4070-a200-bd84290078a4">





Here are some sweet points that I encountered during my exploration.
1. Feedback/Warning on infeasible model

   When I was playing with the parameters, I dragged the bar to extreme low/high points. The main object in the view turned red as a warning     of an infeasible design.
   
   <img width="300" alt="rhino1" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/e3c2f4b6-5e6f-4c00-945b-6267707e2ee9">
   
   <img width="300" alt="rhino2" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/a3293c39-fb21-4235-8182-ff24f9f88601">



2. Locating arrows when searching in Grasshopper.

   <img width="300" alt="grasshopper1" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/17d337de-02c2-4c92-9fe9-4199d9bfc683">
   
   While I was terrified by how complex the Grasshopper module was, I was glad and surprised that there were those tiny arrows that helped you locate the modules you are looking for in real-time. This feature is by far the most smooth and considerate one I encountered in     Rhino/Grasshopper...






#### Illustrator

<img width="300" alt="illustrator-view" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/1bac1133-5780-432c-a0d5-3fa37c24802e">

Since I had some experience with Adobe Illustrator before, I did some edits that I was unconfident about making in Rhino. I curved the corners and customized a rasterized 'K' at the front of the base. 






#### Laser Cut and Outcome
<img width="300" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/28a28e7e-856c-4965-944a-85c10119a3ea">
<img width="300" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/ccf4ad3d-45b1-4522-9249-e82d553a1144">
<img width="300" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/1b976aa1-f37a-4853-9306-b90c31f328b2">
<img width="300" src="https://github.com/Berkeley-MDes/tdf-fa23-katherine-liu0/assets/139127563/769fdb75-3d0d-4c01-ad58-9c73b1a10d13">





### Speculations
While Rhino is an extremely powerful tool in professional 3D design, it requires a high learning curve which is not rookie-friendly. I would prefer built-in tutorials (such as those Adobe Suite would provide when you first enter the software) to provide a vision of the affordances of the software. Even if the tutorial can only provide very basic things, it would make the user feel more confident and welcomed. 

As someone not professional in 3D modeling and only considers casual creation and rapid prototyping, I prefer more lightweight and AI-assisted tools. I have tried Spline 3D, and now they also offer the feature of AI prompts, where you can simply type in text commands, and the AI will create and edit the objects for you. See https://spline.design/ai. Of course, Spline 3D could not be compared to Rhino in terms of versatility and professionalism. But it's a cure for amateurs and a great help for quick prototypes. 
