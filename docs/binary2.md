---
layout: default
title:  Operators in Binary
nav_order: 2
---

# Mathematical Operators in Binary


## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Addition

```yaml 
1. 0 + 0 = 0
2. 0 + 1 = 1
3. 1 + 0 = 1
4. 1 + 1 = 1
```

## Subtraction

```yaml
1. 0 - 0 = 0
2. 1 - 0 = 1
3. 1 - 1 = 0
```

## Multiplication

```yaml
          1  1  0       (6)
      *   1  0  1       (5)
      ------------
          1  1  0 
       0  0  0  x
    1  1  0  x  x
    --------------
    1  1  1  1  0       (30)
    --------------   
```

## Division

```yaml
          1 1 1 1 0 / 1 0 1
         -    1 0 1                     1st 
        -------------
          1 1 0 0 1
         -    1 0 1                     2nd
        -------------
          1 0 1 0 0
         -    1 0 1                     3rd
        -------------
          0 1 1 1 1
         -    1 0 1                     4th
        -------------
            1 0 1 0
         -    1 0 1                     5th
        -------------
              1 0 1
         -    1 0 1                     6th 
        -------------                 -------
                  0                   ans = 6 (110)
        -------------                 -------
```

## Binary system complements

As the binary system has base r = 2. So the two types of complements for the binary system are 2's complement and 1's complement.


### 1's complement

The 1's complement of a number is found by changing all 1's to 0's and all 0's to 1's. This is called as taking complement or 1's complement. Example of 1's Complement is as follows.

```yaml
Given number        1  0  1  0  1
1's complement      0  1  0  1  0 
```
### 2's complement

The 2's complement of binary number is obtained by adding 1 to the Least Significant Bit (LSB) of 1's complement of the number.
2's complement = 1's complement + 1


```yaml
Given number        1  0  1  0  1
1's complement      0  1  0  1  0 

add 1               +           1
                   ---------------
2's complement      0  1  0  1  1             
                   --------------- 

```


# Bitwise Operators

|Operator   |    Explanation   |
|:---------:|:----------------:|
|op1 & op2 | The AND operator compares two bits and generates a result of 1 if both bits are 1; otherwise, it returns 0.|
|op1 or op2 | The OR operator compares two bits and generates a result of 1 if the bits are complementary; otherwise, it returns 0.|
|op1^ op2 | The EXCLUSIVE-OR operator compares two bits and returns 1 if either of the bits are 1 and it gives 0 if both bits are 0 or 1.|
|~op1 | The COMPLEMENT operator is used to invert all of the bits of the operand.|

<div id="container">
<div class="binary">
<div class="column"><div class="column_heading">128</div><div id="7" class="bit" onClick="toggle_bit(7);">0</div></div>
<div class="column"><div class="column_heading">64</div><div id="6" class="bit" onClick="toggle_bit(6);">0</div></div>
<div class="column"><div class="column_heading">32</div><div id="5" class="bit" onClick="toggle_bit(5);">0</div></div>
<div class="column"><div class="column_heading">16</div><div id="4" class="bit" onClick="toggle_bit(4);">0</div></div>
<div class="column"><div class="column_heading">8</div><div id="3" class="bit" onClick="toggle_bit(3);">0</div></div>
<div class="column"><div class="column_heading">4</div><div id="2" class="bit" onClick="toggle_bit(2);">0</div></div>
<div class="column"><div class="column_heading">2</div><div id="1" class="bit" onClick="toggle_bit(1);">0</div></div>
<div class="column"><div class="column_heading">1</div><div id="0" class="bit" onClick="toggle_bit(0);">0</div></div>
<div class="decimal">= <input type="text" id="value_A" onInput="set_bits();" size="3" maxlength="3"></div>
</div><br style="clear: left">
<div id="operators"><select id="operator" onChange="change_operator();">
  <option value="AND">AND</option>
  <option value="OR"> OR</option>
  <option value="XOR">XOR</option>
</select>
<div class="opcol">AND</div>
<div class="opcol">AND</div>
<div class="opcol">AND</div>
<div class="opcol">AND</div>
<div class="opcol">AND</div>
<div class="opcol">AND</div>
<div class="opcol">AND</div>
<div class="opcol">AND</div>
</div><input type="button" value="Calculate" onClick="set_bits();" class="ok" style="margin-top: 22px"><br style="clear: left">
<div class="binary">
<div class="column"><div class="column_heading">128</div><div id="15" class="bit" onClick="toggle_bit(15);">0</div></div>
<div class="column"><div class="column_heading">64</div><div id="14" class="bit" onClick="toggle_bit(14);">0</div></div>
<div class="column"><div class="column_heading">32</div><div id="13" class="bit" onClick="toggle_bit(13);">0</div></div>
<div class="column"><div class="column_heading">16</div><div id="12" class="bit" onClick="toggle_bit(12);">0</div></div>
<div class="column"><div class="column_heading">8</div><div id="11" class="bit" onClick="toggle_bit(11);">0</div></div>
<div class="column"><div class="column_heading">4</div><div id="10" class="bit" onClick="toggle_bit(10);">0</div></div>
<div class="column"><div class="column_heading">2</div><div id="9" class="bit" onClick="toggle_bit(9);">0</div></div>
<div class="column"><div class="column_heading">1</div><div id="8" class="bit" onClick="toggle_bit(8);">0</div></div>
<div class="decimal">= <input type="text" id="value_B" onInput="set_bits();" size="3" maxlength="3"></div>
</div><br style="clear: left">
<div class="binary">
<div class="opeq">=</div>
<div class="opeq">=</div>
<div class="opeq">=</div>
<div class="opeq">=</div>
<div class="opeq">=</div>
<div class="opeq">=</div>
<div class="opeq">=</div>
<div class="opeq">=</div>
</div><br style="clear: left">
<div class="binary">
<div class="column"><div class="column_heading">128</div><div id="23" class="bit">0</div></div>
<div class="column"><div class="column_heading">64</div><div id="22" class="bit">0</div></div>
<div class="column"><div class="column_heading">32</div><div id="21" class="bit">0</div></div>
<div class="column"><div class="column_heading">16</div><div id="20" class="bit">0</div></div>
<div class="column"><div class="column_heading">8</div><div id="19" class="bit">0</div></div>
<div class="column"><div class="column_heading">4</div><div id="18" class="bit">0</div></div>
<div class="column"><div class="column_heading">2</div><div id="17" class="bit">0</div></div>
<div class="column"><div class="column_heading">1</div><div id="16" class="bit">0</div></div>
<div id="result">= 0</div>
</div>
</div>




<style>
#binary			{width: 100%;}
#decimal		{font-family: Arial, Helvetica, sans-serif; float: left; font-size: 5vw; width: 21vw; margin: 2.7vw 0 0 2vw; float: left}
.column_heading	{font-size: 1.6vw; color: #666666}
.binary			{width: 620px; margin: auto}
#container		{width: 560px; display: block; margin: auto; margin-bottom :30px}
#too_big		{display: none; font-style: italic; clear: left}
#operators		{width: 680px; margin: auto; margin-left: -20%}
.decimal		{font-size: 48px; width: 160px; font-size:48px; margin: 25px 0 0 10px; float:left}
#result			{font-size: 48px; width: 160px; margin: 25px 0 0 10px; float:left}
.column			{font-family: Arial, Helvetica, sans-serif; float: left; text-align: center; width: 54px}
.opcol			{float: left; text-align: center; width: 54px; height: 45px; padding-top: 20px; vertical-align:middle; -webkit-transform: rotate(90deg); -moz-transform: rotate(90deg); -o-transform:rotate(90deg); -ms-transform:rotate(90deg)}
.opeq			{float: left; text-align: center; padding-bottom: 10px; width: 54px; height: 30px; font-size: 38px; -webkit-transform: rotate(90deg); -moz-transform: rotate(90deg); -o-transform:rotate(90deg); -ms-transform:rotate(90deg)}
.bit			{font-size: 64px; background-color: #FFFFFF; color:#000000; border-radius: 7px; margin: 2px; border: 1px solid black}
#operator		{display: inline;  background: transparent; border: 0; font-size: 37px; width: 120px; margin: auto; float: left; margin-top: 11px}
#value_A, #value_B	{font-size: 32px; width: 58px; vertical-align: top; padding-top: 0px; margin-top: 6px}
@media screen and (max-width: 720px) {
	#container	{display: none}
	#too_big	{display: block}
}
</style>