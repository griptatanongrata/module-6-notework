# module-6-notework

//INTRO//

WHAT IS REACT
*A JavaScript library for building user interfaces
*It is a JavaScript framework

WHY DO WE USE REACT
*Easier to use
*Maintainable
*Scalable
*Most popular frontend Framework

//REUSABLE COMPONENTS//

WHY USE THEM?
\*Components help reduce code duplication

TWO PARTS
*Creating a component
*Use a component

CREATING A COMPONENT[react-crash-course]
*Create a new file (Todo.jsx)
*Inside of this file, create a new function (function Todo{})
\*Inside of your function, return some JSX
(function Todo {return <div>Finish Frontend Simplified</div>})
\*Export your function (export default Todo)

USING A COMPONENT[react-crash-course]
*Import The File (import Todo from "./components/Todo.jsx")
*Use The Component (<Todo></Todo>)

//PROPS//

WHAT ARE PROPS?
\*Props make components dynamic

TWO PARTS
*Creating props
*Using props
propName = title

CREATING PROPS
\*Pass in the property name and value (<Todo propName="Prop Value" />)
\*Multiple properties can be created for one component (<Todo propName="Prop Value" propTwo="Second Prop Value">)

USING PROPS
\*Accept and use props in a parameter (function Todo({propName}){return <div>{propName}</div>})
\*Multiple properties are utilized by accepting the propNames into the original component parameters (function Todo({ propName, propTwo }) {return <div>{propName}{propTwo}</div>})

PROP LAYOUT
*Parent = <MyComponent test="Testing" />
*Child = function MyComponent({ test }) {
return <div>{test}</div>
}
\*The output should utilize the the test prop and display "Testing" on the server

//EVENT HANDLERS//

WHAT ARE EVENT HANDLERS
*Code that executes when an event occurs
*Examples (onclick on clickable fields, onchange in input[typed] fields)
*When utilizing a new function that is defined by a string with the same name, do not use parentheses because it does not have anything else that needs to be parsed (function deleteTodo() needs console.log('deleteTodo') to work with onClick = {deleteTodo})
*IF it needs a parentheses due to an extra parse in the function, then use a parentheses, but also add the extra following features (function deleteTodo(id [parsed]) needs console.log('deleteTodo', id) to work with onClick={() => deleteTodo([idvalue])})

//REACT HOOKS//

MULTIPLE TYPES
*useState: How we define variables in React
*useEffect: does something as soon as a component mounts

CONDITIONAL RENDERING
\*rendering a component when a certain condition is met
\*if you want to conditionally render a component with a value, all you have to do is ues a tertiary operator (example: let isModalOpen = false works with {isModalOpen ? <Modal title="Are you sure you want to delete" /> : null[or <></>]})(NOTE: isM... && <... /> with no null variable also works)
*using double !! converts any value into boolean
*if you are creating a counter, use a value called "prev[first array variable]" to callback an original value

SETTING VALUES IN REACT HOOKS
*check SCREEN SHOTS for more info
*Numbers: setNum(number)
*Booleans: setBool(true or false)
\*Strings: setStr("Hello World")
*to change the value, make a callback using the prev... item
\*Examples:
-setNum(10) setNum(prevNum => prevNum + 10)
-setBool(true) setBool(prevBool => !prevBool)
-setStr("Frontend") setStr(prevStr => prevStr + "Simplified")
-setObj(prevObj => ({...prevObj, quantity: prevObj.quantity + 1}))
-setArr(prevArr => ([...prevArr, 5]))

PASSING EMISSION
\*Parent scripts are where all the components are imported and utilized (App.jsx) and each component (<Todo />) is utilized as the child page (Todo.jsx)
\*Check SCREEN SHOTS for more info
\*To utilize a function from a child page properly, it is best practice to create the function within the parent function, then parse it into the child function as well as applying the parent function into the html elements of the child function (refer to react-crash-course cancelModal/confirmModal exercise)

USE EFFECTS
\*a function utilizes a callback and a dependency list

//ROUTING//

WHAT IS IT
\*allows navigation around a website via React
\*to fetch multiple items (like usernames for multiple people) you utilize the { useParams } with a const {username} to create a variable around specified paramaters with that username (for more info, refer to SCREEN SHOTS)

//API INTEGRATION//

HOW TO RETRIEVE
\*use fetch or axios
