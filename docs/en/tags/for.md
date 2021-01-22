Tag {for}
=========

```smarty
{for $counter=<start> to=<end> [step=<step>] [index=$index] [first=$first] [last=$last]}
   {* ...code... *}
   {break}
   {* ...code... *}
   {continue}
   {* ...code... *}
{forelse}
   {* ...code... *}
{/for}
```

### {for}
   
The $counter variable takes on a value equal to <start> and increases its value by <step> at each iteration of the loop until it reaches or becomes greater then <end>. <step> is an optional argument. If not specified, it is considered equal to one. $index has the value of the current iteration number. The first iteration is numbered 0. 
$first is TRUE if iteration is the first. 
$last is TRUE if the iteration is last.

Fields <start>, <end>, <step> can be numbers, or variables whose value is converted to numeric. The value of the index, first, last parameters can only be a variable (nesting like $a.b.c is allowed, but the $a.b array must be declared).

### {break}

The `{break}` tag is used to break out of the loop before reaching the last iteration. If the {break} tag is encountered in the loop, the loop ends its work, and then the code immediately following the loop block is executed


### {continue}

The `{continue}` tag is used to interrupt the current iteration. If the {continue} tag is encountered in the loop, the part of the loop following the tag is not executed and the next iteration begins. If the current iteration was the last, the loop ends.


### {forelse}

Тег {forelse} ограничивает код, который должен быть выполнен, если сочетание полей , и не обеспечивают ни одной итерации.
