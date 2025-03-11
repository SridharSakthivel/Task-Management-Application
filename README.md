# Task Management Application

## Project Description:

The Task Management Application is a React-typescript based tool that offers a visual task management system similar to a Kanban board. It enables users to view, manage, and seamlessly move tasks across different status columns: To Do, In Progress, and Done.

### Features Implemented:

- Three-column layout displaying tasks by status (To Do, In Progress, Done)
- Task cards showing name and description
- Right-click context menu for moving tasks between statuses
- Functionalities added for edit and delete of a task
- Click handlers to select individual tasks
- Responsive task state management
- Click-outside detection to close context menu

## Setup and Installation:

## -Frontend:

- git clone task-management-app.bundle my_project
- Cd my_project
- git log --oneline --graph --all
- cd my_project
- npm install
- npm run dev

## -Backend:

- cd server
- node server.js

### Prerequisites:

- Node.js (v14.0.0 or higher)
- npm (v6.0.0 or higher)

### Challenges Faced:

## Context Menu Positioning:

Problem: Implementing a right-click context menu that appears at the cursor position and tracks the selected task’s ID and status was complex. Additionally, the menu needed to close when clicking outside without interfering with other interactions.
-Used e.clientX and e.clientY from the MouseEvent to dynamically set the menu’s position via inline styles with position: fixed.

Problem: The context menu needed to display different options based on the task’s current status (e.g. Move to In Progress for "To Do" tasks, Move to Done for "In Progress" tasks).
-Implemented conditional rendering in the context menu using the taskStatus (current state) stored in the contextMenu state.
