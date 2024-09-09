# Onboarding

The Martech Foundation's onboarding page is a reusable multi-step form element that can be utilized in various parts of an application. It consists of a next button, a back button, and a complete button. The next button progresses to the next step in the form, while the back button allows users to navigate to the previous step.

{% embed url="https://www.loom.com/embed/8278187015d64f0d899ea2146e723e62?sid=e06db1d1-0e85-4102-8faa-f47a87610c38" %}

**Functionality Overview**

* The `var number of steps` field sets the total number of steps in the form.
* The `current step` variable keeps track of the current step, defaulting to 1.
* Clicking the next button triggers a custom event called `navigate step`, incrementing the current step by 1.
* Updating the `current step` variable moves the user to the next step in the form.
* The back button works similarly by decrementing the current step.

**Custom Events**

* The `navigate step` custom event facilitates the navigation between form steps.
* It compares the current step with the total number of steps to progress through the form.

**Onboarding Percentage Tracking**

* The Onboarding percentage tracking feature calculates the completion progress of the form.
* It is useful for redirecting users back to the Onboarding process if incomplete.
