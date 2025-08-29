Ques 1 : What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?

Ans: 
*getElementById finds one element by its id (provided inside it as parmeter) and returs single element or null if not found.
Code : document.getElementById("subscribeButton")
this will return a single element which has the following id named "subscribeButton" or null if not found.

*getElementsByClassName finds all element by its class name (provided inside it as parmeter) return HTMLCollection.
Code: document.getElementsByClassName("item");
this will return a HTML collection which has the following class named "item" .

*querySelector finds first element which matches the css selector (provided inside it as parmeter - (#id, .class, div > p, etc )) and returs single element (Node) .
code : document.querySelector(".item");
this will return a single element (as Node) which has the following class named "item" .

*querySelectorALL finds all element which matches the css selector (provided inside it as parmeter - (#id, .class, div > p, etc )) and returs a list of elements (NodeList) .
code : document.querySelectorAll(".item");
this will return a all element (as Nodelist) which has the following class named "item" .


Ques 2 : How do you create and insert a new element into the DOM?

Ans:
*step 1: take the div where new elements will be inserted Code: const element = document.getElementById("itemDiv")

*step 2: create a new div using javascript, Code: const newDiv = document.createElement("div");

*step 3: fill the div, Code: newDiv= <p> im the new element </p>

*step 4: append the div inside the main div (element) Code: element.appendChild(newdiv)



Ques 3 : What is Event Bubbling and how does it work?

Ans:
Event bubbling means that when an event occurs on a child element, it is first triggered on that element then parent element then root document. If a button is clicked, the event will first go to the button then up to div -> body -> document.


Ques 4 : What is Event Delegation in JavaScript? Why is it useful?

Ans:
Event deligation means using one event listener on parent to catch the event from its child.
if a parent element has 100 buttons we dont need 100 event listener what we can do is give a single event listener on the parent and catch the from its child using event bubbling to our advantage.


Ques 5 : What is the difference between preventDefault() and stopPropagation() methods?

Ans:
event.preventDefault() this prevent the browser default behaviour for an event. For example in a form there is a submit button which has a default behaviour of submitting we can prevent it by using event.preventDefault()
stopPropagation() this is a solution to event bubbling problem where it prevents events from bubbling up.
