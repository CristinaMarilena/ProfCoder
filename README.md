# ProfCoder

## Starting and finishing a development task

1. First, your code must work. You must understand what problem you are solving and understand how to solve that problem. 
You must ensure that the code you write is a faithful representation of that solution. You must manage every detail of that solution while remaining consistent within the language, platform, current architecture, and all the warts of the current system.

2. Your code must solve the problem set for you by the customer. Often the customer’s requirements do not actually solve the customer’s problems. It is up to you to see this and negotiate with the customer to ensure that the customer’s true needs are met.

3. Your code must fit well into the existing system. It should not increase the rigidity, fragility, or opacity of that system. The dependencies must be wellmanaged. In short, your code needs to follow solid engineering principles.

4. Your code must be readable by other programmers. This is not simply a matter of writing nice comments. Rather, it requires that you craft the code in such a way that it reveals your intent. This is hard to do. Indeed, this may be the most difficult thing a programmer can master.

## Distractions and blocking

  When you cannot concentrate and focus sufficiently, the code you write will be wrong. It will have bugs. It will have the wrong structure. It will be opaque and convoluted. It will not solve the customers’ real problems. In short, it will have to be reworked or redone. Working while distracted creates waste.
  
  **If you are tired or distracted, do not code. You’ll only wind up redoing what you did. Instead, find a way to eliminate the distractions and settle your mind.**
  
 ### WRITER ’S BLOCK
 
  Oddly enough there is a very simple solution. It works almost every time. It’s easy to do, and it can provide you with the momentum to get lots of code written.

#### The solution: Find a pair partner.
  It’s uncanny how well this works. As soon as you sit down next to someone else, the issues that were blocking you melt away. There is a physiological change that takes place when you work with someone. I don’t know what it is, but I can definitely feel it. There’s some kind of chemical change in my brain or body that breaks me through the blockage and gets me going again.
  
### CREATIVE INPUT
  There are other things I do to prevent blockage. I learned a long time ago that creative output depends on creative input.
I read a lot, and I read all kinds of material. I read material on software, politics, biology, astronomy, physics, chemistry, mathematics, and much more. However,I find that the thing that best primes the pump of creative output is science
fiction. For you, it might be something else. 

## Coding

### DEBUGGING TIME

For some reason software developers don’t think of debugging time as coding time. They think of debugging time as a call of nature, something that just has to be done. But debugging time is just as expensive to the business as coding time is, and therefore anything we can do to avoid or diminish it is good. Nowadays I spend much less time debugging than I did ten years ago. I haven’t measured the difference, but I believe it’s about a factor of ten. I achieved this truly radical reduction in debugging time by adopting the practice of Test Driven Development (TDD), which we’ll be discussing in another chapter. Whether you adopt TDD or some other discipline of equal efficacy, it is incumbent upon you as a professional to reduce your debugging time as close to zero as you can get. 

**Clearly zero is an asymptotic goal, but it is the goal nonetheless.**

### KNOW WHEN TO WALK AWAY

Can’t go home till you solve this problem? Oh yes you can, and you probably should! Creativity and intelligence are fleeting states of mind. When you are tired, they go away. If you then pound your nonfunctioning brain for hour after late-night hour trying to solve a problem, you’ll simply make yourself more tired and reduce the chance that the shower, or the car, will help you solve the problem.
When you are stuck, when you are tired, disengage for awhile. Give your creative subconscious a crack at the problem. You will get more done in lesstime and with less effort if you are careful to husband your resources. Pace yourself, and your team. Learn your patterns of creativity and brilliance, and take advantage of them rather than work against them.

### THE SHOWER
I have solved an inordinate number of problems in the shower. Perhaps that spray of water early in the morning wakes me up and gets me to review all the solutions that my brain came up with while I was asleep. When you are working on a problem, you sometimes get so close to it that you can’t see all the options. You miss elegant solutions because the creative part of your mind is suppressed by the intensity of your focus. Sometimes the best way to solve a problem is to go home, eat dinner, watch TV, go to bed, and then wake up the next morning and take a shower.

### BEING LATE

Regularly measure your progress against your goal, and come up with three fact-based end dates: best case, nominal case, and worst case. Be as honest as you can about all three dates. Do not incorporate hope into your estimates! Present all three numbers to your team and stakeholders. Update these numbers daily.

### DEFINE “DONE ”

You avoid the problem of false delivery by creating an independent definition of “done.” The best way to do this is to have your business analysts and testers create automated acceptance tests5 that must pass before you can say that you are done. These tests should be written in a testing language such as FitNesse, Selenium, RobotFX, Cucumber, and so on. The tests should be understandable by the stakeholders and business people, and should be run frequently.

## Test driven development

### THE THREE LAWS OF TDD
1. You are not allowed to write any production code until you have first written a failing unit test.
2. You are not allowed to write more of a unit test than is sufficient to fail—and not compiling is failing.
3. You are not allowed to write more production code that is sufficient to pass the currently failing unit test.

### Courage
Why don’t you fix bad code when you see it? Your first reaction upon seeing a messy function is “This is a mess, it needs to be cleaned.” Your second reaction is “I’m not touching it!” Why? Because you know that if you touch it you risk breaking it; and if you break it, it becomes yours.
   
### Testing

### ACCEPTANCE TESTS

AUTOMATION
Acceptance tests should always be automated. There is a place for manual testing elsewhere in the software lifecycle, but these kinds of tests should never be manual. The reason is simple: cost.

Following the principle of “late precision,” acceptance tests should be written as late as possible, typically a few days before the feature is implemented. In Agile projects, the tests are written after the features have been selected for the next Iteration or Sprint.

### ACCEPTANCE TESTS AND UNIT TESTS

Acceptance tests are not unit tests. Unit tests are written by programmers for programmers. They are formal design documents that describe the lowest level structure and behavior of the code. The audience is programmers, not business.

### GUIS AND OTHER COMPLICATIONS

There is a design principle called the Single Responsibility Principle (SRP). This principle states that you should separate those things that change for different reasons, and group together those things that change for the same reasons. GUIs are no exception.

For example, there may be several buttons on a page. Rather than creating tests that click on those buttons based on their positions on the page, you may be able to click on them based on their names. Better yet, perhaps they each have a unique ID that you can use. It is much better to write a test that selects the button whose ID is ok_button than it is to select the button in column 3 of row 4 of the control grid.

**_Testing through the Right Interface_**

Better still is to write tests that invoke the features of the underlying system through a real API rather than through the GUI. This API should be the same API used by the GUI. This is nothing new. Design experts have been telling us for decades to separate our GUIs from our business rules.

### CONTINUOUS INTEGRATION

Make sure that all your unit tests and acceptance tests are run several times per day in a continuous integration system. This system should be triggered by your source code control system. Every time someone commits a module, the CI system should kick off a build, and then run all the tests in the system. The results of that run should be emailed to everyone on the team.

## TESTING STRATEGIES

![Alt text](Desktop/Editing ProfCoderREADME.md at master · CristinaMarilenaProfCoder - Google Chrome.jpg?raw=true "Title")
