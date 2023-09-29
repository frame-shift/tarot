# Daily Tarot Card Draw
This is a dataset of random numbers generated for daily tarot card draws, originally designed for an applet on [Tidbyt](https://github.com/tidbyt/community).

Each number represents an index of potential cards for every tarot card (i.e., 0-77) or just cards from the Major arcana (i.e., 0-21).

Numbers are pushed daily via [Make](https://www.make.com/) every midnight `America/New_York` time.

## Files
- `range_all.json`: A JSON file of card draws where the range of cards includes every tarot card
- `range_major.json`: A JSON file of card draws where the range of cards is limited to the Major arcana
- `card_names.csv`: A list of tarot cards and their index value in the draw list (e.g., if the number drawn is 34, the card is Page of Cups)
- `last_updated.txt`: A text file with a timestamp of the most recent time cards were drawn

## License
Daily Tarot Card Draw © 2023 by frame-shift is licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/?ref=chooser-v1).
