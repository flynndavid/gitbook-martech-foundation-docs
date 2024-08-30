# Martech Foundation Documentation 8785c1fb68db43acbc2172d94c58bf20

## Martech Foundation Documentation

![https://www.notion.so/icons/link\_green.svg](https://www.notion.so/icons/link\_green.svg) \[Discord]\(https://discord.com/invite/fnMfNZY3tR) \[Website]\(https://www.martech-studios.com/) \[Template]\(https://bubble.io/template/martech-foundation-template-1722613672005x484208141463191550) \[Build It For Me]\(https://www.martech-studios.com/foundation-template)

## Overview

The Martech Foundation Template is a comprehensive, modular application framework designed to provide developers with a robust set of foundational features for building complex web applications. It offers a wide range of pre-built functionalities and customizable components, allowing developers to focus on creating quality products and businesses.

### Key Features

* User Authentication and Onboarding
* Admin Portal for app-wide settings and management
* Customizable Dashboard with various modules
* CRM views (Grid, Table, and Card)
* Project Management with Kanban boards
* File Library for document management
* Messaging system
* AI Assistants and Image Generation
* Notification Center
* Subscription and Billing management

### Core Concepts

* Modular design with reusable elements
* Team-based data structure
* User roles and permissions
* Integration with external services (Stripe, OpenAI, Google SSO)
* Customizable email templates and notifications

### Admin Capabilities

* Manage app-wide settings and branding
* Customize user roles and permissions
* Create and manage email templates
* Set up subscription plans and marketplace items
* Monitor user activity and manage waitlists

### User Dashboard

* Customizable analytics and reporting
* Project management tools
* CRM functionality
* File management
* AI-powered assistants and image generation
* Account and billing management

### Development Best Practices

* Build using reusable elements for flexibility
* Utilize universal styles for consistency
* Follow modular design principles
* Leverage pre-built workflows and data structures

The Martech Foundation Template provides a solid starting point for developers looking to create sophisticated web applications with a wide range of features out of the box. Its modular design and extensive customization options make it adaptable to various business needs and use cases.

## Introduction

## Introduction and Overview

Welcome to our Template, feel free to reach out to our team in [Discord](https://discord.com/invite/fnMfNZY3tR)! The Martech Core Foundations Template is designed to provide a robust set of foundational features out of the box so that you can focus more on building a quality product and business. The app is designed in a data first way that heavily relies on re-usable elements. Thanks to this design we are perpetually adding new features making it easier and easier to create larger more complex apps. If you’d like to stay up to date as we add new features and give some away for free, you can join our [Discord](https://discord.com/invite/fnMfNZY3tR) or drop your email here (add email input section).

Please be aware our docs are a work in progress, if you need help please reach out via discord.

## Getting Started

Here are some tips for getting your app setup with Foundation.

[https://www.loom.com/share/e34581aa1a9941bfa59b340e66a941b8?sid=d6e87a84-7134-4fff-96d1-8c879e4b8b42](https://www.loom.com/share/e34581aa1a9941bfa59b340e66a941b8?sid=d6e87a84-7134-4fff-96d1-8c879e4b8b42)

### **Install the template and create your app**

* From within your Bubble account, go to the [Core Foundation marketplace](https://bubble.io/template/foundation-by-automatic-1673596403969x408542417388568600) and install the template.
* Once installed, click "Create an app" and select the Martech Core Foundations template. Then name your app and click Get Started.

### **Bubble Setup & Plan**

* Select your app's default font. The majority of text in the app uses this font.
* Update your primary color. Many buttons and highlighted areas of the app use the Primary color defined here. Update the other colors as needed during development.
* This section is under the styles tab under style variables as shown below
* All plugins required for the template are already installed.
* You’ll then want to place your app on a basic plan

### **Open Admin Portal to Finish Setup**

* Go to the data tab in your app, then the app data section, then search for the users table.
* From here select the admin@template.com email and click "run as" to access the admin page.
* We recommend disabling debug mode so elements display correctly. Just remove this section from the url and any “&” before it.
* The admin portal is where you can customize app-wide settings, add new sections to the dashboard, or incorporate additional features.
* To create a new admin account, you will need to go through the existing Sign Up flow and add the App Admin role (Option set) to your new user from the Bubble database. You can also manage User's roles from the Users tab in the admin portal.

### **Set Up API Keys & External Accounts**

* Some functionality requires external APIs to work. You'll need to add your own API keys to use them.

#### Postmark - transactional emails

**Postmark Setup:**

* Setup an account on [Postmark](https://postmark.com/) and verify your Sender Account. Replace the values in the plugin below with your Postmark API keys.
* The admin portal has an Email section where Email Templates can be customized and managed. This all lives in the reusable “🛠️ Admin - Email Templates”
* Before emails will send, make sure to update the “Sender Email” with a validated email from your Postmark Account.
* The Primary Color is used to update the color of the buttons and top border of the HTML template
* The HTML template is hard-coded in this element. To customize the HTML directly, you can find it in the “var - Template HTML Content” element
* In the admin portal, you can create a new email template or edit existing ones. When creating a new one, you have the option of writing a brief description and allowing AI to generate the copy for you — or starting from scratch.
* Dynamic tags can be used to pass in dynamic data via the backend workflow that sends the email. Tags can be any value wrapped in \{{curly-brackets\}}, but will need to be defined in the ‘send-email-from-template’ backend workflow.
* For quick use, dynamic tags can be added to the Option Set “OS\_Dynamic\_Email\_Tags” and will be displayed in this menu for easy copy & paste.
* Backend workflow “” should be used to send all emails. The API workflow has multiple parameters, many optional, that are used to define the dynamic tags.
  * This workflow also can also be triggered by the ‘create-notification’ workflow that additionally creates an in-app notification that is displayed in a User’s notifications list. This workflow uses the ‘standard-notification’ email template.

#### OpenAI - AI Assistants, Prompts & Image Generation

To enable the built-in chat bot, you'll need to get an API key from [OpenAI](https://platform.openai.com/).

Add your API Key in the API Connector plugin to the OpenAI API

[https://docs.foundationtemplate.com/\~gitbook/image?url=https%3A%2F%2F2579826874-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FV1MErI30ZCe37SndGqT1%252Fuploads%252FMUYhtwAehkXldYBTBWgU%252Fimage.png%3Falt%3Dmedia%26token%3Dabcbf528-2216-4b9e-afb7-ad9042defcfe\&width=300\&dpr=4\&quality=100\&sign=c716aedf\&sv=1](https://docs.foundationtemplate.com/\~gitbook/image?url=https%3A%2F%2F2579826874-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FV1MErI30ZCe37SndGqT1%252Fuploads%252FMUYhtwAehkXldYBTBWgU%252Fimage.png%3Falt%3Dmedia%26token%3Dabcbf528-2216-4b9e-afb7-ad9042defcfe\&width=300\&dpr=4\&quality=100\&sign=c716aedf\&sv=1)

#### Stripe - subscriptions and payment

Stripe is used to capture and manage User subscriptions to your app. The template makes this process super easy to manage and update as needed.

To get started, you'll need a Stripe account and the API keys.

1. Add the keys in two places:
   1. API Connector > Stripe API
   2. Stripe plugin.
2. In the "Get Stripe Prices" API, add 'data.product' to the expand\[] parameter. Example below.
3. Make sure the Stripe Plugin has Checkout v3 selected.

_Make sure to use your development keys while building so you can make test payments._

***

**API Connector Plugin > Stripe:**

[https://docs.foundationtemplate.com/\~gitbook/image?url=https%3A%2F%2F2579826874-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FV1MErI30ZCe37SndGqT1%252Fuploads%252FjnkFNhP34VXYLhmD7rNr%252Fimage.png%3Falt%3Dmedia%26token%3Dfa32ab1a-e1de-4b2b-8823-5b5e843e2e2f\&width=300\&dpr=4\&quality=100\&sign=34ce3f25\&sv=1](https://docs.foundationtemplate.com/\~gitbook/image?url=https%3A%2F%2F2579826874-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FV1MErI30ZCe37SndGqT1%252Fuploads%252FjnkFNhP34VXYLhmD7rNr%252Fimage.png%3Falt%3Dmedia%26token%3Dfa32ab1a-e1de-4b2b-8823-5b5e843e2e2f\&width=300\&dpr=4\&quality=100\&sign=34ce3f25\&sv=1)

**Update Expand Parameter:**

[https://docs.foundationtemplate.com/\~gitbook/image?url=https%3A%2F%2F2579826874-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FV1MErI30ZCe37SndGqT1%252Fuploads%252FvGKEK1aQ7HFDGuLjadwQ%252Fimage.png%3Falt%3Dmedia%26token%3Dc97aeade-214c-4668-9598-b125bf4fc664\&width=300\&dpr=4\&quality=100\&sign=abfa81d5\&sv=1](https://docs.foundationtemplate.com/\~gitbook/image?url=https%3A%2F%2F2579826874-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FV1MErI30ZCe37SndGqT1%252Fuploads%252FvGKEK1aQ7HFDGuLjadwQ%252Fimage.png%3Falt%3Dmedia%26token%3Dc97aeade-214c-4668-9598-b125bf4fc664\&width=300\&dpr=4\&quality=100\&sign=abfa81d5\&sv=1)

**Stripe Plugin:**

[https://docs.foundationtemplate.com/\~gitbook/image?url=https%3A%2F%2F2579826874-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FV1MErI30ZCe37SndGqT1%252Fuploads%252FkzfMDdC747djiZVy5JRi%252Fimage.png%3Falt%3Dmedia%26token%3D522aa107-bd0a-486e-bbe9-4c4dbd0d15da\&width=300\&dpr=4\&quality=100\&sign=a3ce5bd1\&sv=1](https://docs.foundationtemplate.com/\~gitbook/image?url=https%3A%2F%2F2579826874-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FV1MErI30ZCe37SndGqT1%252Fuploads%252FkzfMDdC747djiZVy5JRi%252Fimage.png%3Falt%3Dmedia%26token%3D522aa107-bd0a-486e-bbe9-4c4dbd0d15da\&width=300\&dpr=4\&quality=100\&sign=a3ce5bd1\&sv=1)

#### Google - Single Sign On

You'll need to get an App Secret and an API Key from [Google Cloud Console](https://console.cloud.google.com/apis/credentials/consent) to enable Google Sign On.

[https://docs.foundationtemplate.com/\~gitbook/image?url=https%3A%2F%2F2579826874-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FV1MErI30ZCe37SndGqT1%252Fuploads%252FnaUj0Lwpc1I66O0KiOiq%252Fimage.png%3Falt%3Dmedia%26token%3Dafa80075-4034-4740-a1b7-8d9c73602f09\&width=300\&dpr=4\&quality=100\&sign=c2faf5e5\&sv=1](https://docs.foundationtemplate.com/\~gitbook/image?url=https%3A%2F%2F2579826874-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FV1MErI30ZCe37SndGqT1%252Fuploads%252FnaUj0Lwpc1I66O0KiOiq%252Fimage.png%3Falt%3Dmedia%26token%3Dafa80075-4034-4740-a1b7-8d9c73602f09\&width=300\&dpr=4\&quality=100\&sign=c2faf5e5\&sv=1)

Here's a great video for more help:

[https://www.youtube.com/watch?v=XuUkshWifok](https://www.youtube.com/watch?v=XuUkshWifok)

### Stripe Setup

1. **Connect API Keys**
   * Integrate your API keys with the application.
2. **Delete Template Users**
   * Remove all users that were included with the template. They may contain Stripe data that is referencing the template’s stripe account.
3. **Create a New Admin Account**
   * Sign up as new user via the app’s standard signup flow
   * Go into bubble database and add “App Admin” to the new User’s Role(s)
4. **Delete Existing Stripe Plans and Marketplace Items**
   * Remove any Stripe plans or marketplace items that came with the template. These are connected to the template’s stripe account and will not work with your new stripe account.
   * Datatypes to delete: “Stripe Plan” & “Marketplace Product”
5. Setup Stripe Webhooks:
   * The template has 2 Stripe webhook backend workflows that are already setup. You just need to setup your Stripe webhooks to trigger them.
   * …/api/1.1/wf/stripe-checkout-session-completed
   * …/api/1.1/wf/stripe-webhook-update-subscription
6. **Create New Stripe Plans and Marketplace Items**
   * Use the admin portal to create new Stripe plans and marketplace items as needed.
   * Stripe subscription plans will need to be created in Stripe first, then linked to the app via admin portal.
   * Marketplace products can be created directly in the admin portal and will be created / updated directly in Stripe via API

* _**Error Handling:** there is a workflow in the Header element that runs for any error the app encounters. The workflow creates a database item “Error Logs” so you can see details. It also shows an AirAlert letting the user know an error occurred._

## **Admin Portal**

### Admin Features

#### **Settings Tab**

* Customize app wide branding, icons, logos, and social sharing features.
* Enable Google SSO, waitlist, 2FA sign-up, and demo accounts.
* Set privacy rules and terms & conditions.

#### **Header Section**

* Add user roles and navigation buttons to the header.
* Customize user access, button styles, icons, and links.
* Include additional user info and notification bars.

#### **Page Settings**

* Customize which functionalities should be available on your users dashboards.
* Add buttons, pages, and templates to the app.
* Choose different UI templates for landing pages, marketing pages, and blog pages.

#### **Users**

* Manage app users, user roles, waitlist, and subscriptions.

#### **Email Templates**

* Edit email templates and prepare for scheduled marketing emails.

#### **Subscriptions**

* Create and manage subscription packages on stripe directly or from our app and watch as both stripe and our template sync up.

#### **Marketplace**

* Set up a marketplace for product offerings and discounts.

#### **AI Assistants**

* Access OpenAI assistants calls, let your users use these assistants or let them make their own and share them with your community.

#### **AI Prompts**

* Create savable AI prompts that can be used in workflows within your app. We accomplish this by saving a slug for the workflow and referencing it later in our workflows.

#### **Feature Requests**

* Let your users give you feature or feedback requests, store them in a way that allows users to vote on their importance.

### Admin Reusables

* Settings (🛠️ Admin - General App Settings)
  * Preview
  * Editor
*   Header (🛠️ Admin - Header Nav Mgmt)

    *   Preview

        Template Docs - Header.mp4

        #### **Header Navigation Settings**

        * Customize all of the aspects of your application’s header.
        * Allows for different headers for different user types, personalized user profile display, notifications and many more upcoming aspects.

        #### Header - User Type Personalization

        * In this section you are able to go down the list of different user types that you have and create a personalized header for each user type.
          * Standard User
          * App Admin
          * Affiliate User
          * Logged Out
          * Custom User - Any New User type you want to create
        * Choose which pages and other aspects you want to be visible in the header of your application.

    #### User Profile Display

    * Choose how Users names are displayed in the header
      * First Name
      * Full Name
      * Email
      * Nothing

    #### Notifications

    * Choose whether or not you want users to see the number of notifications that they have in the header.
    * Editor
* Page Settings (🛠️ Admin - Page & Sidebar Settings)
  * Preview
  * Editor
* Individual Page Settings (🛠️ Admin - Pages List)
  * Preview
  * Editor
*   Users (🛠️Admin - Users List)

    *   Preview

        Template\_Docs\_-_Users_.mp4

    #### Users

    * Editor
* Email Templates (🛠️ Admin - Email Templates)
  * Preview
  * Editor
* Subscriptions (Admin - User Subsc. Mgmt)
  * Preview
  * Editor
* Waitlist (🛠️Admin - Waitlist)
  * Preview
  * Editor
* Invites (🛠️Admin - Invites)
  * Preview
  * Editor
* Marketplace
  * Preview
  * Editor
* AI Assistnats (re: Assistants Listing, re: Assistant Thread Container, menu: manage-assistant)
  * Preview
  * Editor
* AI Prompts (Admin: AI Prompts)
  * Preview
  * Editor
* AI Run Logs (admin: Logs Popup)
  * Preview
  * Editor
* Feature Requests
  * Preview
  * Editor

## **User Dashboard**

#### **Analytics**

* Insights and performance metrics
* Data visualization and reporting tools

#### **Onboarding**

* Guided setup process
* User tutorials and walkthroughs
* Forms

#### **CRM Views**

* Customer relationship management dashboards
* Contact and interaction tracking
* Three variations: Table, Card, and Grid

#### **Project Management**

* Task and project tracking
* Collaboration tools and timelines

#### **File Library**

* Document storage and management
* File sharing and version control

#### **Messaging**

* Internal and external communication tools
* Chat and email integration

#### **AI Assistants**

* Automated support and task management
* Intelligent suggestions and workflows

#### **Image Generation**

* Tools for creating and editing images
* AI-powered design features

#### **Notification Center**

* Alerts and updates for various activities
* Customizable notification settings

#### **Accounts and Billing**

* User account management
* Billing information and payment options
* Subscription and plan management

## Best Practices

### Build Everything in a Re-Usable

This makes it easier to move things around and move to different pages as your app evolves. This flexibility allows you to clone or detach RE’s and allows us to more easily provide you with feature updates as we move through roadmap.

### Universal Styles

Use styles consistently across the app and use universal styles found on the styles tab > styles variable tab

### Do I need the Teams Data Type if my MVP only needs to handle one user at a time?

If you ever plan to let your users invite other users to work together under the same umbrella then you will want to keep the Teams data type and functionality during sign up. For your single user MVP we recommend hiding the UI for teams in the settings, onboarding, and invite sections.

The easiest way to disable / hide it will be to remove from the option set account tabs. Remove the “Team Members” Option set.

### Creating New Data Via Popup

[https://www.loom.com/embed/8fd0713e1abb4f9dbc5cfa5bfe29ffa6?sid=b850c08c-439d-4ebb-9a90-34b3c608f76d](https://www.loom.com/embed/8fd0713e1abb4f9dbc5cfa5bfe29ffa6?sid=b850c08c-439d-4ebb-9a90-34b3c608f76d)

### Code Explanation: Reusable Pop-up Component

This code snippet demonstrates the implementation of a reusable pop-up component in an app for creating and editing various types of data. The pop-up component is designed to be versatile and easily adaptable for different sections of the application.

#### Overview

The app includes various types of information that require pop-ups for creating, editing, or adjusting data. The key feature of this template is the use of reusable elements within reusable elements, enhancing the modularity and reusability of the code.

#### Components

1. **Kanban Board**: The Kanban board (RE project Kanban) serves as a reusable component.
2. **Menu Icon**: The menu project icon (Menu Project Icon) is another reusable element nested within the Kanban board.

#### Functionality

* The menu icon component allows users to interact with the data by clicking on it, triggering specific actions based on the data type (e.g., lead, user, assistant, project).
* Various functions can be called within the component, such as displaying data in a pop-up.
* Workflows within the reusable components can be easily referenced and triggered from different sections of the application.

#### Workflow Example

1. When a user clicks on the menu icon within the Kanban board, data is sent to the component.
2. The component triggers the "create edit project" workflow, displaying the relevant data in a pop-up.
3. This workflow structure is a common practice in development, particularly within the Bubble platform, for creating dynamic and interactive pop-ups.

#### Conclusion

The implementation of reusable pop-up components offers a scalable and efficient way to manage data interactions within the application. Developers are encouraged to follow this pattern when adding new features or functionalities to ensure consistency and maintainability.

If you have any questions or need further clarification, feel free to reach out to us on Discord. We are here to assist you. Thank you!

## Core Concepts

* Log In Sign Up (🧰 Signup Login Auth & Onboarding)
  * Re-usable element that can be places anywhere in the app.
  * By Default it lives on the index page
  * Sign Up and Onboarding Flow
    * Basic Email and password sign up (g:step 1 - user info)
    * Optional Google SSO functionality that is turned on and off from the admin portal. Must have google api keys added in the editor to use this.
    * Optional 2FA functionality that is turned on and off from the admin portal. You will need emails set up for this. See email setup here (PUT LINK HERE).
    * Step 2 of the flow has two parts (g:step 3 - profile info - invites)
      * One to create a “Team” data type and make this user the leader of the team (g:step 2 - Profile info)
      * And one to sign up as an invited member of another users team (g:step 2 - Accept an invite?). They are then added to that other team and skip the other steps.
    * Custom workflow that runs at the end of the flow to fill the data field “Date Sign Up Complete” on the user. This will set this date as the current date team
  * Log In Flow
    * Basic email password log in (Auth: Login)
    * Google SSO works in the same way
    * The workflow checks if the current users “Date Sign Up Complete” value is empty. If empty, it will switch back to the sign up flow. If it has a date, it takes them to their proper user role location in the app.
  * Auth Redirect (Read more here) (PUT LINK HERE)
* Team Data Type ([Coming Soon](https://discord.com/invite/fnMfNZY3tR))
* Modularity - Best Practices on Making a New Page ([Coming Soon](https://discord.com/invite/fnMfNZY3tR))
* Notifications and Email ([Coming Soon](https://discord.com/invite/fnMfNZY3tR))
* Stripe and Subscriptions ([Coming Soon](https://discord.com/invite/fnMfNZY3tR))
* User Roles ([Coming Soon](https://discord.com/invite/fnMfNZY3tR))

## Core Reusables

* Dashboard (re: Dashboard Template)
  * Preview
  * Editor
* Onboarding (🎨 Element - Multistep Form)
  * Preview
  *   Editor

      [https://www.loom.com/embed/8278187015d64f0d899ea2146e723e62?sid=e06db1d1-0e85-4102-8faa-f47a87610c38](https://www.loom.com/embed/8278187015d64f0d899ea2146e723e62?sid=e06db1d1-0e85-4102-8faa-f47a87610c38)

      ### Martech Foundation's Onboarding Page Documentation

      The Martech Foundation's onboarding page is a reusable multi-step form element that can be utilized in various parts of an application. It consists of a next button, a back button, and a complete button. The next button progresses to the next step in the form, while the back button allows users to navigate to the previous step.

      #### Functionality Overview

      * The `var number of steps` field sets the total number of steps in the form.
      * The `current step` variable keeps track of the current step, defaulting to 1.
      * Clicking the next button triggers a custom event called `navigate step`, incrementing the current step by 1.
      * Updating the `current step` variable moves the user to the next step in the form.
      * The back button works similarly by decrementing the current step.

      #### Custom Events

      * The `navigate step` custom event facilitates the navigation between form steps.
      * It compares the current step with the total number of steps to progress through the form.

      #### Onboarding Percentage Tracking

      * The onboarding percentage tracking feature calculates the completion progress of the form.
      * It is useful for redirecting users back to the onboarding process if incomplete.
* CRM
  * Grid (🎨 CRM - Grid View)
    * Preview
    * Editor
  * Table (🎨 CRM Table View)
    * Preview
    * Editor
  * Card (🎨 CRM - RG User Profile Cards)
    * Preview
    * Editor
* Project Board (re: Project KanBan)
  *   Preview

      [https://www.loom.com/embed/66196dee7ac5453f810007cfcd77e539?sid=b2828994-7c3f-4286-9b61-2dfc0c825be2](https://www.loom.com/embed/66196dee7ac5453f810007cfcd77e539?sid=b2828994-7c3f-4286-9b61-2dfc0c825be2)

      ### Documentation: Managing Stages in Project Kanban

      This video walkthrough covers the management of stages in the Project Kanban feature.

      #### Edit Stages Popup

      * Located on the reusable element, Project Kanban page.
      * Allows sliding and dragging of sections.
      * Changes can be saved to adjust the order of stages.

      #### Adding New Stages

      * Clicking "Create New Stage" allows for adding a new stage.
      * Fill in the required fields and save the changes to create a new section in the campaign.

      #### Modifying Existing Stages

      * Clicking on existing stages allows for editing or deleting them.
      * The "App Default Stage" is only visible to admins or builders.
      * It serves as a template for default stages for new users signing up.

      By utilizing the Manage Stages section, users can customize and set up stages for their projects effectively.
  *   Editor

      ### Part 1: Kanban Stage Management

      [https://www.loom.com/embed/8b2e4799c006470fa22b8dc2d2d142e7?sid=7efe2014-46ed-4538-83a0-2b9da10e58f9](https://www.loom.com/embed/8b2e4799c006470fa22b8dc2d2d142e7?sid=7efe2014-46ed-4538-83a0-2b9da10e58f9)

      ### Documentation: Managing Kanban Stages Popup

      This documentation explains how the editor side of the Manage Kanban Stages popup works in the Reusable Element project Kanban Reusable, specifically focusing on the Popup Edit Stages element.

      #### Popup Anatomy

      The Popup Edit Stages consists of two sections: a left section and a right section.

      * **Left Section:** Manage, edit, and rearrange different stages, as well as add new stages.
      * **Right Section:** Add or edit values for stages.

      #### Setting Up

      * Ensure you have a paid version of the plugin for full functionality.
      * Check the plugin documentation for available elements, events, and actions.

      #### Working with Draggable Elements

      * Locate and set up the draggable rg section element to enable drag-and-drop functionality within the repeating group.
      * Add an id attribute to the HTML elements for identification.
      * Connect the id attribute to the repeating group id in the draggable rg element to access plugin workflows.

      #### Events and Actions

      * Utilize events like draggable rg section item moved to track item movements.
      * Update sort order field on the kanban stages data type and refresh the repeating group element when items are moved.

      #### Popup Functionality

      * The popup's content type is "Kanban stages" with an initially empty value.
      * Clicking "Add New Stage" resets the popup value.
      * Clicking on existing stages fills the popup with the stage information.
      * Create or edit Kanban stages using the right section of the popup.

      #### App Default Stage

      * Set a stage as the app default stage for standardizing user workflows.
      * Use the app default stage to ensure consistency in user stage progression.

      #### Conclusion

      The Popup Edit Stages facilitates managing, editing, and creating Kanban stages. It dynamically populates information based on user interactions and allows for the creation of new stages or editing existing ones. This documentation covers the essential functionality of the popup for efficient stage management.

      ### Part 2: Creating and Editing Projects

      [https://www.loom.com/embed/d8b2a2b03e234732af7bb0194df9c6d6?sid=bbcae2e6-fa49-4ef1-bdc8-6b4d95d30c4c](https://www.loom.com/embed/d8b2a2b03e234732af7bb0194df9c6d6?sid=bbcae2e6-fa49-4ef1-bdc8-6b4d95d30c4c)

      ### Documentation: Exploring Project KanBan Page Capabilities

      This documentation explains the new project capabilities on the project KanBan page. The key components to note are the reusable elements used to create or edit data, which consist of the main feature segment reusable element (in this case, the project KanBan board) and a pop-up reusable element (menu project) for creating or editing projects.

      #### Reusable Elements:

      1. **Project KanBan Board:**
         * Main reusable element where the core functionality resides.
      2. **Menu Project Pop-up:**
         * Used for creating or editing projects.
         * Functionalities include displaying the pop-up, creating/editing projects, showing proper data, saving changes, resetting inputs, hiding pop-ups, and assigning projects to segments.
         * Additional functionalities like deleting projects can be accessed through the group focus project menu.

      #### Usage:

      * The Menu Project pop-up is designed to simplify project management across different parts of the app without the need to rebuild functionality.
      * To use the pop-up in areas not directly linked to repeating groups, a hidden variant can be referenced.
      * Clicking "new project" triggers the hidden variant to display the pop-up for creating or editing projects.

      For further clarification or assistance, feel free to reach out on Discord. Thank you for watching!

      ### Part 3: Main RG KanBan Page

      [https://www.loom.com/embed/390c40917bdc47689f00f4b43d5153d1?sid=4aee310d-2742-4667-be59-5e2fbe062dc2](https://www.loom.com/embed/390c40917bdc47689f00f4b43d5153d1?sid=4aee310d-2742-4667-be59-5e2fbe062dc2)

      ### Documentation: Setting up the Kanban Board in the Editor

      To set up the Kanban board in the editor, follow these steps:

      1. Use the `Draggable Elements` plugin by Bubble instead of the `Drag and Drop Reorder RG`.
      2. Create an `RG Kanban Column` for the horizontal setup, displaying stages like lead, pending, and in-progress.
      3. Place an `RG Kanban Status Columns` element with one row above the `RG Kanban Item` for the vertical elements.
      4. Add a `Drop Area Kanban Stages` group above the `RG Kanban Item` and place the `RG Kanban` inside it.
      5. In the workflows, ensure that the `Drop Area Kanban Stages` has a group `DragDrop` on it and `Current User's Date Signup Complete` is not empty.
      6. In the workflow, when the drop area changes, update the project's stage based on the stage it was dragged to.
      7. Use the edit icons to edit stages on the vertical cards.
      8. Utilize the reusable element for editing specific projects on the vertical cards.

      That's all you need to do to set up the Kanban board in the editor. If you need further assistance, feel free to reach out on Discord. Thank you for watching!
* Marketplace (re: Marketplace Products (Stripe))
  * Preview
  * Editor
* File Library (re: Files Library)
  * Preview
  * Editor
* Messaging (re: conversations)
  *   Preview and Editor

      [https://www.loom.com/embed/52a9dc09f9214fd6a68c091f7dd56d43?sid=ff81ac47-47e4-495b-a228-467df3cc6142](https://www.loom.com/embed/52a9dc09f9214fd6a68c091f7dd56d43?sid=ff81ac47-47e4-495b-a228-467df3cc6142)

      ### Documentation: Chat Functionality Overview

      This documentation provides an overview of the messaging or chat functionality in the template, focusing on the editor side.

      #### Creating Conversations

      * To create new conversations, click on "Create New Conversation" in the top section.
      * A pop-up labeled "Start/Edit Conversation" will appear, allowing you to create a new conversation.
      * Conversations are displayed on the left side, while the actual conversation content appears on the right side.

      #### Data Structures

      * Two key data structures are used for chat functionality: `Conversation` and `Conversation Message`.
      * `Conversation` includes details like conversation name, list of users, and the most recent message.
      * `Conversation Message` contains the message text, connected conversation, and message read status.

      #### Conversation Interaction

      * Users can create conversations and exchange messages within them.
      * Messages are linked to specific conversations and display who has read them.

      #### User Interface Elements

      * A "New" button triggers the creation of a new conversation.
      * A repeating group on the left side displays existing conversations involving the current user.
      * Clicking on a conversation sends its unique ID to the main group for display.

      #### Messaging Functionality

      * Messages within a conversation are shown in a repeating group.
      * Sending a message triggers the creation of a new conversation message, updates the most recent message in the conversation, and schedules a notification.

      #### Future Enhancements

      * Future updates may include features like adding images, emojis, or graphics to conversations.

      This documentation provides an overview of how the chat functionality works in the template. For more detailed information on specific features, stay tuned for upcoming videos. If you found this documentation helpful, please consider liking the video.
* AI Assistants (re: Assistants Listing, re: Assistant Thread Container, menu: manage-assistant)
  *   Preview and Editor

      [https://www.loom.com/embed/eec0c1db20a841b0a37cab961c42e3a8?sid=4563ef13-3175-4950-9213-e71d909723a9](https://www.loom.com/embed/eec0c1db20a841b0a37cab961c42e3a8?sid=4563ef13-3175-4950-9213-e71d909723a9)

      ### SOP: Message File Logic and Workflow

      #### Objective:

      To understand and execute the message file logic and workflow in the backend system for effective file management and processing.

      #### Key Steps:

      1. **Check Template Version:**
         * Verify if the template has the most up-to-date version by checking the presence of the workflow called "File Multi-File Uploader" in the chat thread messages 2.0.
      2. **Understanding the Add Files Button:**
         * Locate the "Add Files" button in the chat input element.
         * Note that the data type associated with this button is "Chat Message File Upload Log" for storing raw files.
      3. **File Upload Logic:**
         * When a file is uploaded, a custom UI file uploader is triggered, showcasing the preview of the files.
         * Upon clicking "Upload Files," the files are saved on the page and an event is triggered after the saving process is completed.
      4. **Backend Workflow Steps:**
         * Step 1: Create a new Chat Message File Upload Log to store raw files and names, and schedule a backend workflow called "Upload File List Step 1."
         * Step 2: Loop over each file uploaded, creating an AI file data type for each file.
         * Step 3: Attach the AI file data to the message log and upload the file to OpenAI for processing.

      #### Cautionary Notes:

      * File names may not display correctly due to a plugin issue, but this should not affect the functionality of the messages.
      * Ensure that all files are processed and loaded before sending a message to avoid errors.

      #### Tips for Efficiency:

      * Regularly update the file management template to ensure compatibility with the latest logic.
      * If encountering any issues or have suggestions for improvement, reach out for assistance or provide feedback for enhancements.
      * Streamline the file upload process by following the defined backend workflow steps systematically.

      By following these steps, you can efficiently manage file uploads and processing within the messaging system.

      #### Link to Loom

      https://www.loom.com/share/eec0c1db20a841b0a37cab961c42e3a8

      ### Understanding Message File Logic in Loom Transcript

      1. **Introduction**
         * Explanation of the message file logic and its backend workings.
         * Clarification on the version of the template being used.
      2. **Add Files Button**
         * Description of the add files button within the chat input element.
         * Explanation of the data type "chat message file upload log" for storing raw files.
      3. **AI File and Chat Message File Upload Log**
         * Introduction to the AI file data type and its components.
         * Details on the chat message file upload log containing a list of AI files.
      4. **File Uploader UI**
         * Description of the custom file uploader UI and its functionality.
         * Process of uploading files and triggering save on the file uploader plugin.
      5. **Backend Workflow**
         * Overview of the backend workflow involving three steps: step 1, step 2, and step 3.
         * Explanation of passing raw files, team information, and message file upload log in the workflow.
      6. **Step 1 and Step 2**
         * Details on how step 1 schedules step 2 for each file.
         * Looping through the files and creating AI files in step 2.
      7. **Step 3**
         * Purpose of step 3 in attaching AI file data to the message log.
         * Uploading files to OpenAI, storing OpenAI ID, and setting loadIn to null.
      8. **Message Sending Workflow**
         * Brief overview of the message sending workflow.
         * Inclusion of the file log in the message and formatting for OpenAI API call.
      9. **Conclusion**
         * Encouragement for feedback and suggestions on simplifying the process.
         * Offer to assist and provide further clarification if needed.

      #### Link to Loom

      https://www.loom.com/share/eec0c1db20a841b0a37cab961c42e3a8

      ### Documentation: Message File Logic Explanation

      This documentation provides an overview of the message file logic used in the backend of the application. It explains the process of handling file uploads, creating AI files, and sending messages with attachments.

      #### Frontend Logic

      * An "Add Files" button is available in the chat input element.
      * Clicking the button triggers a custom file uploader UI that allows users to upload multiple files.
      * The uploaded files are displayed as previews, and upon clicking "Upload Files," the files are saved using a file uploader plugin.
      * A backend workflow is then scheduled to process the uploaded files.

      #### Backend Workflow Steps

      1. **Step 1:** Creates a new chat message file upload log to store raw files and their names. It then schedules Step 2 for each file.
      2. **Step 2:** For each file, creates an AI file data type with details like OpenAI ID and file ownership.
      3. **Step 3:** Attaches the AI file to the message log and uploads the file to OpenAI, storing relevant data like file size and OpenAI ID.

      #### Message Sending Workflow

      * When sending a message, the file upload log containing raw files and AI files is attached to the message.
      * The message is processed, and if attachments are present, the files are formatted in a JSON object for OpenAI.

      #### Conclusion

      * The process involves creating a data structure to handle uploaded files, converting them to AI files, and sending messages with attachments.
      * Feedback and suggestions for simplifying this process are welcome to improve the system's efficiency and user experience.

      #### Link to Loom

      https://www.loom.com/share/eec0c1db20a841b0a37cab961c42e3a8
* Image Generation (Popup: Generate Magic Image)
  *   Preview and Editor

      [https://www.loom.com/embed/63228d750c5a40818a0cb78a612875ff?sid=44eebdd9-b12c-423d-a2d6-86f4ed8a14c7](https://www.loom.com/embed/63228d750c5a40818a0cb78a612875ff?sid=44eebdd9-b12c-423d-a2d6-86f4ed8a14c7)

      ### Martech Foundation Image Generation Functionality Documentation

      This documentation provides an overview of the image generation functionality within the Martech Foundation template.

      #### Overview

      The image generation functionality allows users to create customized images by inputting text and selecting various parameters like font and size.

      #### Front End Functionality

      * Users can input text and select font and size preferences.
      * Clicking on the "Generate" button initiates the image generation process.
      * The generated image can be saved and downloaded.

      #### Backend Setup

      * The functionality involves making an OpenAI call with specific parameters.
      * Universal headers are used for each OpenAI call.
      * The OpenAI call includes a JSON body with details like the model being used.
      * Initialization of the call is required for the image generation process.

      #### Reusable Element Popup

      * The "Generate Magic Image" popup is a reusable element for image generation.
      * Clicking "Save" likely saves the image to the file library.
      * The "Generate" button triggers the image generation process.
      * A loader is displayed during the generation process.
      * The output of the OpenAI call is displayed in the image with the added text.

      #### Workflow

      * The loader disappears once the image is generated.
      * Users can save the image, creating a new AI file bookmark.

      #### Additional Features

      * The "Reset" button allows users to start the workflow again.
      * The "Download" button enables users to download the generated image.

      #### Conclusion

      The Martech Foundation image generation functionality provides a user-friendly way to create customized images. For more in-depth backend workflow details, refer to future videos. Thank you for watching!
* Notifications (🎨 Notifications)
  * Preview
  * Editor
* Marketing Pages
  * Landing page 1 (re - landing page 1)
    * Preview
    * Editor
  * Preview
  * Editor
* Header (🧰 Header, 🧰 Header GF - User Profile & Menu)
  * Preview
  * Editor
* Affiliate (re: Affiliate Dashboard, fg:affiliate-dashboard)
  * Preview
  * Editor

## Extra Reusables ([Coming Soon](https://discord.com/invite/fnMfNZY3tR))

***

***

***

***

***
