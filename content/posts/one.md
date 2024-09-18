---
title: "On the derivative of a linear operator with a little pedantry"
date: 1924-09-14
draft: false
summary: "clearing up an abuse of notation"
tags: ["differential geo","operators","derivative","abuse of notation"]
categories: ["math"]
showHeadingAnchors: true
showTableOfContents: true
---
{{<katex>}}
{{<rtl>}}

{{</rtl>}}

I'll throw light on a result I wish I'd known during my last quiz. **This, is vengeance.**


To put a long story short, the best linear approximation to a linear operator is itself, everywhere.

To put a long story long, consider a linear operator T, mapping the nice Hilbert space \\(\mathbb{R}^{n}\\) to itself. Yes, an endomorphism, smartypants. The ambient field, the mother to our scalars, being \\(\mathbb{R}\\). To brush up this means \\(T( a\vec{x} +b\vec{y}) =aT\ \vec{x} +bT\ \vec{y}\\) for scalars \\(a,b\\) and vectors \\(\vec{x} ,\vec{y}\\). 

In other words, \\(T\\) distributes over adding and commutes with scaling.

In other other words, 

\\(T \circ \text{add}( \ast ,\ast ) \equiv \text{add}( T\ast ,T\ast )\\) and \\(T\circ \text{mult}\_{a} \equiv \text{mult}_{a} \circ T\\)

Okay, no more obfuscation; promise.



## What is the derivative of \\(T\\)?

Start by familiarising with the following equations (definitions) (1) and (2).


\begin{equation}
T:\mathbb{R}^{n}\rightarrow \mathbb{R}^{n} =x\mapsto Tx\ 
\end{equation}
Dissection: Easy enough. T eats a vector and spits a vector. The second part is true for any function in place of \\(T\\). Enthusiasts of the lambda calculus might prefer \\(T=\lambda x.Tx\\). It is a recursion and a tautology.


\begin{equation}
T':\mathbb{R}^{n}\rightarrow \mathcal{L}\left(\mathbb{R}^{n}\right) =x\mapsto T'( x) :\mathbb{R}^{n}\rightarrow \mathbb{R}^{n}
\end{equation}
Dissection: \\(T'\\) being the derivative of an endomorphism of \\(\mathbb{R}^{n}\\) is a map that eats a vector and, instead of a vector, like \\(T\\) before it, regurgitates another map: an endomorphism. This morphism depends on and changes with the input \\(x\\).



The interesting part is that currying arises naturally here. \\(T'( x)\\) being a map means that \\(T'( x)( y)\\) is a vector. It might be easy to imagine \\(T'( x)\\) as \\(T'_{x}\\): every \\(x\\)'s very own linear map, bestowed by the philanthropic derivative. Explicitly, \\(T'\in \mathcal{L}\left(\mathbb{R}^{n} ,\mathcal{L}\left(\mathbb{R}^{n}\right)\right)\\) or the equally good

\\[
\begin{align*}
 T'\in \mathcal{L}\left(\mathbb{R}^{n} ,\mathcal{L}\left(\mathbb{R}^{n} ,\mathbb{R}^{n}\right)\right)
\end{align*}
\\]


  which adds nothing (but whimsy) to our discussion.

<br>


**To summarize**,
\\[
\begin{align*}
&x\ \text{is a vector} \\
\end{align*}
\\]

\\[
\begin{align*}
&T\ \text{is an endomorphism} \\
\end{align*}
\\]

\\[
\begin{align*}
&Tx\ \text{is a vector} \\
\end{align*}
\\]

\\[
\begin{align*}
&T'\ \text{is a morphism} \\
\end{align*}
\\]

\\[
\begin{align*}
&T'(x)\ \text{is an endomorphism} \\
\end{align*}
\\]

\\[
\begin{align*}
&T'(x)y\ \text{is a vector} \\
\end{align*}
\\]



## Does \\(T'=T\\)?



Short answer, it does, but **never** say it like that.

Long answer, let's take a detour.



An explanation I retrieve from stackexchange goes as follows:

Take in particular \\(f(x) \stackrel{\text{def}}{=} ax\\) on \\(\mathbb{R}\rightarrow \mathbb{R}\\). That is to say, \\(fx=ax\\) or \\(f=a\\).

And what is the derivative of \\(ax\\)? So \\(f'=f\\). Q.E.D.



This is a source of confusion which stems from a notorious abuse of notation. Clearly it cannot be that T' equals T, for both the operators have wildly different (and well, disjoint) codomains. \\(T\\) spits out vectors. \\(T'\\) regurgitates operators. Hell, \\(T'\\) is curried.



Look at \\(f'=f\\) again. What went wrong? Dwell over it now because I'd love to spoil you.



Well, to begin with, that \\(f( x) =ax\\) while \\(f'( x) \equiv a\\) already sparks skepticism. Could they be equal, as if! The solution to the misunderstanding is:

\\[
\begin{align*}
f'( x) &{\equiv} f \\\
f'  \quad \ \  &\boldsymbol{\neq} f \\\
f'( x) &\boldsymbol{\neq} f(x) \\\
f' \quad \ \ &\boldsymbol{\neq} f(x) \\\
\end{align*}
\\]


## Mandatory proof



Recall the definition of the derivative. Primes are easy to lose sight of, so I'll use \\([ DT]\\) for \\(T'\\).

\\([ DT]\(x)\\) is the (unique) map satisfying

\\[
\begin{align*}
 T( x+h) =T( x) +[ DT]\( x) h+o( || h| |) \text{   for x,h}\in \mathbb{R}^{n}
\end{align*}
\\]


Where little-o is tacitly taken as \\(||h||\rightarrow 0\\), which is to say

\\[
\begin{align*}
 f( h) \in o( ||h||) \Longrightarrow \lim _{||h||\rightarrow 0}\frac{f( h)}{||h||} =\vec{0}
\end{align*}
\\]


By linearity of \\(T\\), we have:
\begin{equation}
Th-[ DT]\( x) h=o( ||h||)
\end{equation}
Where we wish to pin down \\([ DT]\( x)\\).



The mathematician's attack of choice here would be to finesse it with an e*****t proof.

Step 1: It is trivial to check that \\([ DT]\( x) =T\\) is linear and satisfies (3)

Step 2: By uniqueness, it is **the** derivative. 

Thus \\(T'( x) =T\\) for all \\(x\in \mathbb{R}^{n}\\), or succinctly put, \\(T'( x) \equiv T\\).


But F the E-word, we're engineers and constructivists and downright idiots. Here's how I'd go around it.

It follows from the little-o in equation (3) that:
\\[
\begin{align*}
\lim _{||h||\rightarrow 0}\frac{( T'( x) -T) \ h}{||h||} =\vec{0}
\end{align*}
\\]



A vector wearing a dapper hat is a unit vector, while zero wearing it is the zero operator. But you already knew that, didn't you?



Absorb the \\(||h||\\) to get
\\[
\begin{align*}
\lim _{h\rightarrow 0}( T'( x) -T) \ \hat{h} =\vec{0}
\end{align*}
\\]

After the dependency on \\(||h||\\) has been killed, \\(\hat{h}\\) remains. It's completely determined by the direction it represents, which should evoke a mental image of the unit sphere. In fact, for the limit to hold, the operator must crush the entire unit sphere to zero.

\\[
\begin{align*}
\forall y\in S_{\mathbb{R}^{n}} :\ ( T'( x) -T) y=\vec{0}\\
\end{align*}
\\]

We can overload the operators to accept sets, leading to the more succinct notation:
\\[
\begin{align*}
( T'( x) -T) S_{\mathbb{R}^{n}} =\\{\vec{0}\\}
\end{align*}
\\]


From this it is an exercise to the reader to see that \\(( T'( x) -T)\mathbb{R}^{n} =\\{\vec{0}\\}\\)

(Hint: For any \\(y\in \mathbb{R}^{n}\\), \\(y=||y||\cdotp \hat{y}\\), and that map is linear)



And that means \\(T'( x) -T=\hat{0} ,\\) or \\(T'( x) =T\\), independent of our choice of x. **A constant map.**



## The upshot, and resolution



I find it best to summarize what we've found as


\\[
\begin{align*}
T=x\mapsto Tx
\end{align*}
\\]
\\[
\begin{align*}
T'=x\mapsto T
\end{align*}
\\]


 Where the first is redundant, trivial, tautological.

And the second, the fruit of our labor, the derivative of the endomorphism.



"But wait", you say, tugging at my shirt as I start to make a swift exit. "You said that T=T' is true, just bad notation. What's up with that?"



Indeed, it is best to say \\(T'( x) \equiv T\\) or \\(T'=x\mapsto T\\) or even \\(T'=\lambda x.T\\), as I prescribe vehemently. However, consider the difference between the following two maps on \\(\mathbb{R}\rightarrow \mathbb{R}\\):
\\[
\begin{align*}
1( x) =x\\
\end{align*}
\\]
\\[
\begin{align*}
\mathbb{O}\mathbb{N}\mathbb{E}( x) =1
\end{align*}
\\]


The first is the identity map. We use 1 to denote it, abusing the isomorphism of the reals with the multiplier functions


\\[
\begin{align*}
\mathcal{M} =\\{mult_{a}( \ast ) :\ a\in \mathbb{R}\\}.
\end{align*}
\\]

The second is the constant map. We use \\(\mathbb{O}\mathbb{N}\mathbb{E}\\) to denote it, abusing the isomorphism of the reals with the constant functions


\\[
\begin{align*}
 \mathcal{C} =\left\\{\text{const}\_{a}( \ast ) :\ \text{const}_{a}(\mathbb{R}) =\\{a\\} ,\ a\in \mathbb{R}\right\\}
\end{align*}
\\]




To see the different streams of thought in action, consider



(1) \\(T( z) \stackrel{\text{def}}{=} e^{i\pi /2} z\\)

"Okay, so \\(T\\) is just a clockwise quarter rotation. In fact, it multiplies like a number and distributes over addition like a number. If I abstract away the \\(( z)\\) from both sides, \\(T=i\\), after all."



(2) \\(f( x) \stackrel{\text{def}}{=} 5\\)

"No matter what you feed \\(f\\), it always returns five. Maybe \\(f\\) stands for five too. I can abstract away the argument from every \\(f\\) in my equation, and `CTRL+H` + `Replace All` to swap the \\(f\\)s for 5s. In that sense, \\(f=5\\), after all."

---

**Served cold, and exacted in full.**