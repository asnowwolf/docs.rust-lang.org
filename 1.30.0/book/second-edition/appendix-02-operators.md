## [Appendix B: Operators and Symbols](appendix-02-operators.html#appendix-b-operators-and-symbols)

This appendix contains a glossary of Rust’s syntax, including operators and
other symbols that appear by themselves or in the context of paths, generics,
trait bounds, macros, attributes, comments, tuples, and brackets.

### [Operators](appendix-02-operators.html#operators)

Table B-1 contains the operators in Rust, an example of how the operator would
appear in context, a short explanation, and whether that operator is
overloadable. If an operator is overloadable, the relevant trait to use to
overload that operator is listed.

<span class="caption">Table B-1: Operators</span>

<table>
<thead>
<tr>
<th> Operator </th>

<th> Example </th>

<th> Explanation </th>

<th> Overloadable? </th>
</tr>
</thead>

<tbody>
<tr>
<td> `!` </td>

<td> `ident!(...)`, `ident!{...}`, `ident![...]` </td>

<td> Macro expansion </td>

<td> </td>
</tr>

<tr>
<td> `!` </td>

<td> `!expr` </td>

<td> Bitwise or logical complement </td>

<td> `Not` </td>
</tr>

<tr>
<td> `!=` </td>

<td> `var != expr` </td>

<td> Nonequality comparison </td>

<td> `PartialEq` </td>
</tr>

<tr>
<td> `%` </td>

<td> `expr % expr` </td>

<td> Arithmetic remainder </td>

<td> `Rem` </td>
</tr>

<tr>
<td> `%=` </td>

<td> `var %= expr` </td>

<td> Arithmetic remainder and assignment </td>

<td> `RemAssign` </td>
</tr>

<tr>
<td> `&` </td>

<td> `&expr`, `&mut expr` </td>

<td> Borrow </td>

<td> </td>
</tr>

<tr>
<td> `&` </td>

<td> `&type`, `&mut type`, `&'a type`, `&'a mut type` </td>

<td> Borrowed pointer type </td>

<td> </td>
</tr>

<tr>
<td> `&` </td>

<td> `expr & expr` </td>

<td> Bitwise AND </td>

<td> `BitAnd` </td>
</tr>

<tr>
<td> `&=` </td>

<td> `var &= expr` </td>

<td> Bitwise AND and assignment </td>

<td> `BitAndAssign` </td>
</tr>

<tr>
<td> `&&` </td>

<td> `expr && expr` </td>

<td> Logical AND </td>

<td> </td>
</tr>

<tr>
<td> `*` </td>

<td> `expr * expr` </td>

<td> Arithmetic multiplication </td>

<td> `Mul` </td>
</tr>

<tr>
<td> `*=` </td>

<td> `var *= expr` </td>

<td> Arithmetic multiplication and assignment </td>

<td> `MulAssign` </td>
</tr>

<tr>
<td> `*` </td>

<td> `*expr` </td>

<td> Dereference </td>

<td> </td>
</tr>

<tr>
<td> `*` </td>

<td> `*const type`, `*mut type` </td>

<td> Raw pointer </td>

<td> </td>
</tr>

<tr>
<td> `+` </td>

<td> `trait + trait`, `'a + trait` </td>

<td> Compound type constraint </td>

<td> </td>
</tr>

<tr>
<td> `+` </td>

<td> `expr + expr` </td>

<td> Arithmetic addition </td>

<td> `Add` </td>
</tr>

<tr>
<td> `+=` </td>

<td> `var += expr` </td>

<td> Arithmetic addition and assignment </td>

<td> `AddAssign` </td>
</tr>

<tr>
<td> `,` </td>

<td> `expr, expr` </td>

<td> Argument and element separator </td>

<td> </td>
</tr>

<tr>
<td> `-` </td>

<td> `- expr` </td>

<td> Arithmetic negation </td>

<td> `Neg` </td>
</tr>

<tr>
<td> `-` </td>

<td> `expr - expr` </td>

<td> Arithmetic subtraction </td>

<td> `Sub` </td>
</tr>

<tr>
<td> `-=` </td>

<td> `var -= expr` </td>

<td> Arithmetic subtraction and assignment </td>

<td> `SubAssign` </td>
</tr>

<tr>
<td> `->` </td>

<td> `fn(...) -> type`, `|...| -> type` </td>

<td> Function and closure return type </td>

<td> </td>
</tr>

<tr>
<td> `.` </td>

<td> `expr.ident` </td>

<td> Member access </td>

<td> </td>
</tr>

<tr>
<td> `..` </td>

<td> `..`, `expr..`, `..expr`, `expr..expr` </td>

<td> Right-exclusive range literal </td>

<td> </td>
</tr>

<tr>
<td> `..` </td>

<td> `..expr` </td>

<td> Struct literal update syntax </td>

<td> </td>
</tr>

<tr>
<td> `..` </td>

<td> `variant(x, ..)`, `struct_type { x, .. }` </td>

<td> “And the rest” pattern binding </td>

<td> </td>
</tr>

<tr>
<td> `...` </td>

<td> `expr...expr` </td>

<td> In a pattern: inclusive range pattern </td>

<td> </td>
</tr>

<tr>
<td> `/` </td>

<td> `expr / expr` </td>

<td> Arithmetic division </td>

<td> `Div` </td>
</tr>

<tr>
<td> `/=` </td>

<td> `var /= expr` </td>

<td> Arithmetic division and assignment </td>

<td> `DivAssign` </td>
</tr>

<tr>
<td> `:` </td>

<td> `pat: type`, `ident: type` </td>

<td> Constraints </td>

<td> </td>
</tr>

<tr>
<td> `:` </td>

<td> `ident: expr` </td>

<td> Struct field initializer </td>

<td> </td>
</tr>

<tr>
<td> `:` </td>

<td> `'a: loop {...}` </td>

<td> Loop label </td>

<td> </td>
</tr>

<tr>
<td> `;` </td>

<td> `expr;` </td>

<td> Statement and item terminator </td>

<td> </td>
</tr>

<tr>
<td> `;` </td>

<td> `[...; len]` </td>

<td> Part of fixed-size array syntax </td>

<td> </td>
</tr>

<tr>
<td> `<<` </td>

<td> `expr << expr` </td>

<td> Left-shift </td>

<td> `Shl` </td>
</tr>

<tr>
<td> `<<=` </td>

<td> `var <<= expr` </td>

<td> Left-shift and assignment </td>

<td> `ShlAssign` </td>
</tr>

<tr>
<td> `<` </td>

<td> `expr < expr` </td>

<td> Less than comparison </td>

<td> `PartialOrd` </td>
</tr>

<tr>
<td> `<=` </td>

<td> `expr <= expr` </td>

<td> Less than or equal to comparison </td>

<td> `PartialOrd` </td>
</tr>

<tr>
<td> `=` </td>

<td> `var = expr`, `ident = type` </td>

<td> Assignment/equivalence </td>

<td> </td>
</tr>

<tr>
<td> `==` </td>

<td> `expr == expr` </td>

<td> Equality comparison </td>

<td> `PartialEq` </td>
</tr>

<tr>
<td> `=>` </td>

<td> `pat => expr` </td>

<td> Part of match arm syntax </td>

<td> </td>
</tr>

<tr>
<td> `>` </td>

<td> `expr > expr` </td>

<td> Greater than comparison </td>

<td> `PartialOrd` </td>
</tr>

<tr>
<td> `>=` </td>

<td> `expr >= expr` </td>

<td> Greater than or equal to comparison </td>

<td> `PartialOrd` </td>
</tr>

<tr>
<td> `>>` </td>

<td> `expr >> expr` </td>

<td> Right-shift </td>

<td> `Shr` </td>
</tr>

<tr>
<td> `>>=` </td>

<td> `var >>= expr` </td>

<td> Right-shift and assignment </td>

<td> `ShrAssign` </td>
</tr>

<tr>
<td> `@` </td>

<td> `ident @ pat` </td>

<td> Pattern binding </td>

<td> </td>
</tr>

<tr>
<td> `^` </td>

<td> `expr ^ expr` </td>

<td> Bitwise exclusive OR </td>

<td> `BitXor` </td>
</tr>

<tr>
<td> `^=` </td>

<td> `var ^= expr` </td>

<td> Bitwise exclusive OR and assignment </td>

<td> `BitXorAssign` </td>
</tr>

<tr>
<td> `|` </td>

<td> `pat | pat` </td>

<td> Pattern alternatives </td>

<td> </td>
</tr>

<tr>
<td> `|` </td>

<td> `expr | expr` </td>

<td> Bitwise OR </td>

<td> `BitOr` </td>
</tr>

<tr>
<td> `|=` </td>

<td> `var |= expr` </td>

<td> Bitwise OR and assignment </td>

<td> `BitOrAssign` </td>
</tr>

<tr>
<td> `||` </td>

<td> `expr || expr` </td>

<td> Logical OR </td>

<td> </td>
</tr>

<tr>
<td> `?` </td>

<td> `expr?` </td>

<td> Error propagation </td>

<td> </td>
</tr>
</tbody>
</table>

### [Non-operator Symbols](appendix-02-operators.html#non-operator-symbols)

The following list contains all non-letters that don’t function as operators;
that is, they don’t behave like a function or method call.

Table B-2 shows symbols that appear on their own and are valid in a variety of
locations.

<span class="caption">Table B-2: Stand-Alone Syntax</span>

<table>
<thead>
<tr>
<th> Symbol </th>

<th> Explanation </th>
</tr>
</thead>

<tbody>
<tr>
<td> `'ident` </td>

<td> Named lifetime or loop label </td>
</tr>

<tr>
<td> `...u8`, `...i32`, `...f64`, `...usize`, etc. </td>

<td> Numeric literal of specific type </td>
</tr>

<tr>
<td> `"..."` </td>

<td> String literal </td>
</tr>

<tr>
<td> `r"..."`, `r#"..."#`, `r##"..."##`, etc. </td>

<td> Raw string literal, escape characters not processed </td>
</tr>

<tr>
<td> `b"..."` </td>

<td> Byte string literal; constructs a `[u8]` instead of a string </td>
</tr>

<tr>
<td> `br"..."`, `br#"..."#`, `br##"..."##`, etc. </td>

<td> Raw byte string literal, combination of raw and byte string literal </td>
</tr>

<tr>
<td> `'...'` </td>

<td> Character literal </td>
</tr>

<tr>
<td> `b'...'` </td>

<td> ASCII byte literal </td>
</tr>

<tr>
<td> `|...| expr` </td>

<td> Closure </td>
</tr>

<tr>
<td> `!` </td>

<td> Always empty bottom type for diverging functions </td>
</tr>

<tr>
<td> `_` </td>

<td> “Ignored” pattern binding; also used to make integer literals readable </td>
</tr>
</tbody>
</table>

Table B-3 shows symbols that appear in the context of a path through the module
hierarchy to an item.

<span class="caption">Table B-3: Path-Related Syntax</span>

<table>
<thead>
<tr>
<th> Symbol </th>

<th> Explanation </th>
</tr>
</thead>

<tbody>
<tr>
<td> `ident::ident` </td>

<td> Namespace path </td>
</tr>

<tr>
<td> `::path` </td>

<td> Path relative to the crate root (i.e., an explicitly absolute path) </td>
</tr>

<tr>
<td> `self::path` </td>

<td> Path relative to the current module (i.e., an explicitly relative path).</td>
</tr>

<tr>
<td> `super::path` </td>

<td> Path relative to the parent of the current module </td>
</tr>

<tr>
<td> `type::ident`, `<type as trait>::ident` </td>

<td> Associated constants, functions, and types </td>
</tr>

<tr>
<td> `<type>::...` </td>

<td> Associated item for a type that cannot be directly named (e.g., `<&T>::...`, `<[T]>::...`, etc.) </td>
</tr>

<tr>
<td> `trait::method(...)` </td>

<td> Disambiguating a method call by naming the trait that defines it </td>
</tr>

<tr>
<td> `type::method(...)` </td>

<td> Disambiguating a method call by naming the type for which it’s defined </td>
</tr>

<tr>
<td> `<type as trait>::method(...)` </td>

<td> Disambiguating a method call by naming the trait and type </td>
</tr>
</tbody>
</table>

Table B-4 shows symbols that appear in the context of using generic type
parameters.

<span class="caption">Table B-4: Generics</span>

<table>
<thead>
<tr>
<th> Symbol </th>

<th> Explanation </th>
</tr>
</thead>

<tbody>
<tr>
<td> `path<...>` </td>

<td> Specifies parameters to generic type in a type (e.g., `Vec<u8>`) </td>
</tr>

<tr>
<td> `path::<...>`, `method::<...>` </td>

<td> Specifies parameters to generic type, function, or method in an expression; often referred to as turbofish (e.g., `"42".parse::<i32>()`) </td>
</tr>

<tr>
<td> `fn ident<...> ...` </td>

<td> Define generic function </td>
</tr>

<tr>
<td> `struct ident<...> ...` </td>

<td> Define generic structure </td>
</tr>

<tr>
<td> `enum ident<...> ...` </td>

<td> Define generic enumeration </td>
</tr>

<tr>
<td> `impl<...> ...` </td>

<td> Define generic implementation </td>
</tr>

<tr>
<td> `for<...> type` </td>

<td> Higher-ranked lifetime bounds </td>
</tr>

<tr>
<td> `type<ident=type>` </td>

<td> A generic type where one or more associated types have specific assignments (e.g., `Iterator<Item=T>`) </td>
</tr>
</tbody>
</table>

Table B-5 shows symbols that appear in the context of constraining generic type
parameters with trait bounds.

<span class="caption">Table B-5: Trait Bound Constraints</span>

<table>
<thead>
<tr>
<th> Symbol </th>

<th> Explanation </th>
</tr>
</thead>

<tbody>
<tr>
<td> `T: U` </td>

<td> Generic parameter `T` constrained to types that implement `U` </td>
</tr>

<tr>
<td> `T: 'a` </td>

<td> Generic type `T` must outlive lifetime `'a` (meaning the type cannot transitively contain any references with lifetimes shorter than `'a`) </td>
</tr>

<tr>
<td> `T : 'static` </td>

<td> Generic type `T` contains no borrowed references other than `'static` ones </td>
</tr>

<tr>
<td> `'b: 'a` </td>

<td> Generic lifetime `'b` must outlive lifetime `'a` </td>
</tr>

<tr>
<td> `T: ?Sized` </td>

<td> Allow generic type parameter to be a dynamically sized type </td>
</tr>

<tr>
<td> `'a + trait`, `trait + trait` </td>

<td> Compound type constraint </td>
</tr>
</tbody>
</table>

Table B-6 shows symbols that appear in the context of calling or defining
macros and specifying attributes on an item.

<span class="caption">Table B-6: Macros and Attributes</span>

<table>
<thead>
<tr>
<th> Symbol </th>

<th> Explanation </th>
</tr>
</thead>

<tbody>
<tr>
<td> `#[meta]` </td>

<td> Outer attribute </td>
</tr>

<tr>
<td> `#![meta]` </td>

<td> Inner attribute </td>
</tr>

<tr>
<td> `$ident` </td>

<td> Macro substitution </td>
</tr>

<tr>
<td> `$ident:kind` </td>

<td> Macro capture </td>
</tr>

<tr>
<td> `$(…)…` </td>

<td> Macro repetition </td>
</tr>
</tbody>
</table>

Table B-7 shows symbols that create comments.

<span class="caption">Table B-7: Comments</span>

<table>
<thead>
<tr>
<th> Symbol </th>

<th> Explanation </th>
</tr>
</thead>

<tbody>
<tr>
<td> `//` </td>

<td> Line comment </td>
</tr>

<tr>
<td> `//!` </td>

<td> Inner line doc comment </td>
</tr>

<tr>
<td> `///` </td>

<td> Outer line doc comment </td>
</tr>

<tr>
<td> `/*...*/` </td>

<td> Block comment </td>
</tr>

<tr>
<td> `/*!...*/` </td>

<td> Inner block doc comment </td>
</tr>

<tr>
<td> `/**...*/` </td>

<td> Outer block doc comment </td>
</tr>
</tbody>
</table>

Table B-8 shows symbols that appear in the context of using tuples.

<span class="caption">Table B-8: Tuples</span>

<table>
<thead>
<tr>
<th> Symbol </th>

<th> Explanation </th>
</tr>
</thead>

<tbody>
<tr>
<td> `()` </td>

<td> Empty tuple (aka unit), both literal and type </td>
</tr>

<tr>
<td> `(expr)` </td>

<td> Parenthesized expression </td>
</tr>

<tr>
<td> `(expr,)` </td>

<td> Single-element tuple expression </td>
</tr>

<tr>
<td> `(type,)` </td>

<td> Single-element tuple type </td>
</tr>

<tr>
<td> `(expr, ...)` </td>

<td> Tuple expression </td>
</tr>

<tr>
<td> `(type, ...)` </td>

<td> Tuple type </td>
</tr>

<tr>
<td> `expr(expr, ...)` </td>

<td> Function call expression; also used to initialize tuple `struct`s and tuple `enum` variants </td>
</tr>

<tr>
<td> `ident!(...)`, `ident!{...}`, `ident![...]` </td>

<td> Macro invocation </td>
</tr>

<tr>
<td> `expr.0`, `expr.1`, etc. </td>

<td> Tuple indexing </td>
</tr>
</tbody>
</table>

Table B-9 shows the contexts in which curly braces are used.

<span class="caption">Table B-9: Curly Brackets</span>

<table>
<thead>
<tr>
<th> Context </th>

<th> Explanation </th>
</tr>
</thead>

<tbody>
<tr>
<td> `{...}` </td>

<td> Block expression </td>
</tr>

<tr>
<td> `Type {...}` </td>

<td> `struct` literal </td>
</tr>
</tbody>
</table>

Table B-10 shows the contexts in which square brackets are used.

<span class="caption">Table B-10: Square Brackets</span>

<table>
<thead>
<tr>
<th> Context </th>

<th> Explanation </th>
</tr>
</thead>

<tbody>
<tr>
<td> `[...]` </td>

<td> Array literal </td>
</tr>

<tr>
<td> `[expr; len]` </td>

<td> Array literal containing `len` copies of `expr` </td>
</tr>

<tr>
<td> `[type; len]` </td>

<td> Array type containing `len` instances of `type` </td>
</tr>

<tr>
<td> `expr[expr]` </td>

<td> Collection indexing. Overloadable (`Index`, `IndexMut`) </td>
</tr>

<tr>
<td> `expr[..]`, `expr[a..]`, `expr[..b]`, `expr[a..b]` </td>

<td> Collection indexing pretending to be collection slicing, using `Range`, `RangeFrom`, `RangeTo`, or `RangeFull` as the “index” </td>
</tr>
</tbody>
</table>
