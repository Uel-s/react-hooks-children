## Purpose for children.

div is the parent to `h1` and `p`

```js
function Header(props) {
  return (
    <div class="container">
      <h1>{props.header}</h1>
      <p>{props.description}</p>
    </div>
  );
}

`The header and description props help us make the Header component reusable, as seen here:`

ReactDOM.render(
  <div>
    <Header header="Hello, I'm in a container!", description="I'm a description!" />
    <Header header="I'm another container", description="Whoa that's weird!" />
    <Header header="A third container!", description="Cray cray" />
  </div>,
  document.getElementById('root')
)
```

## How do we make children?

```js

function Example(props) {
  return <div>{props.exampleProp}</div>;
}

<Example exampleProp="example value" />;


`However, React also allows you to use your components with an opening and closing tag, like most HTML elements:`

<Example exampleProp="example value">
  <h1>Example header!</h1>
  <p>Some example text</p>
</Example>
```

```js

function Example(props) {
  return (
    <div>
      {props.exampleProp}
      {/* using the children prop to render any elements inside the opening and closing tag of Example */}
      {props.children}
    </div>
  );
}

```

You have a component that is able to render its children! Any valid JSX elements, including your own components and nested JSX elements, can be used as children.


