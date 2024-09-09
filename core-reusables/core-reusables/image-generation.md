# Image Generation

{% embed url="https://www.loom.com/embed/63228d750c5a40818a0cb78a612875ff?sid=44eebdd9-b12c-423d-a2d6-86f4ed8a14c7" %}

### Image Generation Functionality <a href="#martech-foundation-image-generation-functionality-documentation" id="martech-foundation-image-generation-functionality-documentation"></a>

This documentation provides an overview of the image generation functionality within the Martech Foundation template.

**Overview**

The image generation functionality allows users to create customized images by inputting text and selecting various parameters like font and size.

**Front End Functionality**

* Users can input text and select font and size preferences.
* Clicking on the "Generate" button initiates the image generation process.
* The generated image can be saved and downloaded.

**Backend Setup**

* The functionality involves making an OpenAI call with specific parameters.
* Universal headers are used for each OpenAI call.
* The OpenAI call includes a JSON body with details like the model being used.
* Initialization of the call is required for the image generation process.

**Reusable Element Popup**

* The "Generate Magic Image" popup is a reusable element for image generation.
* Clicking "Save" likely saves the image to the file library.
* The "Generate" button triggers the image generation process.
* A loader is displayed during the generation process.
* The output of the OpenAI call is displayed in the image with the added text.

**Workflow**

* The loader disappears once the image is generated.
* Users can save the image, creating a new AI file bookmark.

**Additional Features**

* The "Reset" button allows users to start the workflow again.
* The "Download" button enables users to download the generated image.

**Conclusion**

The Martech Foundation image generation functionality provides a user-friendly way to create customized images. For more in-depth backend workflow details, refer to future videos. Thank you for watching!
