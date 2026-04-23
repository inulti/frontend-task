# Frontend Engineering Task

Build a Kanban board application using Vue 3, TypeScript, and Pinia.

## Data source

Use the provided data.json file as the initial data source.

## Board columns

Create the board columns from the columns array in data.json.

Columns must be rendered according to their order property.

Tasks must be displayed in the correct column based on their current status.

## Requirements

### 1. Create task

Provide a simple form for creating a new task.

A new task must include:

- title
- author

All newly created tasks must be added to the column that has the property `default: true`.

A newly created task must appear in the UI immediately.

### 2. Filtering

Allow filtering tasks by:

- author
- title

All active filters must be synchronized with the URL query parameters.

When the page is refreshed or reopened, the filter state must be restored from the URL.

The UI must always reflect the current URL state.

### 3. Persistence

Persist board data in IndexedDB.

On page refresh, previously created or updated tasks must be restored from IndexedDB.

If IndexedDB does not contain board data yet, initialize the application using the provided JSON dataset.

### 4. Drag and drop

Tasks must be movable between columns using drag and drop.

You may use any drag-and-drop library of your choice.

## Technical requirements

- Vue 3
- TypeScript
- Pinia

## Implementation expectations

- We expect clear separation of concerns across components, store logic, and composables.

## Submission

Upload the finished solution to a newly created GitHub repository.

## Expected UI outline

This is only a visual reference for layout and hierarchy. It does not define the exact design.

```text
+--------------------------------------------------------------------------------------+
| Kanban Board                                                                         |
+--------------------------------------------------------------------------------------+
| Filters                                                                              |
| [Author v]   [Search by title.............................]   [Clear filters]        |
+--------------------------------------------------------------------------------------+
| Create task                                                                          |
| [Title.................................]  [Author v]  [Create task]                  |
+--------------------------------------------------------------------------------------+
|                                                                                      |
|  +------------------+  +------------------+  +------------------+  +------------------+
|  | to do            |  | in progress      |  | review           |  | done             |
|  | 12 tasks         |  | 8 tasks          |  | 3 tasks          |  | 15 tasks         |
|  +------------------+  +------------------+  +------------------+  +------------------+
|  | Task title       |  | Task title       |  | Task title       |  | Task title       |
|  | Author name      |  | Author name      |  | Author name      |  | Author name      |
|  | Date             |  | Date             |  | Date             |  | Date             |
|  |                  |  |                  |  |                  |  |                  |
|  | Task title       |  | Task title       |  | Task title       |  | Task title       |
|  | Author name      |  | Author name      |  | Author name      |  | Author name      |
|  | Date             |  | Date             |  | Date             |  | Date             |
|  +------------------+  +------------------+  +------------------+  +------------------+
|                                                                                      |
+--------------------------------------------------------------------------------------+
```
