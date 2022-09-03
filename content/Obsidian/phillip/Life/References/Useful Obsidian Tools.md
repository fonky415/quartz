# Useful Obsidian Tools/Formatting 
Tags: #Reference

There are just so many commands that are useful but hard to memorize, so here is a compilation of tools for me to reference and build along the way. 

## Formatting 
**Indents** 
Indents can only be seen in editing mode, not preview mode. This can be solved by adding `&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` infront of the text, adding 6 invisible spaces infront of the text. 

**Line skip**
Markdown mode ignores all spaces for some reason, so you can use `<br>` to skip lines. It disappears in reading mode. 

**Bigger latex** 
Using `\large` infront of Latex makes it bigger. Here's the comparison. $\large This is the latex with the command.$ $This is without it.$

**Horizontal space**
In Latex, adding space doesn't actually make the space. Using `\space`  solves that. 

**Skipping lines** 
To skip lines in Latex, the normal thing doesn't work for some reason. This is a workaround: ``$$ \begin{aligned} TEXT &= \text{TEXT} \\ MORE TEXT &= \text{MORE TEXT} \\ EVENMORETEXT&= \text{TEXT} \end{aligned} $$.`` Looks like this: $$\begin{aligned} P(S)=\frac{1}{9} \\ P(U)=\frac{1}{8} \\ P(R)=\frac{2}{9} \end{aligned}$$
**Skipping lines + aligning things**
If you want to write several equations together then you can use the `eqnarray` environment. At the end of each equation, you start a new line using `\\` as usual. The `eqnarray`environment lets you align equations so that, for example, all of the equals signs "=" line up. To do this, put ampersand "&" signs around the text you want LaTeX to align, e.g.
```
\begin{eqnarray} 
F &=& ma\\   
V &=& IR 
\end{eqnarray}
```

**Large space in LaTex**
To insert a large space in LaTex, similar to an indent, you can use `\quad` or `\qquad` for an even larger space. It looks like this: $$Hi.\quad Hello.\qquad How\space are\space you?$$

**Subscripts** 
To write in subscript, put the text inside the curly brackets after an underscore. Replace the n for the subscript. You don't need the A in the beginning. ``$A_{n}$`` $\rightarrow$ $A_{n}$

**Image size** 
After an image, add the "|" sign and either write *xlength*x*ylength* or just one of the dimensions if you want the ratio to be the same. Here's an example: ![[Pasted image 20220517060733.png|90]]
![[Pasted image 20220517060743.png|150]]
![[Pasted image 20220517060750.png|700x100]]

### Centering image 
To center an image, place `<span class='centerImg'> ![[image file]] </span>` around the file. Doesn’t support Live Preview yet, but you should be able to see it in Reading mode. Here is example: 

<span class='centerImg'> ![[Pasted image 20220517060733.png|400]] </span>

### Centering text 
Placing `<center>[text here]</center>` around text will put it in the center. Useful for captions.

### Hyperlinks within HTML 
Template: `<a href="Link here">text here</a>`. Keep the quotation marks around the URL.

## Symbols 
**Intersection/and** 
This: $\large \cap$ symbol means "intersection" or "and." In probability, this symbolizes the chances of two events happening at the same time. It looks like a cap, so you do `\cap`.

**Union/or** 
This: $\large \cup$ symbol means "union" or "or." 

**Horizontal bar**
When writing reoccuring decmilas, you put the horizontal bar above the digits that repeat. In Latex, we use `\overline{#}` and put the digits inside the braces. Like this: $6.\overline{96}$

**Big parentheses** 
When writing fractions, for example, and you want the parentheses to be big, you use `\left(` for the left parentheses and `\right)` for the right. This would look something like this: $$(\frac{2}{3})=\left(\frac{6}{4}\right)$$
**Percent symbol** 
Just putting % in Latex doesn't work, so you must proceed it with a backslash like this: `\%` to actually write it. 

**Multiplication Dot** 
Called the interpunct, it's the dot when you multiply things. At least that's one way to do it. Use this dot by typing `\cdot`. ex. $4*4=4 \cdot 4$ 

**Triple dots** 
Do `\cdots` to write $\cdots$ 

**Multiplication Sign**
To type x, just do `\times`. ex. $4 \times 4 = 16$

**Caret on top of something** 
To put the caret symbol (^) on top of something, use `\hat{}`. ex. $\hat{1}$

**Theta** 
In LaTex, `\theta` works, but in normal text, just copy and paste this: 𝞱. 

**Plus or minus sign** 
Use `\pm` to achieve this. ex. $\sqrt{9}=\pm3$

**Pi copy and paste**
𝝅. 

**arrows**
![[Pasted image 20220528180209.png|700]]

**greater than or equal to and less than or equal to**
Greater than or equal to: `\geq`. ex. $y\geq 4$ 
Less than or equal to: `\leq`. ex. $y\leq 4$

**degree symbol copy and paste**
° ex. 20°

## Other 

### Annotator plugin 
Add the property `annotation-target` to the frontmatter of your obsidian note, with a value corresponding to the location of the EPUB/PDF file. The location can either be a file in the vault (such as `Pdfs/mypdf.pdf`), or online (such as `https://arxiv.org/pdf/2104.13478.pdf`)

Then you can, in the open note pane, select "more options" (the three dots in the top right), and a new option "annotate" should be available.

The plugin automatically tries to determine whether the file is an `epub` or `pdf` based on the file path, but in case this doesn't work, you can also add the property `annotation-target-type` and specify whether it is `epub` or `pdf` manually.

### Primary theme 
[Here](https://github.com/ceciliamay/obsidianmd-theme-primary)’s a link to more and more cool stuff. 

#### Callouts
You can have these cool callouts like this: 
> [!important]
> very imporant

There’re so much more. 
>[!celebrate]
>yay!

> [!NOTE] Note  
>> [!tldr] Summary  
>>> [!Infor] Information  
>>>> [!Tip] Tip  
>>>>> [!Done] Done  
>>>>>> [!FAQ] Question  
>>>>>>> [!Warning] Warning  
>>>>>>>> [!Fail] Fail  
>>>>>>>>> [!error] Error  
>>>>>>>>>> [!bug] Bug  
>>>>>>>>>>> [!example] Example  
>>>>>>>>>>>> [!Cite] Quote

#### Progress bars 
<progress value="90" max="100"></progress>
<progress value="100" max="100"></progress>

Super cool. 

`<progress value="90" max="100"></progress>`


https://kapeli.com/cheat_sheets/LaTeX_Math_Symbols.docset/Contents/Resources/Documents/index

https://www-users.york.ac.uk/~pjh503/LaTeX/equations.html