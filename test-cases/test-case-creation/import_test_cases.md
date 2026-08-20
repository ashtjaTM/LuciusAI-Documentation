# Import Test Cases

**Import Test Cases** allows you to bring existing test cases into LuciusAI using a CSV file. You can download the provided template, upload a CSV file, review the imported test cases, select the test cases to add, and confirm the import.

The import workflow consists of the following steps:

1. **Open Import:** From the **Test Cases** workspace, select **Import** to open the import screen.
2. **Download Template:** Select **Download template** to download the CSV template and use the supported format for importing test cases.
3. **Upload CSV:** Upload the CSV file using **Drag & Drop** or **Choose file to upload**. LuciusAI displays the selected file before proceeding with the import.
4. **Import Name:** After the CSV is uploaded, the **Import Name** is automatically populated using the uploaded file name. You can modify the name if required, and LuciusAI validates whether the name is available.
5. **Import:** Select **Import** to upload and process the CSV file. After a successful upload, LuciusAI displays a confirmation showing the number of test cases imported.
6. **Review Imported Test Cases:** After the CSV is processed, LuciusAI displays the imported test cases in a selection window. The test cases are presented as a list with multi-select options, allowing you to select or deselect the test cases that you want to add to the project. Each test case can be expanded to review its **Folder Path** and **Instructions** before confirming the import. The review window offers the following capabilities:

   - **Select/Deselect:** Select individual test cases to include them in the import or deselect them to exclude them.
   - **Select All:** Select all displayed test cases at once.
   - **Folder Path:** View the folder path associated with the imported test case.
   - **Instructions:** Review the instructions and steps associated with the test case.

7. **Confirm Import:** After selecting the required test cases, select **Confirm Import** to add them to the **Test Cases** workspace. You can also use **Clear Selection** to remove the current selection.
8. **Cancel:** Exit the selection screen without confirming the import.
9. **Imported Test Cases:** The uploaded test cases are available under the **Imported Test cases** tab. Select the imported test cases that you want to add to the **Test Cases** workspace.

**Note:** The test cases are added to the **Imported Test cases** tab only after **Confirm Import** is selected. Before confirmation, they remain available only in the import selection window for review and selection.

---

# Parse Test Cases

Once test cases have been imported, they are displayed in the **Imported Test Cases** section along with their current processing status.

## Overview Section

All the test cases associated to a single import are displayed under the **Overview Section.** A test case initially appears with the **Queued** status when it is waiting to be parsed. **Queued does not mean that parsing is currently in progress.** It indicates that parsing has **not yet started** for that particular test case. Users can then initiate parsing either for individual test cases or for multiple test cases together.

### Parse Individual Test Cases

To parse a specific imported test case:

1. Locate the desired test case from the list of available **Imported Test Cases**.
2. Click the **Parse** option associated with the test case.
3. The system starts processing the selected test case.
4. The test case status is updated as the parsing progresses.

This allows users to control which test cases are parsed without processing the entire list.

### Parse All Test Cases

Users can also parse all the imported test cases at once using the **Parse** option available at the top of the section. This allows all the imported test cases to be initiated for parsing together instead of starting the process individually for each test case.

## Progress Section

The **Progress Section** displays the live progress status for **Parsing** and **Generation**.

### Parsing Progress

The **Parsing Progress** tracks the parsing status of the imported test cases. The status shown against each test case indicates where that test case currently stands in the parsing workflow. 

For example: **Queued → Parsing → Parsed**

If the parsing process encounters an issue, the corresponding status should indicate that the test case could not be processed successfully, where applicable.

### Generation Progress

The progress section does not represent only the status of the original import operation. It provides visibility into the **generation lifecycle of the imported test cases**. The status of each test case is updated as it moves through these stages.

A typical workflow is: **Queue → Parsing → Parsing Success → Generating → Generation Success/Failed**

This makes it possible for users to identify which test cases are waiting to be processed, which are currently being processed, and which have completed a particular stage.
