# Weekly Status

## 2/27/25

# Agile Meeting Notes

## Pat

- Documentation
- Backend Install
  - Docker stuff (see below)
- PG Admin
  - When starting up, use username/password of LOCAL machine
- Next:
  - Little more docker
  - Start prepping for testing

## Noah

- Boilerplate for frontend
  - Instructions for setup
- Next:
  - More demo?
  - Continue work with backend
    - Make sure it works
  - Let him know if things work!

## John

- Played around with React / Typescript
- Next:
  - Get docker working
  - Make notes/status repo for milestone

## Josh

- Basic UI design finished
- Looking for some psych resources about motivation / task completion
- Started looking into database layout / relations
  - Will work with whoever's interested to develop it further
- Wrote down some ideas for the actual game's design
- Next:
  - Test out Pat's docker
  - Push some issues to the board for group to vote on
  - Upload meeting notes

---

## Milestone 3: Weekly Status

- Snapshot of tool, add more commentary
  - Pat made the backend repo
- John will do the stuff

---

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

---

## Database Design

- Have another meeting soon to go over design / relations
- Another meeting for database designs:
  - 3:30 p.m. MT on Friday 2/28

---

## "Sideburn" Chart

- Create issues for ideas
  - Group can vote on "will do / want to do / won't do"
  - If we will do it, create a ticket for people to claim
  - For critical, MUST do things, just make the ticket and get it done

---

## UI Design

- Good start, something to work off of
- Check the Excalidraw link, leave notes / critiques
- Maybe 3 unique pages:
  - **Splash page:** What users see when not logged in
  - **Task page:** React-based primary page
    - User avatar on game canvas (left) and task list (right)
    - Task list split into long-term tasks and short-term / daily tasks
  - **Motivation tips / blog page (optional):** Could support the self-improvement theme

---

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

---

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
