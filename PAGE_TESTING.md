# Web Page Design

### We will have the following pages:

- Splash Page
- Game
- User/Account Page
- Login/Register
- Store
- Tips

### A note on testing:

Our frontend testing will look a bit different than that of a regular Flask app with server side rendering. Unlike the Python unittest tests in our backend, our TypeScript frontend tests will use Vitest and React Testing Library. Some of the main characteristics of this approach including testing individual components (to pinpoint bugs), mocking functions (so we don't call the real backend during unit testing), and simulating user interactions like clicking and typing (using userEvent from @testing-library/user-event). 

## Splash Page

#### Route: `/` (root)

This page will appear right when new users visit the site. It will show some basic introductory information about the app and link to the login and signup pages. If the user is still logged in from a previous session, they won't see this page and will be automatically redirected to the task page. 

### Data Needed:

- Not really any dynamic data, other than whether the user is still logged in from a previous session (cookies, localStorage, etc.)
- The page itself will be made up of static assets like images

### Parameters:

- No parameters needed

### Tests:

- Relatively simple/trivial compared to other pages 
- Test that it renders, and that the different parts of it also render 

![Splash](<documentation/img/Screenshot 2025-03-05 at 5.30.15 PM.png>)

## Game (Task)

#### Route: `/task`

This is the game page where users will interact with their Taskagotchi, add new tasks, complete existing tasks, and nourish their Taskagotchi avatar. 

It will show streams of days of consistent task-ing, as well as Taskagotchi stats and inventory options. 

### Data Needed:

- Tasks by user
- Last completed Task date for streak
- Time until complete
- Taskagotchi by user
- Taskagotchi health
- User inventory
- Taskagotchi energy

### Parameters:

We could potentially add the username as a parameter in the URL later on if there was some sort of social feature and we wanted users to be able to share links with their friends that would go directly to their page.

### Tests:

- Unit tests:
  - (Many of these unit tests would be associated with the individual components rather than the page overall, but I will write about the tests collectively for the purposes of this document.)
  - Test that it renders as expected
  - Test that it properly displays data passed as props (separate tests for each piece of data)
  - Test for the expected appearance after the user interacts with the page. For example, a task should appear checked off after the user clicks the checkbox.
  - While mocking the function(s) that make(s) API calls to the backend:
    - Test that it uses the hook properly by making sure the mocked function is called with the expected arguments
    - Test that it properly displays or otherwise acts upon the mocked data returned from the mocked function
    - (This would be multiple different tests for different pieces of data and/or API calls)
- Integration tests (if within scope):
  - Test that the correct data is actually retrieved from the real (not mocked) backend API
  - Test that the API calls work locally when running frontend and backend on different ports, and in the cloud from different domains (need CORS)

![Game](<documentation/img/Screenshot 2025-03-05 at 5.32.08 PM.png>)

## User / Account Page

#### Route: `/user` or `/user/<username>` if using parameters

This page allows the user to change preferences such as their password or the name of their character. There will also be buttons for actions like logging out or deleting their account. They can also manage currency here. We will need to get all this user data from the database and make API requests to update anything that the user changes. We could potentially include the username as a parameter in the URL if there some need to navigate directly here from a link, but this may not be necessary. 

### Data Needed:

- Basically all the information from this user's row in the Users table in the database (see image)

### Parameters:

- Potentially the user's username

### Tests: 

- Unit tests:
  - Test that it renders as expected
  - Test that it properly displays data passed as props (separate tests for each piece of data)
  - While mocking the function(s) that make(s) API calls to the backend:
    - Test that it uses the hook properly by making sure the mocked function is called with the expected arguments
    - Test that it properly displays or otherwise acts upon the mocked data returned from the mocked function
    - (This would be multiple different tests for different pieces of data and/or API calls)
    - The User page will need tests for different types of API requests, although the general flow will be similar
- Integration tests (if within scope):
  - Test that the correct data is actually retrieved from the real (not mocked) backend API
  - Test that the API calls work locally when running frontend and backend on different ports, and in the cloud from different domains (need CORS)

![User](<documentation/img/Screenshot 2025-03-05 at 5.29.24 PM.png>)

## Login / Register Form

#### Routes: `/signup` and `/login` respectively

### Description/data:

- See image text

### Parameters:

- None

### Tests:

- Unit tests:
  - Test that it renders as expected
  - Test that the login page shows up first, and properly links to the sign up page via the sign up button
  - Test that it properly displays data passed as props (separate tests for each piece of data)
  - While mocking the function(s) that make(s) API calls to the backend:
    - Test that it uses the hook properly by making sure the mocked function is called with the expected arguments
    - Test that it properly displays or otherwise acts upon the mocked data returned from the mocked function
    - (This would be multiple different tests for different pieces of data and/or API calls)
- Integration tests (if within scope):
  - Test that the correct data is actually retrieved from the real (not mocked) backend API
  - Test that the API calls work locally when running frontend and backend on different ports, and in the cloud from different domains (need CORS)

![Login](<documentation/img/Screenshot 2025-03-05 at 5.27.55 PM.png>)

## Store

#### Route: `/store`

This page will display information about items the user can buy for their character. We will need to get the information about the customization items from the database, comparing that to the data on what the user has already purchased and their current currency balance. 

### Data Needed:

- Item Data
- User current balance
- User current inventory (so user doesn't re-buy items)

### Parameters:

- Likely none, however links to specific items might be an option

### Tests:

- Unit tests:
  - Test that it renders as expected
  - Test that it properly displays data passed as props (separate tests for each piece of data)
  - Test for the expected appearance based on user data. For example, items that a specific user has already bought should clearly be marked as PURCHASED. 
  - Test for the expected appearance based on user interactions. For example, items that a user buys in a given session should directly change appearance as a result.
  - While mocking the function(s) that make(s) API calls to the backend:
    - Test that it uses the hook properly by making sure the mocked function is called with the expected arguments
    - Test that it properly displays or otherwise acts upon the mocked data returned from the mocked function
    - (This would be multiple different tests for different pieces of data and/or API calls)
- Integration tests (if within scope):
  - Test that the correct data is actually retrieved from the real (not mocked) backend API
  - Test that the API calls work locally when running frontend and backend on different ports, and in the cloud from different domains (need CORS)

![Store](<documentation/img/Screenshot 2025-03-05 at 5.28.47 PM.png>)

## Tips

#### Route: `/about`

This will just be a simple static page with information about the project and tips for using the app in a fun and productive way. We will not need to get any data, just static assets like images. 

### Data Needed:

- None (static assets only)

### Parameters:

- None

### Tests:

- As this page is static, any tests would basically just be to make sure it renders.

![Tips](<documentation/img/Screenshot 2025-03-05 at 5.31.30 PM.png>)
