
# Front-end design choises
***

## Framework
***

We chose Vue 3 as our framework for the front-end project for several reasons. Firstly, Vue was a requirement for the project, as it needed to be built using Vue. Additionally, our team had prior experience with Vue, which allowed for a smoother development process and quicker ramp-up time.

In terms of code maintainability and readability, we opted to use TypeScript instead of JavaScript. TypeScript provides strong typing and static analysis, making the code more predictable and reducing potential errors. This decision was aimed at improving code quality and facilitating collaboration among team members.

Furthermore, we took advantage of Vue 3's Composition API. By leveraging the Composition API, we were able to write more concise and readable code. This approach helped reduce complexity, improve reusability, and future-proof our project by embracing the latest features and best practices of Vue.

Overall, the combination of Vue 3, TypeScript, and the Composition API allowed us to build a front-end project that is both maintainable and scalable, while leveraging our existing knowledge and ensuring a solid foundation for future enhancements.

## User Interface

The user interface (UI) of our front-end project was heavily influenced by the interface of Zoho Analytics, taking into account feedback and examples provided by our stakeholders from World of Content. Our primary focus was to simplify the UI, making it easier for users to create widgets using models.

![example wire frame](https://github.com/Null-Not-Found/DashBuddy-Documentation/blob/main/Learning%20Outcomes/Images/widget%20creator%20wire%20frame.png)

During the initial stage of designing our widget creator, we prioritized the essential components necessary for its functionality. We divided the interface into three distinct parts: the Model Explorer, the Query Creator, and the Widget Preview.

The **Model Explorer** serves as a navigation panel where users can access all the available models within the system. By organizing models in a structured manner, users can easily locate and select the desired model for their widgets.

The **Query Creator** section empowers users to build and customize their widgets by specifying the required widget data. Users can leverage the available models from the Model Explorer to create their desired widgets and choose the appropriate graph type to visualize the data.

The **Widget Preview** provides users with a live preview of their widgets, allowing them to visualize the appearance and behavior of the widgets they are creating. While the preview does not utilize real-time data, it simulates the expected output based on the set data. This approach eliminates the need for the backend to retrieve large amounts of data every time the widget is altered, resulting in a more efficient and responsive experience for users.

Initially, we had planned to implement draggable functionality for the models listed in the Model Explorer section, as we believed it would enhance the interactive and intuitive nature of selecting models. Our intention was to allow users to simply drag and drop models from the Model Explorer directly into the Query Creator area, facilitating a seamless integration process for their widgets.

![draggable models](https://github.com/Null-Not-Found/DashBuddy-Documentation/blob/main/Learning%20Outcomes/Images/Draggable%20models%20.png)

However, during the implementation phase, we encountered challenges primarily due to the limited documentation and resources available specifically for Vue 3 Composition API in combination with drag and drop libraries like Vue Draggable. Despite our best efforts to find solutions and workarounds, we were unable to achieve the desired draggable functionality within the Vue 3 Composition API framework.

In order to maintain our development timeline and ensure a stable solution, we made the decision to temporarily set aside the draggable feature. While it would have enhanced the user experience by making the process of choosing models more interactive, we prioritized delivering a reliable and efficient widget creator.

## Component Design

## Layout

## Navigation Structure


