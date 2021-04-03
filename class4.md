# Code 301 Reading Notes

## Class 04

[<== Previous Lesson](class3.md) [Next Lesson ==>](class5.md)

[<== Home](README.md) 🏠

# React and Forms

letting the browser handle the state:

````javascript
export function LoginForm() {
  const handleSubmit = (e: React.FormEvent) => {
    e.preventDefault();
    const formData = new FormData(e.target as HTMLFormElement);
    api.login(formData.get('email'), formData.get('password'));
  };
  return (
    <form onSubmit={handleSubmit}>
      <div>
        <label htmlFor="email">Email</label>
        <input
          type="email"
          id="email"
          name="email"
        />
      </div>
      <div>
        <label htmlFor="password">Password</label>
        <input
          type="password"
          id="password"
          name="password"
        />
      </div>
      <button>Log in</button>
    </form>
  );
}

// Not a single Hook in sight, no setting the value, and no change listeners either. 





// https://blog.logrocket.com/forms-in-react-in-2020/
````

+ [`FormData`](https://developer.mozilla.org/en-US/docs/Web/API/FormData) built-in browser API *FormData is a handy (and [well supported](https://developer.mozilla.org/en-US/docs/Web/API/FormData#Browser_compatibility)) way to get the field values from our input fields!*
+ We get a reference to the form DOM element via the submit event’s target attribute and create a new instance of the FormData class. Now, we can get all fields by their name attribute by calling formData.get(‘name-of-input-field’).
+ This way, you never really need to handle the state explicitly. If you want default values (like if you’re populating initial field values from a database or local storage), React even provides you with a handy `<span class="pln">defaultValue</span>` prop to get that done as well!

## React Docs - Forms

## React Bootstrap - Forms

### Reading

* [React Docs - Forms](https://reactjs.org/docs/forms.html)

### Bookmark/Skim

* [React Bootstrap - Forms](https://react-bootstrap.github.io/components/forms/)

[<== Home](README.md) 🏠
