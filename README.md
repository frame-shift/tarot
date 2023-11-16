# Daily Tarot Card Draw
This is a dataset of random numbers generated for daily tarot card draws, originally designed for an applet on [Tidbyt](https://github.com/tidbyt/community).

Each number represents an index of potential cards for every tarot card (i.e., 0-77) or just cards from the Major Arcana (i.e., 0-21).

Cards are drawn from two arrays. One array contains integers 0-77 to capture all cards, and another array contains integers 0-21 to capture just the Major Arcana. Each array is shuffled independently via [Make](https://www.make.com/) twice: once to generate a shuffled array for a "single" card draw, and again to generate an array for a three-card "spread." This allows for the card pulled for a "single" draw to also be present, by chance, within the "spread" draw.

New card draws are pushed here every day at 03:00 `America/New_York` [time](https://www.timeanddate.com/time/zone/usa/new-york).

## Files
- `range_all.json`: A JSON file of card draws where the range of cards includes every tarot card
- `range_major.json`: A JSON file of card draws where the range of cards is limited to the Major Arcana
- `card_names.csv`: A CSV list of tarot cards and their index values (e.g., if the number drawn is 34, the card is Page of Cups)
- `last_updated.txt`: A text file with a timestamp of the most recent time new cards were drawn

## License
Daily Tarot Card Draw © 2023 by frame-shift is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
