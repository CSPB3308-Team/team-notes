<h1>Taskagotchi </h1>


Team #4


<h2>Team members:</h2>


Patrick Brown - John Gaynes - Noah Kawaguchi - Joshua Peters


<h2>Table of Contents: </h2>


- README.md [https://github.com/CSPB3308-Team/team-notes/blob/main/README.md](https://github.com/CSPB3308-Team/team-notes/blob/main/README.md)
- WEEKLY_STATUS.md [https://github.com/CSPB3308-Team/team-notes/blob/main/WeeklyStatus/WEEKLY_STATUS.md](https://github.com/CSPB3308-Team/team-notes/blob/main/WeeklyStatus/WEEKLY_STATUS.md)
- PAGE_TESTING.md [https://github.com/CSPB3308-Team/team-notes/blob/main/PAGE_TESTING.md](https://github.com/CSPB3308-Team/team-notes/blob/main/PAGE_TESTING.md)
- SQL_TESTING.md [https://github.com/CSPB3308-Team/team-notes/blob/main/SQL_TESTING.md](https://github.com/CSPB3308-Team/team-notes/blob/main/SQL_TESTING.md)
- FINAL_REPORT.md (you are here)
- **Project presentation files from Presentation Milestone** [https://docs.google.com/presentation/d/1k3BHlx9xJky64LwpZdHXqylh_8QBb_3Ghke61H-Ont4/edit?usp=sharing](https://docs.google.com/presentation/d/1k3BHlx9xJky64LwpZdHXqylh_8QBb_3Ghke61H-Ont4/edit?usp=sharing)
- **Video of demo** : https://youtu.be/-gKoEfC_2_c
- **Source code**
  - **Frontend**: [https://github.com/CSPB3308-Team/productivity-frontend](https://github.com/CSPB3308-Team/productivity-frontend)
  - **Backend**: [https://github.com/CSPB3308-Team/productivity-backend](https://github.com/CSPB3308-Team/productivity-backend)
- **Test Cases**
  - Backend. Clone repo and run `make test`: [https://github.com/CSPB3308-Team/productivity-backend/tree/main/tests](https://github.com/CSPB3308-Team/productivity-backend/tree/main/tests)
  - **Frontend**:
    - [https://github.com/CSPB3308-Team/productivity-frontend/blob/main/src/hooks/useGetRequest.test.ts](https://github.com/CSPB3308-Team/productivity-frontend/blob/main/src/hooks/useGetRequest.test.ts)
    - [https://github.com/CSPB3308-Team/productivity-frontend/blob/main/src/hooks/usePostPutPatchDelete.test.ts](https://github.com/CSPB3308-Team/productivity-frontend/blob/main/src/hooks/usePostPutPatchDelete.test.ts)
    - [https://github.com/CSPB3308-Team/productivity-frontend/blob/main/src/components/Header/Header.test.tsx](https://github.com/CSPB3308-Team/productivity-frontend/blob/main/src/components/Header/Header.test.tsx)
- Source documentation, and auto-doc files
  - **Backend:** [https://github.com/CSPB3308-Team/productivity-backend/blob/main/README.md](https://github.com/CSPB3308-Team/productivity-backend/blob/main/README.md)
  - **Frontend:** [https://github.com/CSPB3308-Team/productivity-frontend/blob/main/README.md](https://github.com/CSPB3308-Team/productivity-frontend/blob/main/README.md)
  - **Notes, Markdown files for Project Milestones and More: [https://github.com/CSPB3308-Team/team-notes](https://github.com/CSPB3308-Team/team-notes)**
- **Link to Public Deployment Site**
  - Frontend (main UI): [https://cspb3308-team.github.io/productivity-frontend/](https://cspb3308-team.github.io/productivity-frontend/)
  - Backend (API endpoints): [https://productivity-backend-7253.onrender.com](https://productivity-backend-7253.onrender.com)


<h2>Project tracker link (Instructor can access):</h2>


You are a member of our public organization and can see the following:


- **Kanban Board** - [https://github.com/orgs/CSPB3308-Team/projects/1](https://github.com/orgs/CSPB3308-Team/projects/1)
- **Burn Down Chart** - [https://github.com/orgs/CSPB3308-Team/projects/1/views/4](https://github.com/orgs/CSPB3308-Team/projects/1/views/4)


<h2>Demo Video:</h2>


<h2>Version control repository link:</h2>


- **Frontend**: [https://github.com/CSPB3308-Team/productivity-frontend](https://github.com/CSPB3308-Team/productivity-frontend)
- **Backend**: [https://github.com/CSPB3308-Team/productivity-backend](https://github.com/CSPB3308-Team/productivity-backend)
- Team Notes: [https://github.com/CSPB3308-Team/team-notes](https://github.com/CSPB3308-Team/team-notes)


<h2>Reflection</h2>


<h3>What We Completed</h3>


We were able to achieve slightly above our MVP (minimum viable product). User accounts could be created, updated, and deleted. A user’s password would be automatically hashed when stored into the database for security. JSON Web tokens were used for authorization for all of our sensitive requests.


Upon User account creation, an Avatar (the Taskagotchi) and a wallet would automatically be created as well. Users could then add custom Tasks (daily, short-term, or long-term) and assign a due date for them to be added to their Lists. Users could also change the status of tasks to ‘complete’ or ‘incomplete’ or delete the Task entirely. Wallets could also be updated – current balances could be retrieved, incremented, and decremented. Avatars could be customized with shirts, shoes, and pants and those items can be purchased by Users and show up on the Transactions table. All of the above could be deleted if a user chooses to delete their accounts.


We successfully deployed our React/TypeScript front-end to Github pages, and were able to communicate to our Render-deployed headless Flask API.


<h3>What We Were in the Middle of Implementing</h3>


We had a number of pull requests in limbo on presentation day including adding a streak to the front-end, which would be used as a currency multiplier to completed tasks. This was also in-progress; users can currently complete tasks but no currency was rewarded; only seeded. There are also a number of static informational pages currently in code review that did not make it into our presentation.


<h3>What We had Planned for the Future</h3>


As part of our initial concept, we wanted the user to be able to decorate their avatar's room with a variety of furniture items, such as a bed, couch, desk, or chairs. This would give the user more things to earn, and therefore more motivation to complete their tasks.


We wanted some additional styling to reinforce the "task manager" aspect of the project. Some ideas were timers or countdowns, or a depleting bar indicating time remaining until a task is due. We also wanted a greater delineation between different task types through the styling. Tasks that were designated long-term (i.e. one week or more until the due date) could have a depleting bar, while short-term tasks would indicate the date and time that the task was due. Daily tasks, which are meant to be repeated, would simply be crossed off with strike-through text, and then revert to their original styling at midnight in the user's local time.


We also wanted to add animations and sound and to enhance the user experience, such as positive sounds for completing tasks or creating new ones, or negative sounds from the avatar to indicate a low energy state to motivate more task completion. Animating the avatar would ideally further encourage the user to complete tasks, as the avatar would feel more responsive and life-like.


We plan to continue developing our product.


<h3>Known Problems (bugs, issues)</h3>


Everything currently deployed is well-tested and reviewed through the official Github code review process. The PR’s currently in review have some issues that need to be ironed out, including


<h3>What changes did you make along the way and why? </h3>


We kept the same concept throughout the project, but we had to reduce the scope given the time constraints. However, we were still able to create a working full stack app with most of the originally planned features implemented. We changed the design of the Avatar from an egg to a humanoid. This required adapting our categories for customization items.


<h3>What would you do differently?</h3>


We would have planned more time for styling and customizing the visual appeal. Also, if we had already had the backend deployment experience, we would have separate production and development branches and configurations – production would have had a minimized Dockerfile only building up the flask server and development would have had the triple-stack of Flask/postgres/pgAdmin instances needed to debugging.


We decided on an idea quickly and immediately started planning out technical details. Instead, we could have spent a bit more time working out our ideas for the semester in a more abstract way.


It may have been beneficial to use base Three.js from the start, rather than React Three Fiber. When it came time to begin implementing customization items for the user's avatar, we realized that React Three Fiber isn't intended for the level of control that we wanted over the avatar. We defaulted back to using Three.js for avatar management, which felt like we were starting from scratch learning the 3D environment tools. Thankfully, some of the skills and knowledge transferred over, but it would have been more useful to use Three.js from the start, even if there may have been a learning curve.


<h2>Reflection of Project and Tools</h2>


<h3>Front End Tools:</h3>


<h4>Node.js</h4>


A JavaScript runtime that allows for JS code without a web browser. Used to compile our TypeScript front end.


- **How did it meet your needs?**
  It allowed us to run a development server locally and preview the frontend’s visuals and functionality. This met our needs very well.


- **How did it fail to meet your needs?**
  It was generally quite easy to use and did not fail in any way.


- **How could you use the tool better?**
  Our use for it was rather simple (not a backend server), but if we were to use it for more than just spinning up the frontend in development, we would need to coordinate the frontend and backend in a more unified way.


- **Is there another tool that might work better?**
  If limited to the task of running JavaScript/TypeScript outside of a browser environment, Node.js seems to be the main/only option. However, if we were to go a completely different and unusual direction with the UI, like Dart/Flutter or Rust/Yew, we might have had a better developer experience.


<h4>Npm (Node Package Manager)</h4>


Used for installing, managing and sharing libraries in our TypeScript / React frontend.


- **How did it meet your needs?**
  It allowed us to install all the packages we needed and resolve dependencies, so it served the basic purpose that we needed from it.


- **How did it fail to meet your needs?**
  The entire package ecosystem of Node is extremely cluttered compared to its counterparts in languages like Python, Go, or Rust. There are many very small, almost trivial packages that the libraries we wanted to use rely on, resulting in overly complicated dependency trees.


- **How could you use the tool better?**
  We could have coordinated more explicitly about how to manage the setup across our various operating systems. Some members had unusual issues like needing to reinstall everything every time a new package was added.


- **Is there another tool that might work better?**
  Absolutely. Yarn and pnpm are alternatives to npm. pnpm in particular is preferable because it stores packages centrally on the device and then links to the files in the project directory instead of downloading a new copy of every dependency for every project.


<h4>TypeScript</h4>


A typed superset of JavaScript we used to catch errors and make our code easier to maintain with some config. We used this for our front end language alongside React.


- **How did it meet your needs?** It helped us stay organized and keep the functionality of our frontend clearer and less ambiguous than if we had used JavaScript.


- **How did it fail to meet your needs?** It was restrictive at times, especially with certain libraries such as Three.js, where it can be helpful to have the flexibility of dynamic typing. There is also a lot of configuration required to do very simple tasks.


- **How could you use the tool better?** We could have used tools like ESLint that help keep code correct and efficient and help with common TypeScript issues.


- **Is there another tool that might work better?** We could have used JavaScript if we wanted more flexibility at the cost of stability and precision. This might have been a beneficial trade-off depending on our priorities.


<h4>React</h4>


A JS library for building user interfaces by returning UI elements from JavaScript/TypeScript functions, allowing for dynamic component-based apps. We used this to build our front end component library.


- **How did it meet your needs?** It met our needs very well. We all liked the compositional way of thinking it encouraged.
- **How did it fail to meet your needs?** It added some complexity and confusion, especially with managing state and hooks.
- **How could you use the tool better?** We could have broken up pages and components more and made our UI more modular and idiomatic to React.
- **Is there another tool that might work better?** There are various tools that serve similar purposes, such as Vue.js, Angular.js, or Next.js, although we didn’t have any particular experience with these or ways of comparing.


<h4>Vite</h4>


A build tool for JS frameworks like React. We used this for building, developing, and deploying our React app.


- **How did it meet your needs?** From repository initialization to production deployment, it streamlined the build process nicely.
- **How did it fail to meet your needs?** It was overall quite easy to use and did not fail us in any way.
- **How could you use the tool better?** We could have researched more how to optimize 3D assets (.glb files and such) in the Vite minification (build) process.
- **Is there another tool that might work better?** create-react-app is deprecated, so Vite seems to be the commonly used replacement. We could have taken a more manual approach, but Vite did not give us any issues, so that likely would not have been a good choice.


<h4>Vitest</h4>


A JS/TS testing library from the Vite team, used for unit tests. We used this to do additional testing on the frontend.


- **How did the tool meet your needs?** It had seamless compatibility with our Vite/TypeScript/React project, unlike popular alternatives like Jest, which often have compatibility issues with projects like ours.
- **How did it fail to meet your needs?** Sometimes the mocking of functions was a bit unintuitive, but that might be the case with all similar options.
- **How could you use the tool better?** We could have researched more on how to get deeper into using its rich features. We definitely just scratched the surface.
- **Is there another tool that might work better?** For a project like this, there likely is not a better tool. If we weren’t using TypeScript and Vite, we might have chosen a more popular and mature tool like Jest.


<h4>React Testing Library</h4>


A front end testing library for React components, focusing on what the user sees. We also used this to test the front end components and interactions of those components.


- **How did the tool meet your needs?** It seamlessly allowed us to use Vitest in a React context.
- **How did the tool fail to meet your needs?** It was sometimes a bit hard to decipher the error output when a test did not pass.
- **How could you use the tool better?** We could have gotten more into making sure we were using it idiomatically. In many respects it was quite unfamiliar territory.
- **Is there another tool that might work better?** There is likely no better tool. When using React, React Testing Library is a standard choice and works well with libraries like Vitest and Jest.


<h4>GitHub Pages</h4>


A free hosting service by github, used to serve static websites or a frontend that communicates with a headless backend, such as we did. We hosted our React/TypeScript frontend using the Github pages service.


- **How did they meet your needs?** We were able to quickly deploy our frontend to github pages and it was able to successfully communicate with our API, which was deployed separately on Render’s services. This was also a great free solution to our needs.
- **How did they fail to meet your needs?** When using react-router-dom, it doesn’t allow client-side routing so we had to figure out workarounds and adjust pathing to retrieve assets. We also needed to add shell commands to deploy in strange ways.
- **How could you use the tools better?** Knowing this ahead of time, we could have adjusted our frontend routing early on.
- **Is there another tool that might work better?** Services like Netlify, Vercel or Cloudflare offer probably more standardized solutions, however they are also premium offerings and may require the same level of hand holding provided to Github Pages.


<h4>Three.js</h4>


WebGL API for Javascript. We used this to make 3d vector graphics for our Taskagotchi Avatar, and Items.


- **How did it meet your needs?**
  Three.js was useful for managing and controlling all of the 3D assets (Avatar model, shirt and shoe models), and dynamically loading in a preview model when the user opens their inventory.
- **How did it fail to meet your needs?**
  Three.js actually managed to do everything we needed it to do, and was fairly simple to work with thanks to its extensive documentation.
- **How could you use the tools better?**
  Three.js renders the scene automatically with a target frame rate of 60 rendered frames per second, whether or not those frames are needed. Our project doesn't really need to render all the time, since the scene is fairly static, so we could have tried to optimize the performance by limiting the re-renders.
- **Is there another tool that might work better**
  Babylon.js is considered a more beginner friendly alternative to Three.js, but Three.js provides lower-level control over a scene. Our team felt comfortable working in 3D development, and so decided that Three.js was the right pick for our project.


<h4>React Three Fiber</h4>


React renderer for Three.js, we used this along with three.js to do the front-end vector graphics of the Taskagotchi.


- **How did it meet your needs?** React Three Fiber (R3F) was helpful for converting static meshes (like the walls and floors) into reusable React components for easier manipulation when we were first spinning up the project.


- **How did it fail to meet your needs?** While R3F was useful for static objects, it is not well suited for the dynamic level of control we wanted over the user's avatar. Attaching other meshes to the avatar model like shirts and shoes, or creating copies of the model for the inventory preview was challenging with R3F.
- **How could you use the tools better?** If we had more static items as we originally wanted, such as furniture models to decorate the room with, we could have made greater use of R3F to load those models in as components.
- **Is there another tool that might work better?** Standard Three.js may have been better to work with from the start. We initially thought that R3F would be more dynamic than it was, and so when we needed finer control over the avatar we opted for using Three.js, meaning we used very little React Three Fiber in the end.


<h3>Backend Tools:</h3>


<h4>Flask</h4>


A lightweight web framework used to build backend APIs and server-side rendered web applications.


- **How did it meet your needs?** Easy to set up URL routing, made backend logic easy to understand. The benefits to Flask are that it is lightweight and has its own built-in routing system.
- **How did it fail to meet your needs?** There were no instances where Flask failed to meet our needs.
- **How could you use the tools better?** The routing was straight forward set up with Flask and worked as intended.
- **Is there another tool that might work better?** Some other popular alternatives are Django, Node.js. A benefit for Django would be its admin interface and better large-scale performance, however the downside to Django is that it is heavier than Flask. Node.js is well-suited for Javascript-based full-stack development and has a non-blocking I/O model, however, the downside is that it requires more verbose coding than flask. Overall, we are satisfied with the choice to use Flask instead of other options.


<h4>PostgreSQL</h4>


An open source relational database used to store structured data. We used SQL and postgres as our database for data on the backend.


- **How did it meet your needs?** It provided reliability and structure with data integrity, schema enforcement to manage users, tasks, avatars and transactions. It was also compatible with Docker and worked seamlessly with the environment. This made testing and development consistent for all team members.
- **How did it fail to meet your needs?** The schema migrations seemed to break easily at times. Conflicts and errors arose when branches weren’t synced or migrations weren’t applied in the correct order. This caused schema updates to become a bottleneck for adding customization items and rolling back migration attempts caused added time and difficulty.
- **How could you use the tool better?** We could have centralized migration ownership to avoid merge conflicts. We also could have used Docker volumes to persist PostgreSQL data so that seed data or test records would not disappear between builds.
- **Is there another tool that might work better?** Possible alternatives are SQLite or Supabase. SQLite does not require a server, does not require configuration and works well with Flask.


<h4>Docker</h4>


A containerization tool used for spinning up development and deployment environments. We used this to quickly spin up development containers and create a unified environment for backend development across all of our machines.


- **How did they meet your needs?** We were able to quickly set every developer on our team up with a unified environment, which led to faster initial development instead of fussing around with local environments across Mac, Windows, and Linux machines. It was nice to automatically link the database, database management GUI, and server quickly and run scripts to quickly spin up, tear down, and test new features.


- **How did they fail to meet your needs?** There was a bit of an initial learning curve, and it was frustrating that only the server and database would link on spin up – the pgAdmin database management container had to be manually linked every time that we spun up a “fresh” container


- **How could you use the tools better?** Making separate ‘development’ and ‘production’ dockerfiles would have saved some headache on our deployment day, as a lot of the docker-related files had to be reworked in order to accommodate Render’s service. We also could have explored more ways to auto-link to pgAdmin, or perhaps another database administration tool like dbeaver.


- **Is there another tool that might work better?** Other alternatives include Podman, although I believe we would need an entirely different set of configuration files and recipes to spin that up. It may even use the Docker engine under the hood. Ultimately, Docker was the best choice as it is the industry standard for a reason.


<h4>Unittest</h4>


Python built in testing framework used for unit testing logic and functionality on the back end. We use this to develop unit tests for our models.


- **How did they meet your needs?** It allowed us to quickly implement unit testing on our backend models to ensure they met specification before merging them into main. Was easy to set up scripts to automatically run tests to check before pushing code.
- **How did they fail to meet your needs?** These only offer simple unit tests. Would have been nice to have a more robust testing suite that could simulate making requests, or return values of routes
- **How could you use the tools better?** With the time deadline being a major factor, we always could have written more testing or have more checks for each bit of logic we tested. We could have also set up Github Actions to automatically run our test suite when a developer opened a pull request.
- **Is there another tool that might work better?** For our use case, not really. It was nice to be able to use the tools we learned about in class so our entire team had the same understanding of how to write, use the tests, and update them as needed. Other alternatives such as pytest, doctest would just add thoroughness and perhaps allow us to do more than simple unit testing. In a more real-world product we would have unit, E2E testing, integration tests, regression testing, performance, etc.


<h4>Bruno</h4>


An API Client used for testing, debugging our headless backend during development before implementing requests on the front end. We used this as we were building our backend.


- **How did they meet your needs?** Helped to build out the backend API without waiting on the front-end client to be completed in order to test. Helped us build out the front/back end of our project in parallel and ensure our routes worked before instructing the front end developers how to perform CRUD operations using our API
- **How did they fail to meet your needs?** This did not fail to meet our needs. There may have been a bit of a learning curve starting out to figure out how to send requests in this way, but this was an invaluable tool
- **How could you use the tools better?** There are ways to share route environments and export them to share with other developers, which may have saved us all individually on work
- **Is there another tool that might work better?** Tools like Postman or Insomnia have more capabilities if we had a more robust API, however those tools are paid. This met the needs of this simple project just fine.


<h4>Render</h4>


A cloud platform for hosting web applications and APIs. We used this to deploy our backend Flask API.


- **How did they meet your needs?** Allowed us to quickly deploy our API backend free of charge. It also was very fast, we could just use the dockerfile to rapidly deploy and it would run the file and execute everything as expected, in the same way it did on our local machine.
- **How did they fail to meet your needs?** We had to rewrite a lot of our development Dockerfile to accommodate for Render, removing the pgAdmin and postgres containers and adding seed logic to the dockerfile instead of being to use our make scripts to run post deploy, as we expected.
- **How could you use the tools better?** We could have tried to deploy using docker earlier to know what to expect. Another way to do this better was to have a deployment branch alongside our development branch, so that we have split config between the two toolings we actually needed
- **Is there another tool that might work better? **There are better, more robust alternatives like Heroku, or AWS or Digital Ocean, however those are paid services and we wanted to keep this free.


<h4>JWT (JSON Web Token)</h4>


A token format for transmitting user identity and authenticating requests to our API. We used this for login, logout, authentication for routes and requests, and getting identity on the front end.


- **How did they meet your needs?** It did well to quickly authenticate users' access to information and routes, protected login and personal information. Fairly quick to implement in our project
- **How did they fail to meet your needs?** A bit of an effort to implement on the front end with TypeScript, but overall a positive experience
- **How could you use the tools better?** More consistent application, we could ALWAYS use the JWT to pull user information on the frontend, would help avoid always providing the user_id in the body of the request
- **Is there another tool that might work better?** Other alternatives include OAuth or SAML or old fashioned session cookies. With the biggest factor to our decision being time, JWT was a good choice but if we were to do this on a larger scale OAuth might be the better choice as it uses verification from other services (Google, FB, etc)



