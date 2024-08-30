# Getting Started

Here are some tips for getting your app setup with Foundation.

[https://www.loom.com/share/e34581aa1a9941bfa59b340e66a941b8?sid=d6e87a84-7134-4fff-96d1-8c879e4b8b42](https://www.loom.com/share/e34581aa1a9941bfa59b340e66a941b8?sid=d6e87a84-7134-4fff-96d1-8c879e4b8b42)

## Install the template and create your app

* From within your Bubble account, go to the [Core Foundation marketplace](https://bubble.io/template/foundation-by-automatic-1673596403969x408542417388568600) and install the template.
* Once installed, click "Create an app" and select the Martech Core Foundations template. Then name your app and click Get Started.

## Bubble Setup & Plan

* Select your app's default font. The majority of text in the app uses this font.
* Update your primary color. Many buttons and highlighted areas of the app use the Primary color defined here. Update the other colors as needed during development.
* This section is under the styles tab under style variables as shown below
* All plugins required for the template are already installed.
* You'll then want to place your app on a basic plan

## Open Admin Portal to Finish Setup

* Go to the data tab in your app, then the app data section, then search for the users table.
* From here select the admin@template.com email and click "run as" to access the admin page.
* We recommend disabling debug mode so elements display correctly. Just remove this section from the url and any "&" before it.
* The admin portal is where you can customize app-wide settings, add new sections to the dashboard, or incorporate additional features.
* To create a new admin account, you will need to go through the existing Sign Up flow and add the App Admin role (Option set) to your new user from the Bubble database. You can also manage User's roles from the Users tab in the admin portal.

## Set Up API Keys & External Accounts

* Some functionality requires external APIs to work. You'll need to add your own API keys to use them.

### Postmark - transactional emails

**Postmark Setup:**

* Setup an account on [Postmark](https://postmark.com/) and verify your Sender Account. Replace the values in the plugin below with your Postmark API keys.
* The admin portal has an Email section where Email Templates can be customized and managed. This all lives in the reusable "🛠️ Admin - Email Templates"
* Before emails will send, make sure to update the "Sender Email" with a validated email from your Postmark Account.
* The Primary Color is used to update the color of the buttons and top border of the HTML template
* The HTML template is hard-coded in this element. To customize the HTML directly, you can find it in the "var - Template HTML Content" element
* In the admin portal, you can create a new email template or edit existing ones. When creating a new one, you have the option of writing a brief description and allowing AI to generate the copy for you — or starting from scratch.
* Dynamic tags can be used to pass in dynamic data via the backend workflow that sends the email. Tags can be any value wrapped in {{curly-brackets}}, but will need to be defined in the 'send-email-from-template' backend workflow.
* For quick use, dynamic tags can be added to the Option Set "OS_Dynamic_Email_Tags" and will be displayed in this menu for easy copy & paste.
* Backend workflow "" should be used to send all emails. The API workflow has multiple parameters, many optional, that are used to define the dynamic tags.
  * This workflow also can also be triggered by the 'create-notification' workflow that additionally creates an in-app notification that is displayed in a User's notifications list. This workflow uses the 'standard-notification' email template.

### OpenAI - AI Assistants, Prompts & Image Generation

To enable the built-in chat bot, you'll need to get an API key from [OpenAI](https://platform.openai.com/).

Add your API Key in the API Connector plugin to the OpenAI API

[OpenAI API Key Setup Image]

### Stripe - subscriptions and payment

Stripe is used to capture and manage User subscriptions to your app. The template makes this process super easy to manage and update as needed.

To get started, you'll need a Stripe account and the API keys.

1. Add the keys in two places:
   1. API Connector > Stripe API
   2. Stripe plugin.
2. In the "Get Stripe Prices" API, add 'data.product' to the expand[] parameter. Example below.
3. Make sure the Stripe Plugin has Checkout v3 selected.

_Make sure to use your development keys while building so you can make test payments._

---

**API Connector Plugin > Stripe:**

[Stripe API Connector Image]

**Update Expand Parameter:**

[Expand Parameter Image]

**Stripe Plugin:**

[Stripe Plugin Image]

### Google - Single Sign On

You'll need to get an App Secret and an API Key from [Google Cloud Console](https://console.cloud.google.com/apis/credentials/consent) to enable Google Sign On.

[Google SSO Setup Image]

Here's a great video for more help:

[https://www.youtube.com/watch?v=XuUkshWifok](https://www.youtube.com/watch?v=XuUkshWifok)

## Stripe Setup

1. **Connect API Keys**
   * Integrate your API keys with the application.
2. **Delete Template Users**
   * Remove all users that were included with the template. They may contain Stripe data that is referencing the template's stripe account.
3. **Create a New Admin Account**
   * Sign up as new user via the app's standard signup flow
   * Go into bubble database and add "App Admin" to the new User's Role(s)
4. **Delete Existing Stripe Plans and Marketplace Items**
   * Remove any Stripe plans or marketplace items that came with the template. These are connected to the template's stripe account and will not work with your new stripe account.
   * Datatypes to delete: "Stripe Plan" & "Marketplace Product"
5. Setup Stripe Webhooks:
   * The template has 2 Stripe webhook backend workflows that are already setup. You just need to setup your Stripe webhooks to trigger them.
   * …/api/1.1/wf/stripe-checkout-session-completed
   * …/api/1.1/wf/stripe-webhook-update-subscription
6. **Create New Stripe Plans and Marketplace Items**
   * Use the admin portal to create new Stripe plans and marketplace items as needed.
   * Stripe subscription plans will need to be created in Stripe first, then linked to the app via admin portal.
   * Marketplace products can be created directly in the admin portal and will be created / updated directly in Stripe via API

* _**Error Handling:** there is a workflow in the Header element that runs for any error the app encounters. The workflow creates a database item "Error Logs" so you can see details. It also shows an AirAlert letting the user know an error occurred._