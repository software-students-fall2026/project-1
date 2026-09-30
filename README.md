# Specification Phase Exercise

A little exercise to get started with the specification phase of the software development lifecycle. In this exercise, your team specifies a set of improvements and new features for [The Slide Machine](https://theslidemachine.com) — see the [instructions](instructions.md) for detail, and the [background](background.md) for an introduction to the software product you are tasked with extending.

## Team members

David Romero – https://github.com/Icegolem4
Sally Hegab – https://github.com/sallyhegab 
Biniam Tsige – https://github.com/BTSM10
Bereket Demeke - https://github.com/Bereket-454
Saajid Rohman - https://github.com/sar9249

## Review of the Current Application

1. **Strength:** The quiz generation feature worked well and produced useful quizzes.
2. **Gap:** There is no easy way to automatically send generated quizzes to students.
3. **Gap:** There is no way to see how many tokens are being used while presenting.
4. **Weakness:** The app sometimes separates content into different slides even when the ideas should remain together.
5. **Strength:** The app accurately transcribed and displayed mathematical formulas.
6. **Weakness:** The AI voice did not read mathematical formulas aloud.
7. **Strength:** Speech recognition was very accurate during presentations.
8. **Strength:** Being able to edit the live transcription was helpful.
9. **Gap:** The app only transcribes speech and generates slides in English.
10. **Strength:** The app translated English content into other languages well.


## Prior Art & Originality

We read the open questions and future works sections of the specification documents of the slide machine. We found that although some concerns our stakeholders had were set to be covered in the future, none of our specific proposals are already planned.

## Stakeholders

### Michael – Professor

When Michael was using the slide deck, I noticed that every time he was moving on to the next topic he would say “next slide.” This would usually create a new slide. However, once he actually started talking about the next topic, the slide machine would create a further slide for the new information, leaving the prior slide blank. I also noticed he talked slower than normal to make sure the slide machine got it. In addition, he felt the need to edit the slides once he was done with the presentation to fix and rearrange things.

#### Michael’s four frustrations:

- He felt the slides dumbed down what he was saying
- He felt like there were slide editing mistakes. Telling the machine to turn a slide into bullet points, split a slide into two, or make a new slide didn’t always work as intended. 
  - There is already a feature to change the format of the slide (into bullet points for example) manually with your mouse, but it didn’t work well with his voice.
- Since the slides weren’t made yet, he couldn’t reference them to remind him what his next topic was. 
  - He needed to make his own outline in a third party app to reference.
- Slide pacing mistakes. The slide would jump forward to topics he hadn't introduced yet.

#### Michael’s four goals/wants:

- He wants to be able to iterate on his presentation in the app. He wants to present the same slide deck multiple times, with the AI having access to his previous practice attempts. That way he can practice giving the slides easily, and the AI has more information on them once he presents them for real.
- He wants to be able to hook in a youtube video.
- He wants to be able to restrict what licenses the AI is allowed to find images with. He could ban licenses that don’t let you use the image commercially, for example
- He wants a different mode for creating the slide vs. editing it once he is done speaking

### Kujo – Student

I gave Kujo a presentation while using the slide machine app as if I was one of his professors, and then sent him an exit ticket quiz to fill out. I noticed that at first he was shocked every time a slide ‘magically’ appeared, but by the end he was just listening as normal. I emailed the exit ticket quiz and at first he didn’t have access to it because he was logged in from a non-nyu account, so I had to edit the quiz settings. Once he got access he said he liked the quiz system and enjoyed that he could do it on his phone on google forms. He didn’t do as well on the quiz as I thought he would, and he said it was because it was hard to pay attention sometimes. Often once the slides for one topic had been generated I’d already have moved on to the next topic, so he felt he had to choose between reading what was on the slides or listening to what I was saying.

#### Kujo’s four frustrations:

- Slides generated too late to always be relevant to what I was saying.
  - He felt he had to choose between reading the slides or listening to me.
- He felt like the slides were dumbing down what I was saying.
- He felt like the slides didn’t add anything, since they didn’t go into more detail than I did.
  - There is a slider that can change how much extra detail the AI can go into. This presentation was given on the default setting.
- He felt like if a professor was actually using this app it wouldn’t inspire him to try hard in the class: “why would I do the work if the professor won’t even make a presentation?”

#### Kujo’s four goals/wants:

- His biggest want was if the AI could summarize the presentation into a notes sheet that could be handed out after. 
  - He finds studying from a notes sheet is much better than a slide deck.
- He wants the slides to be more in-depth.
- He wants the slides to generate faster.
- He wants a more engaging visual theme
  - There is a setting to import themes from google slides. This presentation was given on the default theme.

## Product Vision Statement

We will improve the customizability of the software by allowing professors to better specify how they want their presentations to come out and students better specify how they want to interact with the professor and slides.

## User Requirements

### Professor User

- As a professor, I want to be able to make the Slide Machine go to the next slide so I can more accurately split up my presentation.
- As a professor, I want to be able to stop the Slide Machine from going to the next slide so I can keep all the info for one topic on one slide.
- As a professor, I want to enter a prep mode to easily create a skeleton for my presentation.
- As a professor, I want to create an outline in prep mode with each topic and the order I will be presenting them in so the AI can accurately follow me without jumping around.
- As a professor, I want to be able to edit my outline so I can change my plan if I have a better idea.
- As a professor, I want to be able to delete my outline in case I want to start a new one.
- As a professor, I want to create a project which can hold multiple presentations so I can iterate on my presentations without deleting them.
- As a professor, I want to be able to present another presentation in the same project so that I can practice giving my presentations multiple times, and so the AI has access to all other presentations in the same project and can more accurately follow me.
- As a professor, I want to be able to delete past presentations in one project.
- As a professor, I want to be able to save a presentation to a specific project.
- As a professor, I want to be able to put in the topics for my presentation before presenting so that presentation slides are not split up awkwardly.
- As a professor, I want detailed lecture notes generated from my spoken explanation alongside the slides so that students who need clarification can review explanations that the slides summarize or omit.

### Student User

- As a student, I want to be able to ask questions during the slides so that the professor can cover any missed details.
- As a student, I want to see the questions I and other students have already asked so I can know what has already been covered.
- As a student, I want the professor to be able to respond to my questions in a chat so I can get an answer in writing.
- As a student, I want the questions I asked to be summarized and put on a special questions slide so the professor can answer them.
- As a student, I want to be able to generate a condensed slides notes sheet so that I can be better prepared for lectures and in taking my own notes.
- As a student, I want to be able to save my condensed notes sheets so I can look at them later.
- As a student, I want to manually edit my notes sheet to correct any errors or highlight any important parts.
- As a student, I want to be able to ask AI to edit and iterate on my condensed notes sheet.
- As a student, I want to be able to export my notes sheet to a PDF so I can keep it on my computer and share it.
- As a student, I want to be able to delete a notes sheet if I don’t need it anymore.
- As a student, I want to be able to search slide decks for specific topics so I can find them for easy studying or go to that particular slide as the slides are being generated.

## Activity Diagrams

### Professor User

![Professor Activity Diagram 1](UMLActivityDiagrams/professor-activity-diagram-1.png)

![Professor Activity Diagram 2](UMLActivityDiagrams/professor-activity-diagram-2.png)

### Student User

![Student Activity Diagram 1](UMLActivityDiagrams/student-activity-diagram-1.png)

![Student Activity Diagram 2](UMLActivityDiagrams/student-activity-diagram-2.png)

## Wireframes

![Wireframes](wireframes/Wireframes.png)

## Clickable Prototype

https://www.figma.com/proto/Je0T7tBhZRXypHTDkgVlis/Wireframes?node-id=17-3&m=draw&scaling=min-zoom&content-scaling=fixed&page-id=17%3A2&starting-point-node-id=60%3A300&show-proto-sidebar=1&t=p0AahaOngOoUseYe-1
## Stakeholder Demo

See instructions. Delete this line and place a link to the deck The Slide Machine generated during your presentation here, after you have presented.

## Exit Ticket

See instructions. Delete this line and place a link to the exit-ticket quiz you generated from your demo deck and distributed to the class, along with a short note on what — if anything — you had to correct in the generated questions before publishing.
