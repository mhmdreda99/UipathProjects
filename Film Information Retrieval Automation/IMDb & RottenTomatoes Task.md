---
excalidraw-plugin: parsed
tags:
  - RPA
---
## Project Description: Film Information Retrieval Automation

## Overview:

The Film Information Retrieval Automation project aims to streamline the process of gathering film information from Rotten Tomatoes and IMDb websites. The automation workflow will open the specified movie-related pages, search for a film, extract relevant information, and provide the user with the option to continue searching or close the websites.
### Main Workflow (Main.xaml):

**Desc:** The Main Workflow orchestrates the entire film information retrieval process, including opening Rotten Tomatoes and IMDb, searching for a film, collecting user input, saving and printing information, and finally, closing the browsers.

**Prerequisite:**

- None

**Post-requisite:**

- Film information retrieved from both Rotten Tomatoes and IMDb.
- User interaction completed.
- Browsers closed.

**Activities:**

1. Invoke `Open Rotten Workflow (OpenRotten.xaml)`.
2. Invoke `Open IMDb Workflow (OpenIMDb.xaml)`.
3. Invoke `Search Film Workflow (SearchFilm.xaml)`.
4. Invoke `User Input Film Workflow (UserInputFilm.xaml)`.
5. Invoke `Save Information Workflow (SaveInformation.xaml)`.
6. Invoke `Print Information Workflow (PrintInformation.xaml)`.
7. Invoke `Close Browser Workflow (CloseBrowser.xaml)`.

### Open Rotten Workflow (OpenRotten.xaml):

**Desc:** The Open Rotten Workflow opens the Rotten Tomatoes website.

**Prerequisite:**

- Rotten Tomatoes website accessible.

**Post-requisite:**

- Rotten Tomatoes website opened.

**Activities:**

- Use `Open Browser` activity to open the Rotten Tomatoes website.

### Open IMDb Workflow (OpenIMDb.xaml):

**Desc:** The Open IMDb Workflow opens the IMDb website.

**Prerequisite:**

- IMDb website accessible.

**Post-requisite:**

- IMDb website opened.

**Activities:**

- Use `Open Browser` activity to open the IMDb website.

### Search Film Workflow (SearchFilm.xaml):

**Desc:** The Search Film Workflow performs a search for a film on both Rotten Tomatoes and IMDb.

**Prerequisite:**

- Rotten Tomatoes and IMDb websites opened.

**Post-requisite:**

- Film searched successfully on both websites.

**Activities:**

- Use `Type Into` and `Click` activities to search for the film on Rotten Tomatoes and IMDb.

### User Input Film Workflow (UserInputFilm.xaml):

**Desc:** The User Input Film Workflow prompts the user to input a film name.

**Prerequisite:**

- None

**Post-requisite:**

- User input captured.

**Activities:**

- Use `Input Dialog` activity to get the film name from the user.

### Save Information Workflow (SaveInformation.xaml):

**Desc:** The Save Information Workflow saves film information to variables and invokes the Save Information to Array Workflow.

**Prerequisite:**

- Film information available.

**Post-requisite:**

- Film information saved to variables and array.

**Activities:**

- Use `Assign` activities to set film information variables.
- Invoke `Save Information to Array Workflow (SaveInformationToArray.xaml)`.

### Save Information to Array Workflow (SaveInformationToArray.xaml):

**Desc:** The Save Information to Array Workflow saves film information to an array or DataTable.

**Prerequisite:**

- Film information available.

**Post-requisite:**

- Film information saved to array.

**Activities:**

- Use `Add to Collection` or similar activities to save film information to an array or DataTable.

### Print Information Workflow (PrintInformation.xaml):

**Desc:** The Print Information Workflow displays film information in a message box.

**Prerequisite:**

- Film information available in an array or DataTable.

**Post-requisite:**

- Film information displayed in a message box.

**Activities:**

- Use `Message Box` activity to display film information.

### Close Browser Workflow (CloseBrowser.xaml):

**Desc:** The Close Browser Workflow closes the opened browser instances.

**Prerequisite:**

- Browsers opened during the workflow.

**Post-requisite:**

- Browsers closed.

**Activities:**

- Use `Close Tab` or similar activities to close browser instances.