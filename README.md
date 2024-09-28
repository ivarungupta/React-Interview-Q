# REACT INTERVIEW QUESTIONS 

1. What is React? 
2. Explain the difference between Real DOM and Virtual DOM? 
3. What are the key features of React? 
4. What is JSX? 
5. Why can't browsers read JSX? 
6. What are React components? 
7. Differentiate between a Class component and a Functional component. 
8. What is the difference between state and props in React? 
9. What are React hooks? Name some common hooks. 
10. How do useState and useEffect work in React? 
11. What is the importance of key in React? 
12. Explain the concept of lifting state up in React. 
13. How does one pass data between components in React? 
14. What are the new features introduced in React 18? 
15. What is concurrent rendering in React 18? 
16. How does automatic batching work in React 18? 
17. What is the useTransition hook, and how does it work? 
18. Explain the working of useDeferredValue in React 18. 
19. What is Suspense in React, and how does it work? 
20. How has React 18 improved Suspense? 
21. What is the new startTransition function in React 18? 
22. What is the difference between useTransition and startTransition? 
23. How do you use the Concurrent Features introduced in React 18? 
24. How does React 18 enhance server-side rendering (SSR)? 
25. What is React Server Components, and how does it work with React 18? 
26. What role does the concurrentMode flag play in React 18? 
27. Explain the React lifecycle methods in detail. 
28. What is React Context API, and when would you use it? 
29. What are higher-order components (HOCs) in React? 
30. How does React handle forms and controlled components? 
31. What are uncontrolled components in React? 
32. What is Prop Drilling, and how can it be avoided? 
33. What are React Portals, and when should you use them? 
34. What is the significance of React’s shouldComponentUpdate method? 
35. What are Fragments in React? 
36. Explain the concept of memoization in React using React.memo and useMemo. 
37. How do you optimize performance in a React application? 
38. What are the rules for using React Hooks? 
39. How do you handle errors in React using error boundaries? 
40. What is the componentDidCatch() method in React? 
41. What are synthetic events in React? 
42. How can you test a React component? 
43. What is the role of Jest in React testing? 
44. What is the difference between shallow rendering and full rendering in testing? 
45. How does one implement lazy loading in React?
46. How can you test React hooks?
47. How do you handle forms and validations in React?
48. What is Redux, and how does it relate to React?
49. What are the key principles of Redux?
50. What are actions, reducers, and the store in Redux?
51. What is the difference between useReducer and Redux?
52. How does one connect Redux to a React component?
53. What are React middlewares in Redux, and give examples?
54. What are thunks in Redux?
55. How do you handle asynchronous actions in Redux?
56. Explain the differences between Redux, Context API, and MobX for state management.
57. What is React Router?
58. How do you implement dynamic routing in React?
59. What is the difference between BrowserRouter and HashRouter?
60. What is the significance of Route and Switch in React Router?
61. How do you pass parameters in React Router?
62. What are nested routes in React Router?

Here's a detailed guide with examples for all 62 questions to help you prepare for your tech interviews:

---

### 1. **What is React?**
React is a JavaScript library used for building user interfaces, particularly single-page applications (SPAs). It allows developers to create reusable UI components.
   
   **Example**:
   ```js
   import React from 'react';
   const HelloWorld = () => <h1>Hello, World!</h1>;
   export default HelloWorld;
   ```

### 2. **Difference between Real DOM and Virtual DOM**
- **Real DOM** updates the entire tree structure whenever changes are made.
- **Virtual DOM** is a lightweight copy of the real DOM. React updates only the parts of the DOM that need changes.
  
   **Example**:
   ```js
   const element = <h1>Hello, World!</h1>; // Virtual DOM
   ```

### 3. **Key Features of React**
- Declarative UI
- Component-Based
- Virtual DOM
- Unidirectional data flow
- JSX Syntax
  
   **Example**:
   ```js
   const App = () => <div>Hello, React!</div>;
   ```

### 4. **What is JSX?**
JSX is a syntax extension that looks similar to HTML but is used in React to describe UI components.
  
   **Example**:
   ```js
   const element = <h1>Hello, JSX!</h1>;
   ```

### 5. **Why can't browsers read JSX?**
Browsers can only understand plain JavaScript, and JSX is not valid JavaScript. JSX needs to be transpiled into regular JavaScript using Babel or another compiler.

### 6. **What are React Components?**
Components are the building blocks of a React application. They can be class-based or function-based.
   
   **Example**:
   ```js
   const HelloWorld = () => <h1>Hello, World!</h1>;
   ```

### 7. **Class vs. Functional Components**
- **Class Components**: Can hold state and lifecycle methods.
- **Functional Components**: Use hooks to manage state and lifecycle methods.
   
   **Class Example**:
   ```js
   class Welcome extends React.Component {
     render() {
       return <h1>Hello, Class Component!</h1>;
     }
   }
   ```

   **Functional Example**:
   ```js
   const Welcome = () => <h1>Hello, Functional Component!</h1>;
   ```

### 8. **State vs. Props in React**
- **State**: Internal data of a component.
- **Props**: External data passed to a component.
   
   **Example**:
   ```js
   const Welcome = (props) => <h1>Hello, {props.name}!</h1>;
   ```

### 9. **What are React Hooks?**
Hooks let you use state and other React features in functional components.
   
   **Common Hooks**:
   - `useState`
   - `useEffect`
   - `useContext`

### 10. **How do useState and useEffect work?**
- **useState**: Manages component state.
- **useEffect**: Handles side effects such as data fetching or manual DOM updates.
  
   **Example**:
   ```js
   const [count, setCount] = useState(0);
   useEffect(() => {
     document.title = `Count is ${count}`;
   }, [count]);
   ```

### 11. **Importance of Key in React**
Keys help React identify which items have changed, are added, or are removed. It improves list rendering performance.
  
   **Example**:
   ```js
   const list = items.map((item) => <li key={item.id}>{item.name}</li>);
   ```

### 12. **Lifting State Up**
State is "lifted" to the nearest common ancestor so that multiple child components can share the state.
   
   **Example**:
   ```js
   const Parent = () => {
     const [data, setData] = useState('');
     return <Child data={data} />;
   };
   ```

### 13. **Passing Data Between Components**
Data is passed from parent to child using props.
  
   **Example**:
   ```js
   const Parent = () => <Child message="Hello" />;
   const Child = (props) => <h1>{props.message}</h1>;
   ```

### 14. **New Features in React 18**
- Automatic Batching
- Concurrent Rendering
- `useTransition` hook
- `useDeferredValue` hook
- Improved Suspense
  
   **Example**:
   ```js
   const [isPending, startTransition] = useTransition();
   ```

### 15. **Concurrent Rendering in React 18**
Concurrent rendering allows React to interrupt and prioritize rendering tasks without blocking the UI.

### 16. **Automatic Batching in React 18**
React 18 batches multiple state updates automatically to reduce the number of renders.
  
   **Example**:
   ```js
   setCount((prev) => prev + 1);
   setFlag(true); // Batches these updates
   ```

### 17. **useTransition Hook**
It allows you to mark updates as non-urgent, improving UI responsiveness.

   **Example**:
   ```js
   const [isPending, startTransition] = useTransition();
   startTransition(() => {
     setData(newData);
   });
   ```

### 18. **useDeferredValue Hook**
It defers a value until the render is less urgent, allowing for smoother rendering of lower-priority content.
  
   **Example**:
   ```js
   const deferredValue = useDeferredValue(value);
   ```

### 19. **What is Suspense in React?**
Suspense lets components "wait" for some code to load, such as when performing lazy loading.
  
   **Example**:
   ```js
   const LazyComponent = React.lazy(() => import('./LazyComponent'));
   ```

### 20. **How Has React 18 Improved Suspense?**
React 18 enhances Suspense for concurrent rendering, which allows it to pause renders and continue without blocking.

### 21. **startTransition Function in React 18**
It is used to mark updates as non-urgent.
  
   **Example**:
   ```js
   startTransition(() => {
     setCount(count + 1);
   });
   ```

### 22. **useTransition vs. startTransition**
- `useTransition`: For concurrent updates within functional components.
- `startTransition`: For concurrent updates outside functional components.

### 23. **Using Concurrent Features in React 18**
You can use hooks like `useTransition`, `useDeferredValue`, and Suspense to implement concurrent rendering.
  
   **Example**:
   ```js
   startTransition(() => setData(newData));
   ```

### 24. **React 18's Server-Side Rendering (SSR) Enhancements**
React 18 introduces concurrent features in SSR, such as streaming responses and faster page load times.

### 25. **What are React Server Components?**
React Server Components allow components to be rendered on the server, which optimizes the performance of complex applications.

### 26. **Role of ConcurrentMode in React 18**
`ConcurrentMode` allows React to perform multiple state updates in a single pass.

### 27. **React Lifecycle Methods**
- **Mounting**: `constructor()`, `componentDidMount()`
- **Updating**: `componentDidUpdate()`
- **Unmounting**: `componentWillUnmount()`

### 28. **React Context API**
It allows passing data through the component tree without having to pass props manually at every level.
  
   **Example**:
   ```js
   const MyContext = React.createContext();
   ```

### 29. **Higher-Order Components (HOCs)**
HOCs are functions that take a component and return a new component with enhanced behavior.
  
   **Example**:
   ```js
   const EnhancedComponent = withFeature(OriginalComponent);
   ```

### 30. **React Forms and Controlled Components**
Controlled components have their state controlled by React, usually via `useState`.
  
   **Example**:
   ```js
   const [value, setValue] = useState('');
   ```

### 31. **Uncontrolled Components in React**
Uncontrolled components allow the DOM to control the form data rather than React managing the state.

   **Example**:
   ```js
   const Input = () => (
     <input type="text" defaultValue="Default Value" />
   );
   ```

### 32. **What is Prop Drilling, and How Can It Be Avoided?**
Prop drilling occurs when you pass data through multiple layers of components, even when some components do not need the data.

   **Avoid Prop Drilling** with the **Context API**:
   ```js
   const DataContext = React.createContext();
   ```

### 33. **React Portals**
Portals provide a way to render children into a DOM node that exists outside the main DOM hierarchy.

   **Example**:
   ```js
   ReactDOM.createPortal(<Child />, document.getElementById('portal-root'));
   ```

### 34. **Significance of shouldComponentUpdate Method**
This lifecycle method is used to optimize performance by preventing unnecessary renders.

   **Example**:
   ```js
   shouldComponentUpdate(nextProps, nextState) {
     return nextProps.value !== this.props.value;
   }
   ```

### 35. **React Fragments**
Fragments let you group multiple children elements without adding extra nodes to the DOM.

   **Example**:
   ```js
   const FragmentExample = () => (
     <React.Fragment>
       <h1>Title</h1>
       <p>Description</p>
     </React.Fragment>
   );
   ```

### 36. **Memoization in React using React.memo and useMemo**
- **React.memo**: Memoizes the result of a component render.
- **useMemo**: Memoizes a value computed from dependencies.

   **Example**:
   ```js
   const MemoizedComponent = React.memo(() => <ChildComponent />);
   ```

   **useMemo Example**:
   ```js
   const computedValue = useMemo(() => expensiveCalculation(), [dependencies]);
   ```

### 37. **Optimizing Performance in React**
- Memoization with `React.memo` and `useMemo`
- Lazy Loading Components
- Avoid unnecessary re-renders with `shouldComponentUpdate` or `React.PureComponent`

### 38. **Rules for Using React Hooks**
- Only call hooks at the top level of a component.
- Only call hooks from React function components or custom hooks.

### 39. **Handling Errors in React using Error Boundaries**
Error boundaries catch JavaScript errors in their child component tree and display fallback UI.

   **Example**:
   ```js
   class ErrorBoundary extends React.Component {
     componentDidCatch(error, info) {
       console.log(error, info);
     }
     render() {
       return this.props.children;
     }
   }
   ```

### 40. **What is componentDidCatch() Method in React?**
`componentDidCatch()` is a lifecycle method used by error boundaries to catch errors during rendering.

### 41. **Synthetic Events in React**
Synthetic events are cross-browser wrappers around the native browser events, providing a consistent API across different browsers.

   **Example**:
   ```js
   const handleClick = (event) => console.log(event);
   ```

### 42. **How Can You Test a React Component?**
You can test a React component using testing libraries like **Jest** and **React Testing Library**.

   **Example**:
   ```js
   import { render, screen } from '@testing-library/react';
   ```

### 43. **Role of Jest in React Testing**
Jest is a testing framework used to run tests and assertions in React applications.

### 44. **Shallow Rendering vs. Full Rendering in Testing**
- **Shallow Rendering**: Only renders the top-level component.
- **Full Rendering**: Renders both the parent and child components.
   
   **Example**:
   ```js
   import { shallow } from 'enzyme';
   shallow(<MyComponent />);
   ```

### 45. **Implementing Lazy Loading in React**
Lazy loading defers loading components until they are needed.

   **Example**:
   ```js
   const LazyComponent = React.lazy(() => import('./MyComponent'));
   ```

### 46. **Testing React Hooks**
You can use libraries like `@testing-library/react-hooks` to test hooks directly.
   
   **Example**:
   ```js
   import { renderHook } from '@testing-library/react-hooks';
   const { result } = renderHook(() => useCustomHook());
   ```

### 47. **Handling Forms and Validations in React**
Forms are managed using controlled components and state.
  
   **Example**:
   ```js
   const [inputValue, setInputValue] = useState('');
   ```

   For validation, libraries like **Formik** or **Yup** can be used.

### 48. **What is Redux, and How Does It Relate to React?**
Redux is a state management library often used with React to manage the application state in a predictable way.

   **Example**:
   ```js
   const store = createStore(reducer);
   ```

### 49. **Key Principles of Redux**
- Single source of truth (store)
- State is read-only
- Changes are made with pure functions (reducers)

### 50. **Actions, Reducers, and Store in Redux**
- **Actions**: Describe changes in the application.
- **Reducers**: Pure functions that define how the state changes.
- **Store**: Holds the application state.

### 51. **Difference Between useReducer and Redux**
- `useReducer`: A hook that manages local state inside components.
- **Redux**: Manages global state across the entire app.

### 52. **Connecting Redux to React**
`react-redux` library provides `Provider` to pass down the store and `connect()` or hooks like `useSelector()` and `useDispatch()` to access the store.

   **Example**:
   ```js
   const dispatch = useDispatch();
   const state = useSelector(state => state);
   ```

### 53. **React Middlewares in Redux**
Middlewares in Redux allow you to handle asynchronous actions or log actions. Examples include:
- **Redux Thunk**
- **Redux Saga**

### 54. **What are Thunks in Redux?**
Thunks are functions that return another function to handle asynchronous actions like fetching data.

   **Example**:
   ```js
   const fetchData = () => (dispatch) => {
     fetch('/api/data')
       .then(response => response.json())
       .then(data => dispatch({ type: 'FETCH_SUCCESS', payload: data }));
   };
   ```

### 55. **Handling Asynchronous Actions in Redux**
This is typically done with middlewares like **Redux Thunk** or **Redux Saga**.

### 56. **Differences Between Redux, Context API, and MobX**
- **Redux**: Centralized state management with a strict flow.
- **Context API**: Simple state management for small to medium apps.
- **MobX**: Reactive state management with observable values.

### 57. **What is React Router?**
React Router is a library for handling routing in React applications.

   **Example**:
   ```js
   <BrowserRouter>
     <Route path="/home" component={Home} />
   </BrowserRouter>
   ```

### 58. **Implementing Dynamic Routing in React**
Dynamic routing is done by passing parameters to routes.

   **Example**:
   ```js
   <Route path="/user/:id" component={User} />
   ```

### 59. **Difference Between BrowserRouter and HashRouter**
- **BrowserRouter**: Uses the HTML5 history API for cleaner URLs.
- **HashRouter**: Uses the URL hash for navigation, which is useful for older browsers.

### 60. **Significance of Route and Switch in React Router**
- **Route**: Defines a component to render when the URL matches.
- **Switch**: Renders the first matching route.

   **Example**:
   ```js
   <Switch>
     <Route exact path="/" component={Home} />
     <Route path="/about" component={About} />
   </Switch>
   ```

### 61. **Passing Parameters in React Router**
You can pass parameters via the URL and access them via `useParams()`.

   **Example**:
   ```js
   const { id } = useParams();
   ```

### 62. **Nested Routes in React Router**
Nested routes allow you to render routes inside other routes.

   **Example**:
   ```js
   <Route path="/dashboard" component={Dashboard}>
     <Route path="/dashboard/profile" component={Profile} />
   </Route>
   ```

---
