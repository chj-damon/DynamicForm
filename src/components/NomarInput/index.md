---
title: Input
---

# Input

## 代码演示

<code src="./demo/index.tsx" />

## API

|参数|说明|类型|默认值|是否必填|
|--|--|--|--|--|
|type|表单类型|string|''|是|
|title|标题|string|''|是|
|fieldProps|文本属性|boolean|false|是|
|placeholder|placeholder|string|''|否|
|required|必填判断|boolean|false|否|
|inputType|html input 框类型|string|text|否|
|clear|是否带清除功能|boolean|false|否|
|editable|是否可编辑|boolean|true|否|
|extra|右边注释|string or node|''|否|
|onClick|文字点击事件|function|null|否|

## 组件使用

### NomarInput

<code src="./demo/nomarInput.tsx" />

如需在 `DynamicForm` 中使用，请使用以下 `json`：

```json
{
  type: "input"
  fieldProps: "username",
  required: true,
  placeholder: "请输入",
  title: "用户名",
  inputType: "text",
  clear: true,
}
```

### ReadOnly

<code src="./demo/readOnly.tsx" />

如需在 `DynamicForm` 中使用，请使用以下 `json`：

```json
{
  type: "input",
  fieldProps: "userAge",
  placeholder: "这里只读不可编辑",
  title: "年龄",
  inputType: "text",
  editable: false,
},
```

### StringExtra

<code src="./demo/stringExtra.tsx" />

如需在 `DynamicForm` 中使用，请使用以下 `json`：

```json
{
  type: "input",
  fieldProps: "userClick",
  placeholder: "0.00",
  title: "价格",
  extra: "¥",
  inputType: "number",
  required: true,
}
```

### NodeExtraClick

<code src="./demo/nodeExtraClick.tsx" />

```json
{
  type: "input",
  fieldProps: "userPosition",
  placeholder: "请定位",
  required: true,
  title: "定位",
  extra: extraImg()
  inputType: "number",
}
```

### TextClick

<code src="./demo/textClick.tsx" />

```json
{
  type: "input",
  fieldProps: "userTitle",
  placeholder: "存在点击事件",
  required: true,
  title: "标题",
  editable: false,
  onClick: e => console.log(e)
}
```
