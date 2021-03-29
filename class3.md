# Code 301 Reading Notes

## Class 03

[<== Previous Lesson](class2.md) [Next Lesson ==>](class4.md)

[<== Home](README.md) 🏠

# Passing Functions as Props

## React Docs - Lifting State Up

> A pass at Lifting State Up on my SelectedBeast Modal
>
> *still figuring out where to place the Modal bits and bobbles*

````javascript
//-----------------------------------------------------------------------------------------------x
const displayModal = this.props.displayModal;
const hideModal = this.props.hideModal;
const image = this.props.selectedBeast.image_url;
const title = this.props.selectedBeast.title;
const description = this.props.selectedBeast.description;
const keyword = this.props.selectedBeast.keyword;
//-----------------------------------------------------------------------------------------------x

class SelectedBeast extends React.Component {
  render() {
    return (
      <Modal show={displayModal} onHide={hideModal}>
      <Modal.Dialog>
        <Modal.Header>
          <h2>Lil Horned Beasties</h2>
        </Modal.Header>
        <Modal.Body>
        <Card style={{ width: '26rem'}}>
        <Card.Img src={image} />
            <Card.Body>
              <Card.Title>{title}</Card.Title>
              <Card.Text>{description}</Card.Text>
              <Card.Text>{keyword}</Card.Text>
              <Button onClick = {hideModal} variant="primary" size="lg" block>C L O S E</Button>
            </Card.Body>
        </Card>
      </Modal.Body>
      </Modal.Dialog>
      </Modal>
    )
  }
}

export default SelectedBeast;
````

## React Docs - lists and keys

**Keys**

+ Keys help React identify which items have changed, are added, or are removed.
+ Keys should be given to the elements inside an array to give the elements a stable identity.

> A good rule of thumb is that elements inside the `map()` call need keys.

+ Keys Must Only Be Unique Among Siblings

+ Keys used within arrays should be unique among their siblings. However they don’t need to be globally unique. We can use the same keys when we produce two different arrays:

## React Tutorial through Declaring a Winner

````javascript
function Square(props) {
  return (
    <button className="square" onClick={props.onClick}>
      {props.value}
    </button>
  );
}

class Board extends React.Component {
  renderSquare(i) {
    return (
      <Square
        value={this.props.squares[i]}
        onClick={() => this.props.onClick(i)}
      />
    );
  }

  render() {
    return (
      <div>
        <div className="board-row">
          {this.renderSquare(0)}
          {this.renderSquare(1)}
          {this.renderSquare(2)}
        </div>
        <div className="board-row">
          {this.renderSquare(3)}
          {this.renderSquare(4)}
          {this.renderSquare(5)}
        </div>
        <div className="board-row">
          {this.renderSquare(6)}
          {this.renderSquare(7)}
          {this.renderSquare(8)}
        </div>
      </div>
    );
  }
}

class Game extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      history: [
        {
          squares: Array(9).fill(null)
        }
      ],
      stepNumber: 0,
      xIsNext: true
    };
  }

  handleClick(i) {
    const history = this.state.history.slice(0, this.state.stepNumber + 1);
    const current = history[history.length - 1];
    const squares = current.squares.slice();
    if (calculateWinner(squares) || squares[i]) {
      return;
    }
    squares[i] = this.state.xIsNext ? "X" : "O";
    this.setState({
      history: history.concat([
        {
          squares: squares
        }
      ]),
      stepNumber: history.length,
      xIsNext: !this.state.xIsNext
    });
  }

  jumpTo(step) {
    this.setState({
      stepNumber: step,
      xIsNext: (step % 2) === 0
    });
  }

  render() {
    const history = this.state.history;
    const current = history[this.state.stepNumber];
    const winner = calculateWinner(current.squares);

    const moves = history.map((step, move) => {
      const desc = move ?
        'Go to move #' + move :
        'Go to game start';
      return (
        <li key={move}>
          <button onClick={() => this.jumpTo(move)}>{desc}</button>
        </li>
      );
    });

    let status;
    if (winner) {
      status = "Winner: " + winner;
    } else {
      status = "Next player: " + (this.state.xIsNext ? "X" : "O");
    }

    return (
      <div className="game">
        <div className="game-board">
          <Board
            squares={current.squares}
            onClick={i => this.handleClick(i)}
          />
        </div>
        <div className="game-info">
          <div>{status}</div>
          <ol>{moves}</ol>
        </div>
      </div>
    );
  }
}

// ========================================

ReactDOM.render(<Game />, document.getElementById("root"));

function calculateWinner(squares) {
  const lines = [
    [0, 1, 2],
    [3, 4, 5],
    [6, 7, 8],
    [0, 3, 6],
    [1, 4, 7],
    [2, 5, 8],
    [0, 4, 8],
    [2, 4, 6]
  ];
  for (let i = 0; i < lines.length; i++) {
    const [a, b, c] = lines[i];
    if (squares[a] && squares[a] === squares[b] && squares[a] === squares[c]) {
      return squares[a];
    }
  }
  return null;
}

// Array.prototype.concat() 
// The concat() method is used to merge two or more arrays. This method does not change the existing arrays, but instead returns a new array.
// https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/concat
````

### [React Render HTML](https://www.w3schools.com/react/react_render.asp)

````javascript
// Create a variable that contains HTML code and display it in the root node:

const myelement = (
  <table>
    <tr>
      <th>Name</th>
    </tr>
    <tr>
      <td>Aloysious</td>
    </tr>
    <tr>
      <td>Calliope</td>
    </tr>
  </table>
);

ReactDOM.render(myelement, document.getElementById('root'));


````

**The Root Node**

The root node is the HTML element where you want to display the result.

It is like a *container* for content managed by React.

It does **NOT** have to be a `<div>` element and it does **NOT** have to have the `id='root'`:

````javascript
// The root node can be called whatever you like:

<body>

  <header id="aloysious"></header>

</body>

// Display the result in the <header id="aloysious"> element:

ReactDOM.render(<p>Hallo</p>, document.getElementById('aloysious'));
````

## The Spread Operator [-`Dr. Derek Austin 🥳`-]

**What is the spread operator?**

InJavaScript, [spread syntax](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax) refers to the use of an ellipsis of three dots (`…`) to expand an iterable object into the list of arguments.

> “When `...arr` is used in the function call, it ‘expands’ an iterable object `arr` into the list of arguments.” — [JavaScript.info](https://javascript.info/rest-parameters-spread-operator)

The spread operator was added to JavaScript in ES6 (ES2015), just like the [rest parameters](https://www.geeksforgeeks.org/javascript-rest-operator/), which have the same syntax: three magic dots `…`.

**What else can `…` do?**

The `…` spread operator is useful for many different routine tasks in JavaScript, including the following:

* Copying an array
* Concatenating or combining arrays
* Using Math functions
* Using an array as arguments
* Adding an item to a list
* Adding to state in React
* Combining objects
* Converting NodeList to an array

In each case, the spread syntax expands an iterable object, usually an array, though it can be used on any interable, including a string.

> “The spread operator can expand another item by split an iterable element like a string or an array into individual elements:” — [CodinGame](https://www.codingame.com/playgrounds/7998/es6-tutorials-spread-operator-with-fun).com

The spread operator `…` is useful for working with arrays and objects in JavaScript

### Reading

* [React Docs - Lifting State Up](https://reactjs.org/docs/lifting-state-up.html)
* [React Docs - lists and keys](https://reactjs.org/docs/lists-and-keys.html)
* [React Tutorial through Declaring a Winner](https://reactjs.org/tutorial/tutorial.html)
* [The Spread Operator](https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab)

[<== Home](README.md) 🏠
