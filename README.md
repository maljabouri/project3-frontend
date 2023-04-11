### Social Media App - Full Stack Group Project

## Brief

- Build a full stack web application. Must be your own work.
- Select a Project Idea of your own.
- Use Express with React to build your application
- Deploy on Heroku or a similar platform so application is live on the web
- Craft a README.md file that explains your app to the world

## Deployed Project Link

The deployed project can be accessed at https://stellar-pavlova-831e00.netlify.app/

- Clone the repository to your local machine.
- Install the required dependencies by running npm install in the project directory.
- Set up a MongoDB Atlas database and create a .env file with your database credentials. 
- Start the backend server by running npm run server in the project directory.
- Start the frontend server by running npm start in the project directory.
- Access the app at http://localhost:3000/.

Note: You may need to adjust the API URL in the apiUrl.js file to match the URL of your backend server.

## Overview & Concept

The project is a social media platform where users can create an account, follow other users, and post content in various formats (text, images, videos, etc.). The main goal of the platform is to provide a space for users to share their thoughts, experiences, and creations with others who share similar interests.

## Technologies Used

The project uses the following technologies:

Frontend:
- ReactJS
- HTML/CSS
- Axios
- React Router

Backend: 
- Node.js
- Express
- MongoDB

### Approach Taken

## Planning

As a group we broke up our app into smaller tasks using a Trello board, and then each member picked which tasks they wanted to work on. We worked together on Zoom, group coding the initial setup of the backend. 

## Wireframe

https://www.figma.com/file/0r22Y1xfk9pNu5cdQCQxiu/Social-media-app?node-id=0-1

## Initial ERD

![erd](https://i.imgur.com/PgOxe8H.png)

## Build Process 

The project was developed using an agile methodology, with frequent iterations and feedback loops. The project was divided into several components, each with its own set of features and requirements. My main contribution was to the posts and feed components.

Posts Component:

For the Post component, I used the useState hook to manage state variables for editMode, postData, and updatedPostBody. I fetched post data from the backend API using the findPost function and set the postData state accordingly. I defined functions to handle clicks on the "Edit", "Save", and "Like" buttons, and to handle changes to the post text area. Finally, I conditionally rendered the component UI based on the editMode state.

![snippet1](https://i.imgur.com/G3t4mfE.png)

For the CreatePost component, I used the useState hook to manage state variables for postContent and showForm. I defined a function to handle the form submission, which called the addPost function from the backend API and updated the currentUser state. I conditionally rendered the component UI based on the showForm state.

![snippet2](https://i.imgur.com/DCamqWl.png)

I defined the Feed component as a functional component with the useState hook to manage the state of my posts array. To fetch the necessary data from the backend API, I used the useEffect hook to trigger the API calls and update the state of the component when necessary. I also used conditional rendering based on the currentUser and profilePage props.

![snippet3](https://i.imgur.com/AAU5a2g.png)

Finally, I mapped through the posts array and rendered a Post component for each post. I also conditionally rendered a CreatePost component if the profilePage prop was true, allowing users to create new posts.


Backend Counterparts:
- The backend counterparts for the posts and feed components include a set of APIs for creating, reading, updating, and deleting posts.
- The APIs are implemented using Node.js and Express, with data stored in a MongoDB database.
- The APIs use authentication and authorization to ensure that only authorized users can access or modify data.

## Bugs, Blockers & Wins

During the development process, several bugs and blockers were encountered. Some of the most significant issues included:
- Infinite looping caused by hooks used to update the page
- Difficulties caused by a lack of foresight on how we would build the project as a team, getting stuck on certain parts as we needed features other people had yet to finish



Despite these challenges, the project also had several wins, including:
- A streamlined and user-friendly interface for creating and sharing posts.
- A scalable and flexible backend architecture that could easily accommodate future feature additions and updates.
- A great experience working as a team and some insight into some of the difficulties that can occur when building something alongside other people, and how to overcome those challenges.

## Future Features + Key Learnings

Some potential future features for the project could include:
- A search function to allow users to find specific content or users.
- Advanced filtering and sorting options for the feed.
- Integration with other social media platforms or APIs to expand the platform's reach and functionality.
Some key learnings from the project include:
- The importance of clear and effective communication and collaboration within a development team.
- The value of user testing and feedback in shaping and refining the platform's features and functionality.
- The need for continuous monitoring and maintenance to ensure the platform remains secure and functional over time.
