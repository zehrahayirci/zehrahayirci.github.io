---
title: If On A Winter's Night 
updated: 2021-01-03 15:25
---

My favorite book in 2020 was Italo Calvino's ["If On A Winter's Night A Traveller."](https://www.goodreads.com/book/show/374233.If_on_a_Winter_s_Night_a_Traveler) It is a book about books, so you have a reading experience of reading experiences—the book clubs' meta. 
 
In one chapter, the writer and the reader argued about the book's writing style and repeated words.  

_Lotaria brought me some novels electronically transcribed, in the form of words listed in their frequency order. "In a novel of fifty to a hundred thousand words," she said to me, "I advise you to observe immediately the words that are repeated about twenty times. Look here. Words that appear nineteen times:_

**_blood, cartridge belt, commander, do, have, immediately, it, life, seen, sentry, shots, spider, teeth, together, your..._**

_Words that appear eighteen times:_ 

**_boys, cap, come, dead, eat, enough, evening, French, go, handsome, new, passes, period, potatoes, those, until..."_**

_Don't you already have a clear idea what it's about?" Lotaria says. "There's no question: it's a war novel, all action, brisk writing, with a certain underlying violence. The narration is entirely on the surface._ 

This idea reminds me of  **Tf-idf**. 
Tf-idf stands for term frequency-inverse document frequency. Term frequency (TF) is how often a word appears in a text, divided by how many words there are.  It give the frequency ratio.  Inverse Document Frequency (IDF) is on the other hand, determines how unique your vocabulary is. It searches for our text and thousands of different texts to determine how unique a word is.  
The overall idea for text summarization with Tf-idf is finding words that are both frequent and unique to the text. 

Lotaria analyzed the books based on the most frequent words and tried to grasp the idea behind the story and decide whether the book is worth reading. But she goes beyond the most frequent ones.

_...but to make sure, it's always a good idea to take a look at the list of words used only once, though no less important for that. Take this sequence, for example:_

_**underarm, underbrush, undercover, underdog, underfed, underfoot, undergo, undergraduate, underground, undergrowth, underhand, underprivileged, undershirt, underwear, underweight...**_

_"No, the book isn't completely superficial, as it seemed. There must be something hidden; I can direct my research along these lines."_

Of course, the author feels anxious about this idea. Loteria's thesis may destroy the whole reading experience.

_The idea that Lotaria reads my books in this way creates some problems for me. Now, every time I write a word, I see it spun around by the electronic brain, ranked according to its frequency, next to other words whose identity I cannot know, and so I wonder how many times I have used it, I feel the whole responsibility of writing weigh on those isolated syllables, I try to imagine what conclusions can be drawn from the fact that I have used this word once or fifty times._

I want to test to see if this method is valid to analyze a book. Can we understand the style of the book based on the most and least frequent words? Is Loteria right about her thesis?

To begin with, I want to introduce one more technic called **word embeddings vectors**. These can be used as a metric to give you how two words are related to each other. You can expect that in English language word “cat” is very close to “cats”, “kitten” and “dog”.  Using [fasttext](https://fasttext.cc/) you can create your own embedding or even train your NLP models! But for this little experiment, I will use [Wikipedia English language embeddings](https://fasttext.cc/docs/en/pretrained-vectors.html). 
Let’s start with a classic novel, Jane Austen’s “Pride and Prejudice”. The most common words and their appearances are 

>ELIZABETH: 635 DARCY: 417 BENNET: 323 BINGLEY: 306 JANE: 292 MISS: 283 THOUGH: 226 SISTER: 217 SOON: 216 MAY: 205 MIGHT: 200 WICKHAM: 194 LADY: 191 OWN: 182 COLLINS: 180 AGAIN: 177 LYDIA: 171 SHALL: 163 DEAR: 158 FAMILY: 15

![PrideWordcloud](http://blog.zehrah.net/post_images/PrideWords.png)

By looking and these, I can only assume that this book is about some thoughtful ladys. Following Ludmilla’s idea, these are some words that only appear once in the book:

>'criticise', 'cheap', 'pope', 'wasting', 'originate', 'arch', 'clerk', 'inspire', 'simpered', 'slept', 'bass', 'naming', 'falsely', 'speed', 'rendering', 'celerity', 'arrear', 'sheets', 'network'...

I cannot deduce any further idea by looking at those. Maybe numbers can give us a better idea. 

Let’s look at the variance of these words to understand how distinct words the authos used. 
The variance of most used words is **0.03324658**. The average distance between these words on the other hand is **4.523685051738206**. 
The variance of the least used words is **0.040003102**. The average distance among those **4.881485597880001**. 

I can only say, the most used words go together well, than least used words, which is a natural consequence. By looking at just one book, it is hard to analyze. Let’s look at some more text:

I chose O. Henry’s The Last Leaf, Adventures of Sherlock Holmes by Arthur Conan Doyle, The Canterville’s Ghost by Oscar Wilde, White Fang and The Call of the Wild by Jack London, The Tell Tale Heart by Edgar Allan Poe, and 80 Days Around the World by Jules Verne. 
To make the things a bit interesting, I added two non-fiction to see the results: Communist Manifesto by Marx and Magna-Carta. 

The most common words in Magna Carta:
![MagnaCarta](http://blog.zehrah.net/post_images/magna.png)

Some of the one time appeared words are:
>'unanimous', 'actual', 'ath', 'numerous', 'dr', 'administration', 'excused', 'additions', 'investigated', 'direct', 'determine', 'tithing', 'corrupt', 'modification', 'wide', 'necessarily', 'kydells', 'transcription', 'exists', 'illegal'

![Table](http://blog.zehrah.net/post_images/tablebooks.png)


Well, it is still hard to make any inference, but it is certain that the distribution of the most common words may give us an idea about the content of the text. However, they do not reveal anything about the style. Maybe, we can say that most of the good novels have relevant words together rather than creating a word soup. 

Loteria was also wrong about the least used words. Low variance and high variance of the least used words should not be trusted when analyzing the books. 
In summary, the authors should not feel threatened by Loteria’s thesis. Their word frequency does not reveal their secrets nor reduce their content. 


