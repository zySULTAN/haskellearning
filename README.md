# "zySULTAN Haskell Operators"

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
