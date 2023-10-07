# Daily Tarot Card Draw
This is a dataset of random numbers generated for daily tarot card draws, originally designed for an applet on [Tidbyt](https://github.com/tidbyt/community).

Each number represents an index of potential cards for every tarot card (i.e., 0-77) or just cards from the Major Arcana (i.e., 0-21).

Numbers are daily via [Make](https://www.make.com/) every midnight `America/New_York` time.

## Files
- `range_all.json`: A JSON file of card draws where the range of cards includes every tarot card
- `range_major.json`: A JSON file of card draws where the range of cards is limited to the Major Arcana
- `card_names.csv`: A CSV list of tarot cards and their index values (e.g., if the number drawn is 34, the card is Page of Cups)
- `last_updated.txt`: A text file with a timestamp of the most recent time new cards were drawn

## License
Daily Tarot Card Draw © 2023 by frame-shift is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
