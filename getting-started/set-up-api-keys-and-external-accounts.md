# Set Up API Keys & External Accounts

Some functionality requires external APIs to work. You'll need to add your own API keys to use them.

**Postmark - transactional emails**

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

**OpenAI - AI Assistants, Prompts & Image Generation**

To enable the built-in chat bot, you'll need to get an API key from [OpenAI](https://platform.openai.com/).

Add your API Key in the API Connector plugin to the OpenAI API[https://docs.foundationtemplate.com/\~gitbook/image?url=https%3A%2F%2F2579826874-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FV1MErI30ZCe37SndGqT1%252Fuploads%252FMUYhtwAehkXldYBTBWgU%252Fimage.png%3Falt%3Dmedia%26token%3Dabcbf528-2216-4b9e-afb7-ad9042defcfe\&width=300\&dpr=4\&quality=100\&sign=c716aedf\&sv=1](https://docs.foundationtemplate.com/\~gitbook/image?url=https%3A%2F%2F2579826874-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FV1MErI30ZCe37SndGqT1%252Fuploads%252FMUYhtwAehkXldYBTBWgU%252Fimage.png%3Falt%3Dmedia%26token%3Dabcbf528-2216-4b9e-afb7-ad9042defcfe\&width=300\&dpr=4\&quality=100\&sign=c716aedf\&sv=1)

**Stripe - subscriptions and payment**

Stripe is used to capture and manage User subscriptions to your app. The template makes this process super easy to manage and update as needed.

To get started, you'll need a Stripe account and the API keys.

1. Add the keys in two places:
   1. API Connector > Stripe API
   2. Stripe plugin.
2. In the "Get Stripe Prices" API, add 'data.product' to the expand\[] parameter. Example below.
3. Make sure the Stripe Plugin has Checkout v3 selected.

_Make sure to use your development keys while building so you can make test payments._

***

**API Connector Plugin > Stripe:**[https://docs.foundationtemplate.com/\~gitbook/image?url=https%3A%2F%2F2579826874-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FV1MErI30ZCe37SndGqT1%252Fuploads%252FjnkFNhP34VXYLhmD7rNr%252Fimage.png%3Falt%3Dmedia%26token%3Dfa32ab1a-e1de-4b2b-8823-5b5e843e2e2f\&width=300\&dpr=4\&quality=100\&sign=34ce3f25\&sv=1](https://docs.foundationtemplate.com/\~gitbook/image?url=https%3A%2F%2F2579826874-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FV1MErI30ZCe37SndGqT1%252Fuploads%252FjnkFNhP34VXYLhmD7rNr%252Fimage.png%3Falt%3Dmedia%26token%3Dfa32ab1a-e1de-4b2b-8823-5b5e843e2e2f\&width=300\&dpr=4\&quality=100\&sign=34ce3f25\&sv=1)



**Update Expand Parameter:**[https://docs.foundationtemplate.com/\~gitbook/image?url=https%3A%2F%2F2579826874-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FV1MErI30ZCe37SndGqT1%252Fuploads%252FvGKEK1aQ7HFDGuLjadwQ%252Fimage.png%3Falt%3Dmedia%26token%3Dc97aeade-214c-4668-9598-b125bf4fc664\&width=300\&dpr=4\&quality=100\&sign=abfa81d5\&sv=1](https://docs.foundationtemplate.com/\~gitbook/image?url=https%3A%2F%2F2579826874-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FV1MErI30ZCe37SndGqT1%252Fuploads%252FvGKEK1aQ7HFDGuLjadwQ%252Fimage.png%3Falt%3Dmedia%26token%3Dc97aeade-214c-4668-9598-b125bf4fc664\&width=300\&dpr=4\&quality=100\&sign=abfa81d5\&sv=1)



**Stripe Plugin:**[https://docs.foundationtemplate.com/\~gitbook/image?url=https%3A%2F%2F2579826874-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FV1MErI30ZCe37SndGqT1%252Fuploads%252FkzfMDdC747djiZVy5JRi%252Fimage.png%3Falt%3Dmedia%26token%3D522aa107-bd0a-486e-bbe9-4c4dbd0d15da\&width=300\&dpr=4\&quality=100\&sign=a3ce5bd1\&sv=1](https://docs.foundationtemplate.com/\~gitbook/image?url=https%3A%2F%2F2579826874-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FV1MErI30ZCe37SndGqT1%252Fuploads%252FkzfMDdC747djiZVy5JRi%252Fimage.png%3Falt%3Dmedia%26token%3D522aa107-bd0a-486e-bbe9-4c4dbd0d15da\&width=300\&dpr=4\&quality=100\&sign=a3ce5bd1\&sv=1)



**Google - Single Sign On**

You'll need to get an App Secret and an API Key from [Google Cloud Console](https://console.cloud.google.com/apis/credentials/consent) to enable Google Sign On.[https://docs.foundationtemplate.com/\~gitbook/image?url=https%3A%2F%2F2579826874-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FV1MErI30ZCe37SndGqT1%252Fuploads%252FnaUj0Lwpc1I66O0KiOiq%252Fimage.png%3Falt%3Dmedia%26token%3Dafa80075-4034-4740-a1b7-8d9c73602f09\&width=300\&dpr=4\&quality=100\&sign=c2faf5e5\&sv=1](https://docs.foundationtemplate.com/\~gitbook/image?url=https%3A%2F%2F2579826874-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FV1MErI30ZCe37SndGqT1%252Fuploads%252FnaUj0Lwpc1I66O0KiOiq%252Fimage.png%3Falt%3Dmedia%26token%3Dafa80075-4034-4740-a1b7-8d9c73602f09\&width=300\&dpr=4\&quality=100\&sign=c2faf5e5\&sv=1)

Here's a great video for more help:

[https://www.youtube.com/watch?v=XuUkshWifok](https://www.youtube.com/watch?v=XuUkshWifok)
