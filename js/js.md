#### 1.关于 typeof null 的结果是 object，而不是 null 的问题

在 JavaScript 中，`null` 是一个特殊的值，它属于基本数据类型（也称为原始数据类型或原始类型）。基本数据类型是 JavaScript 中的内置类型，它们代表简单的数据而不是对象。除了 `null`，基本数据类型还包括：

- `Boolean`：表示逻辑实体，其值是 `true` 或 `false`。
- `Number`：表示数值，可以是整数或浮点数。
- `String`：表示文本数据，由一系列字符组成。
- `Symbol`（ES6 新增）：表示一个唯一的、不可变的数据类型。
- `undefined`：表示变量已声明但尚未初始化。

`null` 用于表示一个空或缺失的值，它是一个没有任何对象的引用。在 JavaScript 的类型系统中，`null` 虽然在概念上与对象相似（因为它表示一个空指针），但它本身并不是一个对象。因此，`null` 不是引用类型。

在 JavaScript 的 `typeof` 操作符中，除了 `null` 和 `undefined`，其他基本数据类型都能够被正确地识别为它们各自的类型字符串：

```javascript
typeof true; // "boolean"
typeof 123; // "number"
typeof "text"; // "string"
typeof Symbol(); // "symbol"
typeof null; // "object" (这是一个历史遗留的特殊行为，如前所述)
typeof undefined; // "undefined"
```

尽管 `typeof null` 返回 `"object"` 是一个历史遗留的行为，但在语言的类型系统中，`null` 被分类为基本数据类型。在编写代码时，应该将 `null` 视为一个用来表示空值的特殊值，而不是一个对象。
