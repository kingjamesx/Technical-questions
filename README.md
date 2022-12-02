# 5 Technical React Questions 
This repository contains 5 files to the 5 technical react questions listed below 

## Questions

> **Question 1:**
>
> - We have an API https://example.com/v1/api/login where we send in email,
password using content-type application/json.

This API returns { token: <JWT Token>, user_id: <integer>, role: <string>}.

I want you to write the AUTH Provider to handle authentication of the system.
Please fill in the TODOs.
```
If you don't answer this question fully, we will reject your candidacy.

  const LoginPage = () => {
  const [email, setEmail] = userState('');
  const [password, setPassword] = userState('');

  const handleEmailChange = (event) => {
    setEmail(event.target.value);
  };
  const handlePasswordChange = (event) => {
    setPassword(event.target.value);
  };

  const onSubmit = (event) => {
    //TODO
    //Call Axios
  }

  return (<div>
  <form onSubmit={onSubmit}>
  <input type="email" onChange={}
  </form>
  </div>);
});

//Provider
export const AuthContext = React.createContext();
const initialState = {};

const reducer = (state, action) => {
  switch (action.type) {
    case "LOGIN":
    //TODO
  }
};

const AuthProvider = ({ children }) => {
  const [state, dispatch] = useReducer(reducer, initialState);
  return (
    <AuthContext.Provider
      value={{
        state,
        dispatch,
      }}
    >
      {children}
    </AuthContext.Provider>
  );
}
```

> **Question 2:**
>
``` What wrong with this code? It crashes when I run it

function question_1() {
  const elements = ['one', 'two', 'three'];

  return (
    <div>
      {elements.map((value) => (<span>{value}</span>))}
    </div>
  )
}
``` 

> **Question 3:**
>
> - You are given the following api:
https://example.com/api/v1/model?page=1&limit=10

This API return the following:
{
  list: [{
    id: 1,
    title: 'title',
    description: 'description'
  }],
  num_pages: 10,
  page: 1,
  limit: 10
}

Fill in the following TODO to make this work.
```
If you don't answer this question fully, we will reject your candidacy.

  const TablePage = () => {
  const [data, setData] = useState([]);
  const [page, setPage] = useState(1);
  const [limit, setLimit] = userState(10);
  const [currentPage, setPage] = useState(0);
  const [canPreviousPage, setCanPreviousPage] = useState(false);
  const [canNextPage, setCanNextPage] = useState(false);
  const [pageCount, setPageCount] = useState(0);

  function previousPage() {
    //TODO
  }

  function nextPage() {
    //TODO
  }

  useEffect(() => {
    //TODO
    //Call Axios
  }, []);

  return (<div>
  <table>
  <thead>
  <td>ID</td>
  <td>title</td>
  <td>description</td>
  </thead>
  <tbody>
  {data.map((row, index) => {
    return (<tr>
    <td>{row.id}</td>
    <td>{row.title}</td>
    <td>{row.description}</td>
    </tr>);
  })}
  </tbody>
  </table>
  <div>
  <span>Page{" "}{page} of {pageCount}</span>
  <select value={limit} onChange={(e) => {setLimit(Number(e.target.value)); }}>
    {[5, 10, 20, 30, 40, 50].map((pageSize) => (
      <option key={pageSize} value={pageSize}>
        Show {pageSize}
      </option>
    ))}
  </select>
  <button onClick={previousPage} disabled={!canPreviousPage}>
    &#x02190;
  </button>
  <button onClick={nextPage} disabled={!canNextPage}>
    &#x02192;
  </button>
  </div>
  </div>);
});
```

> **Question 4:**
>
> - 
Which CSS type are you familar with? Styled Components,
Tailwind Class Style, Inline CSS?

I want you to create the following:

Create a component called Polymorphism.

On large desktop view, this component is a circle that
flashes red and blue every 5 seconds.

On laptop size view, this component is a rectangle that
flashes orange and yellow every 5 seconds.

On tablet size view, it becomes a triangle that
flashes pink and green every 5 seconds.

On mobile size view, it becomes a square that
flashes purple and black every 5 seconds.


> **Question 5:**
>
> - What wrong with this code
What are 2 things wrong in this code

```

class Question4 extends React.Component {
	constructor(props) {
    super(props)

    this.state = {
      message: 'Welcome to React world'
    }
  }
  changeState(str) {
  	this.setState({
    	message: str
    });
    //Check message has changed to www
    if (this.state.message == 'www') {
    	alert('This is done correctly');
    }
  }
  render() {
    return <div>Hello {this.props.name}
    <button onClick={() => this.changeState('www')}></button>
    </div>;
  }
}

```
