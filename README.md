# Daily Tarot Card Draw
This is a dataset of random numbers generated for daily tarot card draws, originally designed for an applet on [Tidbyt](https://github.com/tidbyt/community).

Each number represents an index of potential cards for every tarot card (i.e., 0-77) or just cards from the Major Arcana (i.e., 0-21).

Cards are drawn from two arrays. One array contains integers 0-77 to capture all cards, and another array contains integers 0-21 to capture just the Major Arcana. Each array is shuffled independently via [Make](https://www.make.com/) twice: once to generate a shuffled array for a "single" card draw, and again to generate an array for a three-card "spread." This allows for the card pulled for a "single" draw to also be present, by chance, within the "spread" draw.

New card draws are pushed here every day at 03:00 `America/New_York` [time](https://www.timeanddate.com/time/zone/usa/new-york).

## Files
- `draws.json`: A JSON containing single and spread draws across all cards or Major Arcana only. Also includes a last updated timestamp.
- `card_names.csv`: A CSV list of tarot cards and their index values (e.g., if the number drawn is 34, the card is Page of Cups)
- `card_names_array.txt`: A TXT file of the card names in an array format, maintaining the same order as the CSV; useful for copying into code

## Magic
<details>
  <summary><i>Just for the fun of it... </i> ⬇️</summary>

  - Cards are drawn daily at 11:11 `America/New_York` [time](https://www.timeanddate.com/time/zone/usa/new-york).

  - After shuffling the tarot deck, cards are drawn as follows:
    - **Single card draws**: The **3rd** card is drawn
    - **Three-card spread draws**: The **7th, 10th, and 12th** cards are drawn (in that order)
  
</details>

## License
Daily Tarot Card Draw © 2023 by frame-shift is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
