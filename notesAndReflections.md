EVT Reflection / Notes

Day 1
Notes

- Setup for a big project takes some time
- Decoupled web application
- Stack:
	- Front end
		- React Redux
	- Backend
		- Django & Python
		- Ton of dependencies
- Flow: 
- Machine AI records data / information and  translates it into the database
- Info is retrieved through api calls
- Check to see what Models look like
- Other Technologies:
	- Docker

TIPS

- When tackling new code bases, focus on the things that you are tasked to do.
- Start at the home page and navigate through where you want to go while following along with your VS code on the side. You are able to find the components / code you want.
- 'Legacy Code' is older code within the code base.
- This code base is built over 5 years, I have seen all the different variations of react including typescript implementation
- Code is not worth changing, making changes to an existing code base. Just continue on with how it has been already written.
	- i.e. if tasked to rewrite a class component, continue with the syntax do not rewrite it into a functional unless it is completely necessary or told to do so.
- `brew` commands are installs for global level?

Reflection

First day was great, I learned a lot. Set up is a beast. A walkthrough in `django_start.sh` (although instructions can be more specific) as well as the companys `wiki`
- I need to learn:
	- How the app overall works and records data
	- How to add / make changes to the database
	- How docker works
	- Workflow when making changes

Day 2

Notes

TIPS

Reflection


Day 3

Notes

General

- Check global state in order to utilize context for LectureContext

Task
- Worked on creating a button for EVT Slides Platform
- When clicked, button should expand the width of the side bar
- Isolated components needed for this change

- Components are:
	- BystanderLayout.tsx
	- VideoPlayer.tsx
	- SecondaryVideoPlayer.tsx
- Solution:
	- Create state within bystander layout
	- Create properties for interfaces to be able to pass the state and function through child components
	- Create a button within SecondaryVideoPlayer.tsx
	- Use state in Rightbar.tsx
	- Use setWidth within BystanderLayout to change width from screen dimensions to 960px

- Side Effects:
	- There is a toggle that opens and closes the rightbar
	- If width is expanded, closing the bar will no longer work

Todo:
- Need to style CSS and use a nice icon
- Display toggle when hovered?
- Or is it better to just display to show that this toggle is available

Github
- When working with branches, if someone pushes while you are on a branch. It is important to rebase. Rebasing helps so that you can continue working on your task while staying current on the most recent base file
	- This may cause conflicts but you just need to adjust accordingly
	- Be sure to communicate with other developer when merging conflicts


TIPS
- Control Click Things
- Right click and peek references
- Use VS code to commit
- Check Conventional Commits when making your commit notes
- Commit often per every little change
	- Helps yourself in the future
- Give yourself extra time. This ensure that you can estimate a good time while also finishing the task faster than you planned. Better to over deliever than to underperform
- When utilizing interfaces, you set default properties and values for them. If you have passed in a variable for those properties, then those values take priority over the default variables.


Reflection
I think today went very well. I felt a bit of imposter symdrome when monal said that it should take me a few hours to complete this task. When it took me longer.. roughly a little less than a day. Sam reassured me that Dane was on the same page as me and it took him 4 days to fix the button. Sam also reassured me that it takes roughly a month to become acclimated to a new codebase. Completed the task but I took me a little while with the help of Sam.

Working with interfaces was throwing me off because I thought we were having to reset the same properties of interfaces over and over again, when in fact the data was actually being passed through.. and we were setting default interface variables.

Day 4

Notes

TIPS

Reflection


