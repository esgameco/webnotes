# Basic React

## Render

```typescript
import React from 'react'
import ReactDom from 'react-dom'

const jsx: React.JSX = <h1>Test</h1>;

ReactDom.render(
    jsx,
    domElement
);
```

Renders jsx to the innerHTML of the domElement.

***

## Components + Props

#### Functions

```typescript
import React from 'react'

type FuncProps = {
    name: string;
};

const FuncComponent: React.FC<FuncProps> = (props: FuncProps) => {
    return (
        <h1>{props.name}</h1>
    );
};
```

#### Classes

```typescript
import React from 'react'

type ClassProps = {
    name: string;
};

type ClassState = {
    authenticated: boolean
}

class ClassComponent extends React.Component<ClassProps, ClassState> {
    render() {
        return (
            <h1>{this.state.authenticated}</h1>
        );
    }
}
```