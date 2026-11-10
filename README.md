# Daily Tarot Card Draw
This is a dataset of random integers generated for daily tarot card draws, originally designed for an applet on [Tidbyt](https://github.com/tidbyt/community/tree/main/apps/tarotcards).

Each number represents an index of potential cards for every tarot card (i.e., 0-77) or just cards from the Major Arcana (i.e., 0-21). Each number represents a specific card name as designated in `card_names.csv`.

The output `draws.json` holds the result of the card draws. Both the entire tarot deck and a Major Arcana deck contain draws for a single card and a three-card spread.

## Process
Cards are drawn as follows via [Make](https://www.make.com/):
1. Two "decks" of *all* tarot cards are shuffled
   - Two decks containing every tarot card are randomly and independently shuffled via [RANDOM.ORG](https://www.random.org/integer-sets/?sets=2&num=78&min=0&max=77&seqnos=on&order=index&format=plain&rnd=new)
     - **Deck `all1`:** Used to draw a single card
     - **Deck `all2`:** Used to draw three cards for the spread
	 - *If RANDOM.ORG cannot be reached:* [Make](https://www.make.com/) is used as a fallback to generate the two sets as above
2. Two "decks" of only *Major Arcana* cards are shuffled
   - Two decks containing only the Major Arcana are randomly and independently shuffled via [RANDOM.ORG](https://www.random.org/integer-sets/?sets=2&num=22&min=0&max=21&seqnos=on&order=index&format=plain&rnd=new)
     - **Deck `maj1`:** Used to draw a single card
     - **Deck `maj2`:** Used to draw three cards for the spread
	 - *If RANDOM.ORG cannot be reached:* [Make](https://www.make.com/) is used as a fallback to generate the two sets as above
3. Each of the four decks (`all1`, `all2`, `maj1`, `maj2`) is parsed into an array, maintaining each deck's shuffled order
4. Single cards and three-card spreads are drawn from each deck as described in [Magic](#magic)
5. Card draws are pushed here every day at 03:00 `America/New_York` [time](https://www.timeanddate.com/time/zone/usa/new-york)

## Files
- `draws.json`: A JSON containing single and spread draws across all cards or Major Arcana only; also includes a last updated timestamp
- `card_names.csv`: A CSV list of tarot cards and their index values (e.g., if the number drawn is 34, the card is Page of Cups)
- `card_names_array.txt`: A TXT file of the card names in an array format, maintaining the same order as the CSV; useful for copying into code

## Magic
<details>
  <summary><i>Just for the fun of it... </i> ⬇️</summary>

  - Cards are drawn daily at 11:11 `America/New_York` [time](https://www.timeanddate.com/time/zone/usa/new-york) before being pushed here at 03:00

  - After shuffling the tarot decks, cards are [drawn as follows](https://www.britannica.com/topic/number-symbolism):
    - **Single card draws:** The **3rd** card is drawn
    - **Three-card spread draws:** The **7th, 10th, and 12th** cards are drawn (in that order)
  
</details>

## License
Daily Tarot Card Draw © 2023 by frame-shift is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
