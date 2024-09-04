# Stripe Setup

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
