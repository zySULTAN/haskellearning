# zySULTAN Haskell Operators

|Operator     |Type                                          |Notes|
|:-----------:|----------------------------------------------|-----|
| `&&` `\|\|` | `Bool -> Bool -> Bool`                       | AND, OR |
| `== /= `    | `Eq a => a -> a -> Bool`                     | Value equality. |
| `< > <= >=` | `Ord a => a -> a -> Bool`                    | Greater than, Lesser than | 
| `+ - * `    | `Num a => a -> a -> a`                       | Math operations |
| unary `-`   | `Num a => a -> a`                            | Same as `negate` |
| `/`         | `Fractional a => a -> a -> a`                | For integer division use `div` |
| ` ** `      | `Floating a => a -> a -> a`                  | Floating power operation, anti-log |
| `^ `        | `(Num a, Integral b) => a -> b -> a`         | Integral power of a Num |
| `^^`        | `(Fractional a, Integral b) => a -> b -> a`  | Integral power of a Fractional |
| `<>`        | `Semigroup a => a -> a -> a`                 | Semigroup combine |
| `<$>`       | `Functor f => (a -> b) -> f a -> f b`        | Operator for fmap: `f <$> x = fmap f x` |
| ` <$ `      | `Functor f => a -> f b -> f a`               | Shorthand to do a simple replacement with fmap |
| ` <*>`      | `Applicative f => f (a -> b) -> f a -> f b`  | Applicative function application (ap) |
| ` <* `      | `Applicative f => f a -> f b -> f a`         | See `<$` and `>>` |
| ` *> `      | `Applicative f => f a -> f b -> f b`         | See `<$` and `>>` |
| ` >>= `     | `Monad m => m a -> (a -> m b) -> m b`        | Monad bind |
| `>>`        | `Monad m => m a -> m b -> m b`               | Shorthand to discard result of first action |
| `=<<`       | `Monad m => (a -> m b) -> m a -> m b`        | "Monad function application"<br>`(=<<) = flip (>>=)` |
| `.`         | `(b -> c) -> (a -> b) -> a -> c`             | Function composition |
| `$ $!`      | `(a -> b) -> a -> b`                         | Function application operator.<br>`$!` will evaluate the argument first (to WHNF). |
| `++`        | `[a] -> [a] -> [a]`                          | List concatenation |
| `!!`        | `[a] -> Int -> a`                            | Get an element out of a list |

| Function    | Type                                       | Notes |
|:-----------:|--------------------------------------------|-------|
| `lines`     | `String -> [String]`                       | Splits a string into a list of lines (strings), separating at newline characters (`\n`). |
| `unlines`   | `[String] -> String`                       | Joins a list of strings into a single string, adding newline characters between each. |
| `words`     | `String -> [String]`                       | Splits a string into a list of words, using spaces as separators. |
| `unwords`   | `[String] -> String`                       | Joins a list of words into a single string, with spaces in between. |
| `map`       | `(a -> b) -> [a] -> [b]`                   | Applies a function to every element of a list, transforming it. |
| `filter`    | `(a -> Bool) -> [a] -> [a]`                | Filters a list, keeping only elements that satisfy a condition. |
| `foldl`     | `(b -> a -> b) -> b -> [a] -> b`           | Reduces a list from the left using a binary function. |
| `foldr`     | `(a -> b -> b) -> b -> [a] -> b`           | Reduces a list from the right using a binary function. |
| `show`      | `Show a => a -> String`                    | Converts a value into its string representation. |
| `read`      | `Read a => String -> a`                    | Parses a string into a value of type `a`. |
| `interact`  | `(String -> String) -> IO ()`              | Reads input, transforms it using a function, and outputs the result. |
| `take`      | `Int -> [a] -> [a]`                        | Takes the first `n` elements of a list. |
| `drop`      | `Int -> [a] -> [a]`                        | Drops the first `n` elements of a list. |
| `head`      | `[a] -> a`                                 | Returns the first element of a list. |
| `tail`      | `[a] -> [a]`                               | Returns a list without its first element. |
| `length`    | `[a] -> Int`                               | Returns the length of a list. |
| `reverse`   | `[a] -> [a]`                               | Reverses the elements of a list. |
| `zip`       | `[a] -> [b] -> [(a, b)]`                   | Combines two lists into a list of pairs. |
| `concat`    | `[[a]] -> [a]`                             | Concatenates a list of lists into a single list. |
