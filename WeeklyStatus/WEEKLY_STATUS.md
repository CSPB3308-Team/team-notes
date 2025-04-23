# Weekly Status

# 2/27/25

## Agile Meeting Notes

### Pat
- Documentation
- Backend Install
  - Docker stuff (see below)
- PG Admin
  - When starting up, use username/password of LOCAL machine
- Next:
  - Little more docker
  - Start prepping for testing

### Noah
- Boilerplate for frontend
  - Instructions for setup
- Next:
  - More demo?
  - Continue work with backend
    - Make sure it works
  - Let him know if things work!

### John
- Played around with React / Typescript
- Next:
  - Get docker working
  - Make notes/status repo for milestone

### Josh
- Basic UI design finished
- Looking for some psych resources about motivation / task completion
- Started looking into database layout / relations
  - Will work with whoever's interested to develop it further
- Wrote down some ideas for the actual game's design
- Next:
  - Test out Pat's docker
  - Push some issues to the board for group to vote on
  - Upload meeting notes

## Milestone 3: Weekly Status
- Snapshot of tool, add more commentary
  - Pat made the backend repo
- John will do the stuff

## Database Docker
- We may not need to log in
- Quick demo of how it works:
  - `make up`: spins up container
  - `make start`: logs stuff
  - `make migrate`: builds "migrations"
- Contains most of the database stuff
  - Postgres / PGAdmin
  - Everything _should_ sync, even though it's running locally
- Conflicts?
  - Changes to structure are transferred
  - Changes to actual data are local only
- Spin up test container, run it, then terminate it
  - Use "seed" file to prepare tests

## Database Design
- Have another meeting soon to go over design / relations
- Another meeting for database designs:
  - 3:30 p.m. MT on Friday 2/28

## "Sideburn" Chart
- Create issues for ideas
  - Group can vote on "will do / want to do / won't do"
  - If we will do it, create a ticket for people to claim
  - For critical, MUST do things, just make the ticket and get it done

## UI Design
- Good start, something to work off of
- Check the Excalidraw link, leave notes / critiques
- Maybe 3 unique pages:
  - **Splash page:** What users see when not logged in
  - **Task page:** React-based primary page
    - User avatar on game canvas (left) and task list (right)
    - Task list split into long-term tasks and short-term / daily tasks
  - **Motivation tips / blog page (optional):** Could support the self-improvement theme

## Game Design Discussion

### Rewards
- Completing tasks grants coins (or other currency) that can be spent on:
  - New decorations/customization for avatar
  - Helping avatar with needs
- Avatar energy refills when completing tasks
  - More energy for long-term tasks?

### Task Categories
- **Long-term**
  - Specific time/date deadline
  - User can't mark complete too soon
  - Reward claim period after deadline (1-2 days?)
  - Late claims could cost currency
- **Short-term / Daily**
  - Simple check-off tasks
  - Smaller rewards
  - Rewards claimable until noon the following day — or no leeway?
- **Custom vs. Predefined Tasks**
  - Custom preferred
  - Add some simple/common tasks to help users get started

### Task Difficulty
- More rewards for harder tasks?
- Preset/recommended vs. user-defined
  - User-defined might be better (personalized difficulty)
  - Choose with smiley/neutral/frowny face scale?

### STREAKS
- Extra important — rewards for maintaining high streaks

### Task Linking
- Link avatars to others
  - See each other hanging out in-game
  - Completing tasks benefits both
  - Possibly view each other's task lists

## Code Format
- Important for collaboration
  - Consistent style to avoid messy commits
- Use Prettier
  - Auto-formats code to a consistent style
  - Not for Python?
- Possible auto-format on push?
  - Workflows?
  - VS Code extension?
  - Needs consensus

---

# 3/05/25 

## Agile Meeting
### Noah
  - made task page skeleton
  - reviewed backend testing stuff with Pat
  - Next: 
      - front end testing        
  - Blockers:
      - need to consider what other pages we want as a group
        
### Josh
  - got back end and front end up and running on local machine
  - merged Noah's task page skeleton
      - made a new branch for implementing the game canvas      
  - playing around with react-three-fiber to figure out how to implement it
      - extra limitations on top of React's limitations       

  - Next:
      - get basic canvas implemented
      - maybe a basic avatar / simple customizations
    
### John
  - got front end and back end up and running on local machine
  - playing with SQL / flask database
  
  - Next:
      - Learn more about React
    
### Pat 
  - getting tests setup for backend
      - similar to what we did in SQL lab
      
  - Next:
      - get task model ready
      - potentially start getting routes ready as well     

- some Rando forked the frontend repo?        
        
## Webpage Discussion
- (check the Excalidraw for more details)
- Splash Page
- Task Page / Game
- User Page 
- Shop
- About?
- Blog / Tips
- Header
    - some way to have it on every page, without needing to manually add it to each route

---

# 3/12/25 

## Agile Meeting
### Pat
  - rough task model
  - playing with routes
  - Next: 
      - get task model done

### John
  - repos are set up
  - Next:
      - Unit tests for tasks 
  - Blockers:  
      - waiting for Pat to finish stuff

### Josh
  - Playing around more with react-three-fiber canvas stuff
  - Next:
      - push GameCanvas changes 
      - finish / push a few basic customization options
      - update README with react-three-fiber installation instructions
      - look into animation stuff

### Noah
  - page testing
  - working on design of our testing implementation
  - made a few new tickets for task list things
  - Next
      - work on making a few hooks
  - Blockers:
      - we need a header design       
      - needs some idea of what calls / responses will look like
      - might need to rearrange some file structure stuff; make sure Josh pushes his changes

## Splash page
- get people's attention with some moving "bars"
    - called a saccade
    - could be made with some CSS animations / key frames 

---

# 3/19/25
## Agile Meeting
### Josh
  - Animations
  - Basic customization items
  - customization item menu
  - Next:
      - PUSH MEETING NOTES TO THE REPO
  - Blockers:
      - Time 

### Noah
  - Basic tasks display
  - Reviews / project management 
      - checking issues
      - handling pull requests with Pat
  - Next:
      - Interactions for task routes
          - writing to the database
  - Blockers:
      - Maybe more design / style questions 
       
### Pat
  - Reviewed Noah's PRs
  - fleshed out user model
      - more like "final" design
  - Basic login page / auth
      - and cookie storing
  - basic task routes
  - Next:
      - basic user routes
    
## Backend Testing
- Bruno?
    - Pat likes this option!
- give it URL, GET / POST stuff

## Cookie Stuff
- used in routes from utils
    - handles login / getting current user
- jwt website to decode for testing purposes

---

# 4/02/25

## Agile Meeting
### Pat
  - User mutation stuff
      - create / update / delete users  
  - Next:
      - taskagotchi guy / shop stuff
    
### Josh
  - Not much (spring break)
  - Next:
      - check out Pat's PR
      - actually, for real add meeting notes 

### John
  - Not much (spring break)
  - Next:
      - Try to take on issues pull requests
      - Maybe work on writing some tests
        
### Noah
  - PR for task routes
  - Blockers: 
      - someone to confirm pull request
        - Pat's got it!    
  - Next:
      - plan last three weeks of project
      - SQL design

## User DB Testing
- "Create User" generates token 
    - key / value pair in header
- token required for updating / deleting user

## OrbStack
- replacement for docker desktop
- just point docker stuff to it instead and everything should work!

## To Do for MVP
- user can change customization items
    - needs a menu and some toggles
- streak counter 
    - Josh says he'll do it!
- user page
    - update info / password
    - delete account
        - with an "are you sure?" prompt
- splash page
    - create account / login
- avatar
    - get little guy in there
---

# 4/09/25

## Agile Meeting
### Pat
- Avatar / Customization item models
- Updating seed files to make associations
- Next: 
    - Routes for these
    - Ledgder / transaction table
- Blockers:
    - Time

### Joshua 
- Merged Pat's PR
    - Figured out how backend worked with Pat's help
- Looked at Noah's PR
    - everything good, just need to confirm testing 
- Next: 
    - Finish up avatar stuff
        - let him know if there's anything we need!
    - Fix tasks stuff so only current user tasks are shown
        - already fixed, just want team to look at it
- Blockers:
    - Life

### John
- Automation things
    - getting tests setup
- Next: 
    - clean up automation stuff, get it all in
    - Maybe video thing?
- Blockers:
    - Life
  
### Noah
- Login / SignUp routes
- Issue for account page
- Next:
    - Account page 
- Blocker:
    - login / signup PR
    - we need to plan some layout things 

## Professor Meeting
- Scheduled for: Tuesday, April 22 at 2:00 p.m. M.T  

## Planning Stuff / Questions
- Not a lot of time left!
    - Try to be done / deploy by April 18th?

- What left for MVP?
    - Transactions
        - What items do users have?
        
    - Currency
        - Give users currency for completing tasks 
        
    - Avatar
        - Change customization items
            - Get the system in place!
        - Manage energy
            - Energy changes as tasks are completed
            - Face change as energy gets low?
                   
    - Routes
        - Account management
        - Nav Bar
        - Redirect to login if user is not logged in
            - or shuffle pages?
            
    - Streak Counter (low-priority)
        - How to calculate?
            - Simple-ish SQL command
            - Can back-calculate, or store a value for the streak being valid?
        
- What kind of testing?
    - Some Backend, need more Frontend
    - John and Pat can bang out what we need
    
- Styling
    - Can take a long time?
    - Once we get everything / most stuff in, Josh can pivot to figuring out styling
    
- Deployments
    - could be smooth, but may be issues?
    - Best not to save for the end?
    
- Report / Video
    - make some time to rehearse / figure out 

## Timeline
- On April 16: Regular Meeting
- By April 17: Final Features / Implementations 
- By April 18: Styling
- By April 18: Deployment
- By April 21: Meeting for Presentation
- By April 22: Final Testing / Proof
- On April 22: Presentation
- On April 23: Final Meeting
- By April 24: Project Report

---

# 4/16/25

## Agile Meeting
### Pat
  - Finished backend
  - fixed bug with deleting user accounts
  - avatar / wallet / customization stuff
      - "added capitalism"
  - messing around with bootstrapping UI stuff
  - Next:
      - streak counter!
  - Blockers:
      - None

### Josh
  - new model
      - no longer little pill man
  - inventory preview 
      - see lists of customization items
      - see them on character in inventory
  - Next:
      - Avatar energy bar
          - and linking to task completion
      - Final customization assets
          - textures / shaders
      - Stretch goals
          - Simple animations for Avatar
          - Basic game sounds
              - For completing / removing tasks, Avatar mood, etc.
  - Blockers: None
        
### John
  - fixed environment
  - reviewed Pat's PR
  - Next:
      - tackling backlogged issues
      - tests
  - Blockers:
    - Time
    - 
### Noah
  - Account page
  - Reviewed PRs
  - Header bar / nav stuff
  - Fixed issue with stale user tokens
  - Next:
      - frontend testing / deployment
  - Blockers:
    - Time

## Presentation Prep Meeting
- Monday 12:00?

## Task Rewards
- Daily: 1
- Short: 5
- Long: 10
- But multiplied by current streak

## Deployment
- Friday?
