# ZTM - React

## React Key Concepts

How To Be A Great React Developer

1. Decide on Components
2. Decide the State and where it lives
3. What changes when state changes

## React Basics

- With `npx`, we won't have to use `npm install -g`. Example:
  ```bash
  npx create-react-app my-app
  ```
- `Array.prototype.includes` usage:
  ```js
  const filteredMonsters = this.state.monsters.filter((monster) =>
    monster.name.toLocaleLowerCase().includes(this.state.searchString)
  );
  ```
  If `this.state.searchString` equals to `''`, the `includes` still return `true`, so the content of `filteredMonsters` will be the same as `this.state.monsters`.
- The way of improving performance:
  ```js
  const { monsters, searchString } = this.state;
  const { onSearchChange } = this;
  ...
  ```
- When component has called `setState`, it call `render`; when seeing new `props` come in, `render` gets called as well.
