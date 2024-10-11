# Sweet Design: Custom Cake Ordering Application

This project is a web application designed for ordering custom cakes, initially developed for academic purposes. The source code for this application is currently private, as development is ongoing, and it may be intended for commercial use in the future. The application offers users three main ways to order cakes:


1. **Classic Orders**: Users can select cakes from existing offerings and customize certain elements like flavor, edible image, text on the cake and more.

2. **Personalized Orders**: Users can upload an image of a cake they found online and want to order something similar and get an offer for that cake, where they have the option to order the cake by accepting the offer.

3. **Design Your Own Cake**: Users can utilize a design tool to create a cake to their liking, choosing flavors, decorations and other elements. This feature provides interactivity, allowing users to see an approximation of their cake's appearance in real-time. Additionally, the price updates as new items are added enabling immediate ordering upon completion.

## Basic pages and functionalities

### Home Page

The home page provides an overview of the application, featuring sections for classic orders, personalized orders and the cake design tool. Each section guides users to the respective functionalities ensuring an intuitive user experience.

### Cakes Page

The Cakes page displays all available cakes that users can order. Users can filter cakes by various criteria and view detailed information about each cake including images, ingredients, allergens, capacity, price and delivery options. The page also allows users to customize cakes by selecting flavors, adding text, uploading edible images and ordering toppers.

### Personalized Orders

On the home page, users can click a button in the section for personalized orders which opens a modal window where users are prompted to enter their personal details (name, email, phone number), cake flavor and serving size. Users also upload the desired cake image and provide additional information if necessary. Upon submission, an email is sent to the admin notifying admin of the new request. The admin then provides an offer and notification is sent to the user via email. If the user has an account, they are directed to their profile to view the offer, otherwise, they are prompted to register. Users with accounts can accept or reject the offer and upon acceptance they are directed to the payment page.

### Design Your Own Cake

Users start by selecting the cake mold, followed by the serving size, texture (whipped cream, chocolate or fondant) and fondant color if applicable. Next, users choose the flavor, simple decorations (e.g., top and bottom whipped cream, sprinkles) and after that users can place fondant figures on the cake using Drag & Drop functionality. Adding or removing fondant figures adjusts the cake's price. Users then design the top of the cake choosing text type (whipped cream or fondant letters), also users can upload an image if they want edible image on the cake noting that edible images are not allowed if fondant figures are in the center of the cake. Users can also order cake toppers along with the cake order. The design process concludes with an order summary before proceeding to the payment page. At each step, users have the ability to see in real-time how their cake will approximately look like.

### Payment Page

The payment process involves several steps. Users enter their name, email and phone number, which are auto-filled if they are logged in. Next, they provide delivery details including city and address. They then specify the desired delivery or pick-up date and time. The final steps are order review and payment.

### User Profile

The user profile includes three pages: orders, personalized orders and account settings. The orders page displays all user’s orders, their statuses and options to view and reorder the same order. The personalized orders page lists the user's personalized orders and on this page users have the opportunity to see offers for these orders and to reject them or accept active orders. If they accept the order, users are redirected to the payment page. In addition to this, users also have an overview of previous personalized orders. The account settings page allows users to update their personal information and password.

### Admin Panel

Admins have the ability to create, edit and delete cakes, users, flavors and orders. The main dashboard displays three charts showing statistics on orders and users. Also, main dashboard displays information about revenue, users and orders.

### Additional Features

The application includes several additional functionalities to enhance the user experience and maintain robust security:

- **Forgotten Password Functionality**: Users can reset their passwords if forgotten, ensuring they can regain access to their accounts.
- **ProtectedRoute Component**: This component checks user roles when accessing user and admin profile pages, ensuring that only authorized users can access sensitive information.
- **Constants Management**: Data used for designing cakes are stored in a separate file as they are constants. Similarly, other constants used throughout the application are organized in the `appDefaults` file.
- **Context for Cart and User**: Context files for the cart and user are created to allow these states to be used across multiple pages seamlessly.

## Application Structure

The application is organized into several directories, for example:

- **Admin Pages**: All admin-related pages are located in the `Admin` directory.
- **Component Organization**: Each component has its own directory. For example, the `Dashboard` component has a directory containing:
  1. `index.js` - This file contains the component code.
  2. `Dashboard.module.css` - This file contains the CSS module for styling the component.
- **CSS Modules and Global Styles**: While CSS modules are used throughout the project for component-specific styling, global CSS classes that are reused across multiple pages are defined in the `index.css` file.

Here is an example of the application’s frontend directory structure:

/src<br>
&nbsp;&nbsp;&nbsp;&nbsp;/components<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/Admin<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/Dashboard<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/index.js<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/Dashboard.module.css<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/CustomOrders<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/index.js<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/CustomOrders.module.css<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;.<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;.<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;.<br>


## Technologies Used

The frontend is developed with React.js, backend is developed with Node.js and PostgreSQL is used for data storage. In addition to this, firebase is used for authentication (The reason: easy user login via Google and Facebook accounts), although authentication using bycript is also implemented manually. Also, firebase storage is used to store images.


