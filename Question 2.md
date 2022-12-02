Component name In react Cant start with a lower Case
The component name should be changed to Question_1.
This will not crash but a new problem is generated the component Name should be in PascalCase
The component name should be Question1. This work but there is still going to be one problem 
Looping through items in react requires you provide a unique key so react can detect changes 
```
New code: 
function Question1() {
  const elements = ['one', 'two', 'three'];

  return (
    <div>
      {elements.map((value,index) => (<span key={index}>{value}</span>))}
    </div>
  )
}

```