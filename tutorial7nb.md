### @activities true


```template
namespace SpriteKind {
    export const Fornybar = SpriteKind.create()
}
namespace myTiles {
    //% blockIdentity=images._tile
    export const tile0 = img`
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
    `
}
info.onCountdownEnd(function () {
    if (info.score() < 20) {
        game.over(false)
    } else {
        game.over(true)
    }
})
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
    otherSprite.destroy()
    info.changeScoreBy(1)
})
sprites.onOverlap(SpriteKind.Player, SpriteKind.Fornybar, function (sprite, otherSprite) {
    tiles.placeOnRandomTile(otherSprite, assets.tile`transparency16`)
    info.changeScoreBy(1)
})
let havvind: Sprite = null
let energi: Sprite = null
tiles.setTilemap(tiles.createTilemap(
            hex`3200320000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000010101010101010101000000000000000000000000000000000000000000000000000000000000000000000000000000000001010101010101010101010100000000000000000000000000000000000000000000000000000000000000000000000000000101010101010101010101010101010100000000000000000000000000000000000000000000000000000000000000000000010101010101010101010101010101010101000000000000000000000000000000000000000000000000000000000000000000010101010101010101010101010101010101010000000000000000000000000000000000000000000000000000000000000001010101010101010101010101010101010101010000000000000000000000000000000000000000000000000000000000000001010101010101010101010101010101010101000000000000000000000000000000000000000000000000000000000000000101010101010101010101010101010101010100000000000000000000000000000000000000000000000000000000000000010101010101010101010101010101010101010000000000000000000000000000000000000000000000000000000000000001010101010101010101010101010101010101000000000000000000000000000000000000000000000000000000000000010101010101010101010101010101010101010100000000000000000000000000000000000000000000000000000000000101010101010101010101010101010101010101010000000000000000000000000000000000000000000000000000000000010101010101010101010101010101010101010101000000000000000000000000000000000000000000000000000000000001010101010101010101010101010101010101010101000000000000000000000000000000000000000000000000000000000101010101010101010101010101010101010101010100000000000000000000000000000000000000000000000000000000010101010101010101010101010101010101010101010000000000000000000000000000000000000000000000000000000001010101010101010101010101010101010101010101000000000000000000000000000000000000000000000000000000000001010101010101010101010101010101010101010100000000000000000000000000000000000000000000000000000000000101010101010101010101010101010101010101000000020202020202020000000000000000000000000000000000000000000101010101010101010101010101010101010100000202020202020202020202020000000000000000000000000000000000000101010101010101010101010101010101000202020202020202020202020202020000000000000000000000000000000000000001010101010101010101010101010202020202020202020202020202020202000000000000000000000000000000000000000000000000000001010101010102020202020202020202020202020202020202000000000000000000000000000000000000000000000000000000000000000202020202020202020202020202020202020202000000000000000000000000000000000000000000000000000000000000020202020202020202020202020202020202020200000000000000000000000000000000000000000000000000000000000002020202020202020202020202020202020202020200000000000000000000000000000000000000000000000000000000000202020202020202020202020202020202020202020000000000000000000000000000000000000000000000000000000002020202020202020202020202020202020202020202000000000000000000000000000000000000000000000000000000020202020202020202020202020202020202020202020200000000000000000000000000000000000000000000000000000202020202020202020202020202020202020202020202020200000000000000000000000000000000000000000000000000020202020202020202020202020202020202020202020202020000000000000000000000000000000000000000000000000202020202020202020202020202020202020202020202020202000000000000000000000000000000000000000000000000020202020202020202020202020202020202020202020202020200000000000000000000000000000000000000000000000002020202020202020202020202020202020202020202020202020000000000000000000000000000000000000000000000020202020202020202020202020202020202020202020202020200000000000000000000000000000000000000000000000002020202020202020202020202020202020202020202020202020000000000000000000000000000000000000000000000000002020202020202020202020202020202020202020202020000000000000000000000000000000000000000000000000000000202020202020202020202020202020202020202020202000000000000000000000000000000000000000000000000000000000202020202020202020202020202020202020202020000000000000000000000000000000000000000000000000000000000000002020202020202020202020202020202020000000000000000000000000000000000000000000000000000000000000000000000000202020202020202020202000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000`,
            img`
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
            `,
            [myTiles.tile0,sprites.castle.tilePath5,sprites.castle.tileGrass1],
            TileScale.Sixteen
        ))
scene.setBackgroundColor(9)
let mySprite = sprites.create(img`
    . f f f . f f f f . f f f . 
    f f f f f c c c c f f f f f 
    f f f f b c c c c b f f f f 
    f f f c 3 c c c c 3 c f f f 
    . f 3 3 c c c c c c 3 3 f . 
    . f c c c c 4 4 c c c c f . 
    . f f c c 4 4 4 4 c c f f . 
    . f f f b f 4 4 f b f f f . 
    . f f 4 1 f d d f 1 4 f f . 
    . . f f d d d d d d f f . . 
    . . e f e 4 4 4 4 e f e . . 
    . e 4 f b 3 3 3 3 b f 4 e . 
    . 4 d f 3 3 3 3 3 3 c d 4 . 
    . 4 4 f 6 6 6 6 6 6 f 4 4 . 
    . . . . f f f f f f . . . . 
    . . . . f f . . f f . . . . 
    `, SpriteKind.Player)
if (Math.percentChance(20)) {
    tiles.placeOnRandomTile(mySprite, sprites.castle.tilePath5)
} else {
    tiles.placeOnRandomTile(mySprite, sprites.castle.tileGrass1)
}
controller.moveSprite(mySprite)
scene.cameraFollowSprite(mySprite)
for (let index = 0; index < 100; index++) {
    energi = sprites.create(img`
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . f f f f . . . . . 
        . . . . . . f f 5 5 f . . . . . 
        . . . . . . f 5 5 f f . . . . . 
        . . . . . f f 5 f f . . . . . . 
        . . . . f f 5 5 f f f . . . . . 
        . . . . f 5 5 5 5 5 f . . . . . 
        . . . . f f f f 5 5 f . . . . . 
        . . . . . . f 5 5 f f . . . . . 
        . . . . . f f 5 f f . . . . . . 
        . . . . . f 5 f f . . . . . . . 
        . . . . . f f f . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        `, SpriteKind.Food)
    if (Math.percentChance(80)) {
        tiles.placeOnRandomTile(energi, sprites.castle.tilePath5)
    } else {
        tiles.placeOnRandomTile(energi, sprites.castle.tileGrass1)
    }
}
for (let index = 0; index < 200; index++) {
    havvind = sprites.create(img`
        . . . . . . . . . . 8 8 . . . . 
        . . . . . . . . . . 1 8 8 . . . 
        . . . . . . . 8 8 8 . 1 8 8 . . 
        . . . . . . . 8 1 8 8 . 1 8 . . 
        . . . . . . . 1 . 1 8 . . 8 . . 
        . . . . . . . . 8 8 8 . . 8 . . 
        . 8 8 8 8 8 8 8 1 1 1 . 8 8 . . 
        . 1 1 1 1 1 1 1 . . . 8 8 1 . . 
        . . 8 8 8 8 8 8 8 8 8 1 1 . . . 
        . . 1 1 1 1 1 1 1 1 1 . . . . . 
        . 8 8 8 8 8 8 8 8 8 8 . . . . . 
        . 1 1 1 1 1 1 1 1 1 1 8 8 . . . 
        . . 8 8 8 8 8 8 8 8 . 1 8 8 . . 
        . . 1 1 1 1 1 1 1 8 . . 1 8 . . 
        . . . . . . . . 8 8 . . . 8 . . 
        . . . . . . . . 1 1 . 8 8 1 . . 
        `, SpriteKind.Fornybar)
    tiles.placeOnRandomTile(havvind, assets.tile`transparency16`)
}
info.startCountdown(30)
```

# Effektivisering - Samle energi på avstand
## Introduksjon
### Steg 1: Introduksjon @unplugged

Noen ganger er det fint å kunne hente poeng på avstand. Her får du et eksempel på hvordan spillfiguren din kan skyte prosjektiler for å samle energi! 

### Steg 2

Begynn med å hente en ``||controller:on A button pressed||``-blokk fra ``||controller:Controller||``-menyen og plasser den for seg selv på skjermen.

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
	
})
```

### Steg 3

Hent en ``||logic:if true then else||``-blokk fra ``||logic:Logic||``-menyen og legg den inni ``||controller:on A button pressed||``-blokken.

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    // @highlight
    if (true) {
    	
    } else {
    	
    }
})
```

### Steg 4

Hent en ``||controller:is A button pressed||``-blokk fra ``||controller:Controller||``-menyen og plasser den der det står ``||logic:true||``.
Endre ``||controller:A||`` til ``||controller:left||``.

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    // @highlight
    if (controller.left.isPressed()) {
    	
    } else {
    	
    }
})
```

### Steg 5

Hent en ``||sprites:set projectile to projectile from mySprite with vx 50 vy 50||`` fra ``||sprites:Sprites||``-menyen og legg den inn i den første plassen på ``||logic:if true then else||``-blokken.
Endre vx til -200 og vy til 0. (Du må skrive inn tallet -200 fordi slideren på blokken bare går til 100).
Vx er farten i x-retningen. Når den er negativ går prosjektilet mot venstre. Vy er farten i y-retningen.

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    if (controller.left.isPressed()) {
        // @highlight
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . . . . . . . . . . . 
            . . . . . . . . . . . . . . . . 
            . . . . . . . . . . . . . . . . 
            . . . . . . . . . . . . . . . . 
            . . . . . . . . . . . . . . . . 
            . . . . . . . . . . . . . . . . 
            . . . . . . . . . . . . . . . . 
            . . . . . . . . . . . . . . . . 
            . . . . . . . . . . . . . . . . 
            . . . . . . . . . . . . . . . . 
            . . . . . . . . . . . . . . . . 
            . . . . . . . . . . . . . . . . 
            . . . . . . . . . . . . . . . . 
            . . . . . . . . . . . . . . . . 
            . . . . . . . . . . . . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, 0)
    } else {
    	
    }
})
```

### Steg 6

Klikk på det grå kvadratet på ``||sprites:set projectile to projectile from mySprite||``-blokken og tegn eller velg et prosjektil fra galleriet.
I eksemplet er prosjektilet en donut.

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    if (controller.left.isPressed()) {
        // @highlight
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, 0)
    } else {
    	
    }
})
```

### Steg 7

Klikk på det lille plusstegnet nede til venstre på ``||logic:if true then else||``-blokken, til du får tre ledige plasser.

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    // @highlight
    if (controller.left.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, 0)
    } else if (false) {
    	
    } else if (false) {
    	
    } else {
    	
    }
})
```

### Steg 8

Kopier ``||controller:is left button pressed||`` og plasser den i neste ledige sekskant i ``||logic:if true then else||``-blokken.
Endre ``||controller:left||`` til ``||controller:right||``.

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    // @highlight
    if (controller.left.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, 0)
    } else if (controller.right.isPressed()) {
    	
    } else if (false) {
    	
    } else {
    	
    }
})
```

### Steg 9

Kopier blokken ``||sprites:set projectile to projectile from mySprite||`` inn i den neste ledige plassen.
Endre den så det står ``||sprites:vx 200 vy 0||``.

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    if (controller.left.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, 0)
    } else if (controller.right.isPressed()) {
        // @highlight
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 200, 0)
    } else if (false) {
    	
    } else {
    	
    }
})
```

### Steg 10

Hent eller kopier en ny ``||controller:is A button pressed||``-blokk og plasser den i neste ledige sekskant.
Endre ``||controller:A||`` til ``||controller:down||``.

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    // @highlight
    if (controller.left.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, 0)
    } else if (controller.right.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 200, 0)
    } else if (controller.down.isPressed()) {
    	
    } else {
    	
    }
})
```

### Steg 11

Kopier blokken ``||sprites:set projectile to projectile from mySprite||`` inn i den nest nederste plassen.
Endre den så det står ``||sprites:vx 0 vy 200||``.
Positiv y-retning er nedover på skjermen, derfor skytes prosjektilet nedover når farten i y-retning er positiv.

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    if (controller.left.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, 0)
    } else if (controller.right.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 200, 0)
    } else if (controller.down.isPressed()) {
        // @highlight
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, 200)
    } else {
    	
    }
})
```

### Steg 12

Kopier blokken ``||sprites:set projectile to projectile from mySprite||`` og legg kopien i den siste ledige plassen.
Endre blokken så det står ``||sprites:vx 0 vy -200||``.
Nå vil spillfiguren din skyte et prosjektil som går oppover på skjermen når den står stille eller går oppover.

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    if (controller.left.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, 0)
    } else if (controller.right.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 200, 0)
    } else if (controller.down.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, 200)
    } else {
        // @highlight
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, -200)
    }
})
```
### Steg 13

Nå gjenstår hva som skal skje når prosjektilet treffer energien.
Hent en ``||sprites:on sprite of kind player overlaps othersprite of kind player||``-blokk.
Endre det første feltet der det står ``||sprites:Player||`` til ``||sprites:Projectile||`` og det andre feltet til ``||sprites:Food||``.

```blocks
// @highlight
sprites.onOverlap(SpriteKind.Projectile, SpriteKind.Food, function (sprite, otherSprite) {
	
})
```

### Steg 14

Når du treffer en energisprite med et prosjektil, skal du nå få poeng og energien skal forsvinne.
Hent en ``||info:change score by 1||``-blokk fra ``||info:Info||``-menyen og legg den inn i overlap-blokken.

```blocks
sprites.onOverlap(SpriteKind.Projectile, SpriteKind.Food, function (sprite, otherSprite) {
    // @highlight
    info.changeScoreBy(1)
})
```

### Steg 15
Hent en ``||sprites:destroy mySprite||``-blokk fra ``||sprites:Sprites||``-menyen og plasser den under ``||info:change score by 1||``-blokken.

```blocks
sprites.onOverlap(SpriteKind.Projectile, SpriteKind.Food, function (sprite, otherSprite) {
    info.changeScoreBy(1)
    // @highlight
    sprites.destroy(mySprite)
})
```
### Steg 16
Dra variablen ``||variables:otherSprite||`` inn der det står ``||variables:mySprite||``.
Nå forsvinner energien når du skyter den, og du får poeng.

```blocks
sprites.onOverlap(SpriteKind.Projectile, SpriteKind.Food, function (sprite, otherSprite) {
    info.changeScoreBy(1)
    // @highlight
    sprites.destroy(otherSprite)
})
```

### Steg 17 @unplugged
Så langt har du laget prosjektiler som kan gå opp, ned og til begge sider, men hva om du vil ha dem til å gå på skrå?
Spillfiguren går på skrå over skjermen om du holder inne f.eks. knappene "up" og "right" samtidig.
Nå kan du lære hvordan du kan få prosjektilene til å gjøre det samme.
Den neste delen inneholder masse logikk og er vanskeligere enn det du har gjort til nå, så du får lov til å gi deg her om logikk ikke er din greie.
Det som kommer nå er faktisk litt komplisert.

### Steg 18
Det første du må gjøre er å lage 4 nye gap i ``||logic:if-then-else||``-blokken i ``||controller:on A button pressed||``.
Trykk på det lille plusstegnet nederst til venstre i ``||logic:if-then-else||``-blokken 4 ganger.
Den siste ``||sprites:set projectile to projectile from mySprite with vx 0 vy -200||``-blokken skal ligge i det siste gapet under ``||logic:else:||``.
Det skal normalt skje av seg selv, men se på tipset under lyspæren om du lurer på hvordan det skal se ut.

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function on_a_pressed() {
    
    if (controller.left.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
                . . . . . . b b b b a a . . . . 
                            . . . . b b d d d 3 3 3 a a . . 
                            . . . b d d d 3 3 3 3 3 3 a a . 
                            . . b d d 3 3 3 3 3 3 3 3 3 a . 
                            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
                            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
                            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
                            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
                            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
                            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
                            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
                            a a 3 3 3 d d d a a 4 4 4 e e . 
                            . e a a a a a a 4 4 4 4 e e . . 
                            . . e e b b 4 4 4 4 b e e . . . 
                            . . . e e e e e e e e . . . . . 
                            . . . . . . . . . . . . . . . .
            `, mySprite, -200, 0)
    } else if (controller.right.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
                . . . . . . b b b b a a . . . . 
                            . . . . b b d d d 3 3 3 a a . . 
                            . . . b d d d 3 3 3 3 3 3 a a . 
                            . . b d d 3 3 3 3 3 3 3 3 3 a . 
                            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
                            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
                            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
                            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
                            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
                            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
                            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
                            a a 3 3 3 d d d a a 4 4 4 e e . 
                            . e a a a a a a 4 4 4 4 e e . . 
                            . . e e b b 4 4 4 4 b e e . . . 
                            . . . e e e e e e e e . . . . . 
                            . . . . . . . . . . . . . . . .
            `, mySprite, 200, 0)
    } else if (controller.down.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
                . . . . . . b b b b a a . . . . 
                            . . . . b b d d d 3 3 3 a a . . 
                            . . . b d d d 3 3 3 3 3 3 a a . 
                            . . b d d 3 3 3 3 3 3 3 3 3 a . 
                            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
                            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
                            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
                            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
                            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
                            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
                            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
                            a a 3 3 3 d d d a a 4 4 4 e e . 
                            . e a a a a a a 4 4 4 4 e e . . 
                            . . e e b b 4 4 4 4 b e e . . . 
                            . . . e e e e e e e e . . . . . 
                            . . . . . . . . . . . . . . . .
            `, mySprite, 0, 200)
    } else if (false) {
        
    } else if (false) {
        
    } else if (false) {

    } else if (false) {
        
    } else {
        projectile = sprites.createProjectileFromSprite(img`
                . . . . . . b b b b a a . . . . 
                            . . . . b b d d d 3 3 3 a a . . 
                            . . . b d d d 3 3 3 3 3 3 a a . 
                            . . b d d 3 3 3 3 3 3 3 3 3 a . 
                            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
                            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
                            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
                            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
                            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
                            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
                            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
                            a a 3 3 3 d d d a a 4 4 4 e e . 
                            . e a a a a a a 4 4 4 4 e e . . 
                            . . e e b b 4 4 4 4 b e e . . . 
                            . . . e e e e e e e e . . . . . 
                            . . . . . . . . . . . . . . . .
            `, mySprite, 0, -200)
    }
    
})
```

### Steg 19
Nå skal du bruke en ny logisk funksjon.
Blokken ``||logic:and||`` fra ``||logic:Logic||``-menyen undersøker om to ting er sant samtidig.
Du skal nå bruke en ``||logic:and||``-blokk for å sjekke om 2 knapper er trykket inn samtidig med A-knappen.
Hent en sekskantet ``||logic:and||``-blokk fra ``||logic:Logic||``-menyen og legg den inn i sekskanten over det første ledige gapet i ``||logic:if-then-else||``.

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    if (controller.left.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, 0)
    } else if (controller.right.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 200, 0)
    } else if (controller.down.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, 200)
    } else if (false && false) {
    	
    } else if (false) {
    	
    } else if (false) {
    	
    } else if (false) {
    	
    } else {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, -200)
    }
})
```

### Steg 20
Begynn med å sjekke om "Up" og "Left" er trykket inn samtidig.
Hent to ``||controller:is A button pressed||``-blokker fra ``||controller:Controller||``-menyen og legg dem inn i hvert sin sekskant i den nye ``||logic:and||``-blokken.
Endre ``||controller:A||`` til ``||controller:up||``på den første og ``||controller:A||`` til ``||controller:left||`` på den andre av de to nye blokkene.

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    if (controller.left.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, 0)
    } else if (controller.right.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 200, 0)
    } else if (controller.down.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, 200)
    } else if (controller.up.isPressed() && controller.left.isPressed()) {
    	
    } else if (false) {
    	
    } else if (false) {
    	
    } else if (false) {
    	
    } else {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, -200)
    }
})
```

### Steg 21
Kopier en ``||sprites:set projectile to projectile from mySprite||``-blokk fra et av gapene i ``||if-then-else||`` og sett den inn i gapet under ``||logic:and||`` blokken din.
Endre ``||sprites:vx||`` til -200 og ``||sprites:vy||`` til -200.
Om du tester spillet nå, skytes prosjektilet rett til venstre, uten å gå på skrå oppover, selv om du holder inne både ``||controller:up||`` og ``||controller:left||``.
Det skyldes at du allerede har fortalt spillet at så lenge ``||controller:left||`` er trykket inn, skal spillfiguren sende et prosjektil mot venstre.
Spillet skjønner ikke at dette ikke gjelder når ``||controller:up||`` eller ``||controller:down||`` er trykket inn samtidig.
Her er det en konflikt mellom disse to knappekombinasjonene, og den gamle kommandoen vinner.
Men dette skal vi fikse i de neste stegene.

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    if (controller.left.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, 0)
    } else if (controller.right.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 200, 0)
    } else if (controller.down.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, 200)
    } else if (controller.left.isPressed() && controller.up.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, -200)
    } else if (false) {
    	
    } else if (false) {
    	
    } else if (false) {
    	
    } else {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, -200)
    }
})
```

### Steg 22 @unplugged
Nå skal vi introdusere en ny logisk funksjon, ``||logic:not||``.
Den skal hjelpe spillet til å skille mellom varianter av knappekombinasjoner, slik at det ikke blir krøll.

### Steg 23
Dra ``||controller:is left button pressed||`` ut av den øverste sekskanten i ``||logic:if-then else||`` og legg den på skrivebordet til etterpå.
Hent en ``||logic:and||``-blokk og plasser den i sekskanten du nettopp dro ``||controller:is left button pressed||`` ut av.
Hent ``||controller:is left button pressed||`` fra skrivebordet og legg den inn i den første sekskanten i den nye ``||logic:and||``-blokken.

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    if (controller.left.isPressed() && false) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, 0)
    } else if (controller.right.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 200, 0)
    } else if (controller.down.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, 200)
    } else if (controller.left.isPressed() && controller.up.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, -200)
    } else if (false) {
    	
    } else if (false) {
    	
    } else if (false) {
    	
    } else {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, -200)
    }
})
```

### Steg 24
Hent den sekskantede blokken ``||logic:not||`` fra ``||logic:Logic||``-menyen og plasser den i den andre sekskanten i ``||logic:and||``-blokken.
Sjekk tipset under lyspæren så du ser hvordan det skal se ut.

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    if (controller.left.isPressed() && !(false)) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, 0)
    } else if (controller.right.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 200, 0)
    } else if (controller.down.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, 200)
    } else if (controller.left.isPressed() && controller.up.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, -200)
    } else if (false) {
    	
    } else if (false) {
    	
    } else if (false) {
    	
    } else {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, -200)
    }
})
```

### Steg 25
OK! Nå gjelder det å holde tunga rett i munnen her.
Du trenger en ny logisk funksjon.
Den finner du i ``||logic:and||``-blokken, og den heter ``||logic:or||``.
Hent en ny ``||logic:and||``-blokk og legg den inn i den ledige sekskanten i ``||logic:not||``blokken.
Klikk på den lille pilen til høyre for ``||logic:and||`` og endre ``||logic:and||`` til ``||logic:or||``.

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    if (controller.left.isPressed() && !(false || false)) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, 0)
    } else if (controller.right.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 200, 0)
    } else if (controller.down.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, 200)
    } else if (controller.left.isPressed() && controller.up.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, -200)
    } else if (false) {
    	
    } else if (false) {
    	
    } else if (false) {
    	
    } else {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, -200)
    }
})
```
### Steg 26
Nå trenger du to ``||controller:is A button pressed||``-blokker.
Legg en i hver av de to ledige sekskantene i ``||logic:or||`` og endre fra ``||controller:A||`` til ``||controller:up||`` på den ene og ``||controller:down||`` på den andre.
Det kan hende du må oppdatere nettsiden manuelt (refresh-knapp til venstre for adressefeltet i nettleseren) for at denne koden skal oppdateres.
Nå skal du kunne skyte prosjektiler på skrå opp og til venstre.

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    if (controller.left.isPressed() && !(controller.up.isPressed() || controller.down.isPressed())) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, 0)
    } else if (controller.right.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 200, 0)
    } else if (controller.down.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, 200)
    } else if (controller.left.isPressed() && controller.up.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, -200)
    } else if (false) {
    	
    } else if (false) {
    	
    } else if (false) {
    	
    } else {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, -200)
    }
})
```

### Steg 27
Nå må du gjøre det samme for de to neste ``||logic:else if||`` sekskantene i ``||logic:if-then-else||`` blokken, men nå kan du gjøre det litt kjappere.
Kopier hele den store sekskanten du lagde i de forrige stegene og legg kopien inn i den neste ``||logic:else if||``-sekskanten.
Endre ``||controller:left||`` til ``||controller:right||`` i den første sekskanten i kopien.

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    if (controller.left.isPressed() && !(controller.up.isPressed() || controller.down.isPressed())) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, 0)
    } else if (controller.right.isPressed() && !(controller.up.isPressed() || controller.down.isPressed())) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 200, 0)
    } else if (controller.down.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, 200)
    } else if (controller.left.isPressed() && controller.up.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, -200)
    } else if (false) {
    	
    } else if (false) {
    	
    } else if (false) {
    	
    } else {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, -200)
    }
})
```

### Steg 28
Nå må du gjøre det samme for prosjektilene som skal gå nedover.
Dra ``||controller:is down button pressed||``-sekskanten ut av ``||logic:if-then-else||`` og erstatt den med en kopi av den store ``||logic:and-not-or||``-sekskanten.
Endre den første sekskanten i ``||logic:and-not-or||`` til ``||controller:down||``, den neste til ``||controller:left||`` og den siste til ``||lcontroller:right||``, slik at det står ``||logic:else if||`` ``||controller:is down button pressed||`` ``||logic:and not||`` ``||controller:is left button pressed||`` ``||logic:or||`` ``||controller:is right button pressed||`` ``||logic:then||`` på denne blokklinjen.

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    if (controller.left.isPressed() && !(controller.up.isPressed() || controller.down.isPressed())) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, 0)
    } else if (controller.right.isPressed() && !(controller.up.isPressed() || controller.down.isPressed())) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 200, 0)
    } else if (controller.down.isPressed() && !(controller.left.isPressed() || controller.right.isPressed())) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, 200)
    } else if (controller.left.isPressed() && controller.up.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, -200)
    } else if (false) {
    	
    } else if (false) {
    	
    } else if (false) {
    	
    } else {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, -200)
    }
})
```

### Steg 29 @unplugged
Nå har du fått ryddet unna alle konfliktene mellom knappekombinasjoner for prosjektilene.
Den siste retningen, oppover, trenger du ikke gjøre noe med, fordi det er den veien prosjektilene går når ingen av kriteriene over er oppfylt.
Nå kan du begynne å sette inn resten av de skrå prosjektilretningene.

### Steg 30
Hent en ny ``||locic:and||`` blokk fra ``||logic:Logic||``-menyen og sett den inn i den ledige sekskanten over det første ledige gapet i ``||logic:if-then-else||``.
Hent 2 ``||controller:is A button pressed||``-blokker fra ``||controller:Controller||``-menyen og plasser en på hver side av ``||logic:and||`` i blokken du nettopp plasserte.
Endre ``||controller:A||`` til ``||controller:right||`` på den ene og til ``||controller:up||`` på den andre.

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    if (controller.left.isPressed() && !(controller.up.isPressed() || controller.down.isPressed())) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, 0)
    } else if (controller.right.isPressed() && !(controller.up.isPressed() || controller.down.isPressed())) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 200, 0)
    } else if (controller.down.isPressed() && !(controller.left.isPressed() || controller.right.isPressed())) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, 200)
    } else if (controller.left.isPressed() && controller.up.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, -200)
    } else if (controller.right.isPressed() && controller.up.isPressed()) {
    	
    } else if (false) {
    	
    } else if (false) {
    	
    } else {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, -200)
    }
})
```

### Steg 31
Kopier en av ``||sprites: set projectile to...||``-blokkene og sett den inn i det første ledige gapet i ``||logic:if-then-else||``.
Endre blokken slik at ``||logic:vx||`` har verdien 200 og ``||logic:vy||`` har verdien -200.

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    if (controller.left.isPressed() && !(controller.up.isPressed() || controller.down.isPressed())) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, 0)
    } else if (controller.right.isPressed() && !(controller.up.isPressed() || controller.down.isPressed())) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 200, 0)
    } else if (controller.down.isPressed() && !(controller.left.isPressed() || controller.right.isPressed())) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, 200)
    } else if (controller.left.isPressed() && controller.up.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, -200)
    } else if (controller.right.isPressed() && controller.up.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 200, -200)
    } else if (false) {
    	
    } else if (false) {
    	
    } else {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, -200)
    }
})
```

### Steg 32
Hent en ny ``||locic:and||`` blokk fra ``||logic:Logic||``-menyen og sett den inn i den ledige sekskanten over det neste ledige gapet i ``||logic:if-then-else||``.
Hent 2 ``||controller:is A button pressed||``-blokker fra ``||controller:Controller||``-menyen og plasser en på hver side av ``||logic:and||`` i blokken du nettopp plasserte.
Endre ``||controller:A||`` til ``||controller:left||`` på den ene og til ``||controller:down||`` på den andre.

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    if (controller.left.isPressed() && !(controller.up.isPressed() || controller.down.isPressed())) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, 0)
    } else if (controller.right.isPressed() && !(controller.up.isPressed() || controller.down.isPressed())) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 200, 0)
    } else if (controller.down.isPressed() && !(controller.left.isPressed() || controller.right.isPressed())) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, 200)
    } else if (controller.left.isPressed() && controller.up.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, -200)
    } else if (controller.right.isPressed() && controller.up.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 200, -200)
    } else if (controller.left.isPressed() && controller.down.isPressed()) {
    	
    } else if (false) {
    	
    } else {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, -200)
    }
})
```

### Steg 33
Kopier en av ``||sprites: set projectile to...||``-blokkene og sett den inn i det ledige gapet under blokken du nettopp endret i ``||logic:if-then-else||``.
Endre blokken slik at ``||logic:vx||`` har verdien -200 og ``||logic:vy||`` har verdien 200.

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    if (controller.left.isPressed() && !(controller.up.isPressed() || controller.down.isPressed())) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, 0)
    } else if (controller.right.isPressed() && !(controller.up.isPressed() || controller.down.isPressed())) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 200, 0)
    } else if (controller.down.isPressed() && !(controller.left.isPressed() || controller.right.isPressed())) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, 200)
    } else if (controller.left.isPressed() && controller.up.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, -200)
    } else if (controller.right.isPressed() && controller.up.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 200, -200)
    } else if (controller.left.isPressed() && controller.down.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, 200)
    } else if (false) {
    	
    } else {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, -200)
    }
})
```

### Steg 34
Nå gjenstår bare den siste retning, ned og til høyre.
Hent en ny ``||locic:and||`` blokk fra ``||logic:Logic||``-menyen og sett den inn i den ledige sekskanten over det neste ledige gapet i ``||logic:if-then-else||``.
Hent 2 ``||controller:is A button pressed||``-blokker fra ``||controller:Controller||``-menyen og plasser en på hver side av ``||logic:and||`` i blokken du nettopp plasserte.
Endre ``||controller:A||`` til ``||controller:right||`` på den ene og til ``||controller:down||`` på den andre.

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    if (controller.left.isPressed() && !(controller.up.isPressed() || controller.down.isPressed())) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, 0)
    } else if (controller.right.isPressed() && !(controller.up.isPressed() || controller.down.isPressed())) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 200, 0)
    } else if (controller.down.isPressed() && !(controller.left.isPressed() || controller.right.isPressed())) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, 200)
    } else if (controller.left.isPressed() && controller.up.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, -200)
    } else if (controller.right.isPressed() && controller.up.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 200, -200)
    } else if (controller.left.isPressed() && controller.down.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, 200)
    } else if (controller.right.isPressed() && controller.down.isPressed()) {
    	
    } else {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, -200)
    }
})
```

### Steg 35
Kopier en av ``||sprites: set projectile to...||``-blokkene og sett den inn i det siste ledige gapet i ``||logic:if-then-else||``.
Endre blokken slik at ``||logic:vx||`` har verdien 200 og ``||logic:vy||`` har verdien 200.

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    if (controller.left.isPressed() && !(controller.up.isPressed() || controller.down.isPressed())) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, 0)
    } else if (controller.right.isPressed() && !(controller.up.isPressed() || controller.down.isPressed())) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 200, 0)
    } else if (controller.down.isPressed() && !(controller.left.isPressed() || controller.right.isPressed())) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, 200)
    } else if (controller.left.isPressed() && controller.up.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, -200)
    } else if (controller.right.isPressed() && controller.up.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 200, -200)
    } else if (controller.left.isPressed() && controller.down.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, -200, 200)
    } else if (controller.right.isPressed() && controller.down.isPressed()) {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 200, 200)
    } else {
        projectile = sprites.createProjectileFromSprite(img`
            . . . . . . b b b b a a . . . . 
            . . . . b b d d d 3 3 3 a a . . 
            . . . b d d d 3 3 3 3 3 3 a a . 
            . . b d d 3 3 3 3 3 3 3 3 3 a . 
            . b 3 d 3 3 3 3 3 b 3 3 3 3 a b 
            . b 3 3 3 3 3 a a 3 3 3 3 3 a b 
            b 3 3 3 3 3 a a 3 3 3 3 d a 4 b 
            b 3 3 3 3 b a 3 3 3 3 3 d a 4 b 
            b 3 3 3 3 3 3 3 3 3 3 d a 4 4 e 
            a 3 3 3 3 3 3 3 3 3 d a 4 4 4 e 
            a 3 3 3 3 3 3 3 d d a 4 4 4 e . 
            a a 3 3 3 d d d a a 4 4 4 e e . 
            . e a a a a a a 4 4 4 4 e e . . 
            . . e e b b 4 4 4 4 b e e . . . 
            . . . e e e e e e e e . . . . . 
            . . . . . . . . . . . . . . . . 
            `, mySprite, 0, -200)
    }
})
```

### Steg 36
Gratulerer! Dette var den vanskeligste tutorialen av dem alle!
Nå vet du hvordan du lager prosjektiler, og hvordan du får dem til å fly i alle retninger ved hjelp av knappekombinasjoner.
Gå gjerne inn på [Kodekraft.no](https://www.vitensenter.no/kodekraft/kodeoekt/) og sjekk ut neste oppgave.

