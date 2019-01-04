# RAdvancedNotes
## Data Structures

 Dim | Homogeneous | Heterogeneous
--- | ------------ | -------------
1 | Atomic vector | List
2 | Matrix | Data frame
n | Array |

**注：R里面没有0维数据结构，`a=1`a也是一个只有一个元素的vector.**

### Vector
向量是最基本的R语言数据对象，有六种类型的原子向量。 它们是逻辑，整数，双精度，复杂，字符和原始。

```r
# Atomic vector of type character.
print("abc");

# Atomic vector of type double.
print(12.5)

# Atomic vector of type integer.
print(63L)

# Atomic vector of type logical.
print(TRUE)

# Atomic vector of type complex.
print(2+3i)

# Atomic vector of type raw.
print(charToRaw('hello'))

# With the L suffix, you get an integer rather than a double
int_var <- c(1L, 6L, 10L)

c(1, c(2, c(3, 4)))
```
#### Types and tests

Function: `is.character()`, `is.double()`, `is.integer()`, `is.logical()`, `is.atomic()`

- `is.numeric()`判断double和integer
- Coercion 
```r
str(c("a", 1))
```

### Lists
```r
x <- list(1:3, "a", c(TRUE, FALSE, TRUE), c(2.3, 5.9))
str(x)
```
List里面也可以包含List
```r
x <- list(list(list(list())))
str(x)
is.recursive(x)
```
`c()` will combine several lists into one. If given a combination of atomic vectors and lists, c() will coerce the vectors to lists before combining them.
```r
x <- list(list(1, 2), c(3, 4))
y <- c(list(1, 2), c(3, 4))
str(x)
str(y)
```






