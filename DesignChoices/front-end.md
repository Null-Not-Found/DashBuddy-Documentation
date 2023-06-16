
# Front-end design choises
***

This document primarily focuses on the design choices we made for the widget creator, as it was our main focus during the limited time we worked with World of Content. The widget creator is an essential component of the front-end project, allowing users to create customized widgets using models.

## Framework
***

We chose Vue 3 as our framework for the front-end project for several reasons. Firstly, Vue was a requirement for the project, as it needed to be built using Vue. Additionally, our team had prior experience with Vue, which allowed for a smoother development process and quicker ramp-up time.

In terms of code maintainability and readability, we opted to use TypeScript instead of JavaScript. TypeScript provides strong typing and static analysis, making the code more predictable and reducing potential errors. This decision was aimed at improving code quality and facilitating collaboration among team members.

Furthermore, we took advantage of Vue 3's Composition API. By leveraging the Composition API, we were able to write more concise and readable code. This approach helped reduce complexity, improve reusability, and future-proof our project by embracing the latest features and best practices of Vue.

Overall, the combination of Vue 3, TypeScript, and the Composition API allowed us to build a front-end project that is both maintainable and scalable, while leveraging our existing knowledge and ensuring a solid foundation for future enhancements.

## User Interface
***
The user interface (UI) of our front-end project was heavily influenced by the interface of Zoho Analytics, taking into account feedback and examples provided by our stakeholders from World of Content. Our primary focus was to simplify the UI, making it easier for users to create widgets using models.

![example wire frame](https://github.com/Null-Not-Found/DashBuddy-Documentation/blob/main/Learning%20Outcomes/Images/widget%20creator%20wire%20frame.png)

During the initial stage of designing our widget creator, we prioritized the essential components necessary for its functionality. We divided the interface into three distinct parts: the Model Explorer, the Query Creator, and the Widget Preview.

The **Model Explorer** serves as a navigation panel where users can access all the available models within the system. By organizing models in a structured manner, users can easily locate and select the desired model for their widgets.

The **Query Creator** section empowers users to build and customize their widgets by specifying the required widget data. Users can leverage the available models from the Model Explorer to create their desired widgets and choose the appropriate graph type to visualize the data.

The **Widget Preview** provides users with a live preview of their widgets, allowing them to visualize the appearance and behavior of the widgets they are creating. 

We decided to use split panes to divide the three main components of the widget creator. This design element allows users to adjust the size and visibility of each component according to their preferences and the task at hand. By expanding or shrinking the panes, users can focus their attention on the specific part of the widget creator they are currently working on.

### More about the **model explorer**
***
Initially, we had planned to implement draggable functionality for the models listed in the **Model Explorer** section, as we believed it would enhance the interactive and intuitive nature of selecting models. Our intention was to allow users to simply drag and drop models from the Model Explorer directly into the Query Creator area, facilitating a seamless integration process for their widgets.

We also planned a search bar at the top of the **model explorer**. This search functionality would allow users to easily and rapidly locate specific models by typing relevant keywords or terms, simplifying the process of finding the desired models for their widgets.

![draggable models](https://github.com/Null-Not-Found/DashBuddy-Documentation/blob/main/Learning%20Outcomes/Images/Draggable%20models%20.png)

However, during the implementation phase, we encountered challenges primarily due to the limited documentation and resources available specifically for Vue 3 Composition API in combination with drag and drop libraries like Vue Draggable. Despite our best efforts to find solutions and workarounds, we were unable to achieve the desired draggable functionality within the Vue 3 Composition API framework.

In order to maintain our development timeline and ensure a stable solution, we made the decision to temporarily set aside the draggable feature. While it would have enhanced the user experience by making the process of choosing models more interactive, we prioritized delivering a reliable and efficient widget creator.

### More about the **Query Creator**
***
In the **Query Creator** section, we designed the interface with inspiration from Zoho Analytics, aiming to provide users with a seamless and intuitive experience. The Query Creator is structured from top to bottom, guiding users through the widget creation process.

At the top of the Query Creator, users can enter the name of the widget, allowing them to easily identify and manage their creations. This field provides a quick and convenient way to assign a meaningful name to each widget.

Next, users can select a model from the Model Explorer and specify the data for the y and x axes of the widget's graph. By leveraging the available models, users can effortlessly incorporate the desired data into their widgets, ensuring accurate and relevant visualizations.

To enhance the flexibility and customization options, the Query Creator also offers users the ability to apply filters or include additional data. These features enable users to fine-tune their widgets and access specific subsets of data, making it easier to analyze and visualize the desired information.

Finally, users can choose their preferred graph type by selecting the corresponding bullet points or graph icons located at the bottom of the Query Creator. This placement allows users to have a clear overview of the available graph types and easily compare them to select the most suitable option for their visualization needs.

By following this top-to-bottom design approach, we aimed to streamline the widget creation process, ensuring a logical flow and enabling users to effortlessly build customized widgets while leveraging the power of the available models and graph types.

In addition to the previously described elements, the last component nested within the Query Creator is an "Add" button, labeled with a "+". This button serves as the final step in the widget creation process.

Once users have configured their desired widget by specifying the name, selecting a model, setting data for the y and x axes, applying filters or additional data, and choosing a graph type, they can click the "Add" button.

Clicking the "Add" button initiates the action of adding the widget to the user's dashboard. The dashboard is conveniently located in the top-right corner of the Query Creator interface. This placement ensures easy visibility and accessibility for users to view and manage their created widgets within the context of their overall dashboard layout.

### More about the **Widget Preview**
***
For the **Widget Preview**, we decided to utilize the same component as the widgets used on our dashboard. Although the widgets are currently kept simple due to time constraints during the design phase, they still provide a visual representation of the user's created widgets.

To optimize performance and ensure a responsive user experience, we opted to use generated values instead of making backend calls each time the widget is edited or when the data models change. By doing so, we alleviate the load on our program and provide users with faster insights into how their widgets will look.

While the generated values may not reflect real-time data, they effectively simulate the expected output based on the specified widget configurations. This approach strikes a balance between providing users with an immediate preview and maintaining the efficiency and responsiveness of the system.

## Component structure
***
To ensure easy reusability and maintain a structured codebase, we organized our front-end components using a specific file structure. Each component was placed in its own file, and any components used within that component were nested in files beneath it.

This file structure helped us maintain a clear separation of concerns and made it easier to locate and modify specific components when needed. It also promoted code reuse, as components could be easily imported and used in different parts of the application.

Here is an example of the file structure we used for the widget creator component:

![files widget creator](https://github.com/Null-Not-Found/DashBuddy-Documentation/blob/main/Learning%20Outcomes/Images/Widget%20creator%20files%20.png)

In addition to the file structure for specific components, we also had a dedicated folder called "default" that housed our default components. These default components were designed to be used throughout the entire application, providing consistent styles and functionality.

The "default" folder, located directly under the "components" directory, contained components such as buttons, containers, form elements, and other commonly used UI elements. These components followed a similar file structure, with each component having its own file.

Here is an example of the file structure we used for the default components:

![default folder](https://github.com/Null-Not-Found/DashBuddy-Documentation/blob/main/Learning%20Outcomes/Images/default%20folder.png)






