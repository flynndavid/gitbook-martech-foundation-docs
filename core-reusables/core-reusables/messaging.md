# Messaging

{% embed url="https://www.loom.com/embed/52a9dc09f9214fd6a68c091f7dd56d43?sid=ff81ac47-47e4-495b-a228-467df3cc6142" %}

## Chat Functionality Overview <a href="#documentation-chat-functionality-overview" id="documentation-chat-functionality-overview"></a>

This documentation provides an overview of the messaging or chat functionality in the template, focusing on the editor side.

**Creating Conversations**

* To create new conversations, click on "Create New Conversation" in the top section.
* A pop-up labeled "Start/Edit Conversation" will appear, allowing you to create a new conversation.
* Conversations are displayed on the left side, while the actual conversation content appears on the right side.

**Data Structures**

* Two key data structures are used for chat functionality: `Conversation` and `Conversation Message`.
* `Conversation` includes details like conversation name, list of users, and the most recent message.
* `Conversation Message` contains the message text, connected conversation, and message read status.

**Conversation Interaction**

* Users can create conversations and exchange messages within them.
* Messages are linked to specific conversations and display who has read them.

**User Interface Elements**

* A "New" button triggers the creation of a new conversation.
* A repeating group on the left side displays existing conversations involving the current user.
* Clicking on a conversation sends its unique ID to the main group for display.

**Messaging Functionality**

* Messages within a conversation are shown in a repeating group.
* Sending a message triggers the creation of a new conversation message, updates the most recent message in the conversation, and schedules a notification.

**Future Enhancements**

* Future updates may include features like adding images, emojis, or graphics to conversations.

This documentation provides an overview of how the chat functionality works in the template. For more detailed information on specific features, stay tuned for upcoming videos. If you found this documentation helpful, please consider liking the video.
