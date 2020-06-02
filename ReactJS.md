# React
1. JSX is transformed at build time like  `<h1>Shopping List for {this.props.name}</h1>` to `React.createElement('h1', /* ... h1 children ... */)`
2. Keys do not need to be globally unique; they only need to be unique between components and their siblings.
3. 