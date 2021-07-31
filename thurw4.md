## Generated text:

ROMEO:
The nobles ruin's brows what face? a king! Come,
I'll fill'd my cleaser put to sea age me:' quoth she's the fiery,
That wrings thee to be are fouldest and fortune's pen.

KING EDWARD IV:
So wide an bond and sort and speedily together
To the wild-golfed flies. The first and mind
Of thousands mine abroad to the traitor's fifty,
To you foos of it, my lord,
I had a Rutland for it; foreited
Nor quice.

LUCIO:
I have.
O that Lewis or that my father? Warwick,
Hark you to Rome, but if you break! why, you shall
fined by his master's face but think,--cope's my way's boar,
Having but with five thousand monnest! how now, wrave's
Will from thy reprieve untertain your bosom.
Know thou art in with me?
Be mill him, and stick your majesty to him
That they'll occasion with one, why,
Yes, if thou wilt swear to do it?

MERCUTIO:
Good morrow, neighbour Baptista,
I mean, she buildetion: you will have mine out
Takes you with self-bound foes love,
What elsey and nobly feast. Or sugh the world?

GLOUCESTER:
B 

___

## How it was produced/works:

To process the data, the string characters were vectorized and converted to numeric ID then inverted them back to strings using preprocessing.StringLookup, then tf.strings.reduce_join joined the characters back into strings.

The model predicted the next based on the most probable character (after one character, or a sequence of characters)

The model is built as a keras.Model subclass with three layers: input layer (tf.keras.layers.Embedding), a type of recurrent neural network (RNN) (tf.keras.layers.GRU), and an output layer (tf.keras.layers.Dense). 

The model can be trained as a standard classification problem; given the RNN state and an input, the model predicts the "class" of the next character. The model also has a loss function which indicates how sure the model is of its wrong answers (the higher loss, the worst our model is doing).

The model generates text by taking in the passed text and returning a prediction of the next character. The model learns when to capitalize, make paragraphs, and so on. The more epochs, the better the model learns and the better the resulting generated text!