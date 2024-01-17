# Yolo52Deck
Steps taken to train yolo to identify 52 deck playing cards

# Yolo
Install the ultralytics package using pip, check https://github.com/ultralytics/ultralytics

```
pip install ultralytics
```

# Code Environment
Start by preparing this repo to be within a python virtual environment, so we don't affect the system with out package needs.

Make sure you have python3 installed, if you're on a Mac like me, Homebrew is your friend, google it.

## Set the env
A level above this repo run the following
```
python3 -m venv --system-site-packages Yolo52Deck/ Yolo52Deck
```

## Activate the env
Go back into the repo folder and run
```
source bin/activate
```

your terminal will look something like
```
(Yolo52Deck) \>
```

Lets install the YOLO stuff



# Card details
## Measurements

https://tekeye.uk/playing_cards/playing-card-size#:~:text=The%20simple%20answer%20is%20that,2.5%20inches%20by%203.5%20inches.
Used the following site to retrieve most common measurements to calculate most common aspect ratios deltas

Ended up with 
* 1.528 >= ratio >= 1.4 

where 

* h = w * ratio
* w = h / ratio

## Character symbols
For the base 1-10QJK or 2-10QJKA normal characters can be used.

For unicode based on this website https://en.wikipedia.org/wiki/Playing_cards_in_Unicode
For suits one can use unicode:
* Spades
  * Solid ♠ -> U+2660
  * Transparent ♤ -> U+2664
* Clubs
  * Solid ♣ -> U+2663
  * Transparent ♧ -> U+2667
* Hearts
  * Solid ♥ -> U+2665
  * Transparent ♡ -> U+2661
* Diamonds
  * Solid ♦ -> U+2666
  * Transparent ♢ -> U+2662