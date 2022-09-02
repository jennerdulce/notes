EVT Reflection / Notes

Entry 1
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

Entry 2

Notes

TIPS

Reflection


Entry 3

Notes

General

- Check global state in order to utilize context for LectureContext

Task
- Worked on creating a button for EVT Slides Platform
- When clicked, button should expand the width of the side bar
- I was able to Isolate components needed for this change

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
- Control + Click Things
- Right click and peek references
- Use VS code to commit
- Check Conventional Commits when making your commit notes
- Commit often per every little change
	- Helps yourself in the future
- Give yourself extra time. This ensures that you can estimate a good time while also finishing the task faster than you planned. Better to over deliver than to underperform
- When utilizing interfaces, you set default properties and values for them. If you have passed in a variable for those properties, then those values take priority over the default variables.


Reflection
I think today went very well. I felt a bit of imposter syndrome when Monal said that it should take me a few hours to complete this task. When it took me longer.. roughly a little less than a day. Sam reassured me that Dane was on the same page as me and it took him 4 days to fix the button. Sam also reassured me that it takes roughly a month to become acclimated to a new codebase. Completed the task but it took me a little while with the help of Sam.

Working with interfaces was throwing me off because I thought we were having to reset the same properties of interfaces over and over again, when in fact the data was actually being passed through.. and we were setting default interface variables.

I was able to isolate the components / files needed for my task and had a strategy to implement this change. I encountered some difficulties passing props via typescript and interfaces but Sam helped me get unstuck. I need to style the button.

There is a bug that when the width is extended, the button that hides / shows the side bar does not close it entirely. I have to check and see how that button is working and may have to make some minor changes

Entry 4

Notes
- Ngrok hosts your ip so that people can connect to you
- Socket.io are websockets


- How to create globalContext
1. useGlobal
2. Create state using useState()
3. Create the function
4. Add pieces of data and set the static data type
5. Add data to the hook
6. Ensure that you include these variables whereever you put them

TIPS
- Turn autosave off
- You are able to utilize older versions of your dependencies. Access to older documentation is always available (i.e. older version of material UI https://v4.mui.com/components/material-icons/)
- Run `nvm use 14` when restart you computer
	- Signal is terminal fails at 10%

Reflection
Today I continued to work on the button which worked great. I found that the right side bar is affected and is state retrieved through context. I figured that this was the trigger to opening and closing the side bar which I used in my code. Majority of the code is within the BystanderLecture.tsx file.

I need to push a little harder and research more. Maybe become more familiar with typescript. I need to prove myself because There are a lot of things that I am wek in, however I also need to find a good balance when to fit this extra study time.

I need to just stay focused and enjoy my days. Enjoy the process and try my hardest when im putting in that work.

Entry 5

Notes
- Continued to work on the button
- Create a button component referenced from a different component
- May have to create a hover effect but it is fully functional as of now

TIPS

Reflection
I think it is better for me to wake up earlier in the mornings and to ensure I put in my hours. I feel that I am at my peak performance first thing in the morning. I finished my first task and it feels great! Big confidence boost in myself that I was able to finish this challenge in 1 week. Although I wish I was able to complete this task faster.

- I was able to complete the button. There was an issue with the video being rendered with full sized dimensions which was resolved by configuring the containing div element
- I also converted the local state into a global state in order to make it a little bit cleaner. pulling in the data by the useContext hook in necessary components for data, avoiding my previous implementation passing data/props from component to component.

Entry 6

Notes
- Continued to work on the button


TIPS
- Successfully implemented a custom MaterialUI Icon using <SvgIcon> and an SVG image. Refer to ScreenToggleButton.tsx
- Ensure to add the viewbox as an attribute to the <SvgIcon /> component
- Used onMouseEnter and onMouseLeave on the div component as a hover toggle

Reflection
I think it is better for me to wake up earlier in the mornings and to ensure I put in my hours. I feel like I did well on this task.

Entry 7

Notes
- Off day

New Task
- Ver: 0
Next Task:
Create Admin Accounts Workflow as University Admin
	- Look @ Students Create Accounts
		- Similar but an Admin making another account for an Admin
		- As a University Admin, I want to be able to create Admin accounts for each Department Admins and Professor Admins.

Notes
	- University Admin
		- Can make Department & Professor Admin Accounts
		- Can choose Departments for Department and Professor Admins
	- Department Admin
		- Can only make  Professor Admin Accounts
		- Department Admins can choose which course? For Professor Admins

Create Account
‘I am a’ field should differ from Department and University Admins
Password, name, I am a…
University  Admins should be able to choose which Department for Department Admin Accounts
Department Admin Accounts are already within a Department that is assigned by the University  Admin
Exclude grade level and major. Record keeping
Like how prof adds a student
Have University Admin add Department Admin or Professor Admin
Have dept admin add to course


Model user profile
Permsgroups
4 per university
Student
Prof
(University) Admin
Dept
From the for what group I create the account for will reflect on this permsgroups
Universities all be the same

University Admins should be able to make a Department / Professor Admin for any department
When creating a Department Admin as a University Admin
After selecting Department Admin or Professor Admin:
Will need a dropdown for Department options that will assign the new account to that specific apartment same with
When creating a Professor Admin as a Department Admin
Will automatically be assigned the same department as the Department Admin

Check Enrolll User by API on backend
Ref:
Course Management
User Access
Enroll User
DjangoAPI SendEmailSignupEnrollment

Todo:
DJANGO Restframework
Frontend
Isolate components needed / to reference
Look for API calls to backend
Backend
URL
Ref: email_signup_enrollment
Views / Methods connected to URL
Ref: email_signup_enrollment method in views.py
Start by printing request data within method just to check if endpoint is being accessed correctly and to see if dictionary looks correct


Make Admins with EVT BLOOM ACCESS as a selection on the left Admin Panel
	- Clicking the selection will open up the same page
Rename to Admin User Management
Populating departments for the logged in university admin
Grab current logged in user object
Grab list of departments affiliated with the current logged in user based on college affiliation
Display departments within the dropbox




I am able to create a new user with the ‘add admin user button’
Questions I need answered:
	- Given the only information that I have, How will I create a new admin user and set the correct credentials / information for that use
In order to make a department (my_department) Seems like you need a course Object which also requires a semester (my_unisem)
Things I need that I do not have
sem_id
course_id
Without these I cannot add to my department?
With this, I need to also figure out how the tables are linked together
Look into models / schemas

ModelUniveristy
Only need nameid=request.data[‘univ_id’]

ModelUniDepartment
nameid=request.data[‘department’]
university=my_univ



Customers interested
Form a demo
They upload
We create
And send them back



Click Verification Link
	Activates Account
	Good to go


Dept Admin
	- Modify All courses: done
Prof Admin
	- Create Courses

Send Account  -> Create Account and Email User
:semi-done

Newly Create Admin Accounts should show up under Admin User Management: done

In admin user management
If professor account cannot add admin users: Done

 Ver 1: 
Professor can request if TA can create an account
IF they haven’t Verified, Show in a different color or some sort of flag


TIPS
- 

Reflection
I think it is better for me to wake up earlier in the mornings and to ensure I put in my hours. I feel like I did well on this task.

Entry 8

Notes
- QA to ensure that AI created correct data
- Preview snapshots
	- 5 snapshots per slide
	- if progression is losing c
- " I need to to content process"
- replace learn evt ai
with content-prod.bloom.lol
replace n
with slides
- fix slides
click start 'fully processed'
- click saved
	- Press only once
- Magic Link
	- Course management
	- Click on course
	- Click Magic Link
	- Click Copy
	- Check to see if works on incognito window

TIPS
- 

Reflection
I

Entry 9

Notes
- I have been able to connect the front end to the backend successfully
- Create a new url in urls.py and create a method in views.py that is triggered when the endpoint is called
- I have learned to used the redux extension tool efficiently to see what pieces of state I have access to
- I may need to add an extra piece of state for the departments that users are under
- When developing code for the method, I had to sift through all of the models  in order to create a user correctly
- There was one main Model called called ModelUserProfile
- This main model had different values for the columns, the values were specifically other tables. So that in order to put a value in any of these columns, the other Models had to first be created and then inserted into the ModelUserProfile

TIPS
- Isolate files you need
- Multi window on Mac is super helpful
Process: Make a variable that GETS a specific model from a different model based on university name, department, or any other information. In a sense you are not creating a new instance of that model, you are retrieving it. After retrieved, you can used the retrieved model as a value for your main model (ModelUserProfile)

Reflection
Still learning A LOT. I am super sad that Sam left. He was a big help and I feel like working under a senior is a great feeling because you are taken care of. While being alone it feels like 'Oh man I need to get this done..' this feeling can get overwhelming especially when you hit a blocker. Who are you supposed to ask for help? So far everything has been working out fine and I've been doing my best to accomplish my tasks. I just hope that I am doing well and that they see my efforts.



Entry 10

Notes
- I was able to complete the following tasks:
	- Show only the departments the Department Admins are Tied to
	- New Admin Users show up on the Admin User Management
	- Professors have no access to seeing the admin user management
- 'Add Admin User' Button creates an account however does not send emails locally

- What I need to do:
	- Select Multiple departments on 'Add Admin User'

- Questions:
	- Adding an Admin User like this adds a Bloom Account?
	- Are all accounts bloom accounts?
	- When creating a course as a professor, I have no access to semesters I need to know how this works
	- Out of curiosity how will University Admins be assigned their accounts

TIPS


Reflection
This project is coming together. Finally.. I finished the general functionality of what we wanted. What we wanted was to be able to create a new Department / Professor Admin account through Add Admin User. Department Admins may create accounts for Professor Admins.
Todo:
I need to test out the button
Ensure emails and password resets are being sent
Answer the questions that I had

Entry 10

Notes
- I looked into email problem
- Testing on local
	- Again account creation seems consistent
	- Admins from different universities cannot see other accounts
	- Department Admins can only create other Department Admin accounts under the departments they were assigned to by the University Admin
	- Professor Accounts cannot see the button and can only create courses under the department that the Department Admin / University Admin selected for them during the account creation
	- On the 'Course Management' Tab, for the 'Departments' Dropdown, what should we display here? All departments? or only departments that user is assigned to?

TIPS


Reflection

Entry 11

Notes
- Merging Notes
	- Push up to GitLab
	- Merge
	- Run python scripts
		- Consists of opening docker container
		- Creatine new image
		- Saving
		- Restarting Server and uninstalling and reinstalling… things
		- Compile, build, and redeploy to Azure
- TODO:
	- User Stories
	- Test Email
	- Ensure that cannot see other university staff / courses
	- Proper conditional rendering of staff positions / authorization
	- bug: Staff cannot see / pick departments if there is no courses created for them.
		- I personally think that staff should be able to still see and pick the department they have access to, even though there are no courses at the time.

TIPS
- Term date was not showing up because there is no existing term that is currently active
All dates listed in term / quarter were invalid / expired
Solution: change in 'Model Uni Semester' end date in Pfizer
Now ALL Admins are able to create courses and see

Reflection
Monal has a wealth of knowledge and there are a lot of things happening that I am unaware of that he does. Just ask him and he will lead the way. This task has been good, I feel like a little drawn out. I have been working on it for a while now but finished the logic a while ago. Next step is to check and see if the email is being sent out after Admins create an account through 'Add Admin User'.. If not, that is a problem that I will have to figure out and fix. So far, the AWS credentials are on my mind and are the solution on how to fix it.. After my changes have been deployed on to QA, I will create user stories for each role, Univ, Dept, Prof, and Student profiles. And see how creating courses and new Admins affects each of the screens. Also Make a superuser admin. Will need a 2 separate University Admins in order to make sure that Admins from other universities cannot see courses / Admins from universities other than their own.

Just do the task the best you can, ask questions, and be productive. Do not worry too much about it. Report to Monal of any findings and that's all you need to do. The things that Sam was doing is out of my job description. Just stick to what I am given for the time being! But be ready when to learn. Study things and read up on material on your own time.

Entry 12

Notes
- Error 1

｢wdm｣: Compiled with warnings.
[HPM] Error occurred while trying to proxy request /api/universities/ucsd/all/false/false/0/0/ from localhost:3000 to http://localhost:8000 (ECONNRESET) (https://nodejs.org/api/errors.html#errors_common_system_errors)

- What causes the error?
	- When I click Admin User Management



- Error 2

num if not limit or num < limit else 'more than %s' % (limit - 1),
web_1  | evtuserprofile.modelpgroup.ModelUserPermissionsGroup.MultipleObjectsReturned: get() returned more than one ModelUserPermissionsGroup -- it returned 4!

- What causes the error?

	- When attempting to create a prof account (Univ and Dept)
	- I tried to create a new University Admin for USD
		- When attempting to create a new Department Admin for USD

- When am I able to create a prof account?
	- Already be in Admin User Management, signed in as Univ Admin
	- restarted the frontend
	- Refresh localhost:3000 page
	- Sometimes it works
	- Message upon creation and nothing else:

​​NEW ENROLLED USER: prof@gmail.com

- Today as I was logged in as an admin user, I was able to create a Department and Professor Admin Account with no problems
- I logged into the Department account that I created and was able to create a Department Admin Account
- Error came up when I tried to create a Professor Account WHILE logged into a Department Admin Account

num if not limit or num < limit else 'more than %s' % (limit - 1),
web_1  | evtuserprofile.modelpgroup.ModelUserPermissionsGroup.MultipleObjectsReturned: get() returned more than one ModelUserPermissionsGroup -- it returned 4!

- However, when I logged back into an University Admin Account and attempted to create a new Professor, the same error occurred

num if not limit or num < limit else 'more than %s' % (limit - 1),
web_1  | evtuserprofile.modelpgroup.ModelUserPermissionsGroup.MultipleObjectsReturned: get() returned more than one ModelUserPermissionsGroup -- it returned 4!

- I am unsure what is causing it but I have found that it may be linked to this error in the front end

｢wdm｣: Compiled with warnings.
[HPM] Error occurred while trying to proxy request /api/universities/ucsd/all/false/false/0/0/ from localhost:3000 to http://localhost:8000 (ECONNRESET) (https://nodejs.org/api/errors.html#errors_common_system_errors)

- Even through these errors are present, I am able to create a Department Account consistently with no problems.

- Error 3

web_1  |     num if not limit or num < limit else 'more than %s' % (limit - 1),
web_1  | lectureserve.modeldepartment.ModelUniDepartment.MultipleObjectsReturned: get() returned more than one ModelUniDepartment -- it returned 4!

- What causes the error?

	- When trying to create an Dept account (dept: general) with the USD University Admin

- Error 4

web_1  |     num if not limit or num < limit else 'more than %s' % (limit - 1),
web_1  | evtuserprofile.modelpgroup.ModelUserPermissionsGroup.MultipleObjectsReturned: get() returned more than one ModelUserPermissionsGroup -- it returned 4!

- What causes the error?

	- When trying to create an Prof account (dept: electrical eng) with the USD University Admin


TIPS
- Broken until proven otherwise
	- Essays, have grammatical errors
	- Same with code, so many edge cases and other things that can cause issues

Reflection
M

Entry 12

Notes
Errors
- I was able to fix those 2 errors I had with the help of dane
- We added an extra argument when getting the department. The problem was that it was searching for a general department but multiple universities have general departments, so adding the university as an argument with the get query was a quick and easy fix. Selecting the general department while on a USD Admin account seems consistent and I am assuming that it will work for all other organizations
- Second error when attempting to create a Professor Admin Account:
- At first we thought we fixed the problem by dumping and rebuilding the database. The fix did not persist..
- I found out that the problem was, when professors create courses, a new permission is also created. The query method being used for creating a new course is 'get or create'
- I proceeded to change to it to 'get' only. This problem only happens with professors..
- It fixes the current problem and does not create a new permission
- However, it causes a new one where after a course has been created, the professor is unable to see their course on the dashboard
- Logged into different users such as University or Department Admins, We can see the newly created course by the professor
- As of now, I am going back and forth reverting the code to see what data changes or remains so that I can find how the courses are being displayed.
- Or I guess why is creating a new permission necessary for professors to post a course..?
Files:
	backend: add_recording.py

- Other thing is when Admins create accounts, they are set to inactive
- Monal I remember you seeing me create and activate an account, by setting a password. I tried using the localhost email link that it sends and changing it to localhost 3000 but the link does not work anymore. when submitting the new password it gives me a 403 forbidden error.
- I found out that you can only reset your password if the user is set to Active, then by using the link you can activate your account by setting a new password

Containers
- Containers make a little more sense to me, you hop into a container by typing sh docker.sh which is pretty much is the same as you going into a different computer environment's terminal, in a container, it has everything all the different parts in 'images' processor, frameworks, everything
from here you can also run your basic terminal commands for python, node, etc etc. typically what happens is that you enter a container, and you run a script that will do all things necessary to start up your venv downloading all dependencies. Once ran you can exit the venv. type docker compose up which will start the env and run it on your local

TIPS
- Restart DB
Download docker extension on vs code
Right click compose down
sh docker_init.sh 
Docker compose-up
Ver2:
Sh enter_container.sh
python3 manage.py flush



Create super user
While in container:
Sh enter_container.sh
python3 manage.py createsuperuser
python3 manage.py loaddata dump_db_NO_USER_SENSITIVE_DATA_1_20_2021.json 
Python3 initialize_db.py


Reflection

- Yesterday I was working on the 2 problems I expressed above, the first half of my day I was console logging and tinkering with the emails trying to get it to work while is_active is false, was unsuccessful. For some reason, the email activation link does not work while is_active is false. My guess is that it is some permissions issue. Which, I spoke with Dane and Monal, that it makes sense that users cannot even login without setting their password.. Also, the logic behind permissions is changing soon, so me trying to fix this issue is kind of a waste of time. It makes sense that the is_active should be false upon account creation, but it is a not an important fix at the time being.

- Second bug with when retrieving the default professor model. After spending so much time trying to figure out how to go about this. Monal says that the creation of new Permissions for newly created courses are required and are necessary.. So with that in mind I had to find a way to configure the query data for the 'admin_signup_enrollment' method. Dane and I found that the name property is blank for the Permissions Groups that are generated by courses. Previously we were using 'nameid' as part of the query, however the 'nameid' property was being generated with new courses. This was the problem, switching nameid to name fixed the issue. Previously searching by nameid and univ was too vague because the all permissions had this same information.

- I really love my team, they are reassuring and expect the feelings and struggle I am going through. I receive nothing back but positivity and support.


Entry 13

Notes
- Have still be working on the Account Creation
- I would have pushed already but we continue to add features to the existing branch, pushing back my merge
	- I need to remember that I keep making new iterations to the branch and that I am not taking long
- I also learned how to content process slides for Demos

Content Processing:

Setup:
- Download PIA (Private Internet Access)
- Monal shared a username and pass using lastpass as well as a key generated by him
- After downloaded, open software
- Login
- Go to software and use pin to gain access to private IP address
- Before you connect, choose the correct dedicated IP address
- Connect (may take a minute)
- Once connected you are able to access the content-bloom website
	- https://content-prod.bloom.lol/content/ucsd/sp22

Workflow (Slides):
- Once on the website..
- Choose the correct university
- Show all
- Choose the correct course
- Scroll down until you see the content you need to process
- Click the pencil icon next to the course
- Begin editing
- Clip at the very last frame before the next frame
- Delete merges to the left
- Save often
- Saving without Set Active keeps the changes but does not actually upload
- 'Set Active' and check to actually upload
- After organizing slides, change titles
- Choose which slides should be summary
	- Summary slides have to be edited later but I have not yet learned this skill
	- Summary mico service will generate summary and overlay on slides
	- Use for webcam video, blank screen, camera off
	- Typically Beginning and end of presentation
	- 
- Check 'Set Active' and save
- Head over to the pfizer backend to enable titles at:
	- https://learn.evt.ai/pfizer/
	- There are also pfizer links in the content prod (the gear) that bring you directly to the pfizer link to the spcific course.
- After titles have been enabled save.
- Check to see if presentation is presentable at the main website:
	- learn.evt.ai
- If looks good, grab magic link for course send to Monal
- Head back to https://content-prod.bloom.lol/content/ucsd/sp22
- Find course again, Set star to Green
- Put yourself as assignee

Admin Account Creation:
- Still doing good
- Added new columns for department and permission level
- Added University Admin as selection

Notes
- Newly created University admins cannot see the rest of the staff
	- Resolved, need to be set to Administrator
- Newly created accounts crash website
	- This was happening because the table rerenders and looks for new account with the current state
	- Current state does not have new email info
	- So had to make an API call to refresh list of Admins



TIPS


Reflection

