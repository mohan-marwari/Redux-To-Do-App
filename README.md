# Redux To-Do App

This is a simple To-Do application built using **React**, **Redux Toolkit**, **Vite**, and **Tailwind CSS**. The project demonstrates the usage of Redux Toolkit to manage the state in a scalable and organized way.

## Project Structure
```
src/
├── app/
│   ├── store.js           // Redux store configuration
├── features/
│   ├── todos/
│       ├── todoSlice.js   // Redux slice for todos
├── components/
│   ├── TodoApp.jsx        // React component for the To-Do app
├── index.js               // Entry point
├── styles/
│   ├── index.css          // Tailwind CSS configuration
```

## How It Works

### Features
- Add a new task.
- Mark tasks as completed or uncompleted.
- Delete tasks.

### Workflow
1. **State Management**:
   - All tasks are stored in a centralized Redux store.
2. **Add a Task**:
   - Dispatch an `addTodo` action with the task text.
   - The reducer in `todoSlice.js` updates the state by adding the new task.
3. **Toggle Task Completion**:
   - Dispatch a `toggleTodo` action with the task's `id`.
   - The reducer toggles the `completed` state of the task.
4. **Delete a Task**:
   - Dispatch a `deleteTodo` action with the task's `id`.
   - The reducer removes the task from the state.
5. **UI Update**:
   - The `TodoApp` component uses `useSelector` to fetch the updated state and render it.

## Installation
1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```
2. Navigate to the project directory:
   ```bash
   cd redux-todo-app
   ```
3. Install dependencies:
   ```bash
   npm install
   ```
4. Start the development server:
   ```bash
   npm run dev
   ```

## Files Overview

### `src/app/store.js`
- Configures the Redux store.
- Combines reducers from different slices.

### `src/features/todos/todoSlice.js`
- Contains the initial state and reducers for the todos feature.
- Exports actions (`addTodo`, `toggleTodo`, `deleteTodo`) and the reducer.

### `src/components/TodoApp.jsx`
- React component that handles the UI.
- Interacts with the Redux store using `useSelector` and `useDispatch`.

### `src/index.js`
- Wraps the `TodoApp` component with the Redux `Provider` to give access to the store.

### `src/styles/index.css`
- Contains Tailwind CSS configurations and global styles.

## Redux Toolkit Fundamentals
- **Store**: The centralized state container for the app.
- **Slice**: Contains the logic (reducers) and actions for a specific feature.
- **Dispatch**: Sends actions to the store.
- **useSelector**: Retrieves state from the store in React components.

## Example: Adding a Todo
1. User enters "Learn Redux" and clicks "Add".
2. The `handleAdd` function in `TodoApp.jsx` dispatches an action:
   ```javascript
   dispatch(addTodo("Learn Redux"));
   ```
3. The `addTodo` reducer in `todoSlice.js` updates the state.
4. The updated state is fetched using `useSelector` and displayed.

## Advantages of Redux Toolkit
- Centralized state management.
- Simplified syntax for reducers and actions.
- Scalable structure for large applications.

## Screenshots
### Application Preview
![App Screenshot](./screenshots/app-preview.png)

## Future Enhancements
- Add filters (e.g., show all/completed/incomplete tasks).
- Implement local storage to persist tasks.

## Author
- **Mohan Marwari**  
  [Instagram](https://instagram.com/mohan_marwari) | [Twitter](https://twitter.com/mohan_marwari) | [GitHub](https://github.com/mohan_marwari)

---
Feel free to explore and modify the project to learn more about Redux Toolkit! 😊
