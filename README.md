# React-Code

import React,{Component} from 'react';
import './App.css';
import Person from './Person/Person'

class App extends Component {

  state={
    person:[
      {name:"Shayan", age:23},
      {name:"Hamza", age:26},
      {name:"Saad",age:24}
    ],
    passion:[
      {name:"Football"},
      {name:"Tech stuff"}
    ]
  }

  switchNameHandler=()=>{
    // console.log("Was clicked");
    // this.state.person[0].name="Shayan Manzoor" DONT DO THIS!!!!
    this.setState(
      {
        person:
        [
        {name:"Nimra", age:23},
        {name:"Shani", age:26},
        {name:"Ahmed",age:2}
        ]
      }
    )

  }

  render(){
  return (
    <div className="App">
     <h1>Hi, Im a React App</h1>
     <p>This is really working!</p>
     <button onClick={this.switchNameHandler}>Switch Name</button>
     <Person name={this.state.person[0].name} age={this.state.person[0].age} />
     <Person name={this.state.person[1].name} age={this.state.person[1].age}>My Hobbies : {this.state.passion[1].name}</Person>
     <Person name={this.state.person[2].name} age={this.state.person[2].age}/>
    </div>
    );
  }
  // return React.createElement('div',{className:'App'},React.createElement('h1',{className:'App'}, 'Hi, I\'m a React App!!!'));
}

export default App;
