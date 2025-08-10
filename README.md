# Patient Management System

A fully functional Patient Management System written in Java with its corresponding GUI.

## How To Use

* The Patient Management System requires the practitioner to log in using a username/password pair. The default values are:
  * **username:** admin
  * **password:** 1234
* A new patient can be registered with basic personal details:
* Upon selecting the patient from a list more fields become visible allowing the user to edit comments, appointments, and add or remove pictures.
* The field containing the medical condition data is clickable and points to the website indicated by the practitioner at patient creation.
* All fields of a patient record can be edited. How to edit a field depends on the field selected:
  * If the user wishes to edit personal details then it is necessary press the edit button.
  * Comments and appointments can be edited on the fly on their respective tab.
  * Photos can be added or deleted on their respective tabs.
* A patient record can be deleted after the practitioner confirms its deletion.
* The list of patients can be search based on a series of fields. (Only sensible fields are included in the search table).
* A list of selected patients can be exported as a JSON object.
* A list of patient records can be imported as a JSON object and appended to the existing ones in the management system.

## Setup

* **Option 1:** Use the patient-management-system.jar binary included in release v1.0. This requires no setup at all.
* **Option 2:** Build the application from the source files:
  * `/src` contains the .java application source files.
  * `/res` contains the images used by .java source files.
  * `/lib` contains the JSON third party library used to save and read JSON text files.

## Notes
* The official JSON third party java library is used to save and read JSON text files. This library can be found [**_here_**](http://www.json.org/java/) and is open source. You will need to add the library to your build path to be able to launch the project.
* An extensive Javadoc can be found in the `/doc` subfolder.
* A logger is initialised in the directory where the jar is launched. This can be useful for debugging.

## Further Work

- **User Account Management:**  
  Currently, the system uses default login credentials. A key enhancement would be to implement a secure user account creation feature that prompts the practitioner to set a custom username and password during the first launch. This will improve security and allow multiple user profiles in the future.

- **Dynamic Image Resizing:**  
  Patient images currently have fixed sizes which may lead to inefficient use of storage and inconsistent display across different screen sizes. Implementing dynamic image resizing will optimize memory usage by storing and displaying images in appropriate resolutions depending on the context (e.g., thumbnails vs full-size), improving performance and user experience.

- **Optimized Image Storage Solutions:**  
  At present, images might be stored as files or embedded directly which can be inefficient and impact scalability. Exploring better storage methods—such as storing images as binary large objects (BLOBs) within a database or using external cloud-based storage services (e.g., AWS S3, Google Cloud Storage)—can enhance retrieval speed, simplify backup processes, and support larger volumes of patient data efficiently.

- **Enhanced Security Measures:**  
  Adding encryption for sensitive patient data and implementing role-based access control can protect privacy and ensure only authorized users can access or modify records.

- **Improved User Interface and Experience:**  
  Refining the GUI to support responsive layouts, intuitive navigation, and accessibility standards will make the system easier and more pleasant to use across devices.
- **Robust Logging and Error Handling:**  
  Expanding the logging framework to capture more granular information about system operations and exceptions will facilitate faster debugging and maintenance.