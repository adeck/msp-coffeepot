msp-coffeepot
=============

a fun little MSP430 project to turn a "dumb" '90s coffeemaker into a "smart" coffemaker

Goals:
- display -- give the coffeepot a shiny new 16x2 LCD frontend which displays a scrolling banner, and arbitrary
  text provided by the other functional parts
- timed startup / shutoff -- allow the user to set a timer for when the coffeepot should turn on and (if desired)
  a duration the pot should remain on before being switched off again
- temperature control -- currently, the coffeepot has a heating element and a crude temperature sensing mechanism,
  that turns off the heating element when the temperature exceeds a certain level, and then re-enables the heating
  element when the temperature falls below that level again. Unfortunately, the setting is "boiling hot" which is great
  for making the coffee, but after the coffee's made it means the thing doesn't need to be left on very long before the
  coffee's burned. Naturally, I don't want to disable the hardware switch that keeps the thing from going above boiling,
  but it _would_ be nice if it were possible to- once the coffee's made- keep it at some lower baseline temperature so
  it remains warm and unburned for a long while later.
- HTCPCP support -- RFC compliance; the end goal of any coffeepot-based MCU project. I have board-mount female
  RJ45 connectors (or, if that doesn't work out, I have wire strippers and a few tens of feet of some dollar
  store ethernet cable). Let's do this.
- tea mode -- once everything else gets done, I might want to be able to jerry-rig this thing to make steep tea the
  correct amount of time and then remove the teabag / tea ball.
