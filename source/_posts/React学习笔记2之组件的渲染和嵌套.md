---
title: React学习笔记之组件的渲染和嵌套
date: 2017-11-24 15:40:40
tags:
---
# 组件的渲染和嵌套

## 1.组件定义的两种方式

* 函数定义组件

``` jsx
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```

* 类定义组件（使用ES6的class语法）

```jsx
class Welcome extends React.component {
  render() {
    return <h1>Hello, {props.name}</h1>;
  }
}
```

**tips:**&ensp;**组件名称必须以大写字母开头.&ensp;例如：**

```html

const element = <div />;
```

div只是DOM标签,而不是组件

```html

const element = <Welcome name="Sara">
```

Welcome才是组件,而且是用户自定义的组件

## 2.组建的渲染

*当React遇到的元素是用户自定义的组件，它会将JSX属性作为单个对象传递给该组件,这个对象称之为“props”。<br>例如,这段代码会在页面上渲染出”Hello,Sara”:

```jsx
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>
}

const element = <Welcome name="Sara" />;

ReactDOM.render(
  element,
  document.getElementById('root');
);
```

## 3.组建的嵌套

* 一个组件的可以渲染其他组件<br>例如：创建一个组件来多次渲染Welcome组件

```jsx
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>
}

function App() {
  <div>
    <Welcome name="Sara" />
    <Welcome name="Peter" />
    <Welcome name="Lisa" />
  </div>
}

ReactDOM.render(
  <App />,
  document.getElementById('root')
);
```

* 错误的写法

```jsx
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>
}
const element(
  <div>
    <Welcome name="Sara" />
    <Welcome name="Peter" />
    <Welcome name="Lisa" />
  </div>
);

ReactDOM.render(
  element,
  document.getElementById('root')
);
```

**总结：**&ensp;虽然两段代码运行的结果是一样的,但下面的代码并不是两个组建的嵌套,只是将Welcome组件渲染了三次,不涉及另一个组件;而正确的代码中Welcome组件是嵌套在App组件中渲染了三次.




