# LuaBrainFuck
BrainFuck interpreter in lua with new instructions... (New BrainFuck variant)

## Instructions :

## _Cells Navigation_

| Symbol  |  type  | name |
|-|-|-|
|  > |  pointer right | right |
|  < |  pointer left  | left |

## _Data Manipulation_

| Symbol | type  | name |
|-|-|-|
| + | cell add 1 |add|
| - | cell sub 1 |sub|

## _I / O (Input output)_

| Symbol | type  |name|
|---|------------|-|
| . | set output |out|
| , | get input  |in|
|#|input lenght|len|

### How The input works?
A input is a string that turns into a table,

In ASCII Mode The input is separated _char by char_

and in NON-ASCII Mode the inputs have to be separated by ","

### Examples:
|Mode          |input code              | how it is inserted in the cells |
|--------------|------------------------|---------------------------------|
|ASCII mode    |input = "djsanda"       |{100,106,115,097,110,100,097}    |
|Non-ASCII mode|input = "26, 18, 30, 18"|{26,18,30,18}                    |

__REMEMBER:__ THE OUTPUT WILL BE CHARACTERS IN ASCII MODE

## _Memory_ (HOT!)

| Symbol | type  |name|
|---|------------|-|
| : | set Memory |copy|
| ; | get Memory |paste|
| ^ | add from Memory |plus|
| ~ | sub from Memory |minus|

Example:

Getting the input and cloning it:
|Code|Input|Output|
|----|-----|------|
|, get input : copy input . print cell > next cell ; paste . print cell| 7 |7,7|
