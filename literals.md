## Integer Literals

---

**Some of the integer literals are carry-overs from C. Some are unique to newer C++ standards:**

Prefix

* **Decimal \(base 10\): **12345
* **Octal \(base 8\):** 034532
* **Hex \(base 16\):** 0xDEADBEEF
* **Binary \(base 2\):** 0b1110010101101 

Suffix

* **Unsigned int:** u or U \(i.e. 0xDEADBEEFU or 12345u\)
* **Long int:** l or L \(i.e. 0xDEADBEEFL\)
* **Unsigned long int:** ul or UL
* **Long-Long int:** ll or LL 
* **Unsigned long-long int:** ull or ULL

---

## Floating Point Literals

---

**Digit-sequence: **whole number without a decimal separator, exponent is not optional.

> 1e10, 1e-5L ...

**Digit-sequence:  **representing a whole number with a decimal separator, in this case the exponent is optional.

> 1.e-1, 1.07 ...

**Digit-sequence:  **representing a fractional number. The exponent is optional.

> 3.14, .1f, 1.42e100 ...

**Hex-digit-sequence:**  representing a whole number without a radix separator. The exponent is never optional for hexadecimal floating-point literals

> 0x1ffp10, 0X1ffp-1 ...

**Hex-digit-sequence:**  representing a whole number with a radix separator. \(The exponent is never optional for hexadecimal floating-point literals.\)

> 0x0.12fp-1, 0x1p.10 ...

**Hex-digit-sequence:** representing a fractional number with a radix separator.

> 0x0.123-1, 0xa.bp10l ...

**Suffix:**

* e \| E:  The exponent syntax for a decimal floating-point literal.
* p \| P:  The exponent syntax for hexadecimal floating-point literal.
* \(no suffix\) defines **double**
* f \| F: defines **float**
* l \| L: defines **long double**

---

# Character Literals

---

**'c-char':** char

**u8'c-char':** UTF-8 char

**u'c-char':** UCS-2 character- char16\_t

**U'c-char':** UCS-4 character- char32\_t

**L'c-char':** wide-character- implementation-defined .

**'c-char-sequence':** Can be combined with the above pre-fixes.

---

# String Literals

---

**Mostly the same as character literals:**

* "unescaped or escape characters"
* L"unescaped or escaped characters"
* u8"unescaped or escaped characters"
* u"unescaped or escaped characters"
* U"unescaped or escaped characters"
* R"delimiter\(raw characters\) delimiter"

> ### //Raw String Examples
>
> ### auto str = R”foo\(“this is a raw string”/”I \(can\) use all kinds of ‘characters’”\)foo”;

---

# Escape Sequences

---

You have used some of these previously in C. Here is a more comprehensive list:

* \’ : single quote
* \” : double quote
* \? : question mark
* \ : backslash
* \a : audible bell
* \b : backspace
* \f : form feed
* \n : new line
* \r : carriage return
* \t : horizontal tab
* \v : vertical tab
* \nnn: arbitrary octal value
* \Xnn: arbitrary hex value
* \Unnn: universal character name

---

# New C++ nullptr

---

nullptr = a literal that represents a null pointer.

> void foo\(int a\)
>
> {
>
>      //do stuff with a
>
> }
>
>
>
> void foo\(char\* a\)
>
> {
>
>     //do stuff with a
>
> }
>
>
>
> int main\(\)
>
> {
>
>      foo\(0\);
>
>      foo\(NULL\);
>
>      foo\(nullptr\);
>
> }



