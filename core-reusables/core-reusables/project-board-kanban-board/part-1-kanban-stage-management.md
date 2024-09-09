# Part 1: Kanban Stage Management

{% embed url="https://www.loom.com/embed/8b2e4799c006470fa22b8dc2d2d142e7?sid=7efe2014-46ed-4538-83a0-2b9da10e58f9" %}

## Managing Kanban Stages Popup <a href="#documentation-managing-kanban-stages-popup" id="documentation-managing-kanban-stages-popup"></a>

This documentation explains how the editor side of the Manage Kanban Stages popup works in the Reusable Element project Kanban Reusable, specifically focusing on the Popup Edit Stages element.

**Popup Anatomy**

The Popup Edit Stages consists of two sections: a left section and a right section.

* **Left Section:** Manage, edit, and rearrange different stages, as well as add new stages.
* **Right Section:** Add or edit values for stages.

**Setting Up**

* Ensure you have a paid version of the plugin for full functionality.
* Check the plugin documentation for available elements, events, and actions.

**Working with Draggable Elements**

* Locate and set up the draggable rg section element to enable drag-and-drop functionality within the repeating group.
* Add an id attribute to the HTML elements for identification.
* Connect the id attribute to the repeating group id in the draggable rg element to access plugin workflows.

**Events and Actions**

* Utilize events like draggable rg section item moved to track item movements.
* Update sort order field on the kanban stages data type and refresh the repeating group element when items are moved.

**Popup Functionality**

* The popup's content type is "Kanban stages" with an initially empty value.
* Clicking "Add New Stage" resets the popup value.
* Clicking on existing stages fills the popup with the stage information.
* Create or edit Kanban stages using the right section of the popup.

**App Default Stage**

* Set a stage as the app default stage for standardizing user workflows.
* Use the app default stage to ensure consistency in user stage progression.

**Conclusion**

The Popup Edit Stages facilitates managing, editing, and creating Kanban stages. It dynamically populates information based on user interactions and allows for the creation of new stages or editing existing ones. This documentation covers the essential functionality of the popup for efficient stage management.
