在前面的例子中，我们使用组合算子显式地处理错误。 另一种处理这种情形分解的方法是使用 `match` 语句和**提前返回**（*early returns*）的组合形式。

也就是说，我们可以简单地停止执行函数并返回错误（若发生的话）。 而且这种形式的代码更容易阅读和编写。考虑如下版本，这是将之前的例子使用提前返回方式重写的：

{early_returns.play}

现在我们已经学会了使用组合算子和提前返回来显式地处理错误。虽然我们通常希望避免 `panic`，但显式处理我们所有的错误将会麻烦。

在下一节，我们将介绍 `try!`，用在这样的场景，我们只需要简单地 `unwrap` 而避免可能的 `panic`。