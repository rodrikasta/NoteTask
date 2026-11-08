 
# Notetask 
Pre Alpha: Console tool for organizing tasks using the Kanban method  

Disclaimer: This project is under active development and will evolve into a full-stack web application.

## v0.0.1 (pre-aplha)
Currently, the project runs exclusively in the terminal and allows you to:
* **New task:** Create a new task and save it to a .json file.
* **Edit task:** Open, read, and edit a task (JSON file), and apply the changes.
* **Change state:** Easily select and change the status of a task using color-coded visual indicators.
* **Delete task:** deletes a task (JSON file).


    
### Task Structure (JSON)
The tasks managed by the system follow this internal structure:
* **Id** (Unique identifier)
* **Title**
* **Description** (Optional)
* **State:** `To do`, `Doing`, `Done`
* **Priority Level:** `High`, `Mid`, `Low`
* **Dates:**
  * Creation
  * Start doing
  * Finished
## Technical Design & Architecture  

* **Tasks as classes/objects:** Tasks are represented as objects instantiated from a `Task` class. This allows us to encapsulate validation logic (for example, ensuring that the completion date is not earlier than the creation date) and state management methods directly within the object.

* **Storage Format:** Tasks are serialized and persisted individually as unique 

### Activity History & Event Logging
* **Task Lifecycle Tracking:** Instead of just saving the current state, each task's JSON file maintains a `history` array. Every status shift, modification, or checklist completion appends a new event object with a standardized timestamp.
* **Granular Process Tracking:** If a task includes a checklist, checking off an item generates a specific log entry. This provides a transparent timeline of how and when progress was made.

## Authors

- [@rodriKasta](https://www.github.com/rodriKasta)


