# My Tutorial

## Step 1: Introduction @unplugged

In this tutorial, you will learn to 

- :blank: do this
- :mouse pointer: do that
- :game: do this & that

![Tutorial Preview](https://github.com/rymc88/tutorial-intro/blob/master/tutorial-preview.gif?raw=true)

## Create the Sprite 

Get the ``||variables(sprites): set mySprite to||`` block
from the ``||sprites: Sprites||`` drawer in the [**tool box**](#tools "The strip to the left of the workspace that lists block categories.").
Place it in the ``||loops: on start||`` block.

----------

**TIP:** Did you notice that the word ***toolbox*** had a special look.
From time to time, we'll enhance important words.
Roll your mouse over them to see a *definition*.


```blocks
let mySprite = sprites.create(img`
    . . . . . . . . . . b 5 b . . . 
    . . . . . . . . . b 5 b . . . . 
    . . . . . . . . . b c . . . . . 
    . . . . . . b b b b b b . . . . 
    . . . . . b b 5 5 5 5 5 b . . . 
    . . . . b b 5 d 1 f 5 5 d f . . 
    . . . . b 5 5 1 f f 5 d 4 c . . 
    . . . . b 5 5 d f b d d 4 4 . . 
    b d d d b b d 5 5 5 4 4 4 4 4 b 
    b b d 5 5 5 b 5 5 4 4 4 4 4 b . 
    b d c 5 5 5 5 d 5 5 5 5 5 b . . 
    c d d c d 5 5 b 5 5 5 5 5 5 b . 
    c b d d c c b 5 5 5 5 5 5 5 b . 
    . c d d d d d d 5 5 5 5 5 d b . 
    . . c b d d d d d 5 5 5 b b . . 
    . . . c c c c c c c c b b . . . 
    `, SpriteKind.Player)
```

## Add Dialog Box

Get the ``||game: show long text "___"||`` block
from the ``||game: Game||`` drawer in the tool box. 
Place it after the ``||variables(sprites): set mySprite to||`` block.

~hint This content is hidden until the user clicks here 
- Click on the ``||game: "___"||`` in the show long text block
- Type what you want to be displayed in the dialog box
- Click ``||game: [bottom]||`` to change the dialog box 's placement
hint~

```blocks
let mySprite = sprites.create(img`
    . . . . . . . . . . b 5 b . . . 
    . . . . . . . . . b 5 b . . . . 
    . . . . . . . . . b c . . . . . 
    . . . . . . b b b b b b . . . . 
    . . . . . b b 5 5 5 5 5 b . . . 
    . . . . b b 5 d 1 f 5 5 d f . . 
    . . . . b 5 5 1 f f 5 d 4 c . . 
    . . . . b 5 5 d f b d d 4 4 . . 
    b d d d b b d 5 5 5 4 4 4 4 4 b 
    b b d 5 5 5 b 5 5 4 4 4 4 4 b . 
    b d c 5 5 5 5 d 5 5 5 5 5 b . . 
    c d d c d 5 5 b 5 5 5 5 5 5 b . 
    c b d d c c b 5 5 5 5 5 5 5 b . 
    . c d d d d d d 5 5 5 5 5 d b . 
    . . c b d d d d d 5 5 5 b b . . 
    . . . c c c c c c c c b b . . . 
    `, SpriteKind.Player)
// @highlight
game.showLongText("Move Ducky using the arrow keys", DialogLayout.Bottom)
```

## Add Controls

Get the ``||controller: move mySprite with buttons||`` block
from the ``||controller: Controller||`` drawer in the tool box. 
Place it after the ``||game: show long text "___"||`` block.

----------

**TIP:** Click the ➕ icon on the 
``||controller: move mySprite with buttons||`` block
to show the preloaded arugment that sets both the
``vx`` and ``vy`` value to ``100``. Increase or 
decrease those values to *speed up* or *slow down*
``||variables(sprites): mySprite's||`` movement.

```blocks
let mySprite = sprites.create(img`
    . . . . . . . . . . b 5 b . . . 
    . . . . . . . . . b 5 b . . . . 
    . . . . . . . . . b c . . . . . 
    . . . . . . b b b b b b . . . . 
    . . . . . b b 5 5 5 5 5 b . . . 
    . . . . b b 5 d 1 f 5 5 d f . . 
    . . . . b 5 5 1 f f 5 d 4 c . . 
    . . . . b 5 5 d f b d d 4 4 . . 
    b d d d b b d 5 5 5 4 4 4 4 4 b 
    b b d 5 5 5 b 5 5 4 4 4 4 4 b . 
    b d c 5 5 5 5 d 5 5 5 5 5 b . . 
    c d d c d 5 5 b 5 5 5 5 5 5 b . 
    c b d d c c b 5 5 5 5 5 5 5 b . 
    . c d d d d d d 5 5 5 5 5 d b . 
    . . c b d d d d d 5 5 5 b b . . 
    . . . c c c c c c c c b b . . . 
    `, SpriteKind.Player)
game.showLongText("Move Ducky using the arrow keys", DialogLayout.Bottom)
// @highlight
controller.moveSprite(mySprite, 100, 100)
```