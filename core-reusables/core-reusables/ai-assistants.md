# AI Assistants

{% embed url="https://www.loom.com/embed/eec0c1db20a841b0a37cab961c42e3a8?sid=4563ef13-3175-4950-9213-e71d909723a9" %}

### Message File Logic and Workflow <a href="#sop-message-file-logic-and-workflow" id="sop-message-file-logic-and-workflow"></a>

**Objective:**

To understand and execute the message file logic and workflow in the backend system for effective file management and processing.

**Key Steps:**

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

**Cautionary Notes:**

* File names may not display correctly due to a plugin issue, but this should not affect the functionality of the messages.
* Ensure that all files are processed and loaded before sending a message to avoid errors.

**Tips for Efficiency:**

* Regularly update the file management template to ensure compatibility with the latest logic.
* If encountering any issues or have suggestions for improvement, reach out for assistance or provide feedback for enhancements.
* Streamline the file upload process by following the defined backend workflow steps systematically.

By following these steps, you can efficiently manage file uploads and processing within the messaging system.

### Understanding Message File Logic in Loom Transcript <a href="#understanding-message-file-logic-in-loom-transcript" id="understanding-message-file-logic-in-loom-transcript"></a>

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

### Message File Logic Explanation <a href="#documentation-message-file-logic-explanation" id="documentation-message-file-logic-explanation"></a>

This documentation provides an overview of the message file logic used in the backend of the application. It explains the process of handling file uploads, creating AI files, and sending messages with attachments.

**Frontend Logic**

* An "Add Files" button is available in the chat input element.
* Clicking the button triggers a custom file uploader UI that allows users to upload multiple files.
* The uploaded files are displayed as previews, and upon clicking "Upload Files," the files are saved using a file uploader plugin.
* A backend workflow is then scheduled to process the uploaded files.

**Backend Workflow Steps**

1. **Step 1:** Creates a new chat message file upload log to store raw files and their names. It then schedules Step 2 for each file.
2. **Step 2:** For each file, creates an AI file data type with details like OpenAI ID and file ownership.
3. **Step 3:** Attaches the AI file to the message log and uploads the file to OpenAI, storing relevant data like file size and OpenAI ID.

**Message Sending Workflow**

* When sending a message, the file upload log containing raw files and AI files is attached to the message.
* The message is processed, and if attachments are present, the files are formatted in a JSON object for OpenAI.

**Conclusion**

* The process involves creating a data structure to handle uploaded files, converting them to AI files, and sending messages with attachments.
* Feedback and suggestions for simplifying this process are welcome to improve the system's efficiency and user experience.
